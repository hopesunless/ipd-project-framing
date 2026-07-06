# IPD Project Framing / IPD 项目梳理框架

`ipd-project-framing` is a reusable project-framing workflow for structuring engineering projects, product-package work, and applied research initiatives with an IPD-style lifecycle.

`ipd-project-framing` 是一个可复用的项目梳理工作流，用于按照 IPD 风格生命周期组织工程项目、产品包项目和应用研究项目。

It combines 4W2H questioning, a six-phase IPD process, technical and decision reviews, quality built-in thinking, and dynamic response mechanisms. The goal is to help teams turn early project ideas into review-ready project documents, decision material, and presentation outlines.

它结合了 4W2H 提问、六阶段 IPD 流程、技术评审与决策评审、质量内建思想和动态响应机制，帮助团队把早期项目想法整理成可评审、可决策、可推进的项目文档和汇报大纲。

This repository can be used as:

本仓库可作为：

- an AI-agent skill or prompt package
- AI 智能体 skill 或提示词包
- a project-management checklist
- 项目管理检查清单
- a workshop facilitation guide
- 工作坊引导指南
- a template source for IPD-style documents and slide outlines
- IPD 风格文档和 PPT 大纲模板源
- a starting point for organization-specific IPD customization
- 面向组织内部 IPD 流程定制的起点

## What This Is / 这是什么

This workflow is inspired by common IPD (Integrated Product Development) practices and adapted for practical project framing. It is not an official Huawei process document and should be tailored to each organization's governance, terminology, and review requirements.

本工作流参考通用 IPD（Integrated Product Development，集成产品开发）实践，并将其调整为更适合项目梳理和项目评审准备的实用框架。它不是华为官方流程文件，使用时应根据具体组织的治理机制、术语体系和评审要求进行裁剪。

The framework is especially useful when a project needs to answer:

当一个项目需要回答以下问题时，这个框架尤其有用：

| English | 中文 |
|---|---|
| Why should this project exist? | 这个项目为什么应该存在？ |
| What exactly will be delivered? | 项目到底要交付什么？ |
| Who will use, fund, review, build, verify, or operate it? | 谁会使用、投入、评审、建设、验证或运营它？ |
| When are the key milestones and decision points? | 关键里程碑和决策点是什么时候？ |
| How will the technical or research route work? | 技术路线或研究路径如何展开？ |
| How much resource, cost, effort, risk, and value are involved? | 涉及多少资源、成本、工作量、风险和价值？ |

## Use Cases / 适用场景

Use this workflow to:

可以用这个工作流来：

| English | 中文 |
|---|---|
| clarify a vague product, engineering, or research idea | 澄清一个模糊的产品、工程或研究想法 |
| prepare IPD-style project charters | 准备 IPD 风格的项目章程 |
| generate project documents and gate-review materials | 生成项目文档和阶段评审材料 |
| compare technical routes or research paths | 对比技术路线或研究路径 |
| define TR/DCP checkpoints | 定义 TR/DCP 评审节点 |
| build quality, verification, and risk plans | 建立质量、验证和风险计划 |
| structure research-to-engineering transfer plans | 梳理研究成果向工程转化的路径 |
| create PPT outlines for project review meetings | 生成项目评审汇报 PPT 大纲 |
| align cross-functional teams around value, scope, evidence, and decisions | 围绕价值、范围、证据和决策对齐跨职能团队 |

## Repository Structure / 仓库结构

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

主要文件：

| File | Description | 中文说明 |
|---|---|---|
| `skills/ipd-project-framing/SKILL.md` | Compact instructions for an AI assistant or facilitator. | 面向 AI 助手或流程引导师的核心指令文件。 |
| `skills/ipd-project-framing/references/ipd-framework.md` | Detailed IPD reference, templates, phase definitions, quality rules, and PPT outline. | 详细 IPD 参考框架、模板、阶段定义、质量规则和 PPT 大纲。 |
| `skills/ipd-project-framing/agents/openai.yaml` | Optional metadata for environments that support skill discovery. | 面向支持 skill 发现机制的环境的可选元数据。 |

## Core Method: 4W2H / 核心方法：4W2H

The workflow starts with 4W2H to establish a clear project baseline before entering detailed planning.

该工作流先用 4W2H 建立项目底座，再进入详细的 IPD 阶段化梳理。

