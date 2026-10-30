### Hi there, I'm Faisal Ahamed Rahad 👋

  Full-stack developer experienced in building and deploying multi-tenant SaaS, e-commerce, and ERP systems. Specializes in Next.js, GraphQL, Node.js, Prisma, and PostgreSQL, with expertise in system architecture, RBAC, payment integration, and cloud deployment. Focused on scalable solutions, efficient development, and emerging technologies.


  🌐 **Portfolio:** https://portfolio-2026-alpha-blush.vercel.app/
  💼 **LinkedIn:** https://www.linkedin.com/in/rahad-dev24/
  📫 **Email:** rahad.dev24@gmail.com
  ✅ **Open to work** — full-time or contract, remote-friendly


  ---

  #### 🛠️  Tech Stack

  <p>
    <img src="https://img.shields.io/badge/Next.js-000?style=for-the-badge&logo=next.js&logoColor=white" />
    <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
    <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" />
    <img src="https://img.shields.io/badge/shadcn/ui-000?style=for-the-badge&logo=shadcnui&logoColor=white" />
    <img src="https://img.shields.io/badge/Framer_Motion-0055FF?style=for-the-badge&logo=framer&logoColor=white" />
  </p>

  <p>
    <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" />
    <img src="https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white" />
    <img src="https://img.shields.io/badge/Apollo_Server-311C87?style=for-the-badge&logo=apollographql&logoColor=white" />
    <img src="https://img.shields.io/badge/Express-000?style=for-the-badge&logo=express&logoColor=white" />
    <img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" />
    <img src="https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=sequelize&logoColor=white" />
  </p>

  <p>
    <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
    <img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white" />
    <img src="https://img.shields.io/badge/Redis-DD0031?style=for-the-badge&logo=redis&logoColor=white" />
    <img src="https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white" />
    <img src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
  </p>

  <p>
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
    <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" />
    <img src="https://img.shields.io/badge/PM2-2B037A?style=for-the-badge&logo=pm2&logoColor=white" />
    <img src="https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white" />
    <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
    <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
  </p>

  <p>
    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
    <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" />
    <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  </p>


  ---

  #### 🚀 Currently building

  - **[School SaaS](https://school-saas-demo-two.vercel.app/)** — production-ready multi-tenant school management platform. Subdomain tenancy, role-gated GraphQL, Redis caching with
  auto-invalidation, bKash + PayStation payments, exam scheduling, fees, attendance, payroll, library, question bank, automated SMS.

  - **SchoolOS (Expo)** — companion mobile app for the school SaaS. One binary serves every school: students enter their school's host URL at first launch (the setup screen pings the API
  before locking it in), and every GraphQL call routes through that host. Built on a SQLite read-through cache so the dashboard keeps working offline — successful queries are written back, and
   on network failure the last-known data is served with a "stale" banner. Hand-rolled session-cookie jar over React Native's cookieless `fetch`, per-tenant cache isolation, Expo push tokens
  registered/unregistered on login/logout, and AdMob for monetization.
    Tech: Expo SDK 56, React Native 0.85, React 19.2, TypeScript 6, Expo Router, expo-sqlite, expo-notifications, expo-secure-store, expo-image, react-native-reanimated 4,
  react-native-google-mobile-ads, GraphQL.

  - **NexCart** — Bangladesh-first e-commerce platform built as a **Turborepo monorepo**: Next.js 15 storefront, separately-gated Next.js 15 admin panel, Apollo Server v4 on Express, and an
  Expo React Native app — all sharing a typed GraphQL contract via codegen. Per-user data (carts, orders) lives on **hash-sharded PostgreSQL** routed by `userId` through a custom
  `ShardRouter`; the catalog and auth stay on a primary. Three payment paths live behind one provider interface — **bKash Tokenized Checkout, SSLCommerz, Stripe**. Redis cache-aside +
  cache-on-write with hit/miss counters surfaced via `prom-client` on `/metrics`, DataLoader-backed resolvers, and time-bounded TTL clamping on Hot Deals so stale promotions can't linger past
  `endsAt`. Idempotent `deploy.sh` with `flock`, health-check polling, tarball/registry image shipping, and one-flag rollback to a previously-loaded image tag.
    Tech: Turborepo + pnpm, Next.js 15 (App Router), TypeScript, Auth.js v5, TanStack Query, Zustand, Apollo Server v4 + Express, GraphQL Codegen, Prisma 5, DataLoader, PostgreSQL 16
  (sharded), Redis (ioredis), Stripe / bKash / SSLCommerz, Expo Router, Sentry, prom-client, Nginx, Docker Compose, Jest, Playwright, lefthook.

  ---

  #### 💼 Experience

  - **Full Stack Developer** — MRAM Technologies *(Apr 2025 – Aug 2025)*
    Lead on a multi-tenant school SaaS, supervised 2 junior devs, shipped 5+ modules, integrated bKash + PayStation, optimized slow queries.
  - **Associate Software Engineer** — BayShore Communications *(Oct 2024 – Mar 2025)*
    Migrated legacy Next.js projects to Next.js 15, shipped a project from scratch, contributed to 10+ running projects.

  ---

  #### 🎓 Education

  - **MS in CSE** — Jahangirnagar University (2021 – 2023) • CGPA 3.2/4
  - **BS in CSE** — Gono Bishwabidyalay, Savar (2016 – 2020) • CGPA 3.41/4

  ---

  #### 🌱 Right now

  - Learning **FastAPI**
  - Watching where Next.js / React Server Components go next
  - Trying to keep things simple

  ---

  #### About me

  - 👀 Interested in cats, anime, and coding
  - 😄 Pronouns: well... it's not she/her 😄
  - ⚡ Fun fact: cat music is the best remedy for debugging code 😆
  - 📫 You're already here — might as well drop a ⭐ and mail me at **rahad.dev24@gmail.com**

  ---

  <p align="center">
    <img src="https://komarev.com/ghpvc/?username=rahad-dev24&style=for-the-badge&color=blueviolet" alt="Profile views" />
  </p>

  <p align="center">
    <a href="https://portfolio-2026-alpha-blush.vercel.app/">Portfolio</a> •
    <a href="https://www.linkedin.com/in/rahad-dev24/">LinkedIn</a> •
    <a href="mailto:rahad.dev24@gmail.com">Email</a> •
    <a href="https://github.com/rahad-dev24">GitHub</a>
  </p>
