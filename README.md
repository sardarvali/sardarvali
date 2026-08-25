# Syed Sardar Valli

**Backend engineer — Java · Spring Boot · PostgreSQL.** I build and operate
[ClassVault](https://www.classvault.page), a multi-tenant SaaS platform that is live in production
with its first institution.

B.Tech Computer Science & Engineering (Cloud Computing, with Google Cloud), Lovely Professional
University — graduated May 2026. Based in Bengaluru. **Open to backend and platform engineering
roles, available immediately.**

[![Portfolio](https://img.shields.io/badge/Portfolio-syedsardarvalli.web.app-1f6feb?style=flat-square)](https://syedsardarvalli.web.app)
[![ClassVault](https://img.shields.io/badge/Live_product-classvault.page-16a765?style=flat-square)](https://www.classvault.page)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-syed--sardar--valli-0a66c2?style=flat-square)](https://linkedin.com/in/syed-sardar-valli)
[![Email](https://img.shields.io/badge/Email-syedsardarvali246@gmail.com-c14438?style=flat-square)](mailto:syedsardarvali246@gmail.com)

---

## ClassVault — the work worth reading first

A multi-tenant school-management platform. Institutions are onboarded as tenants; there is no
individual self-signup. I designed it, built it, deployed it, and I operate it — alone.

**→ [Technical reference](https://github.com/sardarvali/ClassVault) · [Live platform](https://www.classvault.page)**
*(the repository is public documentation; the source itself is private)*

| | |
|---|---|
| **Backend** | Java 17 · Spring Boot 3.2 · PostgreSQL 16 · Redis · Flyway |
| **Scale** | 250+ REST endpoints across 118 controllers · 203 JPA entities · 210 tables · 170 migrations |
| **Tested** | 1,029 backend test methods across 120 test classes |
| **Features** | RBAC across 6 distinct roles · WebSocket/STOMP real-time messaging · Razorpay payments · Azure Blob storage |
| **Clients** | Next.js 15 / React 19 web console · native Kotlin Android app |
| **Runs on** | Docker · Nginx |

**The decision I'd most want to be asked about.** ClassVault originally ran on Azure Kubernetes
Service. I measured what the cluster actually cost against what the workload actually needed,
concluded the orchestration wasn't earning its keep, and re-architected it into a modular monolith on
Docker and Nginx — **with no downtime for the institution already depending on it.**

Choosing to remove infrastructure rather than add it, and executing that cutover against live users,
taught me more than any feature I have shipped.

---

## Other things I've built

**ClassConnect** — a role-based Android classroom app, ~22,500 lines of Kotlin across 161 files.
One APK serves student, teacher and admin. Firebase (Auth, Firestore, Storage, FCM, Crashlytics),
Hilt, coroutines and Flow, CameraX + ML Kit QR attendance, Gemini-powered features, and a live
XML → Jetpack Compose migration. Targets API 36. *Signed release build submitted and in production
review.*

**DeepFake Detector** — video authenticity classifier in PyTorch, served over FastAPI.
EfficientNet-B4 + BiLSTM, 93–96% AUC. The interesting part was diagnosing and correcting a bad class
imbalance in the training set rather than the architecture.

**[GAIL Gas Management](https://github.com/sardarvali/GAIL-gas-management-system)** — Kotlin Android
app for gas delivery tracking and customer management, on Firebase.

**[Docker-WebApp](https://github.com/sardarvali/Docker-WebApp)** — a 3-tier Node.js + MongoDB stack
wired together with Docker Compose, written as a working reference for containerisation.

---

## Stack, honestly tiered

I would rather tell you where I actually am than list every logo.

**Use daily** — Java · Spring Boot · PostgreSQL · REST API design · Docker · Git · Linux

**Comfortable** — Kotlin / Android · Next.js · React · TypeScript · Redis · Python · FastAPI ·
Nginx · Azure · SQL performance work

**Still learning properly** — Kubernetes · Terraform · CI/CD at team scale · observability

---

## Certifications

**Oracle Cloud Infrastructure 2025 — Generative AI Professional** (Oct 2025 – Oct 2027)
**Oracle Cloud Infrastructure 2025 — DevOps Professional** (Oct 2025 – Oct 2027)

---

## Experience & education

**Developer — ClassVault** (self-employed) · Sep 2025 – present
Designing, building and operating the platform described above.

**Industry Immersion Program, DevOps track — Broadridge Financial Solutions** · Jun – Jul 2025
Two-month programme; first exposure to enterprise DevOps practice.

**B.Tech, Computer Science & Engineering (Cloud Computing, with Google Cloud)**
Lovely Professional University, Punjab · Aug 2022 – May 2026

---

## Reach me

**syedsardarvali246@gmail.com** · [LinkedIn](https://linkedin.com/in/syed-sardar-valli) ·
[Portfolio](https://syedsardarvalli.web.app) · Bengaluru, India

*Happy to do a take-home task or a short paid trial — I'd rather show the work than describe it.*
