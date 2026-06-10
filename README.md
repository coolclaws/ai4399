# AI4399 · AI 小游戏厅

一个由 AI（Claude）编写的纯静态小游戏合集，打开就能玩。

**在线游玩：** 部署于 Cloudflare Pages（见下方部署说明）

## 游戏列表

| 游戏 | 类型 | 入口 |
|------|------|------|
| 深渊五层 Depths of Five | 回合制 Roguelike | [`/roguelike/`](roguelike/) |
| 血色深渊 Crimson Abyss | 第一人称射击 | [`/fps/`](fps/) |
| 疾风卡丁 GP | 3D 卡丁车竞速 | [`/kart/`](kart/) |

## 添加新游戏

1. 在仓库根目录新建一个游戏文件夹，入口必须是 `index.html`（依赖一并放入该文件夹，保持自包含）
2. 在根目录 [`index.html`](index.html) 的 `GAMES` 数组里加一条记录（目录名、标题、简介、标签）
3. 提交并推送，Cloudflare Pages 会自动重新部署

## 部署（Cloudflare Pages）

纯静态站点，无构建步骤：

- **Framework preset:** None
- **Build command:**（留空）
- **Build output directory:** `/`

连接本仓库后，每次 push 到 `main` 自动部署。
