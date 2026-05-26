# Hi there 👋 I'm Bharadwaj Bingi  

### **Backend Engineer | Enterprise Java & Spring Boot Specialist**  
🚀 Building enterprise-grade, high-performance distributed systems with focus on asynchronous batch pipelines, multi-layer security, and resilient cloud architectures.

---

## 🛠️ Tech Ecosystem  

### **Programming Languages**
![Java](https://img.shields.io/badge/Java_17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

### **Backend & Core Frameworks**
![Spring Boot](https://img.shields.io/badge/Spring_Boot_4.0-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Spring Batch](https://img.shields.io/badge/Spring_Batch-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate_ORM-59666C?style=for-the-badge&logo=hibernate&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API_Design-009688?style=for-the-badge&logo=api&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)

### **Database & Connections**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_15-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway_Migrations-CC292B?style=for-the-badge&logo=flyway&logoColor=white)
![HikariCP](https://img.shields.io/badge/HikariCP-FF6F00?style=for-the-badge&logo=connection&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)

### **Cloud & DevOps**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-232F3E?style=for-the-badge&logo=amazons3&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)

### **Security Systems**
![JWT](https://img.shields.io/badge/JWT_Auth-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![OAuth2](https://img.shields.io/badge/OAuth_2.0-3F51B5?style=for-the-badge&logo=oauth&logoColor=white)
![AES-256](https://img.shields.io/badge/AES_256_GCM-4CAF50?style=for-the-badge&logo=security&logoColor=white)
![TOTP 2FA](https://img.shields.io/badge/TOTP_2FA-E91E63?style=for-the-badge&logo=googleauthenticator&logoColor=white)

### **Testing & Quality**
![JUnit5](https://img.shields.io/badge/JUnit_5-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![Mockito](https://img.shields.io/badge/Mockito-FF9800?style=for-the-badge&logo=mock&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-00C853?style=for-the-badge&logo=docker&logoColor=white)

---

## ⚡ Featured Project

### 🛡️ **TradeStream Engine — Enterprise Trade Ingestion Platform**
> **Java 17, Spring Boot 4.0, Spring Batch, PostgreSQL, AWS S3, Docker, GitHub Actions**  
> *Enterprise-grade asynchronous trade file ingestion, verification, and lifecycle management system*  
> 🔗 **Live Demo:** [d2i9y8go17l95q.cloudfront.net](https://d2i9y8go17l95q.cloudfront.net/)

- **High-Performance Ingestion:** Architected a **5-module Maven system** (API, Service, Batch, DAO, Model) that ingests massive financial trade CSV files (up to **1GB**) with sub-second HTTP 202 upload response, processing them completely asynchronously via a robust scheduler-driven queue.
- **Robust Processing Pipeline:** Engineered a chunk-based Spring Batch pipeline (**250 records/chunk**) featuring 21-field semantic validation, real-time progress indicators, in-batch duplicate detection using high-concurrency memory structures (`ConcurrentHashMap`), and bulk database deduplication.
- **Enterprise-Grade Security:** Enforced stateless **JWT authentication** (HMAC-SHA256, 30-min expiry), Google **OAuth2** auto-registration, multi-factor **TOTP 2FA** for sensitive file exports with dynamic secret keys encrypted at rest via **AES-256-GCM**, IP-based rate limiting (120 req/min), and deep multi-tenant row-level data isolation using JPA Specifications.
- **Resilient Database Architecture:** Structured a highly normalized PostgreSQL schema (9 tables) equipped with schema-migration control via **Flyway**, custom indexes on key search paths (`file_id`, `transaction_id`), and Hibernate validation mode to eliminate schema drift risk.
- **Audit-First Archival Pipeline:** Constructed an asynchronous AWS S3 export pipeline utilizing pre-signed secure URLs, automated background cleanup tasks for expired files via scheduled tasks, and a soft-delete architecture preserving exhaustive audit trails across historic data tables.
- **Production-Grade DevOps & CI/CD:** Developed a full-cycle GitHub Actions workflow incorporating JUnit 5 unit-gating, Docker multi-stage builds published to DockerHub, and SSH deployment to AWS EC2. Integrates an auto-recovery background service that resumes interrupted chunk ingestion on container restarts.
- **Paginated Search & Query APIs:** Exposed 20+ REST endpoints utilizing dynamic filtering based on JPA Criteria APIs, allowing seamless paginated lookup across file metadata, trade validation errors, and clean records.
- **Enterprise Testing Rigour:** Maintained high quality metrics using **JUnit 5**, **Mockito** mock objects, parameterized edge-case validators, and **Testcontainers PostgreSQL** integration environments, measured using **JaCoCo** reports.

---

## 🧩 Other Projects

### 📝 **Writebase — Rich Blogging Platform (Full-Stack)**
> **React, Node.js, Express, MongoDB, Tailwind CSS, JWT, ImageKit, Google Gemini AI**
- Developed a highly interactive blogging platform with rich-text capabilities, content categorization, and secure cloud media uploads.
- Integrated **Google Gemini AI** to empower creators with real-time editing assistants, content ideas, and semantic text suggestions.
- Enforced stateless user sessions using JWT security and styled with fully custom glassmorphic Tailwind designs.
- [Live Demo](https://writebase.vercel.app/) | [Source Code](https://github.com/bharadwajbingi/writebase)

### 🛍️ **Lazyvastra — Custom D2C E-commerce Brand (Shopify & Liquid)**
> **Shopify Liquid, Custom Themes, JavaScript, CSS3, Payment Gateways (Razorpay & Stripe)**
- Founded and launched Lazyvastra, a custom direct-to-consumer e-commerce clothing brand.
- Designed and built highly responsive Shopify store fronts from scratch, creating custom Shopify Liquid themes that drove storefront conversion rates up by **25%**.
- Integrated secure Razorpay and Stripe API payment pipelines to process customer checkouts seamlessly.
- Designed automated inventory sync controls and optimized media assets, reducing page loading latency by **40%**.

---

## 🏅 Professional Certifications
- **Smart Coder Program** — Masters in Data Structures & Algorithms, *Smart Interviews*
- **Complete Web Development Masterclass** — Full-Stack Engineering, *Udemy*
- **Git & GitHub Essentials** — Advanced Version Control & CI/CD workflows

---

## 📊 Analytics & Coding Metrics
<div align="center">
  <table border="0">
    <tr>
      <td width="50%" align="center">
        <img src="https://leetcard.jacoblin.cool/bharadwajbingi?theme=dark&font=Baloo&ext=contest" alt="LeetCode Stats" width="100%" />
      </td>
      <td width="50%" align="center">
        <img src="https://github-readme-stats.vercel.app/api?username=bharadwajbingi&show_icons=true&theme=radical" alt="GitHub Stats" width="100%" />
      </td>
    </tr>
    <tr>
      <td width="50%" align="center">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=bharadwajbingi&layout=compact&theme=radical" alt="Top Languages" width="100%" />
      </td>
      <td width="50%" align="center">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=bharadwajbingi&repo=writebase&theme=radical" alt="Writebase Pin" width="100%" />
      </td>
    </tr>
  </table>
  <br/>
  <img src="https://github-readme-streak-stats.herokuapp.com?user=bharadwajbingi&theme=radical" alt="GitHub Streak" width="100%" />
</div>

---

## 📫 Connect & Collaborate

<div align="center">
  <a href="https://linkedin.com/in/bharadwajbingi" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>&nbsp;&nbsp;
  <a href="https://github.com/bharadwajbingi" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge"/>
  </a>&nbsp;&nbsp;
  <a href="https://leetcode.com/bharadwajbingi" target="_blank">
    <img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode Badge"/>
  </a>&nbsp;&nbsp;
  <a href="mailto:bharadwajbingi555@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Badge"/>
  </a>
</div>

<br/>
<div align="center">
  <sub>Built with ❤️ by Bharadwaj Bingi.</sub>
</div>
