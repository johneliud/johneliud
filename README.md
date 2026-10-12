# John Eliud Odhiambo

**Full Stack Developer**

---

[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://johneliudodhiambo.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/john-odhiambo-6b1863307)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:johneliud4@gmail.com)

---

## About Me

Full stack developer with 3 years building scalable web and mobile applications.

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
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) ![GitLab CI](https://img.shields.io/badge/gitlab%20CI-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white) ![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white) ![SonarQube](https://img.shields.io/badge/sonarqube-%234E9BCD.svg?style=for-the-badge&logo=sonarqubeserver&logoColor=white) ![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)

### Databases
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/mongodb-%2347A248.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![SQLite](https://img.shields.io/badge/sqlite-%23003B57.svg?style=for-the-badge&logo=sqlite&logoColor=white)

---

## Notable Projects

### [Neo4flix](https://github.com/johneliud/neo4flix) - Microservices Movie Recommendation Platform

Neo4flix is a full-stack, microservices-based movie recommendation platform designed around domain isolation, stateless services, and polyglot persistence.

The backend consists of five independently deployable Spring Boot 4 (Java 25, Maven) services fronted by a reactive Spring Cloud Gateway (WebFlux) that acts as the single entry point that handles centralized JWT (JJWT HS256) validation and user-context propagation, Bucket4j-based rate limiting (e.g. 5 logins / 15 min / IP), CORS, and security headers.

The User Microservice owns identity through registration, login, refresh-token rotation, TOTP-based 2FA, profile management, and watchlists backed by PostgreSQL 15 via Spring Data JPA/Hibernate with Flyway migrations and Spring Security 7. The Movie, Rating, and Recommendation services share a Neo4j 5 graph via Spring Data Neo4j. Movie Service manages the catalog as entities with paginated multi-filter Cypher search and admin-only writes. Rating Service models edges, validates movie existence against the Movie Service, and propagates average-rating updates back. Recommendation Service is a stateless read-only engine that runs raw Cypher to combine collaborative filtering with content-based filtering, then merges, dedupes, scores by relevance, filters, and paginates.

All services share a consistent security model (tokens issued by User Service, validated locally with a shared secret), error handling, Jakarta Validation, Lombok records-based DTOs, and unit test coverage.

The frontend is an Angular 21 SSR application with standalone components, signals, reactive forms, RxJS, JWT interceptors, role-based route guards, Tailwind CSS 4 styling, and Vitest coverage, orchestrated locally with Docker Compose and a `start-services.sh` multi-terminal boot script.

### [buy-01](https://github.com/johneliud/buy-01) - Microservices E-Commerce Marketplace

buy-01 is an end-to-end e-commerce marketplace built around role-based commerce, event-driven consistency, and independent deployability.

The backend consists of five independently deployable Spring Boot 4 (Java 25, Maven) services fronted by a reactive Spring Cloud Gateway that acts as the single entry point that handles centralized JWT validation and user-context propagation, Bucket4j-based rate limiting (e.g. 5 logins / 15 min / IP), CORS, and security headers.

The User Service owns identity through client/seller registration, JWT authentication with 24-hour expiry, BCrypt password hashing, profile and avatar management, and role-based access control. The Product Service manages the catalog with CRUD, name/description search, price-range and category filtering, sorting, pagination, and stock tracking. The Media Service handles multi-image product uploads with type/size validation and serving. The Order Service owns the persistent cart, pay-on-delivery checkout with delivery address, and the full order lifecycle PENDING - CONFIRMED - SHIPPED - DELIVERED with buyer cancellation and seller status advancement plus paginated, searchable order views.

Services stay decoupled through Apache Kafka (Confluent 7.5.0, local via Docker Compose with Zookeeper): `product-deleted` drives automatic media cleanup, `order-placed` feeds user analytics and product stock updates, and `order-status-changed` keeps profiles in sync. Each service owns its MongoDB Atlas database for cloud-native persistence without local DB setup. Analytics close the loop with buyer spend / most-purchased insights and seller revenue / best-seller stats.

The frontend is an Angular 21 SSR application with standalone components, signals, reactive forms, RxJS, JWT interceptors, role-based route guards, Tailwind CSS 4 styling, and Vitest coverage, orchestrated locally with Docker Compose and a `start-services.sh` multi-terminal boot script.

### [netcat](https://github.com/johneliud/netcat) - Concurrent TCP Group Chat in Go

netcat is a from-scratch reimplementation of NetCat as a concurrent TCP group-chat system, built with dependency-free Go 1.22 using only the standard library.

The server listens on a configurable port (default `:8989`, validated to 1024-65535), accepts connections in a loop, and hands each one off to a goroutine. Shared state, the client registry (capped at 10 concurrent connections with backpressure), message history, and broadcast fan-out is guarded by `sync.Mutex` pairs  to stay race-safe under concurrent joins, leaves, and broadcasts.

The connection lifecycle is deliberately hardened: ASCII-art banner on connect, handshake with empty-name and case-insensitive duplicate-name rejection, a 60-second join timeout that is cleared after authentication, replay of persisted chat history to late joiners, join/leave notifications fanned out to all peers except the originator, timestamped `[DATETIME][username]:` prompts, 4KB message framing with empty-message rejection, and graceful EOF handling with registry cleanup.

The result is a small but technically complete study in low-level networking: TCP socket management, per-connection goroutines, mutex-synchronized shared memory, deadline-based resource protection, and a text protocol interoperable with the real `nc` client all with zero external dependencies.

---

**Utilizing The Power Of Code To Tackle Pressing Issues.**
