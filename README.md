# BioMinute Shorts Studio 🎬

> AI-powered health-science YouTube Shorts production pipeline — from master plan spreadsheet to published video.

[![Version](https://img.shields.io/badge/version-v0.2.0-blue.svg)](VERSION.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-teal.svg)](LICENSE)
[![Node](https://img.shields.io/badge/Node-24-green.svg)](https://nodejs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-blue.svg)](https://www.typescriptlang.org)
[![pnpm](https://img.shields.io/badge/pnpm-workspaces-orange.svg)](https://pnpm.io)
[![React](https://img.shields.io/badge/React-19-61DAFB.svg)](https://react.dev)
[![Status](https://img.shields.io/badge/Status-Active-success)](https://github.com/0utLawzz/biominute-shorts-studio)

## What is this?

**BioMinute Shorts Studio** is a monorepo production system for the **BioMinute** health channel — 60-second, science-backed YouTube Shorts. Full episode lifecycle: spreadsheet master plan → animated scenes → export → review → publish.

---

## Pipeline flow

```mermaid
flowchart LR
    A[Master Plan XLSX] --> B[biominute-reels React scenes]
    B --> C[export-video Playwright + ffmpeg]
    C --> D[exports/Episode-NN-slug/]
    D --> E[publishing-dashboard]
    E --> F[api-server + YouTube Data API]
    F --> G[YouTube Shorts]
```

---

## Workspace layout (core)

| Package / path | Role |
|----------------|------|
| `artifacts/biominute-reels` | Animated episode scenes |
| `artifacts/publishing-dashboard` | Review, approve, metadata |
| `artifacts/api-server` | API + YouTube publish |
| `lib/db` | Drizzle / Postgres |
| `exports/` | Generated episode media |
| `docs/` | INSTALL, RUN, USAGE |

---

## Quick start

```bash
git clone https://github.com/0utLawzz/biominute-shorts-studio.git
cd biominute-shorts-studio
pnpm install
pnpm --filter @workspace/db push-force
pnpm --filter @workspace/scripts exec tsx ./src/seed-episodes.ts
# Start api-server, publishing-dashboard, biominute-reels in separate terminals
```

Full docs: [`docs/INSTALL.md`](docs/INSTALL.md) · [`docs/RUN.md`](docs/RUN.md) · [`docs/USAGE.md`](docs/USAGE.md)

---

## Contributing & Security

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

---

## License

MIT © BioMinute Studio / Nadeem (OutLawZ) — see [LICENSE](LICENSE).

---

## Author

**Nadeem (OutLawZ)**  
Custom Automation Specialist  

- GitHub: [0utLawzz](https://github.com/0utLawzz)  
- Contact: net2outlawzz@gmail.com  

*Need custom YouTube Shorts / content production automation? Contact me.*
