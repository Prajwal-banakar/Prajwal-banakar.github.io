---
title: "How I Started Contributing to Apache Fluss"
date: 2026-04-10T14:00:00+05:30
draft: false
tags: ["GitHub", "Apache Fluss", "Distributed Systems", "Learning"]
categories: ["Open Source", "Apache Fluss"]
---

I started exploring open source seriously with one goal: to bridge the gap between theoretical knowledge and real-world distributed systems.

Before diving into OSS, I already knew the basics of Git and GitHub, but nothing prepared me for the scale of a real-world project. My journey led me to **Apache Fluss (incubating)**, and like many developers, my first day was overwhelming. Thousands of lines of Java code, complex streaming logic, and a high-performance architecture stared back at me.

### The Struggle Before the Success

I’ll be honest: at first, I was lost. I forked and downloaded the project locally, but things felt so "weird" and complicated that I ended up deleting the entire folder and re-downloading it several times.

I had to sit back, stay calm, and actually **read the documentation**. I focused on the contributing guidelines and finally set up the repository properly, configuring the checkstyle and IDE settings. When I finally saw "BUILD SUCCESS" on my terminal, it felt like a massive victory.

### The Starting Point

I decided to start small. My first contributions weren't complex features; they were documentation and testing improvements. I realized that the best way to learn a system is to try and explain it to others.

One of my early wins was working on the **Typed API documentation**. By documenting how POJOs (Plain Old Java Objects) interact with the Fluss engine, I forced myself to understand the serialization layer and the end-to-end data flow.

Around this time, I joined the Slack channel and the dev mailing list. I introduced myself and was met with a huge, warm response from the maintainers. That welcome made me realize I wasn't just a random person on the internet; I was part of a team.

### Moving to Next

A major turning point happened when one of the maintainers, **Giannis**, messaged me on Slack: *"Try to solve this issue if you're interested, I can assign it to you."* The task was to solve a major pain point: configuration documentation was manual and hard to maintain. I took the initiative to implement the **`fluss-docgen` module**, which automated the entire process. This was a significant milestone. I was no longer just "fixing" typos, I was building infrastructure that improved the developer experience for the entire community.

### Becoming Part of the Community

Beyond the code, the most rewarding part has been participating in the Apache "process." I’ve had the chance to:
* **Montly calls:** Joining the monthly community calls where we discuss the roadmap, challenges, and future plans for Fluss.
* **Read and Review:** Deeply analyzing existing code and participating in PR reviews.
* **Participate in Governance:** Engaging in mailing list discussions and voting on Release Candidates (RCs) for the official releases.
* **Contribute to Clients:** Working on improvements for the Rust, C++, and Python clients.

### What's Next?

I’m currently focused on **FIP-37 (Apache Fluss Improvement Proposal)**, which aims to integrate **Native RoaringBitmap** support directly into the storage engine.

I’m starting this blog to document my journey, the technical challenges I face, and everything I learn from the Apache community. Whether you're a seasoned engineer or just starting your OSS journey, I hope my story shows you that it’s okay to feel overwhelmed—as long as you keep going.

---

*“The best way to learn a complex system is to start contributing to it.”*