# CS 230: The Gaming Room - System Architecture & Software Design

## Project Overview
This repository contains the completed software design documentation, architectural evaluations, and object-oriented migration plan for **The Gaming Room's** flagship game, *"Draw It or Lose It"*.

---

## Course Reflection & Portfolio Artifact Analysis

### 1. Client & Software Requirements Summary
The client, **The Gaming Room**, wanted to transition their standalone Android game, *"Draw It or Lose It"*, into a scalable, multi-platform, web-based application. The primary requirements were to support concurrent players across various operating platforms (Windows, macOS, Linux, and mobile browsers), ensure unique player and team naming constraints, and maintain high performance and security without incurring excessive operating overhead.

### 2. Strengths in Documentation Development
I did particularly well in evaluating cross-platform trade-offs and architecting the server infrastructure. By analyzing operating system characteristics, I clearly justified selecting a Linux server environment to eliminate proprietary OS licensing fees while detailing memory management, virtual memory paging, and hybrid storage strategies (relational PostgreSQL for accounts/scores and ext4/S3 object storage for clue assets).

### 3. Impact of the Design Document on Code Development
Working through the design document prior to development established a clear architectural blueprint. Defining constraints and the Domain Model early clarified how the **Singleton pattern** for `GameService` would interact with the underlying Java Virtual Machine (JVM) memory space. This prevented design bottlenecks, minimized redundant memory allocation, and streamlined code implementation.

### 4. Areas for Revision & Future Improvement
If I could revise one part of the document, I would expand the **Distributed Systems and Networks** section to include detailed API sequence diagrams. While REST endpoints and WebSockets were specified for handling stateless and real-time operations, visual sequence diagrams would further clarify state synchronization and failover handling during sudden network disconnects.

### 5. Interpreting User Needs & User-Centric Design
The user's needs were interpreted by focusing on accessibility and seamless cross-platform play. Instead of requiring users to download platform-specific binaries, the architecture shifted toward a responsive web interface served over HTTPS. Considering end-user needs ensures that the system is intuitive, accessible across any device, and secure without compromising gameplay responsiveness.

### 6. Design Approach & Strategies for Future Applications
My approach focused on defense-in-depth security, cost optimization, and modular software architecture. In future projects, I will continue using design patterns (like Singleton and Factory methods), upfront UML domain modeling, and continuous authorization checks rather than relying on perimeter-only security models.

---

## Deliverables in this Repository
* `CS_230_Software_Design_Document.docx`: Complete Software Design Document (Projects 1–3).
* `README.md`: Architectural overview and course reflection.

## Author
* **Carlos Castellanos** — Computer Science Student, Southern New Hampshire University