| Dimension | Core Question | IPD Interpretation | 中文问题 | IPD 对应内容 |
|---|---|---|---|---|
| What | What problem is being solved, and what will be delivered? | concept, requirements, scope, deliverables | 解决什么问题，交付什么？ | 概念、需求、范围、交付物 |
| Why | Why should this be done now, and what value does it create? | market insight, application value, opportunity, strategy | 为什么现在要做，创造什么价值？ | 市场洞察、应用价值、机会、战略意义 |
| Who | Who uses, accepts, funds, decides, builds, or supports it? | stakeholders, team roles, governance, receivers | 谁使用、验收、投入、决策、建设或支持？ | 干系人、团队角色、治理机制、接收方 |
| When | What are the time windows, milestones, and decision points? | roadmap, TR/DCP timing, delivery plan | 时间窗口、里程碑和决策点是什么？ | 路标、TR/DCP 节点、交付计划 |
| How | What route, architecture, method, or experiment will be used? | technical path, implementation, verification approach | 采用什么路线、架构、方法或实验？ | 技术路径、实施方案、验证方法 |
| How much | What resources, cost, effort, benefit, and success criteria apply? | resource plan, cost/value model, metrics | 需要多少资源、成本、工作量，收益和成功标准是什么？ | 资源计划、成本/价值模型、指标 |

For sparse project input, start with only three questions:

当项目信息很少时，先问三个问题：

1. What core problem and expected deliverable should be addressed?
   中文：要解决的核心问题和预期交付物是什么？
2. Why is the project worth doing, and what happens if it is not done?
   中文：为什么这个项目值得做？如果不做会有什么影响？
3. Who will use, accept, decide, or be affected by the outcome?
   中文：谁会使用、验收、决策或受到影响？

Then add targeted follow-up questions for timing, route, cost, resources, and success metrics.

之后再围绕时间、路线、成本、资源和成功指标追加有针对性的追问。

## IPD Architecture / IPD 架构

The workflow uses a five-layer architecture:

该工作流采用五层架构：

| Layer | Focus | 层级 | 关注点 |
|---|---|---|---|
| Input Layer | market opportunity, customer needs, policy environment, competitive intelligence, technology trends | 输入层 | 市场机会、客户需求、政策环境、竞争情报、技术趋势 |
| Decision Layer | investment review, portfolio priority, resource allocation, DCP decisions, quality gates | 决策层 | 投资评审、组合优先级、资源分配、DCP 决策、质量门控 |
| Execution Layer | CDP -> PDP -> ADP -> VAP -> RAP -> LMP | 执行层 | CDP -> PDP -> ADP -> VAP -> RAP -> LMP |
| Support Layer | CBB, technology platforms, knowledge management, tools, reusable assets | 支撑层 | CBB、技术平台、知识管理、工具链、可复用资产 |
| Output Layer | manufacturable, procurable, serviceable, profitable, transferable, or research-to-engineering-ready package | 输出层 | 可制造、可采购、可服务、可盈利、可转化或可工程化的项目包 |

For applied research, the output layer can be interpreted as a verifiable, reusable, transferable capability rather than a commercial product package.

对于应用研究项目，输出层可以理解为可验证、可复用、可转化的能力，而不一定是商业化产品包。

## Six-Phase Lifecycle / 六阶段生命周期

| Phase | Full Name | Goal | Typical Review | 中文阶段 | 目标 | 典型评审 |
|---|---|---|---|---|---|---|
| CDP | Concept Development Phase | clarify why to do it and what to build or research | TR1 + CDCP | 概念阶段 | 明确为什么做、做什么 | TR1 + CDCP |
| PDP | Plan Development Phase | clarify how, when, with what resources, and at what quality level | TR2 + PDCP | 计划阶段 | 明确怎么做、何时做、用多少资源、达到什么质量标准 | TR2 + PDCP |
| ADP | Development Phase | implement the product, prototype, model, process, or research artifact | TR3/TR4 + ADCP | 开发阶段 | 完成产品、原型、模型、工艺或研究成果实现 | TR3/TR4 + ADCP |
| VAP | Validation Phase | verify requirement satisfaction and release/transfer readiness | TR5/TR6 | 验证阶段 | 验证需求满足度和发布/转化准备度 | TR5/TR6 |
| RAP | Release Phase | release, transfer, launch, pilot, or enable adoption | LDCP | 发布阶段 | 发布、转化、上市、试点或赋能采用 | LDCP |
| LMP | Lifecycle Management Phase | manage iteration, value, quality feedback, knowledge, and end-of-life | lifecycle decision | 生命周期管理阶段 | 管理迭代、价值、质量反馈、知识沉淀和退场 | 生命周期决策 |

## Fourteen Core Modules / 十四个核心模块

The reference framework organizes project material into 14 non-overlapping modules.

参考框架将项目材料组织为 14 个尽量不重叠的核心模块。

