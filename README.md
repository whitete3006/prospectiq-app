# prospectiq-app
prospectiq-app/
├── package.json                   # Root monorepo workspace configuration
├── .env.example                   # Environment configuration template
├── README.md                      # Quickstart documentation
│
├── apps/
│   ├── backend/                   # Node.js + Express + TypeScript Backend
│   │   ├── package.json           # Backend dependencies (playwright, express, prisma, bullmq)
│   │   ├── tsconfig.json          # TypeScript compiler config
│   │   ├── prisma/
│   │   │   └── schema.prisma      # PostgreSQL multi-tenant database models
│   │   └── src/
│   │       ├── server.ts          # REST API server entrypoint
│   │       ├── middlewares/
│   │       │   └── tenantAuth.ts  # Multi-tenant authentication header validation
│   │       └── scrapers/
│   │           └── playwrightEngine.ts # Headless scraper engine
│   │
│   └── frontend/                  # Web Dashboard UI
│       ├── package.json           # Static server launcher
│       ├── index.html             # Tailwind CSS portal interface
│       └── src/
│           └── js/
│               └── app.js         # API integration & lead pipeline logic
