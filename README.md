## HI THERE! 

D.R.E.A.M. Track 的同学们你们好
欢迎去 [isaacbao.cn](https://isaacbao.cn) 看看～

---

## 项目说明

单文件 H5 纪念页，文艺暖调，Chagee 品鉴者主题。无依赖、无构建，改完 `index.html` 刷新即可。

线上部署在 Vercel，绑定域名 isaacbao.cn。

### 本地预览

双击 `index.html` 用浏览器打开；或者：

```
python3 -m http.server 8000
```

然后访问 http://localhost:8000

### 部署备忘

Vercel 连接本仓库即可，无需构建配置。一个坑：根路径必须有 `index.html`，否则访问 `/` 直接 404（2026-09-01 踩过，当时文件名叫 isaac_mdl_h5.html）。

### 页面结构

| 区块 | 说明 |
|------|------|
| 首屏 | 名字、@MDL、一句介绍；点茶杯有彩蛋 |
| 品鉴手记 | 三杯茶的记录卡片，文案和评分可直接改 |
| 联系我 | 邮箱、复制按钮、@MDL |

文案、茶单、联系方式都在 `index.html` 里改；配色在 `:root` 的 CSS 变量里，改一处全页生效。
