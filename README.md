# 差点视频｜XPIN Video

一个自包含、渐进读取的 GPT → Codex 视频后期 Skill：原文分镜 → 参考/素材/元素 → 单镜制作 → 剪辑/音效/渲染。**所有生产规则均在本仓，无需安装或运行时读取旧差点后期、AE、Blender Skill。**

## Codex 使用

打开本仓库，`AGENTS.md` 将加载 `.agents/skills/xpin-video/SKILL.md`；按当前工作阶段仅读取 4 个 stage 中的 1 个：

```text
AGENTS.md
└─ .agents/skills/xpin-video/SKILL.md     核心原则
   └─ stages/01-storyboard.md             原文、括号类型、全片节奏
   └─ stages/02-direction.md              需求、风格、参考、素材、元素
   └─ stages/03-production.md             AE / Blender / HTML / Codex 执行与工程修改
   └─ stages/04-finish.md                 音画、审片、三档渲染
```

无需先读完所有文件，也无需为了做一个简单局部修改扫描完整项目。已有授权可直接执行；现有工程先**原目录外备份、原路径原位最小修改**。

维护历史和下一步见 [PROGRESS.md](PROGRESS.md)。旧仓库仅是开发本 Skill 时已提炼的来源，不是生产依赖；后续经验优先合并/替换既有内容，避免越加越长。
