# 台账、方法记录与报告契约

## 1. 版本与文件

当前 Input/Report **1.4**，EvidenceQuality **1.2**，DecisionQuality **1.0**。

技能包操作版本2.0.0保持这四份契约。研究底稿和决定性论证作为artifact_paths附录；工具调用和估算仍记录在search/calculation log与E/P/M/method_audit。模板不允许任意新增JSON字段。定向方法试验可交备忘录与台账，不能标成完整1.4报告或伪填质量字段。

- [input.schema.json](input.schema.json)：用户自然语言补全的对象、范围、访问、评价设置和输出。
- [report.schema.json](report.schema.json)：实体、工作、原始来源、主张、证据、参数、要求、比较、模型、判断和覆盖。
- [evidence-quality.schema.json](evidence-quality.schema.json)：quality_audit、来源/证据依赖、共同前提、可见性、兑现、G1–G12 放行。
- [decision-quality.schema.json](decision-quality.schema.json)：method_audit、情境、M1–M9、集合综合及行动/组合/治理。

这四份契约只约束结构与部分语义，不证明事实正确。技能由模型使用已有工具执行，包内未提供自动采集、模型求值或语义校验器。不要宣称程序已自动验证。

## 2. 输入自动补齐

`evaluation` 包含 purpose、perspectives、decision_owner、objective_notes、preference_notes、proposed_actions、resource_boundary。仅评价贡献可 contribution_audit；多个视角分项，无默认总分。公共投入为问题或实际资金依据成立时才采用 public_funder，不预设全部研究由纳税人出资。

quality_policy 自动设 protocol_version=1.2、independence_mode=claim_specific，以及 outcome_blind_selection、require_search_matrix、require_premise_audit、require_quality_gates、require_visibility_audit、require_commercialization_review、require_method_audit=true。前者表示筛选标准不依结果方向，不能据此宣称实际盲法。

默认未知资源、决策主体和目标假设仍可继续；实际缺口写明。用户不用填 JSON。只需要修改已获授权的运行选择；不新增付费、公开发布或外部联系。

按 [输入发现](input-discovery.md)自动补 target 类型、identifiers/source_refs/notes、scope 和访问限制。项目只有名称/简介时按实际 proposal/report/mixed 材料记录身份/阶段，不新造 project 输入枚举。团队代表人物默认先作发现入口；用户授权只深读代表样本（本技能设计已有该偏好）时用 analysis_mode=sampled、sampling.method=purposive，并按既有字段记录 user_requested 的真实授权来源、frame、strata/实际 sample_size、limits；不伪造授权或统计代表性。全范围要求仍 comprehensive。

## 3. 引用与记录组织

为不同实体使用稳定 ID，例如 T/W/S/C/E/P/R/CMP/M/J、CTX/MC/SYN/FUND/FC/OPT/PORT/IMP/GOV。前缀是本地约定，无普遍标准；引用必须指向实际实体，不把自由文字当 ID。

两层输出映射：第一层学术/科学/方法/工程创新用 value_profile 数组中 dimension=academic 的范围记录，具体探索理由用 exploratory；第二层产业/商业/市场分别用 industrial 的不同 scope/notes 和 J/CTX 关联，社会用 social，组合资源含义用 resources。同维度的不同情境分别记录；不新加顶层 layer、commercial/market 维度或 low/high 枚举。详见 [两层评价](two-level-assessment.md)。搜索矩阵/需求表保存在日志/附录，其证据/关系/要求/方法接回原字段。

双版本是同一记录的两份 Markdown：report.md 与 report-public.md，input.output.formats 仍用 markdown/json/csv，选择保存在原请求/运行记录或既有 extensions 说明；report.artifact_paths 指向两版和映射位置。大众版新增事实/重算先更新台账和专业版，再重新放行/生成。主要结论/数字到 J/E/P/M 的映射在报告附录/等价记录，不新造 public_judgments 等必要字段。参数 JSON 字段是 origin/status，不是 type/state。

| M 模块 | completed 时的 record_ids 指向 |
| --- | --- |
| M1 评价情境 | decision_contexts.context_id |
| M2 集合确定性 | evidence_syntheses.synthesis_id |
| M3 资金额外作用 | funding_reviews.funding_review_id |
| M4 预测兑现/校准 | forecast_reviews.forecast_review_id |
| M5 信息价值 | research_options.option_id |
| M6 阶段/退出 | research_options.option_id；可与 M5 同记录，理由分别填写 |
| M7 组合增量 | portfolio_reviews.portfolio_review_id |
| M8 完整后果 | impact_reviews.impact_review_id |
| M9 治理与纠错 | governance.governance_id |