| No. | Module | 中文模块 |
|---|---|---|
| 1 | Market insight: Why | 市场洞察：Why |
| 2 | Product/project concept and roadmap | 产品/项目概念与路标 |
| 3 | Competitiveness planning | 竞争力规划 |
| 4 | Technical implementation path | 技术实现路径 |
| 5 | Manufacturable/procurable/serviceable analysis | 可制造/可采购/可服务分析 |
| 6 | Intellectual property and technical barriers | 知识产权与技术壁垒 |
| 7 | Project plan and milestones | 项目计划与里程碑 |
| 8 | Engineering development | 工程开发 |
| 9 | Quality built-in system | 质量内建体系 |
| 10 | System verification | 系统验证 |
| 11 | Market release and sales/use design | 市场发布与销售/使用设计 |
| 12 | Cash flow, cost, and profitability/value analysis | 现金流、成本与盈利/价值分析 |
| 13 | Dynamic response mechanism | 动态响应机制 |
| 14 | Lifecycle management | 生命周期管理 |

For non-commercial research work, profitability can be reframed as application value, strategic value, transfer value, or capability value.

对于非商业研究项目，可以把盈利分析改写为应用价值、战略价值、转化价值或能力价值分析。

## Quality Built In / 质量内建

Quality is treated as a cross-lifecycle design concern, not as a final inspection step.

质量被视为贯穿生命周期的设计问题，而不是最后的检查环节。

| Phase | Quality Focus | 阶段 | 质量关注点 |
|---|---|---|---|
| CDP | CTQ identification, quality goals, initial compliance judgment | 概念阶段 | CTQ 识别、质量目标、合规初判 |
| PDP | quality plan, FMEA/DFMEA planning, test strategy, supplier or partner quality assumptions | 计划阶段 | 质量计划、FMEA/DFMEA 计划、测试策略、供应商或合作方质量假设 |
| ADP | design review, code review, unit/integration tests, process audit, issue closure | 开发阶段 | 设计评审、代码评审、单元/集成测试、过程审计、问题闭环 |
| VAP | system tests, reliability/safety/compliance verification, beta or pilot feedback | 验证阶段 | 系统测试、可靠性/安全/合规验证、Beta 或试点反馈 |
| RAP | release quality, SPC or operational metrics, customer/user satisfaction | 发布阶段 | 发布质量、SPC 或运行指标、客户/用户满意度 |
| LMP | quality retrospectives, VAVE, continuous improvement, knowledge capture | 生命周期管理阶段 | 质量复盘、VAVE、持续改进、知识沉淀 |

## Dynamic Response / 动态响应

Projects often change because of policy, market, customer, supply-chain, or technology shifts. This workflow uses a closed loop:

项目经常会因为政策、市场、客户、供应链或技术变化而调整。该工作流使用闭环响应机制：

| Step | English | 中文 |
|---|---|---|
| 1 | Sense: What changed? | 感知：发生了什么变化？ |
| 2 | Analyze: Which phase, scope, cost, quality, compliance, or schedule is affected? | 分析：哪个阶段、范围、成本、质量、合规或进度受到影响？ |
| 3 | Decide: Should the team use a normal DCP, lightweight DCP, CRB, or roadmap decision? | 决策：走普通 DCP、轻量 DCP、CRB，还是路标决策？ |
| 4 | Execute: Adjust technology, business/use model, supply chain, compliance, or roadmap. | 执行：调整技术、业务/使用模式、供应链、合规或路标。 |
| 5 | Feedback: Did the response work, and what should be captured for future projects? | 反馈：响应是否有效？哪些经验需要沉淀？ |

## TR and DCP Rules / TR 与 DCP 规则

Every DCP should produce a clear decision:

每个 DCP 都应该输出明确决策：

| Decision | Meaning | 中文含义 |
|---|---|---|
| Go | continue | 继续推进 |
| Kill | terminate | 终止 |
| Redirect | adjust direction | 调整方向 |
| Hold | pause | 暂停 |

TR reviews are organized around evidence:

TR 评审应围绕证据展开：

| TR | Review Focus | 中文评审焦点 |
|---|---|---|
| TR1 | requirements and concept | 需求与概念 |
| TR2 | system specification and plan | 系统规格与计划 |
| TR3 | high-level design | 概要设计 |
| TR4 | detailed design | 详细设计 |
| TR5 | prototype, sample, model, or staged result | 原型、样机、模型或阶段成果 |
| TR6 | pilot, small-batch, or final validation readiness | 试点、小批量或最终验证准备度 |

## Expected Outputs / 预期输出

When used end to end, the workflow usually produces two deliverables:

端到端使用时，该工作流通常生成两个交付物：

1. IPD-style project document
   中文：IPD 风格项目文档
2. IPD-style presentation outline
   中文：IPD 风格汇报大纲

The project document may include:

项目文档通常包含：

