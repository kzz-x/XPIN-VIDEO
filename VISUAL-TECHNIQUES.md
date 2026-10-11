# 视觉技巧库 · Visual Technique Library

> 用途：把“我想要某种画面变化”的自然语言，反查为 **可迁移的运动机制 → 可靠参考 → 复刻途径**。这是技法检索库，不是默认风格，也不意味着全部技巧必须叠加。版本：2026-10-11 / 首批 12 卡。
>
> 查询只需扫下方索引；命中后才读对应卡。只把命中卡的目的、画面机制、参考、验收带入制作任务，不转发整库。
>
> **证据标记**：［原作］作者/官方项目页；［教程］公开教学/官方文档；［设计推演］合理的复刻路径，尚非原作者技术揭秘或实机验证；［用户参考］聊天中提供的截图，未知完整动态。

## 自然语言反查索引

| 你可能会说 | 命中 | 技巧/英文检索词 |
|---|---|---|
| 玻璃像布一样软，落下后贴到屏幕 | T01 | Soft Glass / Cloth-to-Glass / Conforming Membrane |
| 一个二维图标变成真实立体物件 | T02 | UI Materialization / 2D-to-3D Morph |
| 圆角卡片像柔性薄片一样翘起、折叠、翻动 | T03 | Elastic UI / Deformable Surface / Fold |
| 一层层半透明玻璃卡片在空间分离、重叠 | T04 | Layered Acrylic / Translucent UI Stacks |
| 玻璃、凝胶、金属之间像活物一样互相变化 | T05 | Material Metamorphosis / Soft Body |
| 模型表面有细密纹理，微距下质感特别真实 | T06 | Tactile CGI / Micro Surface / Roughness Detail |
| 二维画面随着运镜突然变成三维空间 | T07 | Spatial UI / 2D-3D Transition / Parallax |
| 光线扫过柔软曲面，高光和折射随形变流动 | T08 | Specular Flow / Animated Reflection / Refraction |
| 产品由线框、扫描网格逐渐显出真实实体 | T09 | Wireframe-to-Solid / Reveal Shader |
| 地板墙面底座都是屏幕，上面有动态图形 | T10 | Screen-Based Stage / Spatial Motion Graphics |
| 地面点阵和灯带随着镜头或产品节奏依次亮起 | T11 | Dot Matrix / LED Chaser / Light Sequencing |
| 新式短促数字错乱，不是老旧 RGB 雪花故障 | T12 | Temporal Glitch / Pixel Sorting / Data Corruption |

## Microsoft 系：物理材质动效 / Physical Material Motion

