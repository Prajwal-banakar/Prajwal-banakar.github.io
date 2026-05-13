---
title: "My Journey to Google Summer of Code 2026"
date: 2026-05-01T10:00:00+05:30
draft: false
tags: ["GSoC", "Apache", "Open Source", "Java", "Distributed Systems", "Journey"]
categories: ["Open Source", "Personal"]
---

### Introduction

I'm Prajwal, and this is the story of my journey from a small village in Karnataka to being a Google Summer of Code contributor with the Apache Software Foundation. This is not a tale of overnight success, but one of struggle, perseverance, and the transformative power of open source. I hope my story can guide and inspire students who are on a similar path.

### Humble Beginnings and a Spark of Interest

I come from a small village called Kuppinakeri in Karnataka. My parents are farmers, and I grew up in a humble environment. After scoring 86% in my 10th grade in 2020, I got into Morarji Desai PU college, a government institution that provided free education. This was my first time living in a hostel. My elder brother, [Guru Prasanna](https://www.linkedin.com/in/gurubanakara), who works at Morgan Stanley, has been my guiding light. On his advice, I chose PCMCs (Physics, Chemistry, Mathematics, Computer Science) over PCMB. It was here that my love for computer science, particularly C++, began to blossom, thanks to my supportive lecturer, Sanjay sir.

### The Unforgiving Path to Engineering

After my PU exams in 2022, I came home with a newfound passion for C++. I spent my holidays watching C++ tutorials on YouTube. The results came, and I had scored only 68%, with a saving grace of 94 in Computer Science. My KCET rank was a disheartening 1,50,000, which worsened to 1,75,000 after re-results were announced. I applied to countless colleges but didn't get a seat in the first round. I even tried for management seats to no avail. In the second round, I was allotted a mechanical engineering seat, which I rejected. I was on the verge of giving up on my engineering dream. Finally, in the third round, I was allotted a seat in the Information Science branch at Ghousia College of Engineering in Ramanagara. Initially, I didn't like the college, but I had no other choice.

### A New Chapter and New Struggles

On December 3, 2022, my brother Guru and I traveled to Ramanagara for my admission. The journey back home was emotional as my brother shared his own engineering struggles, which inspired me a lot! My engineering life officially began on December 12, 2022. Being an introvert, I found it hard to open up to people. After a desperate search and a visit to the social welfare office, I finally secured a place to stay in a Government hostel.

### The Self-Taught Engineer

The first year of engineering was a mixed bag. While I excelled in coding subjects due to my C++ background, I struggled with mathematics, though Jyothi mam's teaching helped me improve. I soon realized that the quality of teaching in my college was not up to the mark. I started bunking classes and spending my time in the hostel, learning Java from YouTube tutorials and watching web series; 'Aspirants' was my favorite one. I created GitHub and LinkedIn accounts but didn't know how to use them. My brother gave me his old laptop, but I barely knew how to use it. I was just exploring when it got damaged after a few days. Food was another challenge, and there were days I went hungry. I ended my first year with a 6.5 SGPA. I failed in one subject but passed after re-evaluation.

### The Dawn of Open Source

In my third year, my interest in Git and GitHub grew, and I started spending my nights in the hostel's computer room, which had only one working computer. I had to fight for access to it, but I was determined. My brother bought me a new laptop at the end of my third year, which was a huge motivation. I started maintaining my GitHub profile with green marks and building more projects.

### The GSoC Revelation

I was applying for many internships but getting no response. My resume was not impressive enough. On December 17, 2025, my friend [Ajay](https://www.linkedin.com/in/ajaykumarhn/) sent me a message on WhatsApp: "Guru GSoC ge apply madana," and that changed everything. I had no idea what GSoC was, but a quick YouTube search revealed that it was Google Summer of Code, a program that revolved around open-source contributions. I was already learning Git and GitHub, so this piqued my interest. I watched countless videos of previous GSoC students and decided to give it a shot.

### My First Steps into the Open Source World

I started by exploring organizations. I blindly picked Jenkins, found a documentation issue, and opened a pull request using ChatGPT. It was rightly rejected. I was disheartened but not defeated. I then came across the Apache Software Foundation (ASF), a prestigious organization, where I found a project called **Apache Fluss**.

Fluss is a streaming storage system designed for real-time analytics, which means it helps companies process and analyze massive amounts of data as it's generated. It's a complex, high-performance Java project, and at first, I was completely lost. I forked the repository, but things felt so "weird" that I ended up deleting the entire folder and re-downloading it several times.

I had to sit back, stay calm, and actually **read the documentation**. I focused on the contributing guidelines and finally set up the repository properly. When I finally saw "BUILD SUCCESS" on my terminal, it felt like a massive victory.

### A Breakthrough and a Welcoming Community

With the project finally set up, I found a small documentation issue, asked to be assigned, and opened my first pull request (#2261) on December 26, 2025. A maintainer merged it and sent a celebratory emoji. My confidence soared.

I joined the Slack channel and the dev mailing list, introduced myself, and was met with a huge, warm response. The maintainers at Apache Fluss are incredibly supportive and cool. They don't just expect you to know everything; they guide you. That welcome made me realize I wasn't just a random person on the internet; I was part of a team.

A major turning point happened when one of the project maintainers messaged me on Slack about a bigger task: the project's configuration documentation was manual and hard to maintain. I didn't even know how to solve it, but I said "yes" anyway. I took the initiative to implement the **`fluss-docgen` module**, which automated the entire process. This was a significant milestone. I was no longer just "fixing" typos; I was building infrastructure that improved the developer experience for the entire community.

### Becoming Part of the Community

Beyond the code, the most rewarding part has been participating in the Apache "process." I’ve had the chance to:
*   **Join Monthly Calls:** Participating in the monthly community calls where we discuss the roadmap, challenges, and future plans for Fluss.
*   **Read and Review:** Deeply analyzing existing code and participating in PR reviews.
*   **Participate in Governance:** Engaging in mailing list discussions and voting on Release Candidates (RCs) for the official releases.
*   **Contribute to Clients:** Working on improvements for the Rust, C++, and Python clients.

### The Road to GSoC

My journey to GSoC was a marathon, not a sprint. By the time I submitted my proposal, I had a total of **17 PRs (12 merged, 5 open)**. I was also credited in the [Apache Fluss v0.9.0-incubating release](https://github.com/apache/fluss/releases/tag/v0.9.0-incubating) and the [Fluss clients v0.1.0 release](https://fluss.apache.org/blog/fluss_rust_client_release/), and contributed to the [temporary repository for Flink UDFs](https://github.com/flink-extended/flink-roaringbitmap). You can see a full list in my [contribution tracker](https://github.com/Prajwal-banakar/open-source-contributions).

### The Proposal Journey

When the time came to write a GSoC proposal, I was lost. After some research, I had an idea for a project on RoaringBitmap integration, but a maintainer initially rejected it, explaining that Fluss is not a query engine. I was devastated and almost gave up. But with some self-motivation, I refined my proposal, and this time, he was impressed. He suggested I formalize it as a Fluss Improvement Proposal (FIP).

I drafted the FIP and started a discussion on the mailing list. The community's feedback was invaluable. When I realized Fluss was not listed as a GSoC project under ASF, I reached out to the maintainers. They created a JIRA ticket and agreed to be my mentor. I submitted my [proposal](https://drive.google.com/file/d/1QVQqtdMlnK-oG44vmFqR30jy0EQlX1wp/view?usp=sharing) on March 30, 2026, and continued to refine the [FIP-37 proposal](https://cwiki.apache.org/confluence/display/FLUSS/FIP-37%3A+Native+RoaringBitmap+Integration+for+Apache+Fluss) based on the maintainers' feedback.

### The Moment of Truth

The result day, April 30, 2026, was filled with anxiety. I was at home, and no one—not my family or friends—knew about my GSoC preparations. I hadn't shared my journey because I didn't want to disappoint them if I wasn't selected. As the clock ticked past 11:30 PM, my friend [Vidya](https://www.linkedin.com/in/vidyavathi-gk/) was sending continuous messages asking what had happened. I was worried, refreshing the website constantly. At 11:35 PM, the status on the GSoC website changed from 'Submitted' to 'Accepted.' I was overwhelmed with joy. I woke up my parents and shared the news. They didn't understand what GSoC was, but they were shocked and happy for me. After that, I called Vidya to share my happiness; she was literally screaming in her PG. She is the only one who watched this journey closely. The next day, I announced the news to the Fluss community and on LinkedIn. My college was shocked and proud.

### Conclusion: My Two Cents

My journey was not easy, but it taught me the importance of consistency, hard work, and self-belief. Throughout my engineering journey, I never bought or joined an online course, nor did I pay for an internship. I learned everything from free online resources and let my work speak for itself.

Discipline is more important than motivation. Motivation comes from watching videos and fades away, but discipline is what keeps you going. As Virat Kohli says, "The only time you truly fail is when you decide to give up."

My dream of a 5 LPA package now seems small in comparison to what I have achieved. To all the students out there, my advice is simple: be consistent, be curious, and never be afraid to fail. The open-source community is a welcoming place, and if you are willing to learn, there are people who will guide you. Believe in yourself and your dreams, and you will achieve them.

### What's Next?

This post is just the beginning. In my upcoming posts, I'll dive deeper into:

*   What is Apache Fluss and why is it so cool?
*   What is FIP-37 and what problem does it solve?
*   A detailed look at my GSoC project and what I'm building.

Be Kind, Stay tuned!
