<div align="center">

# Vignesh Chintakayala

**Solo Founder & Full-Stack AI Engineer** · Building production AI SaaS with Claude Code as daily driver

[![Location](https://img.shields.io/badge/Jersey_City,_NJ-0A0A0A?style=flat-square&logo=googlemaps&logoColor=white)](#)
[![Status](https://img.shields.io/badge/F1_OPT-Authorized_to_Work_in_US-1f6feb?style=flat-square)](#)
[![Education](https://img.shields.io/badge/MS_MIS-Stevens_Institute_of_Technology-A31F34?style=flat-square)](#)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vignesh-chintakayala-a009b4172/)

</div>

---

## What I'm building

**VelocityFlow Automations** — an AI-native outreach and workflow platform for SMBs, unifying voice (Bland AI), SMS (Twilio A2P 10DLC), email (SendGrid), and WhatsApp Business into a single agent-orchestrated pipeline. Launching end of April 2026. Wyoming LLC formed, EIN obtained, Mercury bank account live, full TCPA / FTC DNC / A2P 10DLC compliance in place.

## The numbers

A single-operator codebase, built and shipped solo:

| VelocityFlow Automations |  | Einstein Brain Server |  |
|---|---:|---|---:|
| Commits on `main` | **670** | Routing rules | **186** |
| Backend API endpoints (FastAPI) | **132** | Circuit breaker layers | **8** |
| AI agent files | **47** | MCP tools exposed | **59** |
| Frontend pages (React 18 + Vite) | **40** | Golden-set nDCG@5 | **0.883** |
| Frontend components | **181** | Golden-set MRR | **0.901** |
| Active branches | **22** | Mean retrieval latency | **436 ms** |

Eval pipeline on 25-query golden dataset: **hit_rate 0.96**, **recall@5 0.92**, **MRR 0.901**, **nDCG@5 0.883**.

## How I build

Claude Code is my daily driver. Every feature in VelocityFlow — from the FastAPI endpoints to the React components to the Stripe billing flow — was shipped in partnership with **Claude Opus 4.6** (co-author visible in git log), with **Sonnet** and **Haiku** powering the in-product agents themselves. Local development runs on a MacBook Air with the Claude Max subscription and a Claude Code CLI — no API-key billing for my own dev loop. For code review I lean on **Ollama** running `qwen3:8b` locally. This is not a hobby workflow; it's how a solo operator ships a 670-commit production system.

## Engineering systems I've designed

- **MCP server** — a Model Context Protocol server exposing 59 tools to Claude, giving the orchestrator typed access to the full build environment.
- **8-layer circuit breaker** — token budget, cost cap, error rate, time limit, action count, file scope, API rate, and a deadman switch, enforced before any agent action executes.
- **Autonomy governance (L1–L4)** — per-agent, per-operation autonomy levels. Auth, billing, and TCPA-touching operations are hard-pinned to L1 (observe-only) across every agent, always.
- **Model tiering** — Opus for orchestration, Sonnet for specialist work, Haiku for routing and classification. Every agent carries a stable 1,500-token prefix to keep KV-cache hits predictable.
- **Hybrid retrieval** — BM25 + vector embeddings + KuzuDB graph traversal + temporal ranking, feeding a 110-node knowledge graph.
- **Eval harness** — golden-dataset regression tests on nDCG@5, MRR, hit_rate, recall@5, and latency, run on every registry change.
- **Path-traversal-hardened self-healer** — filesystem-modifying agents are gated by a dedicated `UnsafeRelatedPath` exception.

## VelocityFlow stack highlights

- **Backend:** FastAPI · Python · Celery · Redis · PostgreSQL · Supabase
- **Frontend:** React 18 · TypeScript · Vite · Tailwind · custom "Liquid Glass" dark/light design system
- **Billing:** Stripe — 4 tiers, webhooks, trial logic, `BillingGate` enforcement
- **Messaging:** Bland AI · Twilio A2P 10DLC · SendGrid · WhatsApp Business
- **Infra:** Docker · Railway · Sentry · CI/CD on every push

## Core stack

<p>
<img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
<img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img alt="React" src="https://img.shields.io/badge/React_18-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img alt="Tailwind" src="https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
<img alt="Supabase" src="https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white" />
<img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
<img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img alt="Railway" src="https://img.shields.io/badge/Railway-0B0D0E?style=for-the-badge&logo=railway&logoColor=white" />
<img alt="Claude" src="https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white" />
</p>

## Connect

- **LinkedIn:** [vignesh-chintakayala](https://www.linkedin.com/in/vignesh-chintakayala-a009b4172/)
- **Email:** mailforyouvignesh07@gmail.com

---

> My production work — VelocityFlow Automations and the Einstein Brain server that orchestrates it — lives in private repositories. The public repos here are older academic and capstone work and are not representative of what I ship today. Happy to walk through the real codebase in a conversation.
