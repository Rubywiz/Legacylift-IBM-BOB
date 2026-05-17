# LegacyLift

> **AI-powered legacy modernisation. 18 months of technical debt. 24 hours with Bob.**

[![Hackathon](https://img.shields.io/badge/hackathon-IBM%20Bob%20May%202026-blue)](https://lablab.ai/ai-hackathons/ibm-bob-hackathon)
[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://cargotracker-ibm-bob.vercel.app/)
[![Risk Engine](https://img.shields.io/badge/risk%20engine-Node.js-green)](https://github.com/Rubywiz/Legacylift-IBM-BOB)
[![Stack](https://img.shields.io/badge/stack-Jakarta%20EE%2010%20%7C%20React%20%7C%20Node.js-orange)](https://github.com/Rubywiz/Legacylift-IBM-BOB)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue)](LICENSE.md)

---

> **[Live Dashboard →](https://cargotracker-ibm-bob.vercel.app/)**  
> **[Bob Analysis Output →](bob-outputs/)**  
> **[Hackathon Submission →](HACKATHON.md)**  
> **[Modernisation Roadmap →](bob-outputs/modernisation-plan.md)**

---

## Why LegacyLift?

Enterprise Java applications carry decades of risk — outdated dependencies, unscored CVEs, monolithic bounded contexts with no migration plan, and modernisation timelines measured in years. Most organisations don't even know where to start.

LegacyLift changes that. We fed IBM Bob a production-grade Jakarta EE 10 application — **Eclipse Cargo Tracker**, 105 source files, 20 dependencies, built on Domain-Driven Design — and told it to analyse, plan, and modernise. No hand-holding. No pre-written scripts. Just Bob doing what it does.

The result: **44% risk reduction in 24 hours**, two critical CVEs patched, a complete modernisation roadmap, and a live risk dashboard built entirely by AI.

---

## What Bob Did

| # | Action | Output |
|---|--------|--------|
| 01 | Read all 105 source files and mapped every dependency | `dependency-map.json` |
| 02 | Scored risk across 6 DDD modules and 4 risk categories | `risk-summary.json` |
| 03 | Generated architecture diagrams and bounded context maps | `architecture-diagram.md` |
| 04 | Planned safe modernisation with human approval gates | `modernisation-plan.md` |
| 05 | Pinned `commons-lang3` to `3.14.0` — eliminating both critical CVEs | commit `3dc333` |
| 06 | Added cloud-native batch REST endpoint | `src/` |
| 07 | Improved Javadoc on `HandlingEventFactory` | `src/` |
| 08 | Re-analysed entire codebase post-changes | `risk-summary-after.json` |

**Verified outcome: 35.7% risk reduction on the Handling bounded context. 44% overall.**

---

## Impact

| Metric | Before Bob | After Bob |
|--------|-----------|-----------|
| Overall risk score | 68 / 100 | 38 / 100 |
| Handling context risk | 70 — HIGH | 45 — MEDIUM |
| Critical CVEs | 2 | 0 |
| Estimated remediation cost | $147,000 | $120,000 |
| Estimated timeline | 18 months | 14 months |
| Time Bob needed | — | **24 hours** |

---

## Bob Modes Used

| Mode | How we used it |
|------|---------------|
| **Ask** | Initial codebase orientation across all 105 files |
| **Advanced** | Deep dependency analysis and CVE scoring |
| **Plan** | Modernisation planning with human approval gates |
| **Code** | Built the Risk Engine API and React dashboard |
| **Orchestrator** | Coordinated multi-file redesign across bounded contexts |
| **BobShell** | Full audit trail — every action logged and reviewable |

---

## DDD Bounded Context Risk Map

| Context | Score | Status |
|---------|-------|--------|
| Interfaces | 80 | 🔴 Critical |
| Infrastructure | 75 | 🔴 Critical |
| Handling | 70 → **45** | ✅ Modernised by Bob |
| Cargo | 65 | 🟠 High |
| Voyage | 45 | 🟡 Medium |
| Location | 40 | 🟢 Low |

---

## Project Structure

```
legacylift-ibm-bob/
├── src/                          # Jakarta EE 10 legacy Java application
├── bob-outputs/                  # Everything Bob generated
│   ├── risk-summary.json         # Pre-modernisation risk scores
│   ├── risk-summary-after.json   # Post-modernisation risk scores
│   ├── dependency-map.json       # 20 dependencies with CVE scoring
│   ├── architecture-diagram.md   # DDD bounded context maps
│   ├── modernisation-plan.md     # Handling context modernisation plan
│   └── java17-upgrade-plan.md    # Java 17 upgrade roadmap
├── risk-engine/                  # Node.js API serving risk data
├── dashboard/                    # React risk visualisation dashboard
├── pom.xml                       # Maven build
└── HACKATHON.md                  # Full hackathon write-up
```

---

## Quick Start

### Prerequisites

| Tool | Version | Install |
|------|---------|---------|
| Java | 11+ | [adoptium.net](https://adoptium.net) |
| Maven | 3.8+ | [maven.apache.org](https://maven.apache.org) |
| Node.js | 18+ | [nodejs.org](https://nodejs.org) |

### Run the Risk Engine API

```bash
cd risk-engine
npm install
npm start
# API running at http://localhost:3001
```

### Run the Dashboard

```bash
cd dashboard
npm install
npm run dev
# Dashboard running at http://localhost:5173
```

Or just use the **[live demo →](https://cargotracker-ibm-bob.vercel.app/)**

---

## Roadmap

Bob generated a full modernisation plan. Here's what's next:

- [ ] Java 11 → 17 LTS upgrade *(full plan in `bob-outputs/java17-upgrade-plan.md`)*
- [ ] H2 → PostgreSQL migration
- [ ] MicroProfile Health endpoints
- [ ] Circuit breaker on `ExternalRoutingService`
- [ ] OpenAPI documentation
- [ ] GitHub Actions CI with automated Bob re-analysis on every PR

---

## Built With

- **IBM Bob** — AI agent (Ask, Advanced, Plan, Code, Orchestrator, BobShell modes)
- **Eclipse Cargo Tracker** — Jakarta EE 10 reference application (base codebase)
- **Node.js + Express** — Risk Engine API
- **React + Vite + Tailwind** — Risk Dashboard
- **Vercel** — Dashboard deployment

---

## Team

**Team Status 200** — IBM Bob Hackathon, May 2026

> *Built by Ruby O. Khupe*

---

## License

[Apache 2.0](LICENSE.md)
