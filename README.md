## AccuKnox-PM-Trainee
Vigil is a cloud posture prototype that reframes CSPM around risk paths, coverage clarity, and actionable prioritization for security and platform teams.

# Problem Statement

Modern cloud environments generate an overwhelming number of security findings. Most Cloud Security Posture Management (CSPM) tools surface long lists of misconfigurations without sufficient context, leaving engineers to manually infer impact, urgency, and remediation effort.

As a result:
- Critical risks are buried under low-impact issues  
- Teams struggle to prioritize effectively  
- Fixes are delayed despite available automation  
- Security posture becomes difficult to reason about at a glance  

Vigil addresses this gap by reframing cloud posture around **risk concentration**, **exposure paths**, and **operational effort**, instead of raw policy failures.

---

## User Persona

**Primary User:**  
Cloud Security Engineer / Platform Security Engineer

**Context:**  
- Manages multi-account cloud environments (AWS-first, extensible to others)  
- Responsible for visibility, risk reduction, and remediation guidance  
- Time-constrained and context-switching across tools  

**Needs:**  
- Fast understanding of overall security health  
- Clear identification of critical risk paths  
- Confidence in what to fix first  
- Practical, effort-aware remediation signals  

---

## Design Goals

1. **Clarity over completeness**  
   Surface fewer metrics, but ensure each one is meaningful.

2. **Risk before rules**  
   Emphasize impact and exposure instead of isolated misconfigurations.

3. **Progressive disclosure**  
   High-level posture first, detailed findings only when needed.

4. **Operational realism**  
   Acknowledge that not all fixes are equal in effort or feasibility.

---

## Information Architecture

Vigil organizes cloud posture into four orthogonal risk domains:

1. **Identity & Privilege Risk**  
   Who can do what, and whether access is excessive or stale.

2. **Exposure & Attack Surface Risk**  
   What is reachable, internet-facing, or forms an attack path.

3. **Data Protection Risk**  
   How sensitive data is stored, encrypted, and potentially exposed.

4. **Control & Visibility Risk**  
   Whether logging, monitoring, alerting, and governance controls are reliable.

Each domain follows the same structure:
- Coverage indicators  
- One primary visualization  
- A ranked, scrollable findings timeline  
- Clear calls to action  

---

## Main Dashboard (Screen 1)

The main dashboard provides a fast, high-confidence snapshot of posture.

### Key Elements
- **Coverage & Scanning Metrics**  
  Percentage of assets evaluated, last scan time, and blind spots.

- **Top Risk Signals**  
  High-level health indicators for access, exposure, and data risk.

- **Four Risk Cards**  
  One per domain, showing:
  - % unhealthy
  - Top contributing issue
  - Trend over time

- **Findings Timeline**  
  A unified, ordered list of findings ranked by risk priority and fix complexity.

- **Fix Complexity Breakdown**  
  Separation of auto-fixable, low-effort, manual, and architectural changes.

---

## Domain Screens (Screens 2–4)

Each risk domain expands into a focused detail view.

### Shared Structure
- **Coverage Summary Card**  
  What is evaluated and what is missing.

- **Primary Visualization**  
  A single chart that explains *why* risk exists (e.g. concentration by asset type).

- **Canonical Findings List**  
  Findings displayed as ordered entries with:
  - Clear human-readable title  
  - Contextual severity  
  - Environment and service tags  
  - Direct remediation CTA  

The findings list acts as a **risk-first timeline**, not a raw alert feed.

---

## Prioritization Logic (Conceptual)

Findings are ranked using a contextual risk model that considers:

- Severity of the underlying issue  
- Sensitivity of affected assets  
- Environment (production vs non-production)  
- Exposure level (public vs internal)  
- Evidence confidence  
- Remediation effort  

This allows Vigil to surface issues that are both **dangerous** and **actionable**, rather than simply noisy.

---

## What This Prototype Is (and Is Not)

**This is:**
- A design and product-thinking exploration  
- A risk-centric CSPM interface concept  
- A foundation for future engineering discussion  

**This is not:**
- A full backend implementation  
- A replacement for native cloud tooling  
- A complete remediation engine  

---

## Bonus: Development Discussion Starters

If taken forward with an engineering team, early discussions would include:
- Asset graph construction and identity-exposure correlation  
- Confidence scoring for findings  
- Safe automation boundaries for remediation  
- Cross-account and cross-service normalization  
- UX strategies for trust and explainability  

---

## Status

This repository represents a **design submission** and conceptual prototype.  
All data shown in the wireframes is illustrative.

---

## Author
Aryan Verma

aryanverma7021@gmail.com

https://www.linkedin.com/in/aryan-verma-5a4883284/

Designed and conceptualized as part of a cloud security posture exploration project.


