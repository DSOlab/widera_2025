# The AETHEREUS R&I Agenda

## Thoughts ...

The R&I Agenda will basically cover tasks and activities related to the four 
hubs/flagship software. Given that the call does not fully endorse R&I activities, we 
ll have to be cautious on describing them. Hence, this section will cover only the 
limited R&I we’ll do within the project to validate and benchmark the flagship tools 
(not to do new science). Think: methods validation, inter-comparisons, benchmarks with DOIs, 
uncertainty budgets, and contributions to standards. It must stay within the ≤20% 
total budget cap and live in WP3??.

Purpose & boundary. The Agenda defines a focused set of validation, inter-comparison, streamlining 
and standardisation activities that underpin our four capacity flagships/hubs and Living Labs(??). 
In line with EEI-CSA scope, R&I is limited to methods validation (≤20% budget); all 
development/platformisation sits in WP3, and deployment/uptake in (WP5?? maybe...). This 
keeps the project squarely on institutional reform, skills, and digital capacity, 
with R&I serving as quality assurance and credibility for services. 

The Agenda’s validation outputs (benchmarks with DOIs, acceptance thresholds, 
uncertainty budgets) de-risk and operationalise the four flagships, creating institutional 
capacity that will underpin future cutting-edge research beyond the grant. All protocols 
align with, and feed into, international geodesy services and working groups (GGOS, 
IGS/ILRS/IDS/EUREF), strengthening collaboration and visibility. By making benchmarks 
and APIs open and FAIR, we enable downstream uptake in Living Labs and lay the foundations 
for sustainable service lines operated by trained staff certified through WP2??. 
All validations are executed on the Alliance’s/CoE's digital capacity—containerised pipelines, 
CI/CD, FAIR data services, APIs, and security/monitoring—so results are operational, 
reproducible, and service-ready.

## Cross-cutting enablers (some/all could be used)

==Enablers== are horizontal things that every hub/flagship and every seed validation 
relies on. They’re not extra projects; they’re the shared capabilities, rules, and 
tools that make the whole agenda operational, comparable, and credible.

Standards & reference alignment
: Use common conventions (IAG/GGOS; IGS/ILRS/IDS/EUREF), reference products, and 
comparison protocols so results are comparable. Outputs: methods/standards roadmap; 
submissions to WGs. KPI: # standards contributions; % products in required formats.

FAIR benchmarks & openness
: Curated datasets with DOIs, rich metadata, and reproducible notebooks so anyone 
can verify results. Outputs: benchmark DOIs; notebook gallery. KPI: # DOI’d benchmarks; 
metadata completeness.

Digital/DevOps platform
: Containerised pipelines, CI/CD, auth/security, observability—so validations are 
repeatable and auditable. Outputs: signed images, runbooks, dashboards. KPIs: uptime %, 
p95 latency, MTTR, vulnerability scans passed.

QA & metrics
: Shared accuracy/uncertainty metrics and live QA dashboards (e.g., SLR RMS; tide-gauge RMSE).
Outputs: thresholds table; dashboards. KPIs: targets met per flagship; incident rate.

AI for operations (not research)
: ML used for quality flags, anomaly detection, and semantic search over docs/code—speeding 
ops, not inventing science. Outputs: flagging services; search portal. KPI: % issues 
auto-detected; search adoption.

Governance & assessment (CoARA/OTM-R)
: Narrative-CV, rubrics, SOPs/SLAs recognition—so validation outputs “count” in 
careers and decisions. Outputs: policy kit; templates. KPI: % panels using narrative 
CV; % decisions citing software/data/service evidence.

Security, ethics, GDPR
: Minimal data protection, access control, backups, audits—keeps services trustworthy.
Outputs: audit reports; incident playbooks. KPI: audits passed; remedial actions closed on time.

Skills & credentials
: Micro-credentials, Train-the-Trainer, skills registry—so capacity persists.
Outputs: issued credentials; TtT graduates. KPI: # certified staff; adoption of artifacts at home HEIs.

## Instruments & workflow

* Seed R&I calls (2 waves): small, 6–9-month validation pilots led by widening hubs; each tied to a flagship question.
* Inter-comparison campaigns: scheduled, documented runs with community references; public Validation Reports.
* Benchmark & release workshops: annual methods workshops to freeze metrics, thresholds, and data citations.
* Visiting fellows: short residencies to co-author validation protocols/benchmarks and coach widening teams.

All benchmarks and reports are open, with DOIs, metadata, and reproducible notebooks; list where they’ll be hosted and how they’re cited.

## Too Technical 

Thematic priorities & validation questions (by Hub)

Space Geodesy & Mission Support (POD Suite)
- Questions: multi-tech orbit consistency; force-model sensitivity; reference frame robustness.
- Validation: SLR residual RMS thresholds; GNSS day-boundary overlaps; inter-comparison vs IGS/ILRS/IDS references; uncertainty budgets documented.

Environment & Climate (Coastal Altimetry Processor)
- Questions: near-shore retracking performance; cross-mission harmonisation; river/lake height fidelity.
- Validation: RMSE vs tide gauges at virtual stations; mission drift checks; uncertainty and QC flags; regional presets for Mediterranean/Black Sea.

Earth System Modeling (Gravity Change Processor)
- Questions: SH vs mascon consistency; GIA/leakage impacts; closure with sea-level/hydrology.
- Validation: benchmark basins with DOIs; ensemble/comparison vs CSR/JPL/GFZ; uncertainty partition (seasonal/trend) reported.

Geohazards (GNSS Deformation & Early-Warning)
- Questions: robustness of cleaning/step detection; velocity/strain field agreement; transient thresholds.
- Validation: cross-checks vs independent solutions; strain consistency tests; alert false-positive/false-negative rates; optional ingestion of external InSAR products (no new InSAR chain).
