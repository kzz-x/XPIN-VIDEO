# 差点视频｜XPIN Video

面向 GPT → Codex 的**完整视频后期导演与制作 Skill**。输入原文，拆分（素材/元素/二维/三维等）镜头，搜索高质量参考与准确资产，做视觉锚点，再逐镜产出可编辑工程与高完成度视频。

**原则：最短有效路径、先参考后制作、只改该改的、先预览后精渲。**

## 使用

1. 在 Codex 中打开本仓库；根目录 [AGENTS.md](AGENTS.md) 会指向 [Skill 核心](.agents/skills/xpin-video/SKILL.md)。
2. 提供原文及括号类型（可不标，AI 自行判断）。GPT 先提供分镜、节奏与重点镜头；定方向后交 Codex 单镜制作。
3. 发起「设计 S03」「制作 S03」「只改 S03 镜头运动」「审片/输出成片」等指令，仅加载对应阶段规则。

## 渐进读取

```text
AGENTS.md
  └─ .agents/skills/xpin-video/SKILL.md     共同原则（短）
       └─ stages/01-storyboard.md           全文→分镜
       └─ stages/02-direction.md            问卷→参考/资产→关键帧
       └─ stages/03-production.md           Codex单镜制作/局部修改
       └─ stages/04-finish.md               审片/配乐剪辑/三档渲染
```

只读当前阶段，遇到实际 AE、Blender、素材、元素任务时，再按需调用原专业仓库的 Mini/单一模块，不复制其庞大实现细节。

## 维护与跨对话续接

查看 [PROGRESS.md](PROGRESS.md)：整合状态、来源、下一步、可复制的新对话恢复指令。新增经验**优先替换/压缩现有规则**，不无止境加文件、条件和提示词。

本仓是生产指导，不意味着当前助手或 Codex 已安装全部软件、模型或已连上 MCP；实际生产能力必须现场验证。