| English | 中文 |
|---|---|
| executive summary | 执行摘要 |
| 4W2H project definition | 4W2H 项目定义 |
| IPD architecture-layer mapping | IPD 架构层映射 |
| project background and opportunity | 项目背景与机会 |
| customer or application scenario | 客户或应用场景 |
| objectives and success metrics | 目标与成功指标 |
| scope and non-scope | 范围与非范围 |
| requirements | 需求 |
| technical route and alternatives | 技术路线与备选方案 |
| six-phase IPD plan | 六阶段 IPD 计划 |
| TR/DCP checkpoints | TR/DCP 节点 |
| quality built-in plan | 质量内建计划 |
| dynamic response mechanism | 动态响应机制 |
| organization and stakeholder map | 组织与干系人地图 |
| risks, assumptions, and dependencies | 风险、假设与依赖 |
| verification, acceptance, release/transfer, and lifecycle plan | 验证、验收、发布/转化和生命周期计划 |
| next actions | 下一步行动 |

The presentation outline often includes:

汇报大纲通常包含：

| No. | English | 中文 |
|---|---|---|
| 1 | Project name and decision request | 项目名称与决策请求 |
| 2 | IPD architecture view | IPD 架构视图 |
| 3 | 4W2H project definition | 4W2H 项目定义 |
| 4 | CDP: opportunity and concept | CDP：机会与概念 |
| 5 | PDP: plan and path | PDP：计划与路径 |
| 6 | Technical route and competitiveness | 技术路线与竞争力 |
| 7 | Manufacturable/procurable/serviceable/transferable analysis | 可制造/可采购/可服务/可转化分析 |
| 8 | ADP: development implementation | ADP：开发实现 |
| 9 | VAP: verification plan | VAP：验证方案 |
| 10 | RAP: release or transfer plan | RAP：发布或转化计划 |
| 11 | LMP: lifecycle and iteration | LMP：生命周期与迭代 |
| 12 | Quality built in | 质量内建 |
| 13 | Dynamic response | 动态响应 |
| 14 | TR/DCP review plan | TR/DCP 评审计划 |
| 15 | Decision request and next steps | 决策请求与下一步 |

## Example Prompts / 示例提示词

For an AI assistant or facilitation session:

用于 AI 助手或项目工作坊时，可以这样提问：

```text
Use the IPD project framing workflow to clarify this applied research project:
We want to study a new visual inspection algorithm for production-line defect detection, but we only have an early idea.

使用 IPD 项目梳理框架澄清这个应用研究项目：
我们想研究一种新的视觉检测算法，用于产线缺陷识别，目前只有初步想法。
```

```text
Use this workflow to prepare TR1 and CDCP review material for the concept phase.

使用这个工作流准备概念阶段的 TR1 和 CDCP 评审材料。
```

```text
Structure this engineering project into an IPD-style document and PPT outline:
<project background>

把这个工程项目整理成 IPD 风格文档和 PPT 大纲：
<项目背景>
```

```text
Continue from the previous project context and move into PDP. Focus on technical implementation path, resource plan, quality plan, and TR2/PDCP readiness.

基于上一次项目上下文继续推进到 PDP，重点梳理技术实现路径、资源计划、质量计划和 TR2/PDCP 准备度。
```

## Using With Different Tools / 用于不同工具

This repository is tool-agnostic:

本仓库不绑定特定工具：

| Context | How to Use | 中文说明 |
|---|---|---|
| AI-agent environment | Load `SKILL.md` as the primary instruction file and load `references/ipd-framework.md` when detailed templates are needed. | 在 AI 智能体环境中，可将 `SKILL.md` 作为主指令文件，需要详细模板时加载 `references/ipd-framework.md`。 |
| Manual workshop | Use the 4W2H table and six-phase lifecycle as the facilitation agenda. | 在人工工作坊中，可用 4W2H 表和六阶段生命周期作为引导议程。 |
| Project management | Copy the document and slide outline sections into internal templates. | 在项目管理实践中，可将文档结构和汇报大纲复制到内部模板。 |
| Organization rollout | Adapt terminology, review gates, quality roles, and deliverable names to match internal governance. | 在组织内部推广时，可调整术语、评审门、质量角色和交付物名称以匹配内部治理。 |

## Customization Ideas / 定制建议

| English | 中文 |
|---|---|
| Add organization-specific DCP/TR templates. | 增加组织特定的 DCP/TR 模板。 |
| Add industry-specific compliance checklists. | 增加行业合规检查清单。 |
| Add Word or PowerPoint templates under an `assets/` directory. | 在 `assets/` 目录下加入 Word 或 PowerPoint 模板。 |
| Add scripts to generate `.docx` or `.pptx` deliverables automatically. | 增加脚本自动生成 `.docx` 或 `.pptx` 交付物。 |
| Narrow the workflow for applied research, hardware products, software platforms, manufacturing process projects, or internal tools. | 针对应用研究、硬件产品、软件平台、制造工艺项目或内部工具进一步裁剪流程。 |

## License / 许可证

Add a license that matches the intended use before public distribution.

公开发布前，请根据预期使用方式添加合适的许可证。
