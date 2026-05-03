# Radar — External Peer Practice Scan

## Purpose
This file stores external-practice context complementary to Radar source files. It is not the core Radar state file. It captures how Radar compares to real-world financial-services and adjacent analytics/engineering practices.

## Bottom Line
Radar is not crazy. It is directionally aligned with where advanced financial-services firms are going, but the full version described here is not yet routine for analytics teams.

Radar sits at the edge between:
- AI knowledge assistant
- Data catalog
- Lineage / dependency engine
- Analyst copilot
- Institutional-memory system

The closest peer patterns are partial analogs, not exact matches.

## Core Assessment

| Dimension | Assessment |
|---|---|
| Conceptual craziness | Low |
| Implementation novelty | Medium-high |
| Analytics-specific novelty | High |
| Regulated-industry risk | High |
| Strategic upside | Very high |

## What Is Routine vs. Novel

| Pattern | Routine? | Read |
|---|---:|---|
| Internal LLM portal | Yes | JPMorgan-style internal LLM access is becoming normal. |
| Knowledge assistant over internal documents | Increasingly routine | Morgan Stanley is a strong public benchmark. |
| AI-assisted self-service analytics | Emerging | M1 Finance-style use cases are relevant. |
| Source-code/data lineage for analytics engineering | Established but still maturing | Ramp/Foundational and UBS/Neo4j validate this category. |
| LLM over SQL/procs/dashboard dependencies | Emerging | Common experimentation area, fewer public mature examples. |
| Git-backed institutional learning loop from analyst investigations | Not routine | This is one of Radar's most novel components. |
| Analyst-native research OS spanning code, metadata, lineage, lessons, and fixes | Not routine | This is where Radar is ahead of typical analytics practice. |

## Peer / Analog Examples

### Morgan Stanley — Knowledge Assistant Analog
Morgan Stanley built AI @ Morgan Stanley Assistant with OpenAI to help financial advisors access firm knowledge quickly. Public materials describe broad advisor-team usage, growth from a smaller question set to a large internal-document corpus, and a strong evaluation process involving advisor and prompt-engineer review.

Relevance to Radar:
- Validates the internal knowledge-assistant model in financial services.
- Validates the need for evals and expert scoring.
- Does not fully validate Radar's technical analytics-research model because Morgan Stanley's use case is more document/intellectual-capital retrieval than SQL/proc/dashboard investigation.

Radar implication:
- Do not pitch Radar as "AI that knows our data."
- Better framing: evidence-backed analyst investigation acceleration.

### JPMorgan Chase — Enterprise LLM Platform Analog
JPMorgan's LLM Suite is a broad internal assistant/platform made available to a large employee population for tasks such as writing, idea generation, document summarization, and research-style assistance.

Relevance to Radar:
- Validates that large financial institutions are normalizing controlled internal LLM access at scale.
- More analogous to the centralized LLM portal than to Radar.

Radar implication:
- If Radar relies on local repos, VSCode, Claude, GitHub, and code context, the control story needs to be clear.
- A senior reviewer may ask why Radar is not mediated through an approved internal platform.

### M1 Finance — AI Self-Service Analytics Analog
M1 Finance is a relevant fintech example because it connects AI-assisted self-service analytics with structured/governed data. The core problem is business users needing accurate data without SQL proficiency, while wrong outputs could affect portfolios or executive planning.

Relevance to Radar:
- Validates the need for AI-assisted analytics access in a finance context.
- Closer to governed structured analytics Q&A than Radar's broader research/debugging/institutional-memory system.

Radar implication:
- Radar's accuracy will likely be strongest where metadata, dependency maps, and lessons are structured.
- It will be weaker where business logic exists only in ambiguous naming, old comments, Slack memory, or undocumented exceptions.

### Ramp / Foundational — Source-Code Lineage for Analytics Engineering
Ramp's Analytics Engineering group used source-code lineage and governance tooling to improve data quality, developer experience, and change confidence.

Relevance to Radar:
- Strong analog for Radar's dependency and impact-analysis use cases.
- Commercial lineage/governance tooling is more established than homegrown LLM-enabled analyst research systems.

Radar implication:
- Radar's lineage/dependency angle is not weird; it maps to real value categories.
- The novel part is making it analyst-native and self-improving via Git.

### UBS / Neo4j — Graph-Based Lineage for Risk Reporting
UBS used graph technology for data lineage and governance in risk-reporting contexts, especially where previous lineage/dictionary approaches struggled with complex joins, slow queries, and weak visualization.

Relevance to Radar:
- Validates lineage and dependency traversal as a serious financial-services need.
- Supports auditability, impact analysis, and risk-management use cases.

Radar implication:
- Radar's dependency graph is orthodox.
- LLM-driven analyst assistance layered on top is the newer move.

### Deloitte Financial-Services Case — Fragmented BI/Data Environments
A Deloitte financial-services case described scattered/siloed data, limited metadata documentation, unclear definitions, weak searchability, and fragmented BI environments as blockers to trusted analytics and lineage.

Relevance to Radar:
- Validates the underlying disease Radar is trying to address.
- Does not prove Radar is the right implementation.

Radar implication:
- Radar is solving a real, mainstream financial-services pain: fragmented analytics knowledge.

