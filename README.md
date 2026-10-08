# Academic Value Audit | 学术真实价值审计

**Academic Value Audit** is a Codex skill for evidence-grounded reviews of research claims and their real academic, industrial, social, and public-funding value. The current skill package version is **2.2.0**.

It is designed to answer questions such as:

- What did a paper, project, patent, prize-winning work, researcher, or research group actually contribute relative to the strongest relevant prior work?
- Which technical or scientific bottleneck does the contribution change, and does that change reach a useful task or system outcome?
- What do practitioners, critics, failed deployments, and competing approaches reveal that promotional narratives may omit?
- What should a funder support, defer, or decline next, and what evidence would change that recommendation?

The skill separates **publication-time academic contribution** from **current practical value**. It builds a task and system model, compares credible alternatives, checks claims against primary sources, and traces recommendations back to evidence and explicit assumptions. Reports normally include a detailed policy/funder version, a public-facing version, and source, search, parameter, calculation, and coverage records.

Both reports explain the actual work, its operating mechanism, the strongest alternatives, and the causes of the field's bottlenecks. The public report defaults to a detailed plain-language article rather than a short summary. See the [explanatory-depth and writing guide](references/explanatory-depth-and-public-writing.md).

## Standards, theories, and methods it draws on

The audit workflow adapts established methods to cross-disciplinary research and funding questions. It does not treat any framework as a universal scoring formula, and inclusion here does not mean that the framework's publisher endorses or has validated this skill.

- **Responsible research assessment:** DORA, the Leiden Manifesto, and CoARA inform content-based assessment, transparent indicators, and safeguards against journal-metric shortcuts.
- **Evidence quality and search transparency:** Cochrane evidence-synthesis guidance and GRADE inform study-level bias and body-of-evidence certainty; Evidence to Decision separates evidence from recommendations; PRISMA-S informs reproducible search records.
- **Technology and system value:** Health Technology Assessment (HTA), techno-economic analysis (TEA), life-cycle assessment (LCA), ISO 14040, and systems engineering inform task definition, system boundaries, alternatives, and whole-life consequences.
- **Demand and public impact:** the OECD Oslo Manual, customer-discovery methods, the UK Green Book, the Magenta Book, and Theory of Change inform demand testing, counterfactuals, additionality, distribution, and causal links from outputs to outcomes.
- **Maturity and next-step decisions:** GAO Technology Readiness Assessment guidance, TRL, value-of-information analysis (VOI/EVSI), and staged testing inform readiness, uncertainty reduction, and whether to support, defer, or stop the next step.
- **Specialized evidence collection:** WIPO patent-landscape guidance, AAPOR disclosure standards, and grey-literature search methods inform source discovery and method checks where applicable.

Each method is used only for the question it can answer, with its domain, version, assumptions, and limits checked. The [method-source register](references/method-sources.md) links the sources and records key adaptation limits. Domain modules may add field-specific standards, models, and source routes.

## Install

Copy this folder into your Codex skills directory:

```text
~/.codex/skills/academic-value-audit/
```

On Windows, the default location is:

```text
%USERPROFILE%\.codex\skills\academic-value-audit\
```

Then invoke it explicitly, for example:

```text
$academic-value-audit Review DOI 10.xxxx/example. Compare the claimed contribution with the field's strongest alternatives, trace the application claim to task-level evidence, and give a funding recommendation with sources and calculations.
```

## What's included

- `SKILL.md` — entry point and audit contract
- `references/` — research workflow, evidence and decision quality, source discovery, practitioner debate, cost and demand analysis, and domain-specific modules
- `assets/` — professional/public report templates, research workbook, decisive-argument template, and a template for expert-authored domain modules
- `agents/openai.yaml` — Codex-facing display metadata

## Contributing domain modules

