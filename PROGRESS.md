# XPIN-VIDEO · 整合进度 / 续接入口

更新：2026-10-10 · **v1.0 精简版已提交** · 当前状态：文档/路由检查通过；真实 AE/Blender/HTML 制作测试待做。

## 任务进度

- [x] **P0 盘点**：确认新仓库与旧版后期、AE、Blender、视频 Agent、VibeMotion Lab 来源；检索 Library 动画升级与 PHOTON/Xtacking 复盘。
- [x] **P1 提炼**：保留视觉第一、反向专业术语检索、Reference/Asset First、三轮收敛、全片规划/逐镜制作、工程安全、控件、时间轴、渲染质量。删除重复说明和大型架构。
- [x] **P2 落地**：`AGENTS.md` + `.agents/skills/xpin-video/SKILL.md` + 4 个阶段按需文件 + `README.md`。Skill 主文件仅约 1.4k 字符；不复制旧仓完整规则。
- [x] **P3 交叉核对**：逐项覆盖（三维/二维/素材）、问卷、参考视频/Banana、差点元素、短 P2 提示词、原位工程异地备份/局部保护、实时控件、音频/Marker、关键帧→低清预览、三档质量、估时/后台渲染。
- [x] **P4 路由静态检查**：已从 GitHub 回读验证全部 8 个文件及 SKILL frontmatter，路径正确；以 `（三维）准确设备结构 → 参考+3D资产 → 专用 Blender/HTML/AE`、`（二维）RAM 隐喻 → 参考+AE/HTML`、`（素材）发布会 → 官方真实视频` 模拟三条路由。**这不是实际生产运行测试。**
- [ ] **P5 真实试运行（下一步，优先）**：拿一段 3 镜头文稿，GPT 给分镜→锁关键帧/资产→Codex 制作其中 1 个 S/A 镜头→测试控件、Marker、异地备份与低清预览；记录耗时、参考匹配与修改回归。
- [ ] **P6 小幅迭代（视试运行结果）**：只修真实失败点；成熟可调用模板/元素/素材索引可放在外部专用库，主 Skill 不继续长胖。

## 新对话直接复制

「继续 `kzz-x/XPIN-VIDEO` 的差点视频 Skill 整合。先读仓库 `PROGRESS.md` 和 `AGENTS.md`；完成下一个未勾选阶段 P5，测试有证据后再只修改必要规则。不要重读全部旧仓库，也不要堆新结构。每次做完更新 PROGRESS.md 并提交。」

## 关键来源（仅维护时查阅，生产不预读）

- [差点后期](https://github.com/kzz-x/chadian-post-GTP-project)：`skill/SKILL.md`、`skill/references/{post-details,reference-first,asset-first,prompt-writing,motion-v5,project-state}.md`，素材/元素/片段独立模块。
- [差点 AE](https://github.com/kzz-x/XPIN-AE-SKILL) / [差点 Blender](https://github.com/kzz-x/XPIN-Blender-Skill)：`AGENTS.md` 的 Mini/Full 和 Read Before Write。
- [差点视频 Agent](https://github.com/kzz-x/chadian-video-agent)：`SKILL.md`，项目进度及任务恢复理念；不可把尚未验证的 Worker 能力当成已接通。
- [VibeMotion Lab](https://github.com/kzz-x/vibemotion-lab)：Hero Reference / Render / QA 方法。
- Library：《差点动画升级-Skill-v4.md》《屏幕互动模板开发复盘与避坑指南.docx》《Xtacking三维动效制作复盘与避坑指南.docx》及 AE Skill。

## 维护边界

本轮**重点研读相关主规范/关键 reference 和核心复盘**，未逐个精读所有旧风格文件、细分能力及 Library 历史档案；不将此误称“历史全部文件已完整审核”。未来只有遭遇新任务/真实失败、现有 Skill 不足时，才查相关来源；经验优先合并/替换旧段落而不是新增规则。

本仓是可被 Codex 读取的生产指导文件，并非运行程序；尚未在用户 Windows/AE/Blender/HTML 环境做完整端到端测试。下一步必须拿真实项目确认视觉效果、性能和工程保护确实成立。
