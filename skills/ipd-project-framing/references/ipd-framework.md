# IPD Architecture Reference

This reference summarizes the user's IPD architecture guide and adapts it for engineering projects, product package work, and applied research projects.

## Overall Architecture

Use five layers:

| Layer | Meaning | Questions |
|---|---|---|
| Input layer | market opportunity, customer requirement, policy environment, competitive intelligence, technology trend | What evidence proves this is worth doing? |
| Decision layer | IRB/PM-style decisions, resource allocation, priority, DCP, quality gate | What decision is needed and who owns it? |
| Execution layer | CDP -> PDP -> ADP -> VAP -> RAP -> LMP | Which phase is the project in now? |
| Support layer | CBB, technology platform, knowledge management, toolchain | What can be reused or institutionalized? |
| Output layer | manufacturable, procurable, serviceable, profitable product package | What complete package will be delivered or transferred? |

For applied research, interpret the output layer as: transferable, reusable, verifiable, and valuable research-to-engineering capability.

## Six IPD Phases

| Phase | Name | Goal | Main Deliverables | Review |
|---|---|---|---|---|
| CDP | Concept Development Phase | Clarify why to do it and what to build | market insight report, competition analysis, requirement list, concept description, roadmap, product/project package requirements, initial business/value plan, risk assessment, quality goals, CTQ list | TR1 + CDCP |
| PDP | Plan Development Phase | Clarify how and when to do it | competitiveness plan, IP strategy, technical barrier plan, system architecture, technical implementation path, cooperation plan, manufacturable/procurable/serviceable analysis, project plan, resource plan, milestone plan, quality plan, test strategy | TR2 + PDCP |
| ADP | Development Phase | Implement according to design specification | detailed design, prototype/sample/model, CBB list, FMEA/DFMEA, test report, audit report, issue tracker, supplier/partner plan | TR3/TR4 + ADCP |
| VAP | Validation Phase | Verify requirement satisfaction and release readiness | system test report, beta/pilot report, compliance evidence, quality achievement evaluation, residual issue list, maturity assessment, pilot run/process validation report | TR5/TR6 |
| RAP | Release Phase | Release, transfer, or enable adoption | release plan, marketing/use enablement package, training material, ramp-up plan, SPC or operation-monitoring report | LDCP |
| LMP | Lifecycle Management Phase | Maximize value and manage iteration/end-of-life | cash-flow/value analysis, VAVE plan, quality monthly report, policy impact assessment, version iteration plan, change request, EOL decision report, service continuation plan, knowledge archive | lifecycle decision |

## 4W2H Mapping

| Dimension | IPD Interpretation | Common Deliverable |
|---|---|---|
| What | product/project concept, requirement, deliverable, non-scope | concept description, requirement list |
| Why | market/application opportunity, policy/customer pain, value | market insight, value proposition |
| Who | customer, user, receiver, decision maker, PDT, quality roles | stakeholder map, RACI |
| When | milestones, TR/DCP timing, version roadmap | milestone plan, review calendar |
| How | architecture, technical path, research route, CBB, test path | architecture, route comparison |
| How much | resources, target cost, profitability, effort, research value | resource plan, cost/value model |

## Fourteen Core Modules

Use these modules to avoid duplicate thinking:

| No. | Module | Phase |
|---|---|---|
| 1 | Market insight: Why | CDP |
| 2 | Product/project concept and roadmap | CDP |
| 3 | Competitiveness planning | PDP |
| 4 | Technical implementation path | PDP |
| 5 | Manufacturable/procurable/serviceable analysis | PDP |
| 6 | Intellectual property and technical barrier | PDP |
| 7 | Project plan and milestones | PDP |
| 8 | Engineering development | ADP |
| 9 | Quality built-in system | All phases |
| 10 | System verification | VAP |
| 11 | Market release and sales/use design | RAP |
| 12 | Cash flow, cost, and profitability/value analysis | LMP |
| 13 | Dynamic response mechanism | All phases |
| 14 | Lifecycle management | LMP |

