# GCC Intelligence Hub

AI-driven enterprise research engine for deep aftermarket intelligence.

## Architecture

- **Backend** (`backend/`): `gcc_pipeline.py` — two-phase Gemini pipeline. Deployed as part of [it-deals-api](https://github.com/vibhorkumar1209/it-deals-api) on Render.
- **Frontend** (`frontend/app/gcc-intel/`): Next.js page. Deployed as part of [it-deals-frontend](https://github.com/vibhorkumar1209/it-deals-frontend) on Vercel.
- **Live URL**: https://it-deals-frontend.vercel.app/gcc-intel

## Modules

### Module 1 — Enterprise Domain Tech Stack
Phase 1 (Fact-Finding): Gemini 2.5 Flash + Google Search across 15 aftermarket domains.  
Phase 2 (Synthesis): Structured tech stack table grouped by domain.

### Module 2 — Vendor Readiness Signals
Phase 2: Score a target vendor per domain — Signal Strength, Opportunity Type,
Incumbent, Readiness Score (0–100), Rationale.

### Module 3 — IT Budget Estimation
Phase 2: Domain-level IT budget estimates anchored to financial disclosures.

## Domains Covered
Warranty Management, Service Operations, Quality Management, Knowledge Management,
Parts & Spare Parts, Dealer Management (DMS), Supply Chain, Manufacturing Execution,
Engineering & PLM, Customer Experience, Finance & ERP, HR & Workforce,
Data Foundation & Analytics, AI & Automation, Cybersecurity & Compliance.

## API

```
POST /api/gcc-intel
{
  "company_name": "Daimler Truck North America",
  "domain": "daimler-trucks.com",
  "target_vendor": "Tavant",
  "focus_domains": []
}
```

## Environment Variables
- `GOOGLE_AI_API_KEY` — Google AI Studio paid key (set on Render)
