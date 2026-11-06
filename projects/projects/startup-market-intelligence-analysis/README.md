# Finding the Market: Identifying Viable Startup Clients for Research and Decision-Support Services

> An exploratory market analysis of 26 startups across 5 countries, built with Excel, Power Query and Power BI.

**Headline result:** 25 of 26 startups showed a need, but only 15 (58%) were viable core targets once capability gaps and ability to pay were considered.

---

## Project Overview

This project investigates where there is a real market for data, research, analytics and decision-support services among startups, what forms that need takes, and which types of startups are viable targets.

Rather than assuming what startups need, I built a dataset of 26 startups and coded what could be observed about each one: country, sector, business model, funding stage, team size, funding evidence, internal research and analytics capability, estimated ability to pay and priority. I cleaned the data, analysed it against five business questions, and presented the results in a five-page Power BI dashboard.

## Research Objectives

1. Identify where startups show the strongest signs of needing data, research and decision support.
2. Separate startups that *need* support from those that could realistically *buy* it.
3. Understand what forms the need takes and how well startups already cover it in-house.
4. Define the profile of viable target startups and estimate how large that group is in the sample.
5. Recommend which services to lead with and which startups to approach first.

## Research Questions

| # | Question | Dashboard page |
|---|----------|----------------|
| 1 | In which sectors, countries and funding stages do startups show the strongest signs of need? | Page 1 |
| 2 | Where does a visible need coincide with the capacity to pay? | Page 2 |
| 3 | What forms does the need take, and does it differ by business model? | Page 3 |
| 4 | Do startups meet these needs in-house, through tools, or not at all, and where are the gaps? | Page 4 |
| 5 | What profile of startup combines need, ability to pay and low internal capability, and how large is that group? | Page 5 |

## Methodology

**Sample.** 26 startups: Nigeria (11), United States (7), Kenya (5), United Kingdom (2) and India (1). They span AI, B2B SaaS, health tech, fintech and financial services, HR tech, logistics and retail. Business models are B2B (17), B2B2C (6), B2B + B2C (2) and B2B + B2G (1). Funding stages run from Pre-Seed to Series A.

**Data collection.** Each startup was coded from publicly available information. Need was coded Yes or No for four need types: market research, customer research, business intelligence and decision support. Capability, ability to pay, priority tier and outsourcing potential are researcher-coded ratings.

**Data cleaning.** Standardised categories that almost matched, split cells holding more than one response, trimmed column headers, and removed a blank row that was inflating counts. Throughout, I asked whether each change made the data easier to analyse or quietly changed the story, and I documented every merge rule.

**Derived fields.** Sector Group, Stage Group (combined stages mapped to the latest stage reached), Business Model Group, Team Size Group (1-10, 11-50, 51+), Capability Profile and Target Segment.

**Target Segment rules.** A startup is a **core target** if it shows all four needs, has low internal research capability, has Medium or High ability to pay, is Tier 1 priority and has high outsourcing potential. It is in the **wider market** if it meets the first three tests only. These thresholds are my judgement and are stated on the dashboard.

**Analysis.** Descriptive analysis in Power BI using matrices, 100% stacked bars, profile charts, a funnel and a target list. Small groups are flagged, and sample sizes appear in chart titles.

## Key Findings

1. **Need is nearly universal, so it does not locate the market.** 25 of 26 startups showed all four need types. Only one showed none.
2. **The difference is capability.** 21 of 26 startups have low internal research capability, while analytics is better covered (19 moderate, 5 high, 2 low). The gap is in research, not analytics, and it is widest at Pre-Seed and Seed.
3. **Ability to pay is mostly modest.** 20 startups are rated Medium and 5 High. None of the five High payers has a low research gap. They are the five US-based Series A AI startups.
4. **The viable group is narrower than need alone suggests.** The funnel runs 26 startups, then 25 with need, 20 with low research capability and Medium or High ability to pay, and 15 once Tier 1 priority and high outsourcing potential are applied.
5. **Profile of the 15 core targets.** 14 are Pre-Seed or Seed, 9 are B2B, 4 are B2B2C and 2 are B2B + B2C, and 10 have teams of 11 to 50 people. Ten are Nigerian health and fintech startups. Five are Seed-stage B2B SaaS startups in the UK, US and India with disclosed funding of $1.2M to $5M.
6. **Business model.** B2B is the largest segment, but B2B2C startups converted to core targets at a higher rate (4 of 6, against 9 of 17). No pure B2C startups were sampled, so that segment is untested.

## Recommendations

- **Lead with research and decision support.** The widest gap is in research. Keep analytics and reporting as secondary offers, since most startups already partly cover them in-house.
- **Primary target:** early-stage (Pre-Seed and Seed) B2B startups with 11 to 50 people, especially Nigerian health and fintech companies. Scope services for early-stage budgets, such as project-based research and light-touch decision support.
- **Secondary target:** Seed-stage B2B SaaS startups in the UK, US and India, who show the clearest ability to pay among startups with a gap.
- **Treat B2B2C and hybrid models as a strong next segment,** using different approaches for different stages and markets.
- **Deprioritise well-resourced Series A startups,** who can pay but have less need for outside research.
- **Validate before scaling** through short interviews or a survey on budget and current research practice.

## Dashboard Preview

![Page 1: Where is the need?](images/page-1-overview.png)
![Page 2: Need and ability to pay](images/page-2-ability-to-pay.png)
![Page 3: Forms of need](images/page-3-forms-of-need.png)
![Page 4: Capability gaps](images/page-4-capability-gaps.png)
![Page 5: Viable targets](images/page-5-viable-targets.png)

## Tools Used

- Microsoft Excel (dataset construction and initial cleaning)
- Power Query (transformations and conditional columns)
- Power BI (dashboard design and visualisation)
- DAX (measures and calculated columns)

## Project Files

Project documentation, dashboard screenshots and supporting materials are organised in this repository.

```
├── README.md
├── data/
│   └── Finding-the-Market-Research.xlsx
├── dashboard/
│   └── Finding-the-Market.pbix
├── images/
│   └── (dashboard screenshots)
└── docs/
    └──
