# AGENTS.md — DreamTrackTest（Isaac 个人主页）

## 这是什么项目

Isaac 的个人 H5 纪念页。面向 D.R.E.A.M. Track 的同学，主题「Chagee 品鉴者」，文艺暖调（米纸底、暖棕字、抹茶绿点缀）。

- 单文件 `index.html`：全部页面，无依赖、无构建，改完直接刷新
- GitHub：git@github.com:Ganzhe2028/dreamTrackTest.git（分支 main）
- 部署：Vercel，绑定域名 isaacbao.cn
- 本地预览：双击 index.html，或 `python3 -m http.server 8000`

## 红线

- 根路径必须保留 `index.html`。Vercel 静态部署访问 `/` 只认 index.html，改名会 404（2026-09-01 踩过）
- README 顶部那段「HI THERE! …」问候语是 Isaac 在 GitHub 网页上自己写的，不要动
- Isaac 会直接在 GitHub 网页上编辑仓库（index.html 已改过多轮）。本地版本随时过期，任何改动前先 `git pull`，2026-09-01 因没 pull 被拒过一次

## 改动时要知道

- 文案、茶单、联系方式都在 index.html 里，搜文字定位；配色在 `:root` 的 CSS 变量，改一处全页生效
- 首屏那句「茶需慢慢摇，心急则味散」、七杯茶的记录和评分词（人上人 / NPC+ 体系）是 Isaac 2026-09-01 自己在 GitHub 上改的，保持原样，别当占位改写；联系卡片的 @MDL 行和页脚被注释掉了，他有意的，别恢复
- 交互点：茶杯点击冒小字、复制邮箱按钮、滚动入场 reveal；prefers-reduced-motion 已处理

## 验证流水线（已跑通）

1. 提取 `<script>` → `node --check`
2. Playwright 用系统 Chrome：executablePath 指到 `/Applications/Chrome.app/Contents/MacOS/Google Chrome`（channel 默认找 /Applications/Google Chrome.app，路径差一个单词）
3. 截图三段（首屏 / 品鉴手记 / 联系我）人工看渲染；断言 `scrollWidth == innerWidth`、无 pageerror

## 时间线

- 2026-09-01：建页面 → git init 推送 → 文件改名 index.html 修复 Vercel 404 → README 合并（保留用户问候语）→ 建本文件
