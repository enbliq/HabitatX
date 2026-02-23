# HabitatX

Welcome to **HabitatX**! This is a **monorepo** managing the frontend, backend API, and Stellar payment services for the HabitatX platform.

HabitatX is a rental marketplace connecting **landlords** and **tenants** directly — removing middlemen by enabling property listings, transparent reviews, and seamless rent payments.

We use **[pnpm workspaces](https://pnpm.io/workspaces)** for dependency management and **[TurboRepo](https://turbo.build/)** for high-performance build orchestration.

---

## 🚀 Tech Stack

- **Monorepo Manager:** pnpm workspaces + TurboRepo  
- **Frontend:** React + TailwindCSS  
- **Backend:** Node.js, Express, TypeScript  
- **Payments:** Stellar SDK  
- **Language:** TypeScript (Strict Mode)

---

## 🛠 Prerequisites

Before you start, ensure you have the following installed:

1. **Node.js** (v18 or higher recommended)  
2. **pnpm** (We use this instead of npm/yarn)

```bash
corepack enable
# OR
npm install -g pnpm
````

---

## ⚡️ Getting Started

Follow these steps to get the entire platform running locally.

### 1. Clone & Install

```bash
git clone <your-repo-url>
cd HabitatX

# Install all dependencies for all apps and packages
pnpm install
```

### 2. Run Development Server

This command starts **all** applications (Web, API, and Stellar Service) in parallel.

```bash
pnpm dev
```

You will see output from all services in your terminal. They are available at:

* **Web App:** [http://localhost:3000](http://localhost:3000)
* **Backend API:** [http://localhost:3001](http://localhost:3001)
* **Stellar Service:** [http://localhost:3002](http://localhost:3002)

---

## 📂 Project Structure

```text
HabitatX/
├── apps/
│   ├── web/               # React Frontend (Tenant & Landlord Interface)
│   ├── api/               # Core Backend API (Express + Node.js)
│   └── stellar-service/   # Isolated Service for Payments
│
├── packages/
│   ├── types/             # Shared TypeScript interfaces & DTOs
│   ├── config/            # Shared configurations (TSConfig, ESLint)
│   └── ui/                # Shared React UI components (Tailwind)
│
└── turbo.json             # Build pipeline configuration
```

---

## 📜 Available Scripts

Run these from the **root** folder:

| Command      | Description                                  |
| ------------ | -------------------------------------------- |
| `pnpm dev`   | Starts all apps in development mode.         |
| `pnpm build` | Builds all apps and packages for production. |
| `pnpm lint`  | Runs ESLint across the entire monorepo.      |
| `pnpm test`  | Runs tests for all packages (when added).    |
| `pnpm clean` | Clears Turbo cache and artifacts.            |

---

## 🧩 Adding Dependencies

Since we use a monorepo, you must specify **where** to install a package.

**To add a library to the Frontend (`apps/web`):**

```bash
cd apps/web
pnpm add framer-motion
```

**To add a library to the Backend (`apps/api`):**

```bash
cd apps/api
pnpm add mongoose
```

**To use a shared package (example: shared types):**

```bash
cd apps/api
pnpm add "@HabitatX/types@workspace:*" -D
```

---

## 🏠 Core Platform Idea

HabitatX is designed around two primary user roles:

### 👤 Tenants

* Browse and discover properties
* View building and landlord reviews
* Apply directly without agents
* Renew rent through the platform

### 🏢 Landlords

* Advertise houses, shops, lands, and buildings
* Manage listings and tenants
* Receive secure payments
* Build credibility through reviews

---

## ⭐ Trust & Transparency

HabitatX introduces a reputation layer where tenants can leave honest reviews about properties and landlords, helping create a more transparent and trustworthy rental ecosystem.

---

## 💸 Payments

Rent payments and renewals are powered by the **Stellar ecosystem**, enabling efficient and secure transactions.

---

## ⚠️ Troubleshooting

**"Module not found" or Type Errors**

If you just pulled fresh code or switched branches:

```bash
pnpm install
# If issues persist, force a clean install
rm -rf node_modules
pnpm install
```

**Git is ignoring files I want to commit**

We strictly ignore `node_modules` and build artifacts (`dist`, build caches).

* **Do not** force commit `node_modules`.
* If your `node_modules` are showing up in Git:

```bash
git rm -r --cached .
git add .
git commit -m "fix: clear cached node_modules"
```

---

## 🤝 Contribution Guidelines

HabitatX is open-source and community-driven — contributions are welcome from developers of all levels.

1. Always run `pnpm lint` before pushing.
2. Keep shared logic (types, configs, UI) inside `packages/`.
3. Do not edit `apps/*/node_modules` manually.
4. Keep PRs focused and clearly described.

Whether you are fixing bugs, improving UI, or adding core features — your contribution matters.

---

## 🚀 Vision

HabitatX aims to become a trusted, agent-free rental marketplace where tenants and landlords connect directly, backed by community reviews and seamless digital payments.

Built with ❤️ by the community.

```
```