每 context 的 M1–M9 各一次；M1/M9 适用，其余按实际主张。一个记录可供相关检查复用，但同对象/范围/时间必须相符。method_check 记录的 claim/judgment IDs 应覆盖其服务的结论。applicability undetermined 不允许 status completed；not_applicable 理由需实质成立。

claim_reviews 关联 decision_context_ids、method_check_ids、evidence_synthesis_ids。每条关键判断和时间视角必须有独立放行依据；不可用事后全量证据支持事前论证。G1–G12 各一次，完成字段数量不能代替内容。

标准的编号/版本/原条款/状态与采用依据建 S/E，实际工程必要要求建既有 R，符合原质量规则才 gate_eligible；版本/条款矩阵保存日志/附录。奖励规则建独立 CTX，规范目标与偏好保存在既有 objective 的依据/证据、preferences、goal_challenge、use_limits，真实条件/符合性仍建 C/J，正式权重/模型有 P/M。资格/奖励必要条件不直接混成应用 R 的 gate_eligible。奖励矩阵文件用 artifact_paths，不新增 award_criteria 顶层或未知枚举；数值综合按 input.output.composite_score / preference_specification 原约束。

## 4. 生成过程中必须人工/工具核对的语义

- 来源存在且有真实定位，visible_scope 与实际读取一致；身份、版本、纳入/排除和覆盖分母未偷偷变化。
- 少量输入的身份/候选、关键词查询、对象—成果关系、团队代表选择及未覆盖部分可追溯；无全文项目的原文/补充/背景/推断/未知分开，不用相关论文补写申请书或结果。新发现文件用 artifact_paths，既有 work归属/取得/分析与 coverage 分母按实际状态。
- 标准/奖励规则版本符合评价时点，关键条款实际读取；技术门槛与奖项资格分开，AND/OR/等级与有出处权重不互换；取得受限不自动判不符合。
- 所有 ID 可解析到正确实体；不存在同 ID 对应两个不同对象；仅框架依赖不当成共享数据。
- 数字、单位、失效定义、要求适用与 gate_eligible 一致；未知不参与计算；删失不当精确寿命。
- 派生参数能回溯输入/模型/假设；金额/时间/作用边界一致；供应商、客户与公共收益不混加。
- 每个关键终点/工况有实际集合综合；一致性不能由排除不利材料得到；确定性不换成价值或成功概率。
- 公共资金/预测/下一步/组合/实际影响的适用检查有对应记录；unknown 不伪装不适用；partial 只支持相称措辞。
- 数量校准有参考类别/固定分母/随访；quantitative_voi 有概率/效用/模型/输出和敏感性，不用模型确信度补分布。
- context 的目标/主体/行动与建议一致；项目目标与上层需求的未验证前提明确；重叠效益和选择价值不重复计入。
- 每 judgment 与 claim_review 的范围、时点、method/quality 关联一致；正文不超过 permitted_wording。
- 专业/大众版及标题/图注的对象、时间、两层结论、确定性、数字/单位/分母、反证/未知、归因和行动强度一致；新事实不只进入科普版。量化/原理分析有实际过程或适用缺口，模板章节不能代替推导/执行。
- 更正保存原版与变更依据，受影响记录重新计算/放行。未收到回应、未做独立审查不编记录。

可使用已有 schema 校验工具作结构检查，但只有实际运行且任务授权测试/验证时才报告通过。本文不是校验器的替代证明。

## 5. 局部状态、缺失和迁移

完整约定范围和来源充分性分开。status 为 in_progress/needs_identity/partial/complete，source_coverage 为 sufficient_for_scope/source_limited。quality release 可以限制/暂缓某判断；这不使整个任务无限等待。

报告中不适用数组可为空，但由对应 check 解释；适用且缺数据可建 partial/unassessed 记录，保存未知与影响。不填假日期、价格、关系、统计量或模型结果。

旧报告 1.3/质量 1.1 升级须补 evaluation、method_audit、M1–M9、G11/G12 和引用。原始有效材料可以复用；未取得的保留未知。不能只改版本，不能用旧版本结构读取结果声称当前行为已验证。

Markdown、CSV 与 report.json 出自同一记录，更新后同时改派生输出。复杂图、读图估计或模型文件在 artifact_paths 保存位置；本地交付使用可点击绝对路径。公开论证保留前提/依据/推导/反例/结论，不输出未经核查的长推测。
