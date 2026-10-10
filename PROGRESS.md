# XPIN-VIDEO · 整合进度 / 跨对话续接

更新：2026-10-10 · **v1.2 深挖整合版** · 当前只做知识提纯，**实测由用户自己负责**。

## 约定（后续必须延续）

1. **自包含**：生产只读取本仓 `AGENTS.md → SKILL.md → 当前 stage`，不得运行时跳旧 Skill 仓库；旧仓和 Library 仅是维护期间的来源。
2. **少而精**：经验优先合并或替换原句；不复制旧规范全文、不添加多套子 Skill、风格大全和故障档案。
3. **只整合，不擅自实测**：不再自己启动 Codex/AE/Blender/HTML 制作或验收。用户提供实测反馈时，再核对失败根因并修改相应 1–2 条规范。
4. **不猜结果**：实际检索、实际阅读、软件运行测试分开说明。Library 的 Daily Review 是候选意见，不等于通过实测或用户批准。

## 阶段状态

- [x] P0–P4：首轮仓库/Library 盘点、核心 4 阶段与 `AGENTS.md` 建立、渐进读取静态检查。
- [x] P5a（历史）：曾制作和测试 Web RAM 小样，记录见下；**不继续自动实测**。
- [↗ 用户负责] P5b：Windows Codex + AE/Blender 的真实工程、控件、Marker、画质与安全回归；**不作为 AI 下一步任务**。
- [x] **P6 深度整合（本轮）**：重点深挖 Library 新版分镜、动画升级 v5、Daily Review、旧后期/AE/Blender/视频 Agent 的高价值源文件；仅改原有阶段内容，未新增 stage/Skill。
- [ ] **P7 后续持续整合**：按主题进一步精选还未逐篇审查的具体视觉/风格案例、模板资产索引与剪辑/音效经验；有可迁移的新原则才入仓，避免重复。仍然**不实测**。

## P6 本轮实际深入的来源与吸收

**Library**
- 《差点分镜 Agent｜核心提示词》与 10/06 Daily Review：信息单元优先、连续镜头、实际制作路线按质量/工期/修改/复用选择、可复用资产标记、全局 Brief + 单镜任务隔离。
- 《差点动画升级-Skill-v5》：Previs 负责叙事/动作意图，Target 负责视觉质量；有源工程读取真实实现；选可观察的 Signature Features；别只修 Bug 而忽略艺术性。
- 《差点动画.docx》及 10/04 Daily Review：路径与速度曲线分开、少量有效关键帧、动态录制后平滑/降噪再精简、编辑与渲染解耦。
- 《屏幕互动模板》《Xtacking》复盘及旧版升级指南：连续空间、共享时间、参考级画面与真实文件验收。已存在的规则仅核对，**没有重复追加**。
- Library《差点后期_Universal_SKILL.md》：保持授权范围、标注优先、来源真实性、用户已有锁定项不漂移。

**旧 GitHub 仓库（只在本次维护中读取）**
- `chadian-post-GTP-project`：参考/搜索/资产、风格索引、画面诊断、并行协议、现成资源目录。
- `XPIN-AE-SKILL`：Motion Principles、Animation QA、Speech-Driven Motion、Controls、Modify Existing、Previs First、模板母版隔离。
- `XPIN-Blender-Skill`：原生关系/控件、F-Curve、人可独立修改。
- `chadian-video-agent`：共享任务上下文、独立任务状态/依赖、失败只影响分支；具体未验证 Worker 功能不移植。

**已更新的生产规则**
- `01-storyboard.md`：连续信息段落、路由四维度、可复用标记、镜头任务隔离。
- `02-direction.md`：从参考提取少数具体可执行视觉特征；实际资产/开源库的轻量入口，不写死技术栈。
- `03-production.md`：Previs/Target 分工、编辑与渲染可分离；源工程读取与异地备份；模板母版只读；Marker 优先于 ASR，仅读当前使用音频；Path/Speed 分离与非破坏动画。
- `04-finish.md`：模板感也是视觉失败；码率不能代替正确采样、抗锯齿和实际画面验收。
- `AGENTS.md` / `README.md`：维护者只整合、实测归用户。主 `SKILL.md` 保持不增长。

**审过但不搬入**
- 000–017 风格全集、每种特效细节、Style Pack 多层目录、故障 Adapter、MCP 指令、具体 AEP/Blender 数值与重复 QA 表；
- 尚未验证的多 Agent 节省 Token、全平台统一 Animation IR 等宏大架构；
- 强制所有镜头四宫格、所有镜头做 Hero、无条件复杂运镜、强制全量控件、按 HTML 大小机械拆分等反模式。

## 历史 P5a 记录（不代表本轮执行）

原有 [RAM HTML 小样](tests/p5-ram-pilot.html) 曾在本地验证时间线 seek、部分实时控件、4 个 Marker 数据、640×360 / 12fps / 5 秒 / 60 帧低清输出与 HTML 异地备份模拟。**未验证**：Marker 拖动、准确口播、商用级视觉、Windows 上 AE/Blender/Codex。相关产物曾保存到 Library `/XPIN-VIDEO/P5/`。该记录只用于解释历史，不触发自动测试。

## 下一轮如何继续

「继续整合 `kzz-x/XPIN-VIDEO`：先读 `PROGRESS.md` 和 `AGENTS.md`，从 P7 的**资料提纯**继续。只读相关 Library 和旧仓库文件找可复用的核心规则，优先压缩修改现有 4 个 stage，不增加外挂旧 Skill 依赖。不要制作样片或实测——这些由我自己来。每轮更新 PROGRESS.md 并提交。」

**注意：** 本轮只对重点文件做了针对性深读，不能声称遍历了所有 Library 文件与所有旧仓子目录；源文件已保留，后续按真实场景持续补充而非盲扫。
