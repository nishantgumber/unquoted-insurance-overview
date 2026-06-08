<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:164e63,100:0891b2&height=200&section=header&text=Unquoted&fontSize=64&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Insurance%20Comparison%20%7C%20Purchase%20%7C%20Policy%20Management%20%7C%20Claims&descAlignY=58&descSize=15&descColor=a5f3fc)

<br/>

[![Status](https://img.shields.io/badge/Status-Paused-6b7280?style=for-the-badge)]()
[![Stack](https://img.shields.io/badge/Stack-Next.js%20%7C%20React%20%7C%20Firebase-0f172a?style=for-the-badge)]()
[![Type](https://img.shields.io/badge/Type-Two--Sided%20Marketplace-0891b2?style=for-the-badge)]()

</div>

---

## What is Unquoted?

Unquoted is an insurance comparison and management platform — a single place where Canadians can **compare policies across providers, purchase coverage, manage all their active policies, and file claims** without switching between insurer portals.

The product targets a fragmented market where the average Canadian holds 4–6 insurance policies (auto, home, life, tenant, travel, health) each managed separately, often without any visibility into whether they're over-insured, under-insured, or paying more than they should.

---

## The problem

Shopping for insurance in Canada is broken:

- 🔍 **Comparison is manual** — brokers give quotes over the phone, aggregator sites are incomplete, and most Canadians end up with whatever their bank offers
- 📁 **Policy management is fragmented** — auto with one insurer, home with another, life with a third, each with its own portal and renewal date
- 📋 **Claims are opaque** — filing a claim means navigating a provider's process from scratch every time, with no central history
- 💸 **Switching costs are high** — most people renew on autopilot because comparing alternatives takes more effort than it's worth

Unquoted was designed to solve all four.

---

## Core features

### 🔎 Insurance comparison engine
Users input their profile (age, location, coverage needs) and Unquoted queries multiple provider APIs to return ranked, side-by-side policy comparisons across auto, home, life, tenant, travel, and health insurance categories.

### 🛒 In-platform purchase
Users can select and purchase a policy directly through Unquoted — no redirect to the provider's site, no re-entering information. The platform handles the handoff with the insurer via API.

### 📂 Policy management dashboard
All active policies consolidated in one view — coverage details, premium amounts, renewal dates, and provider contacts. Renewal reminders sent automatically before expiry.

### 📝 Claims processing assistant
Guided claims filing — users select the policy, describe the incident, upload supporting documents, and Unquoted submits to the provider and tracks status. No more navigating insurer portals from scratch.

---

## Tech stack

| Layer | Technology |
|-------|-----------|
| Frontend | Next.js, React, Tailwind CSS |
| Backend | Next.js API Routes, RESTful APIs |
| Database & Auth | Firebase (Firestore, Firebase Auth) |
| Hosting | Vercel |
| Real-time | Firebase real-time data sync |
| Performance | Load-tested to 1,000+ concurrent users |

---

## Architecture overview

```
┌──────────────────────────────────────────────────────┐
│                  Next.js Frontend                     │
│     (Comparison UI · Dashboard · Claims flow)         │
└──────────────────────┬───────────────────────────────┘
                       │
┌──────────────────────▼───────────────────────────────┐
│               Next.js API Routes                      │
│    (Quote aggregation · Policy mgmt · Claims API)     │
└──────┬───────────────┬──────────────────┬────────────┘
       │               │                  │
┌──────▼──────┐ ┌──────▼──────┐ ┌─────────▼──────────┐
│  Firebase   │ │  Insurance  │ │   Notification      │
│ (Firestore  │ │  Provider   │ │   Service           │
│  + Auth)    │ │  APIs       │ │   (Reminders)       │
└─────────────┘ └─────────────┘ └────────────────────┘
```

---

## Why it's paused

Unquoted is a **two-sided marketplace** — it only works if insurance providers are integrated on the supply side. Getting major Canadian insurers (Intact, Aviva, TD Insurance, Desjardins) to open API access requires commercial agreements, compliance reviews, and regulatory groundwork that isn't achievable as a solo developer without institutional backing.

The product architecture, comparison engine, dashboard, and claims flow are fully designed and partially built. The blocker is provider-side API access, not technical execution.

This is a genuine market opportunity — the comparison and management layer for Canadian insurance doesn't have a strong independent player. It's a paused project, not an abandoned one.

---

## What was built

- [x] Insurance comparison UI with side-by-side policy views
- [x] User authentication and profile management
- [x] Policy management dashboard
- [x] Dynamic data dashboards with real-time updates
- [x] Third-party API integration layer
- [x] AWS cloud infrastructure with load testing (1,000+ concurrent users)
- [x] Secure document upload for claims
- [ ] Live insurer API integrations *(blocked — requires commercial agreements)*
- [ ] In-platform purchase flow *(blocked — requires insurer partnerships)*
- [ ] Production claims submission *(blocked — requires insurer partnerships)*

---

## Market context

- Canadian P&C insurance market: **~$75B CAD annually**
- Average Canadian household spends **$4,000–6,000/yr** on insurance premiums
- Existing comparison tools (Rates.ca, RATESDOTCA) are lead-gen focused — they hand users off to brokers, not platforms
- No dominant independent platform owns the full comparison → purchase → manage → claim loop in Canada

---

## Contact

**Nishant Gumber** — Builder

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nishant-gumber/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nishantgumber123@gmail.com)

> ⚠️ This repository contains the public-facing product overview. Source code is maintained in a private repository.

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:0891b2,50:164e63,100:0f172a&height=100&section=footer)
