---
title: "My Journey Towards Google Summer of Code GSoC'26"
date: 2024-07-26T10:00:00+05:30
draft: false
tags: ["GSoC", "Apache", "Open Source", "Java", "Distributed Systems", "Journey"]
categories: ["Open Source", "Personal"]
---

### Introduction

My name is Prajwal, and this is the story of my journey from a small village in Karnataka to being a Google Summer of Code contributor with the Apache Software Foundation. This is not a tale of overnight success, but one of struggle, perseverance, and the transformative power of open source. I hope my story can guide and inspire students who are on a similar path.

### Humble Beginnings and a Spark of Interest

I come from a small village called Kuppinakeri in Karnataka. My parents are farmers, and I grew up in a humble environment. After scoring 86% in my 10th grade in 2020, I got into Morarji Desai PU college, a government institution that provided free education. This was my first time living in a hostel. My elder brother, [Guru Prasanna](https://www.linkedin.com/in/gurubanakara), who works at Morgan Stanley, has been my guiding light. On his advice, I chose PCMCs (Physics, Chemistry, Mathematics, Computer Science) over PCMB. It was here that my love for computer science, particularly C++, began to blossom, thanks to my supportive lecturer, Sanjay sir.

### The Unforgiving Path to Engineering

After my PU exams in 2022, I came home with a newfound passion for C++. I spent my holidays watching C++ tutorials on YouTube. The results came, and I had scored only 68%, with a saving grace of 94 in Computer Science. My KCET rank was a disheartening 1,50,000, which worsened to 1,75,000 after re-results were announced. I applied to countless (almost all) colleges but didn't get a seat in the first round. I even tried for management seats to no avail. In the second round, I was allotted a mechanical engineering seat, which I rejected. I was on the verge of giving up on my engineering dream. Finally, in the third round, I was allotted a seat in the Information Science branch at Ghousia College of Engineering in Ramanagara. Initially, I didn't like the college, but I had no other choice.

### A New Chapter and New Struggles

On December 3, 2022, my brother Guru and I traveled to Ramanagara for my admission. The journey back home was emotional as my brother shared his own engineering struggles, which inspired me a lot! My engineering life officially began on December 12, 2022. Being an introvert, I found it hard to open up to people. My father accompanied me to the hostel, but we were told all the seats were full. After a desperate search and a visit to the social welfare office, I finally secured a place to stay, which for the first year was the hostel library and computer rooms.

### The Self-Taught Engineer

The first year of engineering was a mixed bag. While I excelled in coding subjects due to my C++ background, I struggled with mathematics, though Jyothi mam's teaching helped me improve. I soon realized that the quality of teaching in my college was not up to the mark. I started bunking classes and spending my time in the hostel, learning Java from YouTube tutorials and watching web series; 'Aspirants' was my favorite one. i created GitHub and linkdin accounts but i dont know how to use them, My brother gave me his old laptop, but I barely knew how to use it. I was just exploring when it got damaged after a few days. Food was another challenge, and there were days I went hungry. I ended my first year with a 6.5 SGPA. I failed in one subject but passed after re-evaluation.

### Finding My Way Through the Noise

The second year was no different. The quality of teaching remained poor, and I continued my self-learning journey. I got scolded by lecturers for my low attendance and received low internal marks. I started exploring websites like W3Schools and GeeksforGeeks. My friends were more interested in games and movies, and I started to feel isolated. I was often ridiculed for my dedication to learning. It was a difficult period, but I decided to channel my energy into something positive. I deleted my social media accounts and focused on learning. I met [Vidya](https://www.linkedin.com/in/vidyavathi-gk/), who became my pillar of support.

### The Dawn of Open Source

In my third year, I started building small projects and pushing them to GitHub. I had a mini-project in my 5th semester; I built a food delivery app, which I managed to build while my friends struggled. I also joined a gym, which helped me focus on my physical and mental health. My interest in Git and GitHub grew in these days!, and I started spending my nights in the hostel's computer room, which had only one working computer. I had to fight for access to the computer room, but I was determined. My brother bought me a new laptop at the end of my third year, which was a huge motivation. I started maintaining my GitHub profile with green marks and building more projects.

### The GSoC Revelation

I was applying for many internships but getting no response. My resume was not impressive enough. On December 17, 2025, my friend Ajay mentioned "GSoC". I had no idea what it was, but a quick YouTube search revealed that it was Google Summer of Code, a program that revolved around open source contributions. I was already learning Git and GitHub, so this piqued my interest. I watched countless videos of previous GSoC students and decided to give it a shot.

### My First Steps into the Open Source World

I started by exploring organizations and projects. I blindly picked Jenkins, found a documentation issue, and opened a pull request using ChatGPT. It was rightly rejected. I was disheartened but not defeated. I then came across the Apache Software Foundation (ASF), a prestigious organization. I found a recently committed project called Apache Fluss.

I’ll be honest: at first, I was lost. I forked and downloaded the project locally, but things felt so "weird" and complicated that I ended up deleting the entire folder and re-downloading it several times. I had to sit back, stay calm, and actually **read the documentation**. I focused on the contributing guidelines and finally set up the repository properly, configuring the checkstyle and IDE settings. When I finally saw "BUILD SUCCESS" on my terminal, it felt like a massive victory.

### A Breakthrough and a Welcoming Community

With the project finally set up, I found a small documentation issue, asked to be assigned, and opened my first pull request (#2261) on December 26, 2025. The maintainer, Giannis, merged it and sent a celebratory emoji. My confidence soared.

Around this time, I joined the Slack channel and the dev mailing list. I introduced myself and was met with a huge, warm response from the maintainers. That welcome made me realize I wasn't just a random person on the internet; I was part of a team.

A major turning point happened when Giannis messaged me on Slack about a bigger task: the project's configuration documentation was manual and hard to maintain. I took the initiative to implement the **`fluss-docgen` module**, which automated the entire process. This was a significant milestone. I was no longer just "fixing" typos; I was building infrastructure that improved the developer experience for the entire community.

### Becoming Part of the Community

Beyond the code, the most rewarding part has been participating in the Apache "process." I’ve had the chance to:
*   **Join Monthly Calls:** Participating in the monthly community calls where we discuss the roadmap, challenges, and future plans for Fluss.
*   **Read and Review:** Deeply analyzing existing code and participating in PR reviews.
*   **Participate in Governance:** Engaging in mailing list discussions and voting on Release Candidates (RCs) for the official releases.
*   **Contribute to Clients:** Working on improvements for the Rust, C++, and Python clients.

### The Proposal Journey: A Rollercoaster of Emotions

When the time came to write a GSoC proposal, I was lost. After some research, I had an idea for a project on RoaringBitmap integration, but Jark, another maintainer, initially rejected it, explaining that Fluss is not a query engine. I was devastated and almost gave up. But with some self-motivation, I refined my proposal, and this time, Jark was impressed. He suggested I formalize it as a Fluss Improvement Proposal (FIP).

### The Final Push

I drafted the FIP and started a discussion on the mailing list. The community's feedback was invaluable. I created a prototype and a strong GSoC proposal. When I realized Fluss was not listed as a GSoC project under ASF, I reached out to the maintainers, who were very kind. Jark created a JIRA ticket, and Giannis agreed to be my mentor. I submitted my proposal and continued to contribute to the project, discussing on the mailing list and refining the FIP based on maintainers' feedback!

### The Moment of Truth

The result day, April 30, 2026, was filled with anxiety. I was at home, and no one, not my family or friends knew about my GSoC journey because I hadn't shared it with anyone. As the clock ticked past 11:30 PM, Vidya was sending continuous messages asking what had happened. I was worried, refreshing the website constantly. At 11:35 PM, the status on the GSoC website changed from 'Submitted' to 'Accepted.' I was overwhelmed with joy. I woke up my parents and shared the news. They didn't understand what GSoC was, but they were shocked and happy for me. After that, I called Vidya to share my happiness; she was literally screaming in her PG. The next day, I announced the news to the Fluss community and on LinkedIn. My college was shocked and proud.

### Conclusion: My Two Cents

My journey was not easy, but it taught me the importance of consistency, hard work, and self-belief. Throughout my engineering journey, I never bought or joined an online course, nor did I pay for an internship. I learned everything from free online resources and let my work speak for itself. My dream of a 5 LPA package now seems small in comparison to what I have achieved. To all the students out there, my advice is simple: be consistent, be curious, and never be afraid to fail. The open-source community is a welcoming place, and if you are willing to learn, there are people who will guide you. Believe in yourself and your dreams, and you will achieve them.
