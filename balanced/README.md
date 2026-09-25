# 写实 × 幻想 PCG · F1.0

独立公网入口：https://yuzi-huang.github.io/world-pcg-questionbank/balanced/#flow

本版从 v3.5 的40题改写世界设定、304条地域画面和对应的PCG规则，保留原尺寸、seed、主路拓扑和地域节点映射。20题写实＋20题幻想；4×4 km各4题，8×8 km各12题，100×100 km各4题。写实题保留真实地理文化并加强空间差异，幻想题涵盖神话、黑暗幻想、童话生态、工业幻想与异星科幻。

每题仍为两部分：按地域生图；由图与Prompt生成连续PCG世界。支持总Prompt、PCG使用/不使用Blender两版、整组和单地域生图复制、TXT/JSON导出。当前交付是题面，没有执行生图或PCG生成，尚未验证实际出图的差异化收益。

## 构建与检查

- `base-v3.5.json`：制作本版时的原数据快照。
- `worlds-a.json` / `worlds-b.json` / `worlds-c.json`：逐世界、逐地域新题面。
- `workflow.json`：生图共同标准与检查。
- `prompt-builders.js`：两阶段和单张Prompt的拼装入口。
- `sections.html` / `style.css`：新版说明与展示。
- `build.py`：沿用父目录v3.5的页面结构与规模研究，生成本目录 `index.html`、`question-bank.json`、`app.js`，不改写父目录原版。
- `verify.py`：核验数据映射、复制与导出、筛选、两种制作路线、离线运行和移动布局；报告在 `qa/verification.json`。
- `verify_deployment.py`：核验GitHub Pages构建、公开内容以及原版页面字节未变。

运行 `python build.py` 后运行 `python verify.py`。发布仅增加 `github-pages/balanced/index.html` 和本说明；原版入口和历史题库继续可用。

原版：https://yuzi-huang.github.io/world-pcg-questionbank/?v=3.5#flow

原 image2 / text2 历史页：https://yuzi-huang.github.io/world-pcg-questionbank/legacy.html
