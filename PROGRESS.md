# XPIN-VIDEO · 整合进度 / 续接入口

更新：2026-10-10 · **v1.5.1 生产文案去历史说明** · **只做整合，真实制作/实测由用户负责。**

## 不变约定

- **自包含**：生产只读本仓 `AGENTS.md → SKILL.md → 当前 stage`。旧差点后期/AE/Blender 等仓库、Library 仅供**维护整合时**查阅，不作为生产依赖。
- **少而精**：新增经验优先压缩/替换 4 个 stage 的原文。主 SKILL 极短，不新建外部模块、样例大全、重复风格卡或冗长提示词。
- **真实范围**：没查的资料、没下载的文件、没实际查看的视频、没运行的代码都不得算「完成」。本轮不进行 AE/Blender/Codex/HTML 生产测试。
- **自由度**：目标与已锁定事实必须准确，技术方案留给 Codex。未明确授权的制作不越阶段；用户明确「直接做」时不增设审批表单。

## 已完成

- [x] P0–P4：初版完整工作流、短入口、4 阶段。
- [x] P5a（历史）：HTML RAM 小样的局部机制试验；不代表整片或真实 AE/Blender 验收。`tests/p5-ram-pilot.html` 仅作历史记录。
- [↗ 用户负责] P5b：真实 Codex/AE/Blender/Windows 工程、控件、Marker、画质和回归测试。**后续不要把此项列为 Agent 待执行动作。**
- [x] P6：Library 动画升级 v5、分镜 Agent、日常复盘和旧 AE/Blender 仓库核心经验提纯。
- [x] P7：查 `/Daily Review` 2026-09-17—10-09 共 23 份记录，过滤高价值生产原则。
- [x] **P8（本轮）**：全面盘点 [差点后期旧仓](https://github.com/kzz-x/chadian-post-GTP-project) 的当前文件树；重点研究主 `skill/SKILL.md`、`skill/references/` 的 **20 个直接参考文件**、**000–017 共 18 张风格卡**、`skill/evals/evals.json`、项目说明/状态/交付约定。只提炼 XPIN-VIDEO 尚无的短规则，修改 01–04 阶段文件，**主 `SKILL.md` 不变、无外挂仓库依赖**。
- [x] **P9（本轮）**：深挖 [XPIN-AE-SKILL](https://github.com/kzz-x/XPIN-AE-SKILL) 的当前仓库结构与 Mini / Full 入口，针对工程架构、关系 Rig、视觉反馈、口播、模板、MCP/JSX、动画验收等取得并筛选约 27 份核心文件。只增补现有 02/03/04，主 Skill 不变；未遍历旧 archive 全文，亦未运行 AE/Codex。
- [ ] **P10（下一步，只做整合）**：对比 Library `/差点后期V3`、`/差点后期V4`、`/差点素材` 与 P8 旧仓的增量价值；仅收留能减少返工的新原则，继续压缩既有阶段规则。不建立外挂、不执行实测。

## P8 真正吸收的内容

| 位置 | 提炼结果 |
|---|---|
| `01-storyboard.md` | 分镜优先「对比/因果/状态变化/整体-局部/证据」；明确段前/段后括号标注作用域；「继续/剩下的」依真实镜头状态与授权判断，绝不凭猜测重做 |
| `02-direction.md` | 明确 Truth / Reference / Asset 三种独立检索目标；素材候选与事实信源分开，记录实际观看/风险；资产标记真正取得还是仅候选；元素真实 Alpha、组图和拆分区分；**按需**封面真实产品/双版/可编辑标题区 |
| `03-production.md` | 数据图表统一数据源、来源/时间/单位/口径，避免视觉误导；可编辑性不能用假 UI 冒充（seek≠关键帧编辑、localStorage≠完整工程保存）；生成屡次失败时换参考/机制或精简不必要复杂度，变更已批准媒介需用户同意 |
| `04-finish.md` | 画面来源与事实证据区分，CGI/示意不冒充实拍；检查元素 Alpha/拆分、AI 视频主体连续、工程改值/保存重开；已核、失败、未测分开报告 |

## P8 不照搬的部分（避免规则膨胀）

- **旧 12–20 张参考板、B0/B1/B2 层层审批**不符合「尽量三轮内定位/有效选图」；素材真正需要多找时仍可按用户要求提供更多候选。
- **旧仓从头必须停 A 的绝对状态机**只保留「全文不自动授权生产」的边界，允许用户明确直接制作时合并必要设计/执行。
- **强制转读外部 AE Skill 的 handoff**违背自包含；已内置跨 AE/Blender/HTML 的少量生产标准。
- 18 张风格卡与 000–017 编号是历史设计样本，不复制进主规则；遇到需求应反向检索合适风格，按成片目标选择，而非默认「科技=霓虹/玻璃」。
- 旧仓封面精确配额、完整项目状态文件树、全部参数/面板规范、极长媒介 QA 清单、临时问题/故障说明均不作为每镜必须执行的负担。
- `skill/evals/evals.json` 是旧仓的行为预期集，**不是** XPIN-VIDEO 的真实软件测试结果。

## 2026-10-10｜生产文件去迁移说明

用户明确要求：生产 Skill 不写「已内置」「相当于旧能力」「无需跳旧仓」等历史整合说明。已清理 `AGENTS.md`、`SKILL.md`、`02-direction.md`、`03-production.md` 和 README；具体生产约束保留，迁移历史仅记 `PROGRESS.md`。后续整合默认只增减执行规则，不描述旧仓来源、迁移原因或自包含状态。

## P9 差点 AE 深挖：新吸收与舍弃

**读到的核心：** 最新 `AGENTS.md`、Mini/Full SKILL、Project Context Map、Editable Engineering Gate、Motion Control Architecture、Relationship Rigs、Speech-Driven Motion、AE Implementation/Build Spec、Visual Anchor/Feedback Loop、Creative Authority、Control Surface、Learn AEP、Refactor/Style Pack、动画 QA、原生 AE 和 JSX/Undo 等。

**新增到 XPIN-VIDEO：**
- `02-direction.md`：技术/视觉路由增加 AI 适配度判断；规则化、重复、可验证的任务可直接交 AI，构图/Graph/Taste 主导的 Motion 应先由人或参考锁定关键意图；**不能按“从零/对象多”机械判断难度**。
- `03-production.md`：简单新镜头不强迫搭 Null/CTRL/Rig；**共享 Motion 上移、独特 Motion 保持局部、人工 Offset 与原动画分离**；Attach/Carry/Follow/Target/动态布局先建立真实关系，不复制近似关键帧；有价值的主 Motion 留 Graph，人可微调；既有 CTRL 先复用、模板控件需易找和 Reset；MCP/JSX 失败或超时先读状态，再决定补丁，不盲重复执行；长期工程可维护几百字的合成/控件/素材/依赖/人工区 Fast Path 索引，工程真实状态优先。
- `04-finish.md`：截图优先围绕 Marker、动作峰值与 Hold 取代表帧；**截图识别症状，工程数据定位原因**，连续速度/错帧与手感仍需要真正播放，不以关键帧代替 Motion 验收。

**处理了一项旧资料内部冲突：** 旧 Editable Gate 文档有“新建完整镜头即可进入重工程化”的表述，但当前仓库顶层 `AGENTS.md` / Full 核心明确“仅因实际关系、复杂 Motion 或复用而触发；简单新建用 Mini”。**采用当前顶层路由，不搬旧宽泛触发条件。**

**刻意未移植：** AE26 ExtendScript 特定坑、Engine Room 的 UndoGroup/Purge 细节、工具 JSON 参数与安装说明、巨大历史工程标准、各种 Motion Primitive 参数表、模板库复杂目录方案、学习 AEP 多卡晋升制度。它们是 AE 专用实现/故障知识，不应扩成 XPIN-VIDEO 的日常规则。本轮并非真正的软件质量验证。

## 下轮新对话可直接复制

「继续整理 `kzz-x/XPIN-VIDEO`，读取 `PROGRESS.md`、`AGENTS.md`。从 P10 开始，对比 Library 差点后期 V3/V4 与差点素材文件夹的新增价值，去重后只压缩整合当前 4 个 stage。不要外挂 Skill/复制旧仓内容，也不要执行任何视频或软件实测（我自己测试）。完成后更新进度仓库。」

维护原则：判断经验是否跨任务成立、是否比已有句子更好、是否明显减少返工。**符合才写；否则留作来源或案例。**
