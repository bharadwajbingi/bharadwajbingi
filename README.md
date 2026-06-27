# Bharadwaj Bingi

**Backend Engineer** | Java 17 · Spring Boot · Microservices · AWS

I build backend systems that handle real workloads. Currently building production-grade transaction processing platforms and seeking Java backend roles at product-driven companies.

<p align="left">
  <a href="https://linkedin.com/in/bharadwajbingi"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:bharadwajbingi555@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white"/></a>
  <a href="https://leetcode.com/bharadwajbingi"><img src="https://img.shields.io/badge/LeetCode-132%20solved-FFA116?style=flat&logo=leetcode&logoColor=black"/></a>
  <a href="https://d2i9y8go17l95q.cloudfront.net/"><img src="https://img.shields.io/badge/Live%20Demo-AWS%20CloudFront-FF9900?style=flat&logo=amazon-aws&logoColor=white"/></a>
  <img src="https://img.shields.io/badge/Open%20to%20Work-Java%20Backend%20Roles-brightgreen?style=flat"/>
</p>

---

## Tech Stack

**Backend:** Java 17, Spring Boot, Spring Batch, Spring Security, REST APIs, Microservices  
**Frontend:** React 18, TypeScript, Vite, Tailwind CSS  
**Database:** PostgreSQL, Redis, MongoDB, Flyway, HikariCP  
**Cloud/DevOps:** AWS (EC2, S3, CloudFront), Docker, GitHub Actions, CI/CD  
**Security:** JWT, OAuth2, TOTP 2FA, AES-256-GCM, Rate Limiting  
**Testing:** JUnit 5, Mockito, Testcontainers, JaCoCo  

---

## Featured Project

### TradeStream Engine
> Transaction processing platform | Java 17, Spring Boot, Spring Batch, PostgreSQL, AWS, Docker

Processes CSV trade files up to 1GB asynchronously. Chunk-based batch pipeline (250 records/chunk) with 21-field validation, 3-level duplicate detection, and real-time progress tracking.

**Key engineering decisions:**
- Async upload (sub-second response) + scheduler-driven processing queue
- Multi-layer dedup: in-memory Set, bulk DB query, registry table
- JWT + OAuth2 + TOTP 2FA with AES-256-GCM encrypted secrets
- 5-module Maven architecture (API, Service, Batch, DAO, Model)
- Auto-recovery service resumes interrupted jobs on restart
- React 18 + TypeScript frontend with Vite and Tailwind CSS
- Deployed on AWS EC2 with Docker + GitHub Actions CI/CD

<p align="left">
  <a href="https://d2i9y8go17l95q.cloudfront.net/"><b>Live Demo</b></a> · 
  <a href="https://github.com/bharadwajbingi/tradestream-engine-api"><b>Backend Source</b></a> · 
  <a href="https://github.com/bharadwajbingi/tradestream-engine-ui"><b>Frontend Source</b></a>
</p>

---

## Other Projects

### Writebase
> Blogging platform | React, Node.js, Express, MongoDB, Gemini AI

Full-stack blog with rich-text editing, content categorization, cloud media uploads, and AI-powered writing assistance via Google Gemini.

<a href="https://writebase.vercel.app/">Live Demo</a> · <a href="https://github.com/bharadwajbingi/writebase">Source Code</a>

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

Frontend: React 18 + TypeScript → REST API → Backend Services
```

---

## Stats

<div align="center">
  <img src="https://leetcard.jacoblin.cool/bharadwajbingi?theme=dark&font=Baloo&ext=contest" alt="LeetCode" width="48%" />
  <img src="https://github-readme-streak-stats.herokuapp.com?user=bharadwajbingi&theme=dark" alt="GitHub Streak" width="48%" />
</div>

---

*Open to Java Backend Engineer roles. Let's connect: bharadwajbingi555@gmail.com*
