# John Eliud Odhiambo

**Full Stack Developer**

---

[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://johneliudodhiambo.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/john-odhiambo-6b1863307)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:johneliud4@gmail.com)

---

## About Me

Full Stack Developer with 3 years of experience building scalable web and mobile applications.

I bridge the gap between complex software engineering and high-impact business outcomes. Throughout my career, I have focused on building products that expand market reach, optimize operational efficiency, and drive user adoption.

---

## Tech Stack & Tools

### Frameworks & Libraries
![React](https://img.shields.io/badge/react-%2361DAFB.svg?style=for-the-badge&logo=react&logoColor=white) ![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white) ![React Native with Expo](https://img.shields.io/badge/react%20native%20with%20expo-%23000020.svg?style=for-the-badge&logo=expo&logoColor=white) ![SpringBoot](https://img.shields.io/badge/springboot-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white) ![Gin](https://img.shields.io/badge/gin-%2300ADD8.svg?style=for-the-badge&logo=gin&logoColor=white)

### Languages
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-yellow.svg?style=for-the-badge&logo=javascript&logoColor=white) ![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![Rust](https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white)

### Tools & DevOps
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) ![Linux](https://img.shields.io/badge/linux-%23FCC624.svg?style=for-the-badge&logo=linux&logoColor=white)

### CI/CD & Automation
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) ![GitLab CI](https://img.shields.io/badge/gitlab%20CI-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white) ![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white) ![SonarQube](https://img.shields.io/badge/sonarqube-%234E9BCD.svg?style=for-the-badge&logo=sonarqubeserver&logoColor=white) ![Swagger](https://img.shields.io/badge/-Swagger-%2385EA2D?style=for-the-badge&logo=swagger&logoColor=white)

### Databases
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/mongodb-%2347A248.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![SQLite](https://img.shields.io/badge/sqlite-%23003B57.svg?style=for-the-badge&logo=sqlite&logoColor=white)

---

## Notable Projects

### [neo4flix](https://github.com/johneliud/neo4flix)

Five Spring Boot microservices and an Angular SSR frontend, with a graph database powering recommendations.

- **Gateway:** Spring Cloud Gateway validates JWTs centrally, passes user context downstream, and handles rate limiting, CORS, and security headers.
- **Identity:** Registration, login, refresh-token rotation, TOTP 2FA, and watchlists on PostgreSQL, with Flyway migrations.
- **Recommendations:** A shared Neo4j graph drives filtered catalog search and ratings, and a stateless engine blends collaborative and content-based filtering.
- **Frontend:** Angular 21 with signals, JWT interceptors, and role-based guards for admin-only catalog management.

**Stack:** Java Spring Boot, PostgreSQL, Neo4j, Angular, Tailwind CSS, Docker

### [buy-01](https://github.com/johneliud/buy-01)

A buyer and seller marketplace built on five independently deployable services, kept consistent through Kafka events.

- **Commerce flow:** Catalog with search, filters, and stock tracking; multi-image uploads; a persistent cart; and pay-on-delivery orders through a full lifecycle (Pending → Confirmed → Shipped → Delivered).
- **Event-driven:** Kafka events (`product-deleted`, `order-placed`, `order-status-changed`) keep services in sync without direct coupling.
- **Security:** Gateway-level JWT validation, BCrypt password hashing, and role-based access for clients and sellers.
- **Insights:** Spend and most-purchased stats for buyers, revenue and best-sellers for sellers, with a separate MongoDB Atlas database per service.

**Stack:** Java Spring Boot, Kafka, MongoDB Atlas, Angular, Tailwind CSS

### [netcat](https://github.com/johneliud/netcat)

A from-scratch NetCat-style group chat server in Go, using only the standard library.

- **Concurrency:** One goroutine per connection, with mutex-guarded shared state for the client registry, message history, and broadcasts.
- **Resource protection:** 10-client cap, 60-second join timeout, 4KB message framing, and graceful cleanup on disconnect.
- **Chat features:** Name validation (empty and duplicate names rejected), history replay for late joiners, join/leave notices, and timestamped prompts.
- **Compatibility:** Works with the real `nc` client.

**Stack:** Go

### [log_ingestion_engine](https://github.com/johneliud/log_ingestion_engine)

A Go service that accepts logs over HTTP and moves them reliably through RabbitMQ into storage, with built-in monitoring.

- **Reliable delivery:** Persistent messages with publisher confirms, auto-reconnect with backoff, and consumers that acknowledge only after a log is stored.
- **Failure handling:** A fallback consumer stores logs directly when the queue is unavailable, and dead-lettered logs are written as NDJSON and replayed with a `cmd/replay` command.
- **Storage:** Three SQLite databases, with one consumer per destination queue.
- **Protection and visibility:** Token-bucket rate limiting, a metrics endpoint, and a Tailwind dashboard with charts.

**Stack:** Go, RabbitMQ, SQLite, REST, React, Tailwind CSS

---

**Utilizing The Power Of Code To Tackle Pressing Issues. I am not a GOAT but I fit the description. **