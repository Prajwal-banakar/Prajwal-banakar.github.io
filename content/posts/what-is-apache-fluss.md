---
title: "What is Apache Fluss? A GSoC Story on Making Real-Time Analytics Simpler"
date: 2024-05-23T12:00:00+05:30
draft: false
---

### The Swiggy Problem: Analytics at the Speed of Now

Imagine you're running Swiggy or Zomato. Every second, thousands of orders pour in from across the country. You need to answer critical business questions in real-time: *How many unique customers ordered in Bangalore in the last 10 minutes? Which dish is trending right now?*

This is the world of real-time analytics. You need to process and understand data the instant it arrives.

This is exactly the problem **Apache Fluss** was built to solve. Think of it as a very fast, very intelligent database that never sleeps. It's a **streaming storage system**, built by engineers at Alibaba and now an open-source project at The Apache Software Foundation, home to legendary projects like Kafka and Hadoop. Companies use Fluss to power their real-time dashboards, fraud detection systems, and recommendation engines.

As a Google Summer of Code (GSoC) student with The Apache Software Foundation, I've had the incredible opportunity to contribute to this amazing project. This post is a story about my project, what it solves, and my journey into the world of large-scale open-source development.

### The Challenge: Counting Millions of Unique Users in Real-Time

Let's take another example. Imagine you're Spotify. You want to know: *how many unique listeners heard a song today?*

A simple question, but a massive technical challenge. If a song plays 50 million times to 10 million unique users, you can't just store every single user ID and count them later. It would take far too much memory and time. The traditional `COUNT(DISTINCT user_id)` query that works on your small database will crumble under this load.

The solution is a clever data structure called a **RoaringBitmap**. Think of it like a highly compressed list. Instead of storing 50 million records, you store one small, compressed object that can still tell you the exact number of unique listeners. It’s like compressing a 1GB file to 10MB without losing any information. It's incredibly fast and efficient.

### The Problem: A Powerful Engine with No Steering Wheel

Here's the interesting part: Apache Fluss already had the core engine to do this. It has a feature called the **Aggregation Merge Engine**, which can automatically merge these RoaringBitmaps as data arrives. This is a superpower. It means the database does the heavy lifting of deduplication on the fly.

But there was a catch. This powerful tool was locked in a room with no key.

While the storage engine understood bitmaps, the SQL layer did not. To use it, a developer had to:
1.  Write custom functions (UDFs) in Java or Scala to create and count the bitmaps.
2.  Package these functions into a JAR file.
3.  Manually register these functions in their Flink SQL session every single time.

For example, this is what code looked like before:

```sql
-- Manually register every function, every time
ADD JAR '/path/to/my/custom-udfs.jar';
CREATE TEMPORARY FUNCTION bitmap_cardinality AS 'io.mycompany.udfs.BitmapCardinality';
CREATE TEMPORARY FUNCTION bitmap_or_agg AS 'io.mycompany.udfs.BitmapOrAgg';

-- Finally, write the query
SELECT
  channel,
  bitmap_cardinality(bitmap_or_agg(uv_bitmap)) AS uv
FROM my_table
GROUP BY channel;
```

This was cumbersome, error-prone, and a huge barrier for developers who just wanted to write simple SQL.

### My GSoC Project (FIP-37): Building the SQL Interface for RoaringBitmaps

This is where my GSoC project, officially known as **FIP-37 (Fluss Improvement Proposal)**, comes in. My project is to build the key to that locked room.

The goal is to make RoaringBitmap analytics a native, first-class citizen in Apache Fluss. I'm adding a set of built-in SQL functions so that any data engineer can perform complex, real-time deduplication with simple, clean SQL—no custom code, no JARs, no hassle.

With FIP-37, the query above becomes this:

```sql
-- No setup needed. The functions are built-in.
SELECT
  channel,
  rb_cardinality(rb_or_agg(uv_bitmap)) AS uv
FROM my_table
GROUP BY channel;
```

That’s it. What previously required custom infrastructure and boilerplate code is now a single, clean line of SQL.

I'm implementing a whole suite of functions, including:
*   `rb_build_agg(user_id)`: Creates a bitmap from a stream of user IDs.
*   `rb_cardinality(bitmap)`: Counts the number of unique users in a bitmap.
*   `rb_or_agg(bitmap)`: Merges bitmaps from multiple rows to get the total unique users for a group.
*   `rb_and_agg(bitmap)`: Finds the users who are common across multiple groups.
*   And many more for advanced set operations like unions, intersections, and checking for user presence.

This proposal went through a formal review by senior engineers from companies like Alibaba and Ververica (the creators of Apache Flink). After a community vote, it was unanimously accepted. This summer, I am turning that proposal into code.

*To learn more, check out the [Apache Fluss website](https://fluss.apache.org/) and the official proposal for [FIP-37](https://cwiki.apache.org/confluence/display/FLUSS/FIP-37%3A+Native+RoaringBitmap+Integration+for+Apache+Fluss).*
