# IPD Project Framing

`ipd-project-framing` is a reusable project-framing workflow for structuring engineering projects, product-package work, and applied research initiatives with an IPD-style lifecycle.

It combines 4W2H questioning, a six-phase IPD process, technical and decision reviews, quality built-in thinking, and dynamic response mechanisms. The goal is to help teams turn early project ideas into review-ready project documents, decision material, and presentation outlines.

This repository can be used in multiple ways:

- as an AI-agent skill or prompt package
- as a project-management checklist
- as a workshop facilitation guide
- as a template source for IPD-style documents and slide outlines
- as a starting point for organization-specific IPD customization

## What This Is

This workflow is inspired by common IPD (Integrated Product Development) practices and adapted for practical project framing. It is not an official Huawei process document and should be tailored to each organization's governance, terminology, and review requirements.

The framework is especially useful when a project needs to answer:

- Why should this project exist?
- What exactly will be delivered?
- Who will use, fund, review, build, verify, or operate it?
- When are the key milestones and decision points?
- How will the technical or research route work?
- How much resource, cost, effort, risk, and value are involved?

## Use Cases

Use this workflow to:

- clarify a vague product, engineering, or research idea
- prepare IPD-style project charters
- generate project documents and gate-review materials
- compare technical routes or research paths
- define TR/DCP checkpoints
- build quality, verification, and risk plans
- structure research-to-engineering transfer plans
- create PPT outlines for project review meetings
- align cross-functional teams around value, scope, evidence, and decisions

## Repository Structure

```text
.
├── README.md
└── skills/
    └── ipd-project-framing/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── references/
            └── ipd-framework.md
```

Main files:

- `skills/ipd-project-framing/SKILL.md`: compact instructions for an AI assistant or facilitator.
- `skills/ipd-project-framing/references/ipd-framework.md`: detailed IPD reference, templates, phase definitions, quality rules, and PPT outline.
- `skills/ipd-project-framing/agents/openai.yaml`: optional metadata for environments that support skill discovery.

## Core Method: 4W2H

The workflow starts with 4W2H to establish a clear project baseline before entering detailed planning.

| Dimension | Core Question | IPD Interpretation |
|---|---|---|
| What | What problem is being solved, and what will be delivered? | concept, requirements, scope, deliverables |
| Why | Why should this be done now, and what value does it create? | market insight, application value, opportunity, strategy |
| Who | Who uses, accepts, funds, decides, builds, or supports it? | stakeholders, team roles, governance, receivers |
| When | What are the time windows, milestones, and decision points? | roadmap, TR/DCP timing, delivery plan |
| How | What route, architecture, method, or experiment will be used? | technical path, implementation, verification approach |
| How much | What resources, cost, effort, benefit, and success criteria apply? | resource plan, cost/value model, metrics |

For sparse project input, start with only three questions:

1. What core problem and expected deliverable should be addressed?
2. Why is the project worth doing, and what happens if it is not done?
3. Who will use, accept, decide, or be affected by the outcome?

Then add targeted follow-up questions for timing, route, cost, resources, and success metrics.

## IPD Architecture

The workflow uses a five-layer architecture:

| Layer | Focus |
|---|---|
| Input Layer | market opportunity, customer needs, policy environment, competitive intelligence, technology trends |
| Decision Layer | investment review, portfolio priority, resource allocation, DCP decisions, quality gates |
| Execution Layer | CDP -> PDP -> ADP -> VAP -> RAP -> LMP |
| Support Layer | CBB, technology platforms, knowledge management, tools, reusable assets |
| Output Layer | manufacturable, procurable, serviceable, profitable, transferable, or research-to-engineering-ready package |

For applied research, the output layer can be interpreted as a verifiable, reusable, transferable capability rather than a commercial product package.

## Six-Phase Lifecycle

| Phase | Full Name | Goal | Typical Review |
|---|---|---|---|
| CDP | Concept Development Phase | clarify why to do it and what to build or research | TR1 + CDCP |
| PDP | Plan Development Phase | clarify how, when, with what resources, and at what quality level | TR2 + PDCP |
| ADP | Development Phase | implement the product, prototype, model, process, or research artifact | TR3/TR4 + ADCP |
| VAP | Validation Phase | verify requirement satisfaction and release/transfer readiness | TR5/TR6 |
| RAP | Release Phase | release, transfer, launch, pilot, or enable adoption | LDCP |
| LMP | Lifecycle Management Phase | manage iteration, value, quality feedback, knowledge, and end-of-life | lifecycle decision |

## Fourteen Core Modules

The reference framework organizes project material into 14 non-overlapping modules:

1. Market insight: Why
2. Product/project concept and roadmap
3. Competitiveness planning
4. Technical implementation path
5. Manufacturable/procurable/serviceable analysis
6. Intellectual property and technical barriers
7. Project plan and milestones
8. Engineering development
9. Quality built-in system
10. System verification
11. Market release and sales/use design
12. Cash flow, cost, and profitability/value analysis
13. Dynamic response mechanism
14. Lifecycle management

For non-commercial research work, profitability can be reframed as application value, strategic value, transfer value, or capability value.

## Quality Built In

Quality is treated as a cross-lifecycle design concern, not as a final inspection step.

| Phase | Quality Focus |
|---|---|
| CDP | CTQ identification, quality goals, initial compliance judgment |
| PDP | quality plan, FMEA/DFMEA planning, test strategy, supplier or partner quality assumptions |
| ADP | design review, code review, unit/integration tests, process audit, issue closure |
| VAP | system tests, reliability/safety/compliance verification, beta or pilot feedback |
| RAP | release quality, SPC or operational metrics, customer/user satisfaction |
| LMP | quality retrospectives, VAVE, continuous improvement, knowledge capture |

## Dynamic Response

Projects often change because of policy, market, customer, supply-chain, or technology shifts. This workflow uses a closed loop:

1. Sense: What changed?
2. Analyze: Which phase, scope, cost, quality, compliance, or schedule is affected?
3. Decide: Should the team use a normal DCP, lightweight DCP, CRB, or roadmap decision?
4. Execute: Adjust technology, business/use model, supply chain, compliance, or roadmap.
5. Feedback: Did the response work, and what should be captured for future projects?

## TR and DCP Rules

Every DCP should produce a clear decision:

- `Go`: continue
- `Kill`: terminate
- `Redirect`: adjust direction
- `Hold`: pause

TR reviews are organized around evidence:

| TR | Review Focus |
|---|---|
| TR1 | requirements and concept |
| TR2 | system specification and plan |
| TR3 | high-level design |
| TR4 | detailed design |
| TR5 | prototype, sample, model, or staged result |
| TR6 | pilot, small-batch, or final validation readiness |

## Expected Outputs

When used end to end, the workflow usually produces two deliverables:

1. IPD-style project document
2. IPD-style presentation outline

The project document may include:

- executive summary
- 4W2H project definition
- IPD architecture-layer mapping
- project background and opportunity
- customer or application scenario
- objectives and success metrics
- scope and non-scope
- requirements
- technical route and alternatives
- six-phase IPD plan
- TR/DCP checkpoints
- quality built-in plan
- dynamic response mechanism
- organization and stakeholder map
- risks, assumptions, and dependencies
- verification, acceptance, release/transfer, and lifecycle plan
- next actions

The presentation outline often includes:

1. Project name and decision request
2. IPD architecture view
3. 4W2H project definition
4. CDP: opportunity and concept
5. PDP: plan and path
6. Technical route and competitiveness
7. Manufacturable/procurable/serviceable/transferable analysis
8. ADP: development implementation
9. VAP: verification plan
10. RAP: release or transfer plan
11. LMP: lifecycle and iteration
12. Quality built in
13. Dynamic response
14. TR/DCP review plan
15. Decision request and next steps

## Example Prompts

For an AI assistant or facilitation session:

```text
Use the IPD project framing workflow to clarify this applied research project:
We want to study a new visual inspection algorithm for production-line defect detection, but we only have an early idea.
```

```text
Use this workflow to prepare TR1 and CDCP review material for the concept phase.
```

```text
Structure this engineering project into an IPD-style document and PPT outline:
<project background>
```

```text
Continue from the previous project context and move into PDP. Focus on technical implementation path, resource plan, quality plan, and TR2/PDCP readiness.
```

## Using With Different Tools

This repository is tool-agnostic:

- In an AI-agent environment, load `SKILL.md` as the primary instruction file and load `references/ipd-framework.md` when detailed templates are needed.
- In a manual workshop, use the 4W2H table and six-phase lifecycle as the facilitation agenda.
- In project-management practice, copy the document and slide outline sections into internal templates.
- In an organization-specific rollout, adapt terminology, review gates, quality roles, and deliverable names to match internal governance.

## Customization Ideas

- Add organization-specific DCP/TR templates.
- Add industry-specific compliance checklists.
- Add Word or PowerPoint templates under an `assets/` directory.
- Add scripts to generate `.docx` or `.pptx` deliverables automatically.
- Narrow the workflow for applied research, hardware products, software platforms, manufacturing process projects, or internal tools.

## License

Add a license that matches the intended use before public distribution.
