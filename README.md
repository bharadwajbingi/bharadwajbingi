# Bharadwaj Bingi

**Backend Engineer** building production systems in Java/Spring Boot and Node.js/TypeScript.

Currently shipping transaction processing platforms and full-stack web applications. Previously intern at Mphasis.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/bharadwajbingi)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:bharadwajbingi555@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat&logo=leetcode&logoColor=black)](https://leetcode.com/bharadwajbingi)

---

## What I Work With

**Backend:** Java 17, Spring Boot, Spring Batch, Spring Security, Node.js, Express, TypeScript  
**Frontend:** React, HTML/CSS  
**Database:** PostgreSQL, Redis, MongoDB, Flyway, HikariCP  
**Cloud/DevOps:** AWS (EC2, S3), Docker, GitHub Actions, CI/CD  
**Security:** JWT, OAuth2, TOTP 2FA, AES-256-GCM, Rate Limiting  
**Testing:** JUnit 5, Mockito, Testcontainers, JaCoCo  

---

## Projects

### TradeStream Engine
> Transaction processing platform | Java 17, Spring Boot, Spring Batch, PostgreSQL, AWS, Docker

Processes CSV trade files up to 1GB asynchronously. Chunk-based batch pipeline (250 records/chunk) with 21-field validation, 3-level duplicate detection, and real-time progress tracking.

**Key engineering decisions:**
- Async upload (sub-second response) + scheduler-driven processing queue
- Multi-layer dedup: in-memory Set, bulk DB query, registry table
- JWT + OAuth2 + TOTP 2FA with AES-256-GCM encrypted secrets
- 5-module Maven architecture (API, Service, Batch, DAO, Model)
- Auto-recovery service resumes interrupted jobs on restart
- Deployed on AWS EC2 with Docker + GitHub Actions CI/CD

[Live Demo](https://d2i9y8go17l95q.cloudfront.net/) | [Backend Source](https://github.com/bharadwajbingi/tradestream-engine-api) | [Frontend Source](https://github.com/bharadwajbingi/tradestream-engine-ui)

---


### Writebase
> Blogging platform | React, Node.js, Express, MongoDB, Gemini AI

Full-stack blog with rich-text editing, content categorization, cloud media uploads, and AI-powered writing assistance via Google Gemini.

[Live Demo](https://writebase.vercel.app/) | [Source Code](https://github.com/bharadwajbingi/writebase)

---

## Architecture Snapshot (TradeStream Engine)

```
Upload Request
     |
     v
[API Module] --save--> [PostgreSQL] (status: PENDING)
     |                       ^
     |                       |
[Scheduler] --polls 5s--> picks PENDING files
     |
     v
[Spring Batch Job]
  Reader (CSV) --> Processor (validate + dedup) --> Writer (bulk save)
     |
     v
[JobListener] --> Final status + metrics
```

---

## Stats

<div align="center">
  <img src="https://leetcard.jacoblin.cool/bharadwajbingi?theme=dark&font=Baloo&ext=contest" alt="LeetCode" width="48%" />
  <img src="https://github-readme-streak-stats.herokuapp.com?user=bharadwajbingi&theme=dark" alt="GitHub Streak" width="48%" />
</div>