Domain experts are invited to contribute both **drop-in domain modules** and **more detailed companion sub-skills**. A module should explain the field's real task structure, decisive mechanisms and bottlenecks, strongest alternatives, scale-up constraints, key source routes, common misleading metrics, and the evidence that would change an investment recommendation. A companion sub-skill can provide a deeper field workflow while mapping its conclusions back to the core audit's evidence and decision rules. Start from [`assets/domain-module-template.md`](assets/domain-module-template.md) and follow [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Scope and limitations

This skill guides an AI agent's research and reasoning; it is not an automated database, independent peer review, financial audit, or guarantee of domain-expert accuracy. It requires the agent to state which sources it actually accessed and read, distinguish direct evidence from inference, pursue material counterarguments, and avoid turning missing evidence into a universal proof of zero value. Conclusions remain bounded by available evidence, source access, and the stated audit scope.

The included JSON schemas describe the project's report records; they do not by themselves establish factual correctness or behavioral reliability. Domain experts and users should review consequential conclusions and propose corrections with evidence.

## Version

- First public release: v2.1.1
- Current skill package version: 2.2.0
- Audit date policy: use the execution environment's current date and state it in the report

## License

Licensed under the MIT License. See [`LICENSE`](LICENSE).

---

# Academic Value Audit | 学术真实价值审计

**Academic Value Audit** 是一个 Codex skill，用于以证据为基础，评估学术成果的真实学术、产业、社会与公共经费价值。当前技能版本为 **2.2.0**。

它关注的问题包括：一篇论文、一个项目、一项专利、一个奖项成果或一个团队究竟新增了什么；这项增量是否改变真实任务的关键瓶颈；最强替代方案能否以更低资源完成同一任务；以及下一笔经费应支持、暂缓还是拒绝什么工作。

技能把发表时的学术贡献与当前现实应用价值分开评价，并要求报告交代实际读取的来源、反方争点、参数和推理链。通常交付面向政策与经费管理者的专业版、大众版，以及证据、搜索、计算和覆盖记录。

两版都要讲清成果本体和工作原理、具体创新、最强替代及瓶颈原因。大众版默认采用详细直白的解释性长文，充分说明为什么得到结论，不能自动缩成短摘要。详见[解释深度与写作要求](references/explanatory-depth-and-public-writing.md)。

## 参考的标准、理论与方法

本技能将成熟方法按问题适配，不把任何框架当成跨学科通用打分公式；列出这些方法也不代表其发布机构认可或验证了本技能。

- **负责任的科研评价：** DORA、《莱顿宣言》、CoARA，用于评价具体贡献、透明使用指标，避免以期刊指标替代成果判断。
- **证据质量与检索透明：** Cochrane 指南、GRADE、Evidence to Decision、PRISMA-S，用于审查证据偏倚、证据确定性、证据与建议的区别及可复现检索。
- **技术与系统价值：** 卫生技术评估（HTA）、技术经济分析（TEA）、生命周期评价（LCA）、ISO 14040、系统工程，用于界定任务和系统边界、比较替代方案及全生命周期后果。
- **需求与公共影响：** OECD《奥斯陆手册》、客户发现、英国 Green Book、Magenta Book、变化理论，用于检验需求、反事实、公共资金额外作用、分配和产出到结果的因果链。
- **成熟度与下一步决策：** GAO 技术成熟度评估指南、TRL、信息价值分析（VOI/EVSI）、分阶段验证，用于分析技术阶段、不确定性及下一步的支持/暂缓/停止选择。
- **专项资料搜集：** WIPO 专利景观指南、AAPOR 调查披露标准和灰色文献检索方法，在适用时用于系统发现资料并审查方法。

每种方法只回答其适用的问题，并核对版本、假设和边界。详见[方法来源登记表](references/method-sources.md)，其中列出了来源及采用限制；领域模块可补充相应学科的专用方法和标准。

安装时将本目录复制到 `~/.codex/skills/academic-value-audit/`；Windows 默认位置为 `%USERPROFILE%\.codex\skills\academic-value-audit\`。可通过 `$academic-value-audit` 调用。

本技能是研究与判断工作流，不是自动事实数据库、独立同行评审、财务审计或正确性保证。报告必须说明来源取得范围、事实与推论的区别及调查边界；重要决策仍应由领域专家复核。