## Quality Built-In System

Quality is embedded in the whole lifecycle.

| Phase | Quality Activities | Output |
|---|---|---|
| CDP | CTQ identification, quality goal definition, initial compliance judgment | quality goal plan |
| PDP | DFMEA/FMEA, quality plan, test strategy, supplier or partner quality agreement | DFMEA report, quality plan |
| ADP | design/code review, unit and integration test, process audit | review notes, test report, audit report |
| VAP | system test, reliability verification, beta/pilot, certification/compliance test | verification report, certification evidence |
| RAP | SPC or operation monitoring, market/user issue monitoring, satisfaction survey | SPC/operation report, satisfaction report |
| LMP | continuous improvement, VAVE, quality retrospective, knowledge sedimentation | improvement report, quality retrospective |

Quality roles when relevant:

| Role | Responsibility | Phase |
|---|---|---|
| PQA | whole-process quality planning, audit, issue closure | all phases |
| SQA | supplier/partner quality and incoming quality | PDP-RAP |
| DQA | design review, DFMEA, design conformance | PDP-ADP |
| TQA | test strategy, test case review, defect management | ADP-VAP |
| MQA | process quality, pilot issues, production/operation metrics | VAP-LMP |

## Dynamic Response Mechanism

Use this closed loop:

1. Sense: policy, market, customer, supply-chain, and technology signals.
2. Analyze: impact matrix by phase, scope, cost, quality, compliance, and schedule.
3. Decide: lightweight DCP, CRB, roadmap decision, or normal phase DCP.
4. Execute: adjust technology, business/use model, supply chain, compliance, or roadmap.
5. Feedback: evaluate response effect, archive knowledge, update rules.

Dynamic response examples:

| Phase | Change Type | Response | Decision Owner |
|---|---|---|---|
| CDP | policy direction changes | reassess opportunity and concept direction | IRB |
| PDP | subsidy decline or standard upgrade | adjust target cost, technical route, certification plan | PM |
| ADP | disruptive competitor/product appears | start technical attack, adjust feature priority, file IP | PDT manager |
| VAP | new mandatory regulation | add testing/certification, design change | PQA + PM |
| RAP | demand below expectation | adjust release cadence, promotion, channels | market owner |
| LMP | policy encourages new technical route | start next-generation pre-research, migrate CBB | technology planning |

Architecture elasticity principles:

- Technical elasticity: modular architecture, standardized interfaces, replaceable CBB.
- Cost elasticity: tiered target cost design.
- Compliance elasticity: pre-certification paths and multi-standard compatibility.
- Supply-chain elasticity: dual sourcing and substitution plans.

## DCP and TR

Every DCP must produce one of:

- Go: continue.
- Kill: terminate.
- Redirect: adjust direction.
- Hold: pause.

TR review evidence:

| TR | Focus |
|---|---|
| TR1 | product/project requirement and concept |
| TR2 | system specification and plan |
| TR3 | high-level design |
| TR4 | detailed design |
| TR5 | prototype/sample/model readiness |
| TR6 | pilot/small-batch/final validation readiness |

## Document Template

