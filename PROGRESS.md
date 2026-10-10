# XPIN-VIDEO · 整合进度 / 续接入口

更新：2026-10-10 · **v1.5.11 P18 Blender / AE / WorkBuddy 差异核验完成** · **只做整合，真实制作/实测由用户负责。**

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
- [x] **P9（此前）**：深挖 [XPIN-AE-SKILL](https://github.com/kzz-x/XPIN-AE-SKILL) 的当前仓库结构与 Mini / Full 入口，针对工程架构、关系 Rig、视觉反馈、口播、模板、MCP/JSX、动画验收等取得并筛选约 27 份核心文件。只增补现有 02/03/04，主 Skill 不变；未遍历旧 archive 全文，亦未运行 AE/Codex。
- [x] **P8b（本轮）**：再次逐项核对差点后期旧仓主 Skill、20 个直接 references、000–017 共 18 张风格卡、15+ 行为案例，与 XPIN-VIDEO v1.5.1 去重；仅修改既有四个 stage，不动主入口，不做软件实测。
- [x] **P10a**：读取 Library `/差点素材` 的「差点素材系统指令.txt」（206 行），对照 P8 旧仓和四阶段规则，提炼真实素材的授权范围、剪辑交接动作点和官方 App/软件图标核版要求，仅压入 `02-direction.md`。
- [x] **P10c｜差点灵感深挖（先于剪辑闭环）**：对照此前的「差点灵感」候选方案、Library 的 10/05 Daily Review、「差点分镜」Agent 与已存在的动效资产索引；查证成熟镜头配方系统的真实卡片、动态预览与源码。只精简强化 `02-direction.md`（按叙事/动作机制找卡、参考再创作、用户素材沉淀）和 `03-production.md`（卡片必须对准动态样片及源码），不复制外部卡片或建立生产依赖。
- [ ] **差点灵感独立系统落地**：当前可访问的 Library、Drive 与所查 GitHub 仓库内尚未定位到「差点灵感」独立 Agent 主文件及已积累的完整卡库。早期日报明确标为 Candidate；本轮不是建设完成或产出真实灵感卡的证明。
- [ ] **P10b｜来源不可见，暂不补写**：Library `/差点后期V3`、`/差点后期V4` 文件夹可定位；文件夹普通/递归列表、限定搜索及全库标题补查均未取得其目录下可读内容。不能据此断言原始项目没有资料，也不能假称已对比 V3/V4；以后只有实际发现源文件才继续本项。

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

## P8b 补充提炼：少量可复用的真增量

- `01-storyboard.md`：并行镜头回收必须由主 Agent 检查真实产物、全局风格和镜头衔接；只返工受影响的镜头。
- `02-direction.md`：参考明确借用/不借用的特征；运动关键时用实际动态参考，不从静帧推断；素材检索从可观察画面项出发，先去重候选再标风险；多来源资产统一设计语言。
- `03-production.md`：文案/粗动画/视觉锚点的职责分开，避免「旧视觉全保留」与「外观重做」冲突；程序化随机效果能按时间复现。
- `04-finish.md`：跨镜宏微观空间定位与结构身份连续；网页录制须核查真实录入层、字体、混合模式及容器/编码，而非只看录制成功。
- **不移植**：18 张风格卡正文、强制封面 B0–B2 阶段、定量配额、大型状态文件树、过度参数化工程清单和旧行为测试条款；与现有内容重复的规则也不再追加。旧 `evals` 只是测试用例定义，不当作执行结果。

P8b 仅文本/仓库内容比对与提交，**没有执行任何 AE、Blender、Codex、HTML 或视频实测**。

## P10a Library 素材补充：本轮真实范围

实际读取：Library「差点素材系统指令.txt」（206 行）。已比较其素材渠道、产品官方源、查询词、版权标签、事实/画面分离和剪辑交接规则；多数在 P8 已吸收。

**新增：** `02-direction.md` 压缩加入「商用/改编/署名/平台使用范围不可由网页公开推断；不能遮水印代替授权」「剪辑交付记录口播对应的动作落点和裁切/抠图需求」「真实 App/软件图标核对官方商店/官网当前版本」。

**未迁入：** 原始 206 行大段平台列表、全镜头强制表格、JSON 字段模板、每镜强制搜索词、来自旧 Agent 运行时的内存/工作目录约定。这些对 XPIN-VIDEO 日常生产属于重复、平台特定或过度流程化内容。

V3/V4 本轮仅确认了目标 Library 文件夹的可见性，**没有读到文件内容**；P10b 保持未完成。本轮未做 AE/Blender/HTML/Codex/视频实测。

## P10c｜差点灵感：从收藏升级为可执行配方

**已证实的差异：** 旧资源索引只记录工具/网站，缺少「镜头功能 → 动态机制 → 原始参考 → 可用源码 → 可替换项 → 失败案例」的可追溯链；单纯的 Reference First 也不足以确保 AI 真正复用调校好的动作。

**实际检查过的实例：** [video-shotcraft](https://github.com/Vincentwei1021/video-shotcraft) 的 `graze-face-tour`、`line-carry-transition` 镜头卡；[video-talkcraft](https://github.com/Vincentwei1021/video-talkcraft) 的 `callout-line-label`、`chip-grid-single-select` 镜头卡。这些包含适用意图、关键动作、参数/时序命门、失败坑和准确源码定位。另核验 Motionographer/Stash 作为高质量视觉参考与 Remotion/Onda/RemotionUI 等作为代码案例候选；视觉作品不自动等于可复用源码或使用授权。

**吸收的两条通用原则：** ① 灵感应按叙事功能/镜头动作匹配，用户提供的图片、视频或工程可逆向提炼视觉/动作/技术机制并带来源去重留卡；② 借配方时先对应查看动态预览与真实源码，继承动作的关键因果与节奏，示例文案/品牌/外观应服务新镜头重新设计。旧卡参数不能冒充本项目验收。

**暂不做：** 不复制上百镜头卡/风格卡、不强制某个动画库、不增加新文件夹、不将外部 GitHub/Library 变为日常运行依赖；不声称独立「差点灵感」Agent、索引、自动采集、持久写卡和生产测试已经完成。若后续明确要建设独立 Agent，最小可落地系统应另行设计，非本轮 XPIN-VIDEO 主 Skill 职责。

## P11–P19｜剩余来源逐个深挖计划（2026-10-10）

**执行方法（维护期，不进入生产 Skill）：** 每轮只完成一个来源/明确子批次。先列真实文件与可访问性 → 按需读源码、参考图/成片、复盘 → 与 `01–04` 去重 → **真正有增量才合并或替换**（每轮尽量 ≤3 条，不凑数）→ GitHub 提交并读回核实 → 更新此表状态、实际覆盖和下一项。不同仓库只作研究源；正式视频制作不依赖外仓。未实读的图片/二进制、未观看的视频、没跑的程序一律保留「未核」标记。

| 顺序 / 状态 | 来源和重点 | 结束条件 |
|---|---|---|
| **P11 ✓** | [Xpin](https://github.com/kzz-x/Xpin)：差点动效 Motion/视觉/技术配方、资产调度、16 张风格卡及参考图 | 文本与参考图的代表性核验已完成，增量合入 02/03；原视频不在仓库中，剩余高清原图按需查看 |
| **P12 ✓** | [GPT](https://github.com/kzz-x/GPT)：后期、Vibe Motion、视觉模板 `knowledge/*` 知识卡/失败库；旧动效 Pro 与源索引 | 已抽取真实编辑/AI 连续性增量并修改 02/04，验证镜像/Pro 实际能力边界；不复制旧架构 |
| **P13 ✓** | Google Drive / Library：个人收藏、差点动效融合卡、创意/视觉总监资料、`Kai Motion Knowledge` | 已评估可见源与复用边界并融入 01/02/03；收藏原片多未能访问，不能标记为已观看的案例 |
| **P14 ✓** | 自有案例 Hairline、Marathon、Xtacking、PHOTON、5G-A、DIY PC 与 X-Ray 候选 | 已核对可读工程/复盘/报告并将预设状态、实验晋升、验收分级压入 03/04；X-Ray 独立源码未定位，真实目标设备仍待用户实测 |
| **P15 → 跳过** | 外部镜头配方库 [video-shotcraft](https://github.com/Vincentwei1021/video-shotcraft) / [video-talkcraft](https://github.com/Vincentwei1021/video-talkcraft) | **2026-10-10 用户明确要求跳过**；不继续本阶段、不计为研究完成 |
| **P16 → 跳过** | [vibemotion-lab](https://github.com/kzz-x/vibemotion-lab) 的 Benchmark、Styleboard 和失败复盘 | **2026-10-10 用户明确要求跳过**；不继续本阶段、不计为研究完成 |
| **P17 ✓** | [chadian-video-agent](https://github.com/kzz-x/chadian-video-agent)：依赖/并行、结果恢复、审核与版本证据 | 已按实际代码、状态报告和测试范围去重，仅向 01/03/04 加极少量规则，不迁 Python 调度器 |
| **P18 ✓** | [XPIN-Blender-Skill](https://github.com/kzz-x/XPIN-Blender-Skill)、Library AE 专项与 WorkBuddy 旧资料 | 核对真实原文与重复率；仅往 03 加稳定 AE 目标定位、Blender 控件数据持久化两项，未复用旧 SOP |
| **P19 □** | 最终压缩与缺口审查 | 清理四个阶段内重复/冲突；只在 PROGRESS 留来源历史；列明用户实测项，停止无限扩充 |

**P11 首批（已完成）：** GitHub 树显示 Xpin 296 个文件，`【差点风格】/参考图` 有 109 张 JPG + 1 个 `.nomedia`，另有 16 张文字风格卡。已读取约 25 份具代表性的资产路由、Motion、摄影机、模板、技术/视觉规范及旧测试与来源审计文本；多数与 v1.5.4 重合。**仅将两条真实增量写入 `03-production.md`：按最早发生的问题层级修订；HTML 外部依赖固定版本并备离线方案。** 此段为第一批历史记录；后续 P11 追加检查见下。旧仓测试协议不是本轮实测。

**P11 第二批（本轮完成）：** 读取 Xpin `【差点风格】/风格卡` 000–015 全 16 张、`【差点动效-skill】/02-style-system` 的简式卡/索引/组合规范，并遍查 00–01、03–11 各类 Motion、视觉、技术配方、资产规则、模板、提示词、检查表、实例与历史测试复盘（多为重复的旧版设计，未抄用）。GitHub 树 `【差点风格】/参考图` 共 **109 张 JPG：16 张预览拼图/预览图 + 93 张原始单图**；已**真正打开 16 张预览**（覆盖各组视觉缩略图）以及**16 张不同风格的原始 JPG 高清图**。尚未逐张高清展开另外 77 张，按需可续查；不要将「拼图查看」写成「全图高清验收」。库内未发现 MP4/MOV/WebM/AE/Blender/GLB 成片/工程文件；卡片内 `I###`、`V###F#`、旧原文件名只表明内部引用，不能替代原片核验、授权或真实制作证据。部分视觉样本为封面/海报/播放器截帧/AI 概念图，而非可验证动态源。

**真正补入：** `02-direction.md` 增加按素材类型区分动态/静态/海报/AI/拼贴，缺原片不虚构运动；`03-production.md` 增加 HTML 编辑视图与纯画面录制的目标画幅核对，防止控制面板挤压/遮挡舞台或默认落在非预期空白帧。这两项来自真实源图与历史测试记录，并非本轮软件实测。

**刻意不搬：** 默认强制风格 000、固定 30fps/6–8s、运动百分比模板、16 张风格卡全文、无来源或不可商用的原图、原始大 JSON/编辑器参数/固定文件树、大型检查表/长 Prompt、旧 Agent 测试目录与用户本机路径。源图库主要作为维护时的视觉判断依据；生产依然自包含。**P11 已按「代表性图像 + 全类文本 + 差异整合」的计划范围结项**，不代表 77 张其余原图逐张高清核验，也不代表真实动态复刻/渲染验证。

**P12 GPT 深挖（本轮完成）：** 当前 GitHub 树显示 437 个文件，核对 4 类 `knowledge/{ai-post-production,editing,vibe-motion,visual-template}` 的全部 16 份核心知识卡/决策/失败/来源索引，另复核动效参考站点、仓库级能力/迁移索引、旧动效 WORKFLOW/EXPERIENCE/EVALS/EXAMPLES/TEMPLATES/源对照，及 `【差点动效-Pro】` AGENTS、两份主说明、工程数据协议、Keyframe/Project IO、6 个模板 manifest、HTML/Remotion/HyperFrames 适配器实现与说明，读取 6 份早期 `CD_001–006` 风格卡。旧仓约 437 个文件不是「437 份已全文读完」；旧 archive、全部生成导出/源码模块与所有风格说明未逐个全文验收。

**去重事实：** 通过两个 GitHub 仓的文件树 SHA 核验，GPT `【差点后期】/【差点风格】/参考图` 109 张 JPG **109/109 与 P11 Xpin 对应参考图字节相同**；不重复挖图。GPT 六套 `CD_001–006` 风格卡参考图片目录为空（`.gitkeep`），多为旧的风格描述与 Prompt，不是另一套经过作品核验的视觉案例；其余早期 SOP 与 P8/P11 重复为主。

**真正增量：** `02-direction.md` 在复杂 AI 连续片段用少量入口/主构图/运动变化/出口帧组织短段，不赌一次长生成；`04-finish.md` 把 A-roll/口播清理作为全片剪辑时间线骨架、实拍/录屏/CGI 再分层插入，同时保留读图时长；录设备/软件先清屏并关通知、核文字可读性，交付视频先本地真实检查再上传共享盘/NAS。均为旧 `knowledge/editing`、`ai-post-production` 的实际经验增量，非本轮软件实测。

**Pro 真实范围：** 仓内存在 React/TypeScript 工程、图层/控件/逐帧 JSON/关键帧逻辑和基础导出脚本；`src/exporters/remotion/README.md` 明说主要支持 solid/shape/text 与基础数字曲线，`src/exporters/hyperframes/README.md` 说明 GSAP 时间线仍为占位；脚本预设入口读取示例工程，不能宣称任意 Three/粒子/外来 HTML 可无损互导、透明视频输出已经通过。它是工具原型/研发参考，不把大型编辑器协议或全部控件设为 XPIN-VIDEO 生产强制项。

**没有移植：** 旧强制每镜 4 图或三段生成、固定 fps/样片时长、按阶段堆 v001–v005 文件、每镜三套方案、繁琐质检评分、所有图层控件化、旧 Agent 目录/路径及早期 README 迁移约定。旧资料多为说明与部分代码，**没有本轮 Windows/真实 PR/AE/浏览器/视频导出验证**。P12 以覆盖预定高价值来源和去重结项，非整个 GPT 仓库逐文件全文审查。

**P13 Drive / Library（本轮完成）：** 实际获取并检查 Google Drive `favorites_2026_9_6.html`（约 1.07 MB 的浏览器书签 HTML；解析到 1,267 条书签链接）、`【差点动效-融合卡】.md`、`01_差点创意_系统提示词_完整整理版.md`、`差点创意系统提示词.txt`、`02_差点构图_Agent_系统提示词_整理版.md`、`03_差点视觉总监_Agent_系统提示词_完整整理版.md`、`差点视觉智能体指令原文与全资料归档包.md`；另外通过 Library 阅读 `/Kai Motion Knowledge/motion_workflow_knowledge.md` 全文 76 行。已与 01–04 四个阶段去重，而非将旧 Agent 指令迁入生产规则。

**收藏可用性：** 书签涉及大量 Bilibili 视频页（231 条）、GitHub 链接（79 条）、新片场/站酷成片与工具资源，但多数并非作者原始工程，且不少为早期教程。已从其中挑选公开案例 URL 与仓库候选；新片场/站酷部分作品在本轮尝试访问失败，不能说已观看/核验片段或授权。仅抽查公开 `propjockey/augmented-ui` 的实际 CSS 源码/README 和 BSD-2-Clause 许可证，可确认为可研究的 UI 几何切角实现，**不能算完整动态镜头样片**。书签 HTML 包含可能带会话参数的链接，因此**不上传、复制完整收藏 HTML，也不在进度/Skill 中写入带 token/query 的 URL**；外部链接仍要追作者、原片、分镜动作、实际可用源码与授权，未达标的只算候选。

**创意与视觉总监沉淀：** 「从事实关系/情绪/反差而不是词汇堆砌出发；S/A 找一处观众能记住的视觉变化」「现有认可母版优先、先判断已经成立的视觉部分」「成功/失败案例经明确认可才升级长期标准」与本 Skill 的 Artist Direction First/最小 Patch 基本一致，未复制尺度反转、时间冻结等 10 种名词手法及整套长提示词。归档包披露当时未发现可读的视觉成功/失败/模板记忆卡，因此不能用设计中的文件名宣称已有成熟灵感案例库。

**Motion 与工程增量：** `【差点动效-融合卡】` 强调合成多段 HTML 动效时先隔离 CSS/全局状态、保留主效果视觉，接入共同时间源；Library Motion 工作流强调**最终宿主与人工需要保留的编辑能力决定交付**：原生工程/参数包装/语义重建/部分烘焙/全部烘焙，不追求格式 100% 无损互转。此前 P12 已有少量跨格式导出适配器但不等于真正多宿主互通。

**本轮实际写入：** `01-storyboard.md`：S/A 的认知反差与记忆点；`02-direction.md`：收藏/拼贴必须回查原作及真实动态；`03-production.md`：混合 HTML 效果隔离和单一时间源，以及跨软件按最后编辑需求选原工程/参数化/部分烘焙。总改动局部、保持主 SKILL 极短，未复制收藏或旧 Agent 全文；没有在 AE/PR/Blender/Resolve/浏览器运行实测。

**P13 完成边界：** 可见源资料已核对、真正增量已整合；外部原始成片链接的逐条打开、镜头/源码配对、授权确认并未完成，留作未来独立差点灵感真实样片建卡（及 P15 外部镜头配方库）任务，**不将候选网页登记为“已验证灵感卡”**。

**P14 自有工程与复盘（本轮完成）：** 通过 Library 读取原始 `Xtacking三维动效制作复盘与避坑指南.docx`（6 页）、`屏幕互动模板开发复盘与避坑指南.docx`（PHOTON，8 页）、`AI动效开发核心经验.md`（75 行）；并核对 `5GA-production-report.md`、DIY PC `REPORT.md`（分别 71、68 行）及 2026-10-03/04/07/09 Daily Review 的相关候选/证据边界。实际从 Library 读取了 `Xtacking-Studio.html`、`photon-display-template.html`、`hairline-model-template-recording(1).html`、`差点-Marathon-Renderer.html` 的开头源码及文件元信息，能确认工程文本存在、架构和部分实现特征，**不等于执行/跑通这些 HTML、逐行审阅全部源码、或完成 GPU/成片质量测试**。另确认可见有多个 Marathon 独立模式版本、Hairline 预览/源码包、Xtacking 录屏/源码包；未逐个解包或观看所有视频。X-Ray 独立原始工程未在本轮可读 Library 根目录与标题检索中定位，相关视觉理念已在 PHOTON/Hairline/其他模板出现，不能假装已读 X-Ray 源码。

**交叉验证的失败→修法：** Xtacking 在预设切换后出现跳镜/晶圆模式污染下一预设、翻转穿模与标签独立计时；PHOTON 出现平板几何/泛光掩盖材质、微观映射断裂、屏幕内容与像素不同步。此前主 Skill 已写结构优先、路径优先、同一时间状态、标注同步和少量控件，不重复追加。Marathon 多模式原型与统一版的并存说明风格实验适合先独立验证，再把成熟效果接入共享 Camera/Timeline/Recording，避免主工程积累未通过的实验；仅作合理工程决策，不宣称其所有模式已验收。

**真实证据边界：** Xtacking 文档报告过 7 个预设、3,065 个时间采样点和 1,021 个标注排布检查，且明确仅一次 480×270/24fps/1s 的逐帧录制核验，不代表 1080p/4K 目标机器性能。PHOTON 文档报告几何/Shader 构建及 640×360/24fps/3s Blob 链路，但测试环境 GPU 禁用、预览约 1fps、下载事件未确认，故不能把 Blob 当用户机器可用成片。5G-A/DIY PC 的制作报告声称完整编码、抽帧/测量和可复现证据，**本轮未独立运行其脚本、检查 MP4 解码或主观画面；保留“报告声称”与“本轮亲核”的区别**。5G-A/DIY PC 自评审美仍有明显短板：技术达标不代表 Hero/角色表演/材质达到了目标；不把临时色值、帧数和单次动画手法提升为 Core。

**本轮仅吸收的两组通用增量：** `03-production.md` 补“复杂模式先代表镜头独立验证→晋升共享底座”、以及“每个预设的初始状态与覆盖顺序必须明确、导航从当下可见状态接入，Seek/暂停不遗留旧预设状态”；`04-finish.md` 补“构建/交互/GPU 实际画面/下载解码/目标机性能分别记证据，不能用编译或 Blob 冒充成片”。其他成果已经被 01–04 覆盖，故没有重复存入技术规范、很长的 QA 表或专项数值。**本轮不代替用户做软件实测。**

**P17 chadian-video-agent（本轮完成；用户明确跳过 P15/P16）：** 读取该仓当前 GitHub 源码树及 `README.md`、`STATUS.md`、`TEST_REPORT.md`、`ARCHITECTURE.md`、`docs/TASK_ENGINE.md`、`docs/PRODUCTION_LOOP.md`、`docs/PROJECT_OPERATIONS.md`、`docs/CAPABILITY_REGISTRY.md`、`docs/PHASE_1_TEST_REPORT.md`、`docs/PHASE_2_TEST_REPORT.md` 等；重点复核 `core/orchestrator/engine.py`、`plans.py`、`queue/model.py`、`state/{project,shots}.py`、`production/{workflow,media}.py`、`router/{route,health}.py` 与状态机。实际代码可核：任务依赖 DAG（独立分支可并行，失败阻塞依赖支线）；独立尝试目录与 token、输入/输出 SHA/大小及收据；已完成不重做，中断后优先回收完整收据，拒绝迟到旧结果；镜头只有 Preview 不等于 PASS/FINAL，审核绑定当前产物指纹和抽帧证据，拒绝错版；返工产生新任务版本，不覆盖旧版、下游依赖已引用时阻止静默替换。此处核查是**源码和既有测试报告阅读，未在本轮执行单元/真实视频测试**。

**已核测试边界：** 仓库 `STATUS.md` 标为 v0.4.0-dev.2，PHASE 3 **仍未完成**。仓库报告声称 Linux/Python 3.12 有 PHASE 1 的 20-task 中断/恢复验收、PHASE 2 的路由测试，PHASE 3 的 69 项自动测试和 4 秒、1280×720、24fps 的无声图片镜头返工样片，且有少量 FOUND_FOOTAGE 真实素材进展；但 Remotion 真正渲染仍受环境/权限阻塞、三类镜头全链路尚未通过，Windows/macOS、生产级声音/付费模型/实际用户终审未验证。仓内 `README`、`TEST_REPORT`、`PRODUCTION_LOOP` 对 Remotion 依赖安装状态记载较旧，与 `STATUS` 版本不同，应以具日期/证据的最新状态和实际运行结果为准，不以安装或代码存在认定生产可用。**不把 chadian-video-agent 自动接入或宣称 XPIN-VIDEO 已实现多 Agent 调度器**。

**仅吸收三个生产通用点：** ① `01-storyboard.md` 对上游共用素材/动作/全局约束变更沿依赖关系复查，不盲目全片重做；② `03-production.md` 对失败、中断、超时先核可用旧产物/版本，完整则接续，必要返工保留新旧版本和原因，禁止迟到旧结果覆盖；③ `04-finish.md` 审核绑定当前文件/镜头版本，返工必须重审，旧版 PASS 不可套用。原仓的锁文件/重试次数/Schema、项目目录树/能力注册/成本估算及 CLI 属工具实现细节，不移植。依旧坚持「主 Agent 一份全局 Brief，镜头子任务轻量执行，最后由真实成果与用户审核收口」，不向用户要求命令行操作。

**P18 Blender / AE / WorkBuddy 差异核验（本轮完成）：** 全文读取 `XPIN-Blender-Skill` 所有 **10** 份 Markdown（Mini/Full、Motion Rig、Engineering Gate、控件、模板、场景架构、Visual Anchor、AGENTS/README），对照目前 03 阶段：Parent/Empty、F-Curve、Driver、Delta Transform、N Panel、少量主 Key、复杂运镜保留人工精修及资产/Visual Anchor First **均已覆盖**。Library 阅读 `/after-effects-engineering/references/quick-checklist.md`（59 行）、`/差点AE/references/00_core-invariants.md`（46 行），检查 AE v1.4 工程规范开头的 MCP/JSX/Hybrid、目标定位与资产规则，并盘点差点 AE 相关分组；**AE v1.4 共 2159 行，没有本轮逐行全部重读**，此前 P6/P9 已有专项整合，不能虚称全文新审。

旧 `workbuddy` 仓 135 个文件，43 份 Markdown；与 `GPT`、`Xpin` 两仓 Git blob SHA 对比各有 **92** 个文件一致（主要是同一批 JPG），非 135 份都必须重读。针对性读取 WorkBuddy 入口与动效、素材、封面、片段、元素、风格 SOP 及旧 `workbuddy-memory` 的部分路由、分镜与动效提示词。旧强制多轮审批、固定配色/时长、每段必须动效、指定老模型、无视版权/许可、默认 Downloads 文件树、长提示词等与当前目标冲突或已过时，全部**不导入**。

**唯一增量写入 `03-production.md`：** AE 实际工程目标使用 AI_ID＋合成名＋图层名/类型多重确认，不靠易变图层序号；Blender N Panel 只是控件入口，核心参数随 .blend 的 Custom Properties/Driver 等原生数据保存，不依赖仅存于脚本的临时状态。其它与已有四阶段重合的知识不重复搬运；没有 AE/Blender 实机修改、重新渲染或用户使用验收。P18 按「差异核验」范围结项，而非旧仓所有文件逐一全文阅读。

**历史未解：** P10b Library `/差点后期V3`、`/差点后期V4` 原始文件尚不可读，留待实际取得；不凭空补。独立「差点灵感」Agent/卡库的建设不作为 XPIN-VIDEO 文档整合已完成项。

## 下轮新对话可直接复制

「继续 `kzz-x/XPIN-VIDEO` 的 **P19 最终压缩与缺口审查**。先读 `PROGRESS.md`，确认 P15/P16 依用户要求跳过、P17/P18 已结项。审查主 `SKILL.md` 与 01–04 阶段的重复、冲突、字数/认知负担；优先删改、合并而非继续加条目。列明真正未验证的用户软件实测项与资料缺口，完成后提交并读回核验，更新进度。**不要恢复跳过的 P15/P16，不新建文件/外挂仓库，不擅自运行 AE/Blender/PR 实测。**」

维护原则：判断经验是否跨任务成立、是否比已有句子更好、是否明显减少返工。**符合才写；否则留作来源或案例。**
