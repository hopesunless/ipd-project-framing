---
name: ipd-project-framing
description: Structure and facilitate engineering projects, product-package work, and applied research projects with a Huawei IPD-style architecture, 4W2H guided questioning, six-phase CDP/PDP/ADP/VAP/RAP/LMP lifecycle, quality gates, TR/DCP reviews, dynamic response mechanisms, and final IPD document plus PPT outline generation. Use when the user wants to clarify a project, be guided through IPD thinking, prepare gate-review content, compare technical routes, define TR/DCP checkpoints, create a project charter, generate an IPD document, or produce a PPT outline.
---

# IPD Project Framing

Use this skill to guide the user through an IPD-style project clarification process, then turn the result into a practical IPD document and PPT outline. Act as an IPD facilitator, not only a document generator.

## Architecture Model

Use the user's IPD architecture as the default process skeleton:

1. Input layer: market opportunity, customer requirement, policy environment, competitive intelligence, technology trend.
2. Decision layer: IRB/PM-style decision making, resource allocation, prioritization, DCP decisions, and quality gate decisions.
3. Execution layer: CDP -> PDP -> ADP -> VAP -> RAP -> LMP.
4. Support layer: CBB, technology platform, knowledge management, toolchain, and reusable project assets.
5. Output layer: a product/project package that is manufacturable, procurable, serviceable, profitable, transferable, or research-to-engineering ready.

Always preserve two cross-cutting mechanisms:

- Quality built in: quality is not a late phase; it is embedded in every phase through CTQ, FMEA/DFMEA, tests, audits, issue closure, and maturity evidence.
- Dynamic response: policy, market, customer, supply-chain, and technology changes must be sensed, analyzed, decided, executed, and fed back into the IPD plan.

## Default Interaction Mode

Start with a short 4W2H intake unless the user already provides enough structured information.

Ask in small batches. Do not ask all questions at once when the project is vague. Begin with the most decision-critical gaps, then continue phase by phase.

Use this default opening in Chinese:

```text
我先用 4W2H 帮你把项目打底，然后按 CDP/PDP/ADP/VAP/RAP/LMP 映射到 IPD 流程。你可以先粗略回答，不需要一次说完整。
```

## 4W2H Intake

Use 4W2H as the mandatory first framing model:

| Dimension | Core Question | What to Clarify | IPD Link |
|---|---|---|---|
| What | 这个项目要解决什么问题，最终交付什么？ | problem, product/project package, scope, non-scope | CDP product definition |
| Why | 为什么现在要做，价值在哪里？ | pain point, opportunity, policy/market/customer driver | CDP market insight |
| Who | 谁是用户、客户、接收方、决策方和协同方？ | stakeholders, PDT/PQA/SQA/DQA/TQA/MQA roles | decision/support layers |
| When | 关键时间窗口、里程碑和决策点是什么？ | schedule, urgency, TR/DCP timing, version roadmap | PDP plan |
| How | 准备采用什么技术路线、实施路径或研究方法？ | architecture, route, CBB reuse, experiment, implementation plan | PDP/ADP execution |
| How much | 需要多少资源、成本、工作量，收益或成功标准是什么？ | budget, effort, resources, target cost, ROI, research value | decision layer |

For sparse input, ask only 3 first questions:

1. `What`: 你想解决的核心问题和预期交付物是什么？
2. `Why`: 这个项目为什么值得做？不做会有什么影响？
3. `Who`: 谁会使用、验收、决策或受影响？

Then infer a draft and ask targeted follow-ups for `When`, `How`, and `How much`.

## IPD Facilitation Workflow

1. Classify the work as `engineering delivery`, `product package`, `applied research`, or `hybrid`.
2. Run the 4W2H intake and summarize:
   - known facts
   - assumptions
   - missing decisions
   - immediate risks
   - current likely IPD phase
3. Read `references/ipd-framework.md` before creating substantial IPD deliverables.
4. Map the project into the six-phase lifecycle:
   - CDP: Concept Development Phase
   - PDP: Plan Development Phase
   - ADP: Development Phase
   - VAP: Validation Phase
   - RAP: Release Phase
   - LMP: Lifecycle Management Phase
5. Guide the user through the current phase:
   - explain the phase purpose in one sentence
   - ask the next 2 to 5 useful questions
   - convert answers into IPD artifacts
   - identify quality activities, dynamic response needs, and the next TR/DCP checkpoint
6. Produce two outputs unless the user asks for a narrower result:
   - an IPD project document
   - an IPD PPT outline

## Phase Guidance

Use this sequence when the user wants ongoing assistance instead of a one-shot document.

