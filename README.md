# Academic Value Audit

**Academic Value Audit** is a Codex skill for evidence-grounded reviews of research claims and their real academic, industrial, social, and public-funding value. The first public release packages skill version **2.1.1**.

It is designed to answer questions such as:

- What did a paper, project, patent, prize-winning work, researcher, or research group actually contribute relative to the strongest relevant prior work?
- Which technical or scientific bottleneck does the contribution change, and does that change reach a useful task or system outcome?
- What do practitioners, critics, failed deployments, and competing approaches reveal that promotional narratives may omit?
- What should a funder support, defer, or decline next, and what evidence would change that recommendation?

The skill separates **publication-time academic contribution** from **current practical value**. It builds a task and system model, compares credible alternatives, checks claims against primary sources, and traces recommendations back to evidence and explicit assumptions. Reports normally include a detailed policy/funder version, a public-facing version, and source, search, parameter, calculation, and coverage records.

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

The skill is intended to support expert-authored subdomain modules. A module should explain the field's real task structure, decisive mechanisms and bottlenecks, strongest alternatives, scale-up constraints, key source routes, common misleading metrics, and the evidence that would change an investment recommendation. Start from [`assets/domain-module-template.md`](assets/domain-module-template.md) and follow [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Scope and limitations

This skill guides an AI agent's research and reasoning; it is not an automated database, independent peer review, financial audit, or guarantee of domain-expert accuracy. It requires the agent to state which sources it actually accessed and read, distinguish direct evidence from inference, pursue material counterarguments, and avoid turning missing evidence into a universal proof of zero value. Conclusions remain bounded by available evidence, source access, and the stated audit scope.

The included JSON schemas describe the project's report records; they do not by themselves establish factual correctness or behavioral reliability. Domain experts and users should review consequential conclusions and propose corrections with evidence.

## Version

- Public repository release: first public release
- Skill package version: 2.1.1
- Audit date policy: use the execution environment's current date and state it in the report

## License

Licensed under the MIT License. See [`LICENSE`](LICENSE).

---

# 学术真实价值审计

**Academic Value Audit** 是一个 Codex skill，用于以证据为基础，评估学术成果的真实学术、产业、社会与公共经费价值。当前首个公开版本打包技能版本 **2.1.1**。

它关注的问题包括：一篇论文、一个项目、一项专利、一个奖项成果或一个团队究竟新增了什么；这项增量是否改变真实任务的关键瓶颈；最强替代方案能否以更低资源完成同一任务；以及下一笔经费应支持、暂缓还是拒绝什么工作。

技能把发表时的学术贡献与当前现实应用价值分开评价，并要求报告交代实际读取的来源、反方争点、参数和推理链。通常交付面向政策与经费管理者的专业版、大众版，以及证据、搜索、计算和覆盖记录。

安装时将本目录复制到 `~/.codex/skills/academic-value-audit/`；Windows 默认位置为 `%USERPROFILE%\.codex\skills\academic-value-audit\`。可通过 `$academic-value-audit` 调用。

本技能是研究与判断工作流，不是自动事实数据库、独立同行评审、财务审计或正确性保证。报告必须说明来源取得范围、事实与推论的区别及调查边界；重要决策仍应由领域专家复核。
