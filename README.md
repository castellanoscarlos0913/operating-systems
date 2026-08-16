# CS 230: The Gaming Room - System Architecture & Software Design

## Project Overview
This repository contains the software design documentation, architectural evaluations, and object-oriented migration plan for **The Gaming Room's** flagship game, *"Draw It or Lose It"*. The project transitions a native standalone application into a modern, distributed, web-based platform.

## Architecture Highlights
* **Operating Platform:** Linux-based server deployment utilizing a monolithic, modular kernel for high concurrency and low operating overhead.
* **Data Storage:** Hybrid storage model separating transactional relational data (PostgreSQL) from physical asset storage (`ext4` / Cloud Object Storage).
* **Memory Management:** Java Virtual Machine (JVM) memory isolation with strict enforcement of the **Singleton** pattern for `GameService`.
* **Distributed Communications:** Client-server architecture utilizing RESTful endpoints for stateless operations and low-latency **WebSockets** for real-time multiplayer drawing and guessing.
* **Security & Authorization:** Defense-in-depth architecture featuring TLS/HTTPS encryption, server-level firewalling (`iptables`), and continuous server-side Role-Based Access Control (RBAC) to eliminate perimeter vulnerabilities.

## Repository Contents
* `CS_230_Project_Software_Design_Document.docx` / `.pdf`: Full design specifications, Domain Model UML, cross-platform evaluations, and system recommendations.
* `README.md`: Project summary and architectural overview.

## Author
* **Carlos Castellanos** — Computer Science Student, Southern New Hampshire University