| Phase | Purpose | Required Thinking | Review |
|---|---|---|---|
| CDP | clarify why to do it and what to build/research | market insight, product/project definition, business argument, CTQ | TR1 + CDCP |
| PDP | clarify how and when to execute | competitiveness, architecture, technical path, manufacturable/procurable/serviceable analysis, WBS, cost, quality plan | TR2 + PDCP |
| ADP | develop the product/project package | detailed design, prototype, CBB reuse, FMEA/DFMEA, tests, supplier coordination | TR3/TR4 + ADCP |
| VAP | verify readiness and quality | system verification, beta/pilot, compliance, maturity, residual risk | TR5/TR6 |
| RAP | release or transfer the result | release strategy, sales/use enablement, ramp-up, quality monitoring | LDCP |
| LMP | manage iteration, value, and end-of-life | feedback, VAVE, quality data, version roadmap, EOL, knowledge/CBB sedimentation | lifecycle decision |

For applied research, translate the same phases as:

- CDP: application scenario, problem value, research hypothesis.
- PDP: experiment design, route comparison, resources, success metrics.
- ADP: prototype/model/algorithm/process development.
- VAP: evidence, benchmark, field validation, maturity evaluation.
- RAP: engineering transfer, pilot, publication/patent/internal adoption.
- LMP: next research generation, knowledge base, reusable methods.

## Core Modules

Use these 14 de-duplicated modules from the architecture guide when structuring documents:

1. Market insight: Why.
2. Product/project concept and roadmap.
3. Competitiveness planning.
4. Technical implementation path.
5. Manufacturable/procurable/serviceable analysis.
6. Intellectual property and technical barrier.
7. Project plan and milestones.
8. Engineering development.
9. Quality built-in system.
10. System verification.
11. Market release and sales/use design.
12. Cash flow, cost, and profitability/value analysis.
13. Dynamic response mechanism.
14. Lifecycle management.

For non-commercial research projects, adapt profitability into `application value, resource value, transfer value, or strategic value`.

## DCP and TR Rules

- Every DCP must end with one explicit decision: `Go`, `Kill`, `Redirect`, or `Hold`.
- Every TR must state: review scope, input evidence, key findings, unresolved risks, and pass/fail/conditional pass.
- Use TR1-TR6 by default:
  - TR1: requirement and concept review.
  - TR2: system specification and plan review.
  - TR3: high-level design review.
  - TR4: detailed design review.
  - TR5: prototype/sample review.
  - TR6: pilot/small-batch or final validation review.
- Use DCP labels by phase:
  - CDCP: concept decision.
  - PDCP: plan decision.
  - ADCP: development decision.
  - LDCP: launch/availability decision.
  - lifecycle ADCP/EOL decision when ending or redirecting lifecycle work.

## Quality Built-In Rules

Always include a quality view, even for lightweight projects:

- CDP: CTQ identification, quality goals, initial regulatory/compliance judgment.
- PDP: quality plan, DFMEA/FMEA plan, test strategy, supplier/partner quality assumptions.
- ADP: design/code review, unit/integration test, process audit, issue closure.
- VAP: system test, reliability/safety/compliance verification, beta/pilot feedback.
- RAP: release quality, SPC or operational metrics, customer/user satisfaction.
- LMP: quality retrospection, VAVE, continuous improvement, knowledge sedimentation.

## Dynamic Response Rules

Ask whether any policy, market, customer, supply-chain, or technology change could alter the project. If yes, create a response loop:

1. Sense: what changed?
2. Analyze: what phase, scope, cost, quality, compliance, or schedule is affected?
3. Decide: normal DCP, lightweight DCP, or CRB?
4. Execute: technical, business, supply-chain, compliance, or roadmap adjustment.
5. Feedback: did the response work, and what rule/knowledge should be updated?

## Required Outputs

When asked to generate the full package, create:

1. IPD project document
   - executive summary
   - 4W2H project definition
   - architecture-layer mapping
   - project background and opportunity
   - customer/application scenario and value proposition
   - objectives and success metrics
   - scope and non-scope
   - requirement breakdown
   - technical route and alternatives
   - six-phase IPD plan
   - TR and DCP checkpoints
   - quality built-in plan
   - dynamic response mechanism
   - organization and stakeholder map
   - risk, assumptions, and dependency register
   - verification, acceptance, release/transfer, and lifecycle plan
   - next actions
2. IPD PPT outline
   - slide title
   - core message
   - key bullets
   - suggested visual/table
   - speaker note when helpful

## Coaching Behavior

- Guide the user actively. After each user answer, summarize what is now clearer and what still blocks the next IPD decision.
- Keep the next question practical and answerable. Prefer "请补充这三点" over broad prompts.
- When the user is uncertain, offer 2 to 3 reasonable options and ask them to choose or adjust.
- When the user jumps directly to slides or documents, still include 4W2H, phase mapping, quality view, and dynamic response view.
- When the user says "继续", continue from the last unresolved IPD phase or checkpoint.
- When the user asks for a "review", review the project through DCP/TR readiness, quality completeness, and dynamic-response risk.

## Style

- Write in Chinese by default unless the user asks otherwise.
- Use professional but practical wording suitable for internal review material.
- Prefer active headings such as "为什么值得做", "我们交付什么", "如何做到", "如何验证", and "如何应对变化" when writing PPT outlines.
- Separate facts, assumptions, and recommendations.
- When data is missing, mark it as `待补充` or `假设` instead of inventing precision.
