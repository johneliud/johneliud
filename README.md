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

### [neo4flix](https://github.com/johneliud/neo4flix) - Microservices Movie Recommendation Platform

Neo4flix is a full-stack, microservices-based movie recommendation platform built around domain isolation, stateless services, and polyglot persistence, pairing five Spring Boot services with an Angular SSR frontend.

- **Gateway & services:** Five independently deployable Spring Boot 4 (Java 25, Maven) services behind a reactive Spring Cloud Gateway (WebFlux) handling centralized JWT (JJWT HS256) validation, user-context propagation, Bucket4j rate limiting, CORS, and security headers.
- **User Service:** Identity via registration, login, refresh-token rotation, TOTP 2FA, profiles, and watchlists on PostgreSQL 15 with Spring Data JPA/Hibernate, Flyway migrations, and Spring Security 7.
- **Movie / Rating / Recommendation Services:** Shared Neo4j 5 graph via Spring Data Neo4j; paginated multi-filter Cypher catalog search, edge-based ratings, and a stateless read-only engine blending collaborative and content-based filtering.
- **Cross-cutting:** Shared-secret token model, centralized error handling, Jakarta Validation, Lombok record DTOs, and unit test coverage.
- **Frontend:** Angular 21 SSR app with standalone components, signals, reactive forms, RxJS, JWT interceptors, and role-based route guards for admin-only catalog management; Tailwind CSS 4 styling and Vitest coverage, run via Docker Compose and `start-services.sh`.

### [buy-01](https://github.com/johneliud/buy-01) - Microservices E-Commerce Marketplace

buy-01 is an end-to-end e-commerce marketplace built around role-based commerce, event-driven consistency, and independent deployability, backing an Angular SSR storefront with five Spring Boot services.

- **Gateway & services:** Five independently deployable Spring Boot 4 (Java 25, Maven) services behind a reactive Spring Cloud Gateway handling centralized JWT validation, user-context propagation, Bucket4j rate limiting, CORS, and security headers.
- **User Service:** Identity with client/seller registration, JWT authentication (24-hour expiry), BCrypt hashing, avatar management, and role-based access control.
- **Product / Media / Order Services:** Catalog CRUD with search, price/category filtering, sorting, pagination, and stock tracking; multi-image uploads with type/size validation; persistent cart with pay-on-delivery checkout and the full PENDING - CONFIRMED - SHIPPED - DELIVERED lifecycle.
- **Eventing:** Apache Kafka (Confluent 7.5.0, local via Docker Compose with Zookeeper) decouples services through `product-deleted`, `order-placed`, and `order-status-changed` events.
- **Persistence & analytics:** Per-service MongoDB Atlas databases; buyer spend / most-purchased and seller revenue / best-seller insights.
- **Frontend:** Angular 21 SSR storefront with standalone components, signals, and reactive forms driving catalog browsing, cart/checkout, and seller dashboards; JWT interceptors and role-based guards enforce buyer/seller access, styled with Tailwind CSS 4 and tested with Vitest.

### [netcat](https://github.com/johneliud/netcat) - Concurrent TCP Group Chat

netcat is a from-scratch reimplementation of NetCat as a concurrent TCP group-chat system, built with dependency-free Go 1.22 using only the standard library.

- **Server model:** Listens on a configurable port (default `:8989`, validated 1024-65535) and hands each connection off to its own goroutine.
- **Concurrency:** Mutex-guarded shared state covering the client registry (capped at 10 connections with backpressure), message history, and broadcast fan-out.
- **Lifecycle:** ASCII-art banner, handshake with empty-name and case-insensitive duplicate-name rejection, 60-second join timeout, history replay for late joiners, join/leave notifications, timestamped `[DATETIME][username]:` prompts, 4KB message framing, and graceful EOF cleanup.
- **Scope:** A low-level networking study in TCP sockets, per-connection goroutines, mutex-synchronized memory, and deadline-based resource protection, interoperable with the real `nc` client.

---

**Utilizing The Power Of Code To Tackle Pressing Issues.**