```markdown
# 项目名称：<名称>

## 1. 执行摘要
- 项目一句话定义：
- 项目类型：工程项目 / 产品包 / 应用研究 / 混合型
- 当前IPD阶段：
- 本次决策请求：
- 推荐结论：Go / Kill / Redirect / Hold / 待定

## 2. 4W2H 项目定义
| 维度 | 当前结论 | 证据/来源 | 不确定性 | 下一步 |
|---|---|---|---|---|
| What |  |  |  |  |
| Why |  |  |  |  |
| Who |  |  |  |  |
| When |  |  |  |  |
| How |  |  |  |  |
| How much |  |  |  |  |

## 3. IPD 架构层映射
| 层级 | 本项目内容 | 关键缺口 |
|---|---|---|
| 输入层 |  |  |
| 决策层 |  |  |
| 执行层 |  |  |
| 支撑层 |  |  |
| 输出层 |  |  |

## 4. CDP：概念阶段
- 市场/应用洞察：
- 用户/客户痛点：
- 产品/项目概念：
- 需求清单：
- 初步价值/商业论证：
- CTQ和质量目标：
- TR1/CDCP准备度：

## 5. PDP：计划阶段
- 竞争力规划：
- 技术实现路径：
- 可制造/可采购/可服务或可转化分析：
- 项目计划与里程碑：
- 资源和成本/价值：
- 质量计划与测试策略：
- TR2/PDCP准备度：

## 6. ADP：开发阶段
- 工程开发/研究实现：
- 原型/样机/模型：
- CBB复用或知识资产：
- FMEA/DFMEA和问题闭环：
- TR3/TR4/ADCP准备度：

## 7. VAP：验证阶段
- 系统验证/实验验证：
- 合规/安全/可靠性：
- 试点/Beta/场景验证：
- 成熟度和遗留风险：
- TR5/TR6准备度：

## 8. RAP：发布/转化阶段
- 发布/转化策略：
- 培训/赋能/移交：
- 量产/推广/试运行计划：
- LDCP准备度：

## 9. LMP：生命周期管理
- 版本迭代：
- 价值/成本/质量跟踪：
- VAVE或持续改进：
- 知识归档和CBB沉淀：
- EOL或下一代规划：

## 10. 质量内建计划
| 阶段 | 质量活动 | 输出物 | 责任人 | 状态 |
|---|---|---|---|---|

## 11. 动态响应机制
| 变化信号 | 影响分析 | 决策机制 | 响应动作 | 反馈方式 |
|---|---|---|---|---|

## 12. TR/DCP 评审计划
| 节点 | 类型 | 输入材料 | 评审问题 | 输出决策 | 时间 |
|---|---|---|---|---|---|

## 13. 风险、假设与依赖
| 编号 | 类型 | 描述 | 影响 | 概率 | 应对措施 | 责任人 |
|---|---|---|---|---|---|---|

## 14. 下一步行动
| 行动 | 负责人 | 截止时间 | 产出 |
|---|---|---|---|
```

## PPT Outline Template

| Slide | Title | Core Message | Suggested Visual |
|---|---|---|---|
| 1 | 项目名称与决策请求 | 本次希望通过什么决策 | title + decision tag |
| 2 | IPD 架构视图 | 项目如何落在输入、决策、执行、支撑、输出五层 | architecture map |
| 3 | 4W2H 项目定义 | 用一页讲清项目为什么存在 | 4W2H table |
| 4 | CDP：机会与概念 | 为什么做、做什么 | market/value map |
| 5 | PDP：计划与路径 | 怎么做、何时做、用多少资源 | roadmap + WBS |
| 6 | 技术路线与竞争力 | 推荐路线为何能形成优势 | route comparison |
| 7 | 可制造/可采购/可服务/可转化 | 结果是否能落地 | feasibility matrix |
| 8 | ADP：开发实现 | 如何构建原型、样机、模型或工程结果 | development plan |
| 9 | VAP：验证方案 | 如何证明满足需求和质量目标 | verification plan |
| 10 | RAP：发布或转化 | 如何进入市场、现场、团队或工程体系 | release/transfer plan |
| 11 | LMP：生命周期与迭代 | 如何持续创造价值并沉淀知识 | lifecycle roadmap |
| 12 | 质量内建 | 质量不是最后检查，而是全流程设计 | quality gate map |
| 13 | 动态响应 | 如何应对政策、市场、客户、供应链和技术变化 | response loop |
| 14 | TR/DCP 评审安排 | 关键技术和商业决策如何闭环 | gate timeline |
| 15 | 决策请求与下一步 | Go/Kill/Redirect/Hold 和近期行动 | decision list |
```
