# HabitatX

Welcome to the **HabitatX** codebase! This repository is a **monorepo** powering the complete HabitatX platform — including the web application, backend services, and blockchain payment infrastructure.

HabitatX is a next-generation housing marketplace built to simplify renting. It helps property owners publish listings and manage tenants while enabling renters to discover trusted spaces, compare real experiences, and handle rent transactions digitally — without relying on traditional agents.

We use **[pnpm workspaces](https://pnpm.io/workspaces)** for dependency management and **[TurboRepo](https://turbo.build/)** for fast, scalable builds.

---

## 🚀 Tech Stack

- **Monorepo:** pnpm workspaces + TurboRepo  
- **Frontend:** React + TailwindCSS  
- **Backend:** Node.js, Express, TypeScript  
- **Payments Layer:** Stellar SDK  
- **Language:** TypeScript (Strict Mode)

---

## 🛠 Requirements

Before running the project, make sure you have:

1. **Node.js** (v18+)  
2. **pnpm**

```bash
corepack enable
# OR
npm install -g pnpm
````

---

## ⚡ Quick Start

### 1. Clone & Install

```bash
git clone <your-repo-url>
cd habitatx

# Install dependencies across all apps & packages
pnpm install
```

### 2. Start Development

Run all services together:

```bash
pnpm dev
```

Local services:

* **Frontend:** [http://localhost:3000](http://localhost:3000)
* **API Server:** [http://localhost:3001](http://localhost:3001)
* **Payment Service:** [http://localhost:3002](http://localhost:3002)

---

## 📦 Monorepo Structure

```text
habitatx/
├── apps/
│   ├── web/               # Client application (Renters & Owners)
│   ├── api/               # Main REST API (Express)
│   └── stellar-service/   # Blockchain payment & transaction handler
│
├── packages/
│   ├── types/             # Shared interfaces, schemas, DTOs
│   ├── config/            # Shared linting & TS configurations
│   └── ui/                # Reusable UI components
│
└── turbo.json             # TurboRepo pipeline
```

---

## 📜 Scripts

Run from the project root:

| Command      | What it does                         |
| ------------ | ------------------------------------ |
| `pnpm dev`   | Starts all applications in dev mode  |
| `pnpm build` | Builds all apps and shared packages  |
| `pnpm lint`  | Runs lint checks across the monorepo |
| `pnpm test`  | Runs tests (when available)          |
| `pnpm clean` | Clears caches and build artifacts    |

---

## ➕ Installing Dependencies

Because HabitatX uses a monorepo setup, install dependencies inside the appropriate workspace.

**Frontend example**

```bash
cd apps/web
pnpm add react-query
```

**Backend example**

```bash
cd apps/api
pnpm add prisma
```

**Using shared workspace packages**

```bash
cd apps/api
pnpm add "@habitatx/types@workspace:*" -D
```

---

## 🧭 Platform Overview

HabitatX is built around a dual-sided marketplace model.

### 🧑 Renters

* Explore available homes, shops, and spaces
* Compare listings using reviews and ratings
* Contact owners directly
* Manage renewals and payments online

### 🏠 Property Owners

* Publish and manage property listings
* Track interest and tenant applications
* Communicate directly with renters
* Receive payments through integrated digital rails

---

## 🌟 Reputation-Driven Housing

HabitatX focuses heavily on **trust signals**.

Every property can build a public reputation through:

* Tenant reviews
* Ratings
* Experience feedback
* Owner responsiveness

This helps renters make smarter decisions and encourages higher standards from property owners.

---

## 💸 Digital Payments

HabitatX integrates with the **Stellar ecosystem** to support secure, low-friction rent payments and renewals.

Blockchain usage is intentionally focused on payments to keep the user experience simple and practical.

---

## 🧯 Common Issues

### Dependency or Type Errors

```bash
pnpm install

# If problems persist:
rm -rf node_modules
pnpm install
```

### Files unexpectedly ignored by Git

Build outputs and dependencies are intentionally excluded.

If needed:

```bash
git rm -r --cached .
git add .
git commit -m "fix: reset git cache"
```

---

## 🤝 Contributing

HabitatX is open-source and built for collaboration.

We welcome:

* Feature contributions
* Performance improvements
* UI/UX enhancements
* Documentation updates
* Bug fixes

Contribution basics:

1. Fork the repository
2. Create a feature branch
3. Make focused commits
4. Open a Pull Request

Please run:

```bash
pnpm lint
```

before submitting PRs.

---

## 🔮 Vision

HabitatX aims to redefine how people find and manage spaces — transforming renting into a transparent, community-driven experience where reputation, convenience, and digital payments work together.

Built by developers, for real-world housing challenges.

```
```