### T01 · 柔性玻璃膜吸附屏幕
- **视觉**：看似坚硬透明的薄玻璃先悬浮、弯曲、产生柔软褶皱，沿接触边缘逐渐贴合屏幕，最后恢复平整高光；物体运动与材质认知形成反差。
- **参考**：［教程］[UILEO Blender「布料柔软玻璃」](https://www.bilibili.com/video/BV1n34y137CW/)（页面有玻璃系列/柔软玻璃章节）；［灵感］[Microsoft Future Vision — Tendril](https://tendril.studio/work/ms-future-vision/) 的物理材质+UI融合，**不声称其原片有完全相同的贴屏镜头**。
- **复刻**：［设计推演］Blender 高细分平面＋Cloth/Pinned Vertex Group＋屏幕 Collider，末段用 Shape Key/Shrinkwrap 或贴合权重控制，Solidify/平滑后做透明折射材质、灯箱长条高光；精确可控的镜头可用关键形状混合，复杂碰撞用 Houdini Vellum。
- **可调**：弯曲刚度、初始垂度、接触前沿速度、残留褶皱、透明度与边缘高光；重点验收接触边缘连续、无穿模和折射跳变。

### T02 · 二维 UI 元素实体化
- **视觉**：图标/按钮/圆角矩形从二维图形获得厚度、倒角、真实投影和反射；由界面设计语言自然转成三维对象。
- **参考**：［原作＋R&D］[Microsoft Loop — NotReal](https://notreal.tv/project/microsoft-loop)；团队明确描述 3D 形体与平面 UI 的交互；［原作＋Visual Development］[MS Icons — Nidia Dias/Tendril](https://nidiadias.com/works/ms-icons)。
- **复刻**：［设计推演］SVG/曲线转 Mesh，Extrude/Bevel，保持二维正投影视觉起始状态，再引入厚度、透视与环境反射；末段镜头运动暴露其体积。用 AE 做平面阶段、Blender/C4D 做三维阶段，保持转场画面锚点一致。
- **可调**：厚度、倒角半径、光泽、物体浮起高度、摄影机俯仰。

### T03 · 柔性 UI 面片折叠与弹性形变
- **视觉**：圆角界面像软卡纸、丝带或薄膜一样卷边、翘起、对折、回弹，弯曲过程中图形与内容仍附着表面。
- **参考**：［原作］[Microsoft Loop — NotReal](https://notreal.tv/project/microsoft-loop)（2D/3D 混合设计的视觉语汇，具体折叠动作以实际原片为准）；［教程］[Blender Cloth Examples](https://docs.blender.org/manual/en/latest/physics/cloth/examples.html)。
- **复刻**：［设计推演］Subdivision Plane + Curve/Lattice/Shape Keys 控制单镜头形状；需要受力与碰撞才启用 Cloth。图文作为 UV/Texture 贴在变形网格上；材质可以是纸、软塑、亚克力或玻璃。
- **可调**：折线位置、卷曲半径、弹性延迟、纹理跟随和变形后的可读性。

### T04 · 透明层叠界面的物理空间化
- **视觉**：多个玻璃/磨砂半透明层以微小高度差悬浮、滑移、错层，清晰出现层间遮挡、柔软阴影、边缘高光和折射。
- **参考**：［原作］[Microsoft Future Vision — Tendril](https://tendril.studio/work/ms-future-vision/)；［设计规范］[Microsoft Fluent 2 Elevation](https://fluent2.microsoft.design/elevation/) 解释光影、景深与界面层级。
- **复刻**：［设计推演］真实薄板几何、少量可控层级深度、IOR/Transmission/Roughness、面积光源与背景反差；快速实时版本可用透明/模糊近似而不强行模拟物理折射。
- **可调**：板厚、磨砂、透明、层距、阴影软硬、Z 向展开时序。

### T05 · 反常材质与物理属性切换
- **视觉**：本来坚硬的玻璃、金属或陶瓷忽然表现出柔软、流动、弹跳、拉伸的性质，而外观仍保留高级真实材质。
- **参考**：［原作＋R&D］[Microsoft Future Vision — Tendril](https://tendril.studio/work/ms-future-vision/)（页面列有 Houdini Simulation 团队；**不是**某种特定形变的制作方法证明）；［技术文档］[Houdini Vellum](https://www.sidefx.com/docs/houdini/vellum/overview.html)。
- **复刻**：［设计推演］运动机制独立于着色；先通过 Shape Keys/Soft Body/Vellum 控制物体“怎样动”，再用同一几何切换材质呈现。风格化片段优先可控形变，不必全程真实物理模拟。
- **可调**：刚柔转换点、约束强度、回弹时间、材质切换的过渡范围。

### T06 · 触觉化真实材质与微观质感
- **视觉**：极简形体通过轻微表面纹理、粗糙度变化、细小倒角、接触阴影和柔软高光，产生可以“触摸”的材质感觉。
- **参考**：［微软官方分析］[Behind the Design: Fluent Illustration UX Video](https://microsoft.design/articles/behind-the-design-fluent-illustration-ux-video/)（强调 painterly textures、human imperfections、tactility）。
- **复刻**：［设计推演］PBR Roughness/Normal/Bump 微变化＋控制高光宽度的灯箱布光，必要时摄影机近景展示形态变化；不要让 Noise 取代真实结构与光照。
- **可调**：纹理尺度、粗糙度、Bump 幅度、边缘倒角和接触阴影。

### T07 · 从平面设计滑入三维空间
- **视觉**：前一秒是平面的构图/界面，摄影机倾斜、推进或穿过画面，图形获得透视、遮挡与真实空间深度，切换几乎看不见接缝。
- **参考**：［原作＋R&D］[Microsoft Loop — NotReal](https://notreal.tv/project/microsoft-loop)；［微软官方］[Fluent Illustration UX Video](https://microsoft.design/articles/behind-the-design-fluent-illustration-ux-video/)（提到特殊机位与从平面生长的元素）。
- **复刻**：［设计推演］先锁二维构图，再在 Blender/C4D 用正交/长焦起始机位或屏幕空间投影匹配初始画面；转为真实透视时逐步揭示几何厚度。可在 AE 合成精确衔接。
- **可调**：透视切换、焦距、摄影机轨迹、图形在空间里的真实深度。

### T08 · 材质形变中的高光流动
- **视觉**：软质透明/金属曲面弯曲时，高光像一条柔软的光带滑过表面，表现形状变化与高级材料质感，而非单纯发光描边。
- **参考**：［原作视觉］[MS Icons — Nidia Dias](https://nidiadias.com/works/ms-icons)（作者参与多个镜头的设计与布光）；［材质文档］[Blender Principled BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/principled.html)。
- **复刻**：［设计推演］把高光作为几何、法线、BRDF 与灯箱位置共同作用的结果；使用长条 Area Light、反射卡、合理微粗糙度，配合缓动镜头和表面弯曲。Eevee/Cycles 视觉表现需逐镜比对。
- **可调**：反射带位置与宽度、Roughness、摄影机偏角、表面曲率和高光峰值。

## ROG 系：空间图形与工业实验动效 / Spatial Graphic Tech

> 下列原作素材为用户提供的 ROG 画面截图，属于［用户参考］；只据静帧总结可见的画面组织，具体动画节奏与方式待原片时间码核对。

### T09 · 线框、数据网格向真实材质过渡
- **视觉**：人体、地形或产品在点、线、面与写实实体之间逐区生成、消失或混合，线框与真实材质可同时存在。
- **参考**：［用户参考］ROG 人物立于动态线框数据地形的画面。
- **复刻**：［设计推演］Blender 几何线边/曲线或 Geometry Nodes 线结构与实体双层，利用同一空间遮罩/扫描前沿控制显隐与互补；Three.js 可用 shader alpha mask 或 barycentric wireframe。
- **可调**：网格密度、线宽、过渡前沿、局部材质比例、遮挡关系。

### T10 · 整个场景变成动态图形画布
- **视觉**：地面、展台、墙面或天花板成为显示屏/LED 面板，二维图形沿三维表面铺陈；从俯拍到斜视保持精确透视。
- **参考**：［用户参考］ROG 显示器置于带箭头/结构线/排版的屏幕底座；可搭配本库 T07 的镜头空间转换。
- **复刻**：［设计推演］Blender/Three.js 真实平面＋独立 SVG/Canvas/AE 预渲染的贴图动画，UV 映射到空间；屏幕发光、材质反射、产品运动与摄影机共同调度，视频贴图须与全片时间线同步。
- **可调**：图形主题、网格、摄影机、屏幕亮度、素材切换、布局响应。

### T11 · 点阵与空间灯带的节奏激活
- **视觉**：地面点阵、LED 天花板、墙角灯带分区亮起，在暗场里用光线和密度节奏塑造摄影空间。
- **参考**：［用户参考］ROG 空间灯光和精密图形；［设计理念］可参照 [Microsoft Fluent 2 Elevation](https://fluent2.microsoft.design/elevation/) 理解层级光影。
- **复刻**：［设计推演］将 LED 阵列做成可实例化点/面，按距离场、扫描波、随机种子与节奏轨控制 Emission；Cinema/Blender 负责环境光反射，AE/Three.js 控动画节奏。
- **可调**：点阵间距、区域激活、闪烁波形、节奏落点、Bloom 与曝光。高频闪烁提供低频替代版本。

### T12 · 设计化数字故障 / 时间错位
- **视觉**：局部数据块重排、时间切片、像素排序、抽样与恢复，通常只在动作峰值短暂出现；画面仍保留明确图形构成。
- **参考**：［用户风格意向］ROG 的实验性信号语言，具体动态未核；该类别非微软 Fluent 的固有规范。
- **复刻**：［设计推演］AE 位移贴图＋像素重排/时间偏移；HTML Shader 做局部 UV 偏移与 block corruption。用固定随机种子、局部遮罩、短时触发实现可复现；未经验证的“Datamoshing”效果不要当成已复刻的真实视频压缩错误。
- **可调**：错位粒度、局部范围、时间偏移、恢复速度、持续帧数、节奏同步。

## 经核对的参考与教学入口

- 原创团队/官方： [Tendril · Microsoft Future Vision](https://tendril.studio/work/ms-future-vision/) · [NotReal · Microsoft Loop](https://notreal.tv/project/microsoft-loop) · [Nidia Dias · MS Icons](https://nidiadias.com/works/ms-icons) · [Microsoft Design · Fluent Illustration](https://microsoft.design/articles/behind-the-design-fluent-illustration-ux-video/) · [Microsoft Fluent 2 · Elevation](https://fluent2.microsoft.design/elevation/)
- 复刻学习：[UILEO · 玻璃/柔软玻璃系列](https://www.bilibili.com/video/BV1n34y137CW/) · [Blender Cloth Examples](https://docs.blender.org/manual/en/latest/physics/cloth/examples.html) · [Blender Shrinkwrap](https://docs.blender.org/manual/en/latest/modeling/modifiers/deform/shrinkwrap.html) · [Blender Principled](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/principled.html) · [Houdini Vellum](https://www.sidefx.com/docs/houdini/vellum/overview.html) · [SideFX Cloth Learning Path](https://www.sidefx.com/learn/learning-paths/cfx/cloth/)

## 调用与维护

1. **检索入口**：用中文口语先匹配视觉结果，再扩展英文动作、材质、镜头同义词。按「画面意图 + 动作机制」选 1–3 张卡，而非看见“科技”就全选。
2. **生成用法**：命中后只输出 `想表达什么｜原作及借用点｜画面发生的变化｜推荐实现载体｜可编辑关键项｜预览验收`。默认先参考 / 关键帧，之后按镜头制作。
3. **新增卡片**：有新的用户视频/图片/工程，优先提炼真实动作和术语，查重合并；可观察事实、创作推演、真正测试过的结果分开记录。优先**替换和压缩**，不无限追加列表。
4. **验证边界**：本批核验了项目/教学网页，不等于下载原工程、逐帧观看所有作品或在 Blender/AE/Codex 实机复刻。使用前核下载可得性与许可；作品公开不代表可商用或可二次发布。
