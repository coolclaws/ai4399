# AI4399 · AI 小游戏厅

一个由 AI（Claude）编写的纯静态小游戏合集，打开就能玩。

**在线游玩：** https://4399.myhubs.dev （备用：https://ai4399.pages.dev）

## 游戏列表

| 游戏 | 类型 | 入口 |
|------|------|------|
| 深渊五层 Depths of Five | 回合制 Roguelike | [`/roguelike/`](roguelike/) |
| 血色深渊 Crimson Abyss | 第一人称射击 | [`/fps/`](fps/) |
| 疾风卡丁 GP | 3D 卡丁车竞速 | [`/kart/`](kart/) |
| 2048 | 数字合成益智 | [`/2048/`](2048/) |
| 霓虹贪吃蛇 | 经典街机 | [`/snake/`](snake/) |
| 方块消行 | 落块消行益智 | [`/blocks/`](blocks/) |
| 扫雷 | 推理益智 | [`/mines/`](mines/) |
| 笨鸟先飞 | 一键休闲 | [`/flappy/`](flappy/) |
| 大球吃小球 | 休闲街机 | [`/balls/`](balls/) |
| 都市狂奔 | 三车道跑酷 | [`/runner/`](runner/) |
| 荡绳侠 | 物理摆荡街机 | [`/swing/`](swing/) |
| 包子铺大亨 | 放置经营 | [`/baozi/`](baozi/) |
| 成语方阵 | 成语版 Wordle | [`/idiom/`](idiom/) |

## 添加新游戏

1. 在仓库根目录新建一个游戏文件夹，入口必须是 `index.html`（依赖一并放入该文件夹，保持自包含）
2. 在根目录 [`index.html`](index.html) 的 `GAMES` 数组里加一条记录（目录名、标题、简介、标签）
3. 提交并推送，Cloudflare Pages 会自动重新部署

## 部署（Cloudflare Pages）

纯静态站点，无构建步骤。push 到 `main` 后由 [GitHub Actions](.github/workflows/deploy.yml) 自动执行 `wrangler pages deploy` 部署到 Cloudflare Pages（凭据存于仓库 Secrets：`CLOUDFLARE_API_TOKEN` / `CLOUDFLARE_ACCOUNT_ID`）。