### ING — Risk Stakeholders and Guardrails from the Beginning
ING's genAI chatbot case is customer-facing, but the implementation lesson transfers: risk stakeholders were included early, retrieval and ranking were used, guardrails existed before answers were shown, and rollout was tested before scale.

Relevance to Radar:
- Strong governance/process analog, even if not an analytics tool analog.

Radar implication:
- InfoSec/risk should be treated as design partners, not late-stage approvers.

### Betterment — Observability and QA Lessons
Betterment's chatbot QA example highlights the risk of limited visibility into answer quality, flawed answers, missed intents, and compliance exposure.

Relevance to Radar:
- Useful cautionary analog around observability.

Radar implication:
- Radar needs visibility into sources used, ignored evidence, guesses, answer quality, and lesson quality.

## Where Similar Efforts Succeed

### Pattern 1 — Constrained Domain + Evals
Strong peer examples constrain the domain and build evaluation loops before broad scale.

Radar implication:
- Build evals before broad rollout.
- Do not rely on impressive anecdotes alone.

Minimum eval set should include:
- Known dashboard dependency question
- Known stored-proc lineage chain
- Known deprecated-object impact case
- Known SQL performance issue
- Known false-positive trap
- Known insufficient-evidence case
- Known business-definition conflict

### Pattern 2 — Controlled Enterprise Access
Large finance firms are normalizing internal LLM use, but through controlled enterprise access patterns.

Radar implication:
- Clearly document data flow, local repo exposure, model boundary, telemetry, retention, and permissions.

### Pattern 3 — Structured Data Discipline
AI-assisted analytics works best when grounded in structured, governed context.

Radar implication:
- Radar's strongest near-term use cases should lean into structured assets: dependencies, metadata, repos, documented lessons, and known reporting sources.

### Pattern 4 — Lineage as a Value Layer
Lineage and impact analysis have real value in financial environments.

Radar implication:
- Deprecation impact, technical debt discovery, migration readiness, dependency tracing, and dashboard breakage research are strong initial value domains.

## Where Similar Efforts Fail

### Failure Mode 1 — Cool Assistant Without Trust Infrastructure
Self-service analytics already struggles to balance control and agility. GenAI can worsen compliance, security, and inconsistent-insight problems.

Radar implication:
- Analysts must not trust fluent answers before the system earns trust.

### Failure Mode 2 — Governance Debt Disguised as AI Opportunity
Fragmented data and weak definitions are not solved by AI; they become the substrate the AI reasons over.

Radar implication:
- Radar may expose the analytics mess faster than it fixes it.

### Failure Mode 3 — Hallucination and Opacity
In regulated finance, hallucination and opaque reasoning are unacceptable in high-impact workflows.

Radar implication:
- Plausible wrong SQL with institutional authority vibes is a major risk.

### Failure Mode 4 — Weak Observability
If users cannot see what the system used, ignored, guessed, or learned, trust cannot be managed.

Radar implication:
- Radar needs source traceability, confidence signaling, answer-quality logging, and lesson-quality controls.

## Unvarnished Judgment
Radar is probably ahead of the organization's operating model, not ahead of the industry's technical direction.

The risk sequence:
1. Radar works well enough to attract attention.
2. People overestimate its readiness.
3. InfoSec asks hard questions late.
4. Reliability stays anecdotal instead of measured.
5. Ownership remains tied to one strong contributor.
6. The Git knowledge loop becomes a trust/pollution problem.
7. The tool becomes mission-critical before governance catches up.

Preferred safe framing:
> Radar is an internal alpha for analyst investigation acceleration. Its early results show major promise in dependency analysis, technical debt discovery, and institutional knowledge capture. It is not yet a governed source of truth, autonomous SQL authority, or production recommendation engine.

## Recommended Next Moves

### 1. Build evals before broad rollout
Create a controlled benchmark of known questions, expected answers, false-positive traps, and insufficient-evidence cases.

### 2. Treat InfoSec as a design partner
Document:
- What lives locally
- What is sent to the model
- What remains inside enterprise boundaries
- What gets logged
- What gets retained
- What permissions are inherited
- Which repos/assets are allowed
- Which data classes are prohibited

### 3. Separate retrieval from recommendation
Radar can retrieve, explain, and propose. It should not be framed as autonomous truth.

Recommended wording:
> Radar accelerates investigation and proposes evidence-backed findings. Analysts remain accountable for final interpretation and production changes.

### 4. Govern the Git learning loop
Lessons entering main should be:
- Evidence-backed
- Scoped
- Source-linked where possible
- Dated
- Reviewed or confidence-tagged
- Reversible
- Not overly broad
- Not merely opinion

## Final Read
Radar is not crazy. It is a serious idea.

But it is not routine analytics practice. The industry has strong examples of internal AI assistants, knowledge retrieval, self-service analytics, lineage tooling, and governed AI platforms. What is not clearly visible in public peer examples is the full Radar pattern: analyst-native LLM workspace + SQL/proc/dashboard dependency intelligence + Git-backed institutional learning loop.

Treat Radar as a potentially differentiated internal capability, not a standard tool rollout.

The right next move is controlled hardening: InfoSec review, eval harness, knowledge-loop governance, and narrow use-case proof.

## Confidence Caveat
Low-confidence area: named failed internal finance-industry examples are underreported publicly, so the failure analysis is inferred from published failure patterns, governance warnings, and adjacent examples rather than named bank postmortems.
