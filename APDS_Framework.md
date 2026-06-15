# Agile Project Delivery System (APDS) Framework

> Agile Project Management Measurement and Decision Framework

---

## Table of Contents

1. [Introduction](#1-introduction)
   - [Purpose and Scope](#11-purpose-and-scope)
   - [The Value APDS Brings to Scrum](#12-the-value-apds-brings-to-scrum)
   - [Who Should Use This Framework](#13-who-should-use-this-framework)
2. [Core Concepts](#2-core-concepts)
   - [Work Units (WU)](#21-work-units-wu)
   - [Work Progression Ladder (WPL)](#22-work-progression-ladder-wpl)
   - [Fibonacci Estimation](#23-fibonacci-estimation)
   - [Zone Classification & The Four Indicators](#24-zone-classification--the-four-indicators)
   - [Planned Progress (PP)](#241-planned-progress-pp)
   - [Actual Progress (AP)](#242-actual-progress-ap)
   - [Cumulative Delivery Pace (CDP)](#243-cumulative-delivery-pace-cdp)
   - [Resource Efficiency (RE)](#244-resource-efficiency-re)
   - [Scope Stability (SS)](#245-scope-stability-ss)
   - [Collaboration and Satisfaction (CS)](#246-collaboration-and-satisfaction-cs)
   - [Project Score and Decision Levels](#247-project-score-and-decision-levels)
   - [Forecasting Engine](#248-forecasting-engine)
   - [MoSCoW Prioritization with APDS Scoring](#249-moscow-prioritization-with-apds-scoring)
3. [The APDS Lifecycle: Setup, Refinement, and Planning](#3-the-apds-lifecycle-setup-refinement-and-planning)
4. [Problem Solving Workshop](#4-problem-solving-workshop)

---

## 1. Introduction

### 1.1 Purpose and Scope

Scrum provides an adaptable framework tailored for fast-paced and complex initiatives, organizing work into short, time-boxed sprints that deliver value incrementally. This predictable rhythm allows delivery teams to respond rapidly to changing requirements while maintaining a steady output. However, without systematic tracking of core parameters, such as timeline, budget, team collaboration, stakeholder satisfaction, and scope change, project leadership often relies on subjective intuition rather than empirical data. Isolating only one or two of these areas provides an incomplete narrative of overall performance. To evaluate project health accurately, these distinct dimensions should be analyzed collectively.

A complete health check that combines these key areas helps project teams spot deeper problems before they turn into major issues. For instance, a high delivery speed combined with low stakeholder satisfaction signals an immediate misalignment in priorities. By bringing time, cost, collaboration, satisfaction, and scope changes into a single view, scrum teams can make smarter, data-driven decisions. This turns Scrum from just a process into a real tool for navigating uncertainty, where compromises are clear, improvements are backed by evidence, and the team stays focused on what matters most.

The **Agile Project Delivery System (APDS)** is designed as a supplementary measurement and decision-making framework tailored specifically for initiatives utilizing scrum. APDS does not alter or replace standard scrum mechanics; rather, it fully respects and preserves the underlying scrum framework while introducing pragmatic data tracking and guidance for agile project environments.

While scrum explicitly defines project structures, including ceremonies, artifacts, and roles, it deliberately leaves the specific methods of measurement open-ended. Consequently, project teams frequently rely on subjective feedback to evaluate initiative health. APDS is developed to bridge this gap, introducing concrete, actionable metrics that integrate directly into the scrum lifecycle without creating administrative overhead.

The APDS framework functions essentially as a data dashboard for scrum execution. It systematically tracks **four core indicators**:

- **Cumulative Delivery Pace (CDP)**
- **Resource Efficiency (RE)**
- **Scope Stability (SS)**
- **Collaboration and Satisfaction (CS)**

Each indicator is evaluated and categorized into distinct **Green**, **Amber**, and **Red** performance zones. These four scores feed into a forecasting engine and a single project health score called the **Project Decision**. The project decision score maps directly to a clear action level, directing the Product Owner (PO) to **Proceed**, **Watch**, **Review**, or **Escalate**.

The APDS framework fits seamlessly over the existing rhythm of scrum ceremonies. During Sprint Planning, Daily Scrum, Sprint Review, and Sprint Retrospective, the system defines exactly what data should be calculated, analyzed, and produced. This objective layer addresses the following questions:

- How reliably is the team delivering validated value?
- What does historical trend data indicate regarding current capacity?
- Which project adjustments are supported by empirical evidence rather than subjective impressions?

By making these implicit performance variables visible via a structured dashboard, the APDS framework helps project teams identify bottlenecks early and implement targeted interventions with high confidence.

### 1.2 The Value APDS Brings to Scrum

The APDS provides **five capabilities** that enable teams to utilize the scrum framework with greater confidence:

| Capability | Description |
|---|---|
| **Quantifiable Confidence** | Every indicator produces a numerical value between 0 and 1. Eliminates guesswork and subjective assessments. |
| **Data-Driven Decisions** | The project score maps directly to four defined decision levels: Proceed, Watch, Review, or Escalate. |
| **Early Warning System** | Amber zones flag emerging issues early; red zones demand immediate corrective intervention. |
| **Forecast Accuracy** | Forward-looking forecasts predict the total number of sprints needed to complete the project. |
| **Governance Traceability** | Every decision is backed by documented data. Establishes an auditable, repeatable, and defensible process. |

### 1.3 Who Should Use This Framework

This framework is designed for **Project Managers**, **Product Owners**, **Scrum Masters**, or **team leads** who want to back up decisions with measurable data. It works best when a team already runs scrum and leadership requires numbers to back up professional judgment without interrupting the team's daily work.

---

## 2. Core Concepts

This section covers the building blocks needed to understand the framework before putting it into practice. It introduces the four indicators used to check project health, showing how these individual scores combine into a single project score, map into performance status zones, and feed into the forecasting engine.

### 2.1 Work Units (WU)

A **Work Unit** represents an individual requirement, such as a feature, a work package, a user story, or a task. Regardless of the internal terminology used by an organization, APDS tracks every Work Unit across the project lifecycle using **three elements**:

1. An **effort estimate** based on the Fibonacci sequence (fixed unless scope changes occur)
2. A **tracking state** defined by a specific Rung assignment (R1–R5)
3. A **weighted progress value** calculated by multiplying the Fibonacci estimate by the Rung completion percentage

### 2.2 Work Progression Ladder (WPL)

To track Work Units, the framework utilizes the **Work Progression Ladder**. This evaluation system consists of five Rungs (R1–R5), with every Work Unit continuously mapped to a single Rung. Each level carries a fixed completion percentage that feeds directly into the cumulative actual progress calculations.

| Rung | Description | Completion % |
|---|---|---|
| **R1: Draft** | Work identified and assigned. | 0% |
| **R2: Assembly** | Work is in progress. Components are being built. | 25% |
| **R3: Validation** | Work complete enough for review. Testing/peer review. | 60% |
| **R4: Certified** | Work has passed validation. Approved by reviewer/QC. | 85% |
| **R5: Agreed** | Work fully accepted by PO/customer. No further action. | 100% |

Teams may calibrate Rung descriptions and completion percentages to match their workflow. Rungs are weighted to reflect increasing certainty. Earlier Rungs (R1–R2) carry lower percentages because work is still in development stage. The largest jump at R3 (35 points) reflects the transition from development into validation, which represents the highest-effort phase. Later Rungs (R4–R5) carry smaller increments because the remaining work is verification and acceptance.

### 2.3 Fibonacci Estimation

Every Work Unit gets a **Fibonacci number** that represents expected effort in days:

```
1 = 1 day, 2 = 2 days, 3 = 3 days, 5 = 5 days, 8 = 8 days, 13 = 13 days, ...
```

The Product Owner and the team agree on these estimates together during sprint planning and backlog refinement. Once set, the estimate stays **fixed** unless the scope of the Work Unit changes.

### 2.4 Zone Classification & The Four Indicators

To assess project health, APDS tracks four indicators. These are calculated at the end of each sprint (prior to the next iteration during the sprint planning session) and categorized into one of three status zones:

- **Green (On Track):** No action is required.
- **Amber (Caution):** Close monitoring is advised.
- **Red (Action Required):** Immediate intervention is needed.

Every APDS indicator scores between **0% and 100%** and falls into one of three zones based on threshold ranges:

| Zone | Range | Color | Meaning |
|---|---|---|---|
| On track | 90% – 100% | 🟢 Green | No action required. Continue monitoring. |
| Caution | 80% – 89% | 🟡 Amber | Investigate. Prepare corrective action. |
| At risk | 0% – 79% | 🔴 Red | Immediate intervention required. Escalate if needed. |

**The Four Indicators:**

| Indicator | Formula | Question It Answers |
|---|---|---|
| **Cumulative Delivery Pace (CDP)** | AP_cum / PP_cum | Is delivery on track? |
| **Resource Efficiency (RE)** | SB / SC | Is cost within budget? |
| **Scope Stability (SS)** | 1 − (\|Current − Original\| / Max(Current, Original)) | Is scope stable? |
| **Collaboration & Satisfaction (CS)** | (Collaboration × 0.4) + (Satisfaction × 0.4) + (Communication × 0.2) | Is the team healthy? |

#### 2.4.1 Planned Progress (PP)

The logic behind **Planned Progress (PP_sprint)** dictates that for every Work Unit committed to a given sprint, the plan is to complete 100% of that commitment. Therefore, PP_sprint value is always 1.0 (100%) for the committed scope. The formula weights each committed Work Unit by its estimated Fibonacci duration.

**Formula:**

```
PP_sprint = Σ (WU Fib × 100%) / Σ (WU Fib) = 1.0 (100%)
```

**Example:** If a team commits to three Work Units for an upcoming sprint:
- Login: Fibonacci 5
- Payment: Fibonacci 8
- Dashboard: Fibonacci 3

```
PP_sprint = (5×100% + 8×100% + 3×100%) / (5+8+3) = 1.0 (100%)
```

> **Note:** If scope changes occur mid-sprint, PP_sprint is recalculated to reflect the updated set of committed Work Units.

**Cumulative Planned Progress (PP_cum):**

```
PP_cum = (100% / Total Sprints) × Current Sprint Number
```

#### 2.4.2 Actual Progress (AP)

**Actual Progress (AP)** represents the true completion rate of the sprint. It is calculated by taking every Work Unit in the sprint, multiplying its Fibonacci estimate by its WPL completion percentage, summing those values, and dividing by the total Fibonacci in the sprint.

**Formula:**

```
AP = Σ (WU Fib × Rung Completion %) / Σ (WU Fib)
```

> **Note:** The project team updates the WPL status of every Work Unit during the daily scrum throughout the sprint.

**Example:** Consider a sprint with four committed Work Units totaling 21 Fibonacci points:

| Work Unit | Fib | Rung | Completion % | Weighted Progress |
|---|---|---|---|---|
| Login feature | 5 | R3 | 60% | 3.0 |
| Payment integration | 8 | R4 | 85% | 6.8 |
| User dashboard | 3 | R1 | 0% | 0.0 |
| Admin panel | 5 | R2 | 25% | 1.25 |
| **Total** | **21** | | | **11.05** |

```
AP = 11.05 / 21 = 0.526 (52.6%)
```

This result indicates that the team achieved 52.6% of the total planned effort committed across the specified Work Units for the sprint.

**Cumulative Actual Progress (AP_cum)** is the cumulative weighted progress through the WPL up to the current sprint.

#### 2.4.3 Cumulative Delivery Pace (CDP)

**Cumulative Delivery Pace (CDP)** measures whether the team is delivering work as fast as originally planned. It compares Cumulative Actual Progress (AP_cum) against Cumulative Planned Progress (PP_cum).

**Formula:**

```
CDP = AP_cum / PP_cum
```

**Example:** Consider a project at the conclusion of sprint 5 out of a total 10 planned sprints:
- PP_cum = 50%
- AP_cum = 30%

```
CDP = 30% / 50% = 60% (Critical)
```

**Zone Classification:**

| Zone | Range | Meaning |
|---|---|---|
| 🟢 **Green (Healthy)** | 90% – 100% | Delivery is tracking safely on schedule. The team is meeting its cumulative commitments. |
| 🟡 **Amber (Behind)** | 80% – 89% | Delivery is experiencing minor delays. The schedule requires close monitoring and potential adjustment. |
| 🔴 **Red (Critical)** | 0% – 79% | Delivery is significantly behind schedule. Immediate intervention is required to address root causes. |

#### 2.4.4 Resource Efficiency (RE)

The **Resource Efficiency (RE)** indicator evaluates whether the team is spending resources according to the planned budget. It compares the Sprint Budget (SB) against the actual Sprint Cost (SC).

**Formula:**

```
RE = SB / SC
```

Where Sprint Budget (SB) is:

```
SB = Total Project Budget / Total Number of Sprints
```

> **Note:** RE cannot go above 100%. If sprint spent less than planned, the extra does not count. RE above 100% indicates the sprint was delivered under budget. However, this metric should be cross-checked against CDP:
> - If CDP is 🟢 Green → the under-spend reflects genuine efficiency.
> - If CDP is 🔴 Red → the under-spend likely reflects incomplete work.

**Example:**
- Total Project Budget = $500,000
- Total Sprints = 10
- SB = $500,000 / 10 = $50,000 per sprint
- Sprint Cost (SC) = $53,000

```
RE = $50,000 / $53,000 = 94.3% (On-Target)
```

**Zone Classification:**

| Zone | Range | Meaning |
|---|---|---|
| 🟢 **Green (On-Target)** | 90% – 100% | Resources used efficiently. |
| 🟡 **Amber (Over-Budget)** | 80% – 89% | Resources are not used efficiently. Investigate cost drivers. |
| 🔴 **Red (Critical)** | 0% – 79% | Resources consumed with little progress. Immediate intervention. |

#### 2.4.5 Scope Stability (SS)

**Scope Stability (SS)** evaluates whether the project scope is remaining steady or experiencing frequent changes. While baseline scope modifications typically occur during backlog refinement, this metric also accounts for scope changes driven by stakeholder feedback during the Sprint Review.

**Formula:**

```
SS = 1 − (|Current WU Count − Original WU Count| / Max(Original WU Count, Current WU Count))
```

**Example:**
- Original Scope: 20 Work Units
- Current Scope: 24 Work Units

```
SS = 1 − (|24−20| / Max(24,20)) = 0.833 (83%)
```

A result of 83% places the project scope within the **Amber (Creeping)** zone.

**Zone Classification:**

| Zone | Range | Meaning |
|---|---|---|
| 🟢 **Green (Stable)** | 90% – 100% | The scope is stable. Minor adjustments are well within manageable project tolerances. |
| 🟡 **Amber (Creeping)** | 80% – 89% | The scope is creeping. Backlog refinement or stakeholder feedback has introduced noticeable volume changes that require monitoring. |
| 🔴 **Red (Unstable)** | 0% – 79% | The scope is highly unstable. Significant changes threaten the predictability of the timeline and require immediate re-baselining. |

#### 2.4.6 Collaboration and Satisfaction (CS)

The **Collaboration and Satisfaction (CS)** indicator evaluates the internal health of the project team and external happiness of project stakeholders. This metric combines three sub-scores:

- **Collaboration** (40% weight)
- **Satisfaction** (40% weight)
- **Communication** (20% weight)

All feedback is captured verbally during the sprint review and sprint retrospective:
- **Collaboration & Communication data** is collected from the project team during the sprint retrospective.
- **Satisfaction data** is collected from stakeholders during the sprint review.

Each sub-score converts its raw 1–5 verbal ratings into a normalized 0–1 score.

**Formula:**

```
CS = (Collaboration × 0.40) + (Satisfaction × 0.40) + (Communication × 0.20)
```

**Scoring Method:**

- **Collaboration (40%):** Team members rate 3 statements (1–5 scale). Average = total responses / number of responses, then divide by 5.
- **Satisfaction (40%):** Stakeholders rate 2 statements (1–5 scale). Average = total responses / number of responses, then divide by 5.
- **Communication (20%):** Team members rate 2 statements (1–5 scale). Average = total responses / number of responses, then divide by 5.

**Example:**

| Sub-Score | Responses | Sum | Average | Normalized |
|---|---|---|---|---|
| Collaboration (3 stmts × 5 members) | 15 | 63 | 4.2 | 0.84 (84%) |
| Satisfaction (2 stmts × stakeholders) | — | — | 3.8 | 0.76 (76%) |
| Communication (2 stmts × 5 members) | — | — | 4.5 | 0.90 (90%) |

```
CS = (84% × 40%) + (76% × 40%) + (90% × 20%) = 82% (Damaged)
```

**Zone Classification:**

| Zone | Range | Meaning |
|---|---|---|
| 🟢 **Green (Engaged)** | 90% – 100% | Team collaborates well. Stakeholders are satisfied. |
| 🟡 **Amber (Damaged)** | 80% – 89% | Visible misalignment. Friction exists within the team or stakeholder satisfaction has decreased, requiring attention. |
| 🔴 **Red (Broken)** | 0% – 79% | Severe cultural or relationship breakdown. Immediate leadership intervention is required. |

#### 2.4.7 Project Score and Decision Levels

**Project Score (PS)** is the most important key indicator used to show overall project health and is the average of all four indicators.

**Formula:**

```
PS = (CDP + RE + SS + CS) / 4
```

**Decision Levels:**

| Level | PS Range | Action |
|---|---|---|
| 🟢 **Proceed** | 90% – 100% | All indicators are Green. Project is on track. |
| 🟡 **Watch** | 80% – 89% | One or more indicators have shifted to Amber. Monitor closely. |
| 🟠 **Review** | 70% – 79% | Significant issues. Corrective action needed. |
| 🔴 **Escalate** | 0% – 69% | Project viability is in doubt. Escalate to governance. |

**Example:**
```
PS = (70% + 85% + 90% + 80%) / 4 = 0.81 (81%)
```

A final Project Score of 81% places the project into the **Watch** level. This status alerts the Product Owner that while the project may proceed, specific underlying constraints require close monitoring to prevent a further drop into the Review zone.

#### 2.4.8 Forecasting Engine

The forecasting engine utilizes current project metrics to predict the future. The Product Owner executes this calculation as part of the project health check, subsequently presenting the results in the next sprint planning session.

**Forecast Completion Point (FCP):**

```
FCP = Total Number of Sprints + ((PP_cum − AP_cum) × Total Number of Sprints)
```

**Example:**
- Total Sprints = 10
- Current Sprint 5 → PP_cum = 50%
- AP_cum at sprint 5 = 30%

```
FCP = 10 + ((50% − 30%) × 10) = 12 sprints
```

The project is forecasted at a total of **12 sprints** to reach completion.

#### 2.4.9 MoSCoW Prioritization with APDS Scoring

Requirements (Work Units) are prioritized using the **MoSCoW** technique: **M**ust Have, **S**hould Have, **C**ould Have, and **W**on't Have. APDS makes this technique measurable by assigning a numerical value score to every requirement.

**Value Score Ranges:**

| Category | Score Range |
|---|---|
| Must Have | 80 – 100 |
| Should Have | 50 – 79 |
| Could Have | 20 – 49 |
| Won't Have | Not scored (out of scope) |

**MoSCoW Metrics:**

| Metric | Formula | What It Means |
|---|---|---|
| **MoSCoW Distribution Ratio (MDR)** | Must Have count / Total requirements | Fraction of backlog that is committed, non-negotiable scope. |
| **MoSCoW Value Density (MVD)** | Total Value Score / Total requirements | Average business value per requirement. |
| **MoSCoW Stability Index (MSI)** | 1 − (Changed / Total) | Priority stability over time. 100% means no priorities changed. |

**Example:**
- 40 WUs: 20 Must Have (avg 90), 12 Should Have (avg 65), 8 Could Have (avg 35)
- Total Value Score = (20×90) + (12×65) + (8×35) = 2,860

```
MDR = 20/40 = 0.50 (50%)
MVD = 2,860/40 = 71.5
MSI = 1 − (4/40) = 0.90 (90% stable)
```

##### MDR Zone Classification

| Zone | MDR Range | Meaning & Impact |
|---|---|---|
| 🟢 **Balanced** | 30% – 60% | Healthy distribution. Room to absorb changes. Delivery dates stable. |
| 🟡 **Top-Heavy** | > 60% | Rigid backlog. Too many Must Haves destroy the safety buffer. Delays delivery. |
| 🔴 **Thin** | < 30% | Weak core. Too few Must Haves. Unreliable minimum viable delivery. |

##### MVD Zone Classification

| Zone | MVD Range | Meaning & Impact |
|---|---|---|
| 🟢 **Healthy** | ≥ 50 | High-value backlog. Sprint capacity spent on impactful deliverables. |
| 🔴 **Low-Value** | < 50 | Low-value work dominates. Critical WUs sit undelivered. Delays project benefits. |

##### Cross-Indicator Impact

- **MDR > 60% → SS drops:** Top-heavy backlog causes scope creep, lowering Scope Stability.
- **Frequent MoSCoW re-categorization → CS drops:** Stakeholder disagreement undermines collaboration and satisfaction.
- **MVD < 50 → Financial risk:** Low-value backlog signals value-for-money problem.

---

## 3. The APDS Lifecycle: Setup, Refinement, and Planning

The APDS framework does not start with the first sprint; it begins the moment a project is defined.

### Setup Steps

1. **Log all requirements** — Gather all requirements as candidate Work Units.
2. **Prioritize the requirements** — Use MoSCoW analysis to rank Work Units based on business value, risks, and dependencies.
3. **Map out the release plan** — Organize prioritized Work Units into a structured release plan detailing delivery order across sprints.
4. **Build the product backlog** — Apply initial Fibonacci estimation; identify and map risks/dependencies in the RAID log.
5. **Kick off Sprint Planning** — Pull top-priority items from backlog into the first sprint.

### Release Planning

Once Work Units are established and prioritized using MoSCoW, the next step involves mapping them into a release plan. The release plan acts as an interval-distributed timeline, determining exactly when the prioritized Work Units will be delivered. This plan directly establishes the **overall sprint count** and **baseline budget**.

### Product Backlog

The product backlog serves as the foundational data source for APDS. Every backlog item is classified as a **Work Unit (WU)** requiring three attributes:

- **Fibonacci Duration Estimate** — Fixed unless scope change occurs.
- **Initial Rung Assignment** — Every new WU begins at R1 (Draft).
- **Recorded Dependencies** — Recorded in the RAID log.

### Product Backlog Refinement

When indicators guide priority during refinement:

| Priority | Condition | Action |
|---|---|---|
| **1 (High)** | Any indicator in 🔴 red zone | Address immediately. Backlog priority pivots to resolve critical risk. |
| **2 (Medium)** | Any indicator in 🟡 amber zone | Investigate. Incorporate targeted corrective actions. |
| **3 (Low)** | All indicators in 🟢 green zone | No urgent action. Maintain standard value-driven prioritization. |

### Sprint Planning

APDS introduces two key elements to sprint planning:

- **Planned Progress (PP)**
- **Sprint Budget (SB)**

The PO presents the four indicators, Project Score, and FCP from the previous sprint. Performance indicators directly inform commitment:

- If **CDP was Critical** → consider lighter load.
- If **RE was Critical** → investigate resourcing issues.
- If **SS is Creeping/Unstable** → factor scope growth into commitment.
- If **CS is Damaged/Broken** → address issues before full efficiency is expected.

---

## 4. Problem Solving Workshop

When the **Project Score (PS)** falls into Watch, Review, or Escalate thresholds, a dedicated problem-solving workshop is convened.

| PS Level | PS Range | Workshop Type |
|---|---|---|
| 🟢 Proceed | 90% – 100% | No workshop needed. Standard delivery continues. |
| 🟡 Watch | 80% – 89% | Core delivery team meeting. Focus on affected indicator(s). Assign quick-win corrective actions. |
| 🟠 Review | 70% – 79% | Comprehensive workshop with delivery team + stakeholders. Build formal recovery plan. |
| 🔴 Escalate | 0% – 69% | Escalate to executive governance. Specialized workshop to inform continuation/termination decision. |

### Event Flow

1. **Sprint Retrospective** — Team discusses collaboration, processes, and improvements.
2. **Problem-Solving Workshop** — Dig into root causes of underperforming metrics; draft recovery plan.
3. **Sprint Planning** — Recovery plan fed directly into upcoming sprint.

### Recovery Plan Deliverable

The workshop produces a structured recovery plan containing:

- **Specific Corrective Actions** — Concrete tasks to remediate underperforming metrics.
- **Review Date** — Firm deadline for evaluating intervention effectiveness.

---

## Quick Reference: All Formulas

| Indicator | Formula |
|---|---|
| Planned Progress (PP_sprint) | Σ(WU Fib × 100%) / Σ(WU Fib) = 1.0 |
| Cumulative Planned Progress (PP_cum) | (100% / Total Sprints) × Current Sprint |
| Actual Progress (AP) | Σ(WU Fib × Rung Completion %) / Σ(WU Fib) |
| Cumulative Delivery Pace (CDP) | AP_cum / PP_cum |
| Sprint Budget (SB) | Total Project Budget / Total Sprints |
| Resource Efficiency (RE) | SB / SC (capped at 100%) |
| Scope Stability (SS) | 1 − (\|Current − Original\| / Max(Current, Original)) |
| Collaboration & Satisfaction (CS) | (Collab × 0.4) + (Satisfaction × 0.4) + (Comm × 0.2) |
| Project Score (PS) | (CDP + RE + SS + CS) / 4 |
| Forecast Completion Point (FCP) | Total Sprints + ((PP_cum − AP_cum) × Total Sprints) |
| MoSCoW Distribution Ratio (MDR) | Must Have count / Total requirements |
| MoSCoW Value Density (MVD) | Total Value Score / Total requirements |
| MoSCoW Stability Index (MSI) | 1 − (Changed categories / Total) |

## Quick Reference: Zone Thresholds

| Zone | Range | Color |
|---|---|---|
| On Track / Healthy | 90% – 100% | 🟢 Green |
| Caution / Warning | 80% – 89% | 🟡 Amber |
| At Risk / Critical | 0% – 79% | 🔴 Red |

---

---

## License

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/">
  <a property="dct:title" rel="cc:attributionURL" href="">Agile Project Delivery System (APDS) Framework</a> is licensed under
  <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">
    Creative Commons Attribution-ShareAlike 4.0 International
    <img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt="">
    <img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt="">
    <img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt="">
  </a>
</p>

**Attribution requirement:** Any use, modification, or distribution must include the statement:
*"Based on the Agile Project Delivery System (APDS) Framework by Mo Agiles"* or similar clear credit.

**ShareAlike condition:** Any adapted or modified versions must be distributed under the same CC BY-SA 4.0 license.

---

*APDS Framework v1.0 — For use with Scrum-based project delivery.*
