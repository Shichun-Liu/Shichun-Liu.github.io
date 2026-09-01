# Cloudflare Web Analytics 全站接入设计

## 目标

在网站所有页面启用 Cloudflare Web Analytics，并使用站点 token `eaa0d5fe98d94ecb895702e614f49a68` 上报访问数据。

## 方案

将 Cloudflare 官方的模块化 beacon `<script>` 标签添加到 `_includes/analytics.html`。该 include 由 `_includes/scripts.html` 引用，而 `_layouts/default.html` 会在 `</body>` 前加载 `scripts.html`，因此脚本会位于所有使用默认布局的页面 `<body>` 末尾。

Cloudflare 脚本放在现有 Google Analytics 条件块之外，使其不依赖尚未配置的 `google_analytics_id`，也不受页面级 `analytics: false` 设置影响。站点不新增配置项、依赖或自定义 JavaScript。

脚本使用 Cloudflare 当前文档中的手动接入格式：`type="module"`、`https://static.cloudflareinsights.com/beacon.min.js`，以及包含站点 token 的 `data-cf-beacon` 属性。

## 数据流与故障行为

浏览器渲染页面后从 Cloudflare 域名异步加载模块脚本，并由 beacon 向 Cloudflare 上报 Web Analytics 数据。脚本加载或网络请求失败不会阻止页面主体渲染；本站无需增加错误处理逻辑。

## 验证

运行 Jekyll 构建并检查生成的首页和博客页面，确认：

- 每个页面只包含一个 Cloudflare beacon；
- beacon 位于 `<body>` 内并出现在 `</body>` 之前；
- 脚本地址、`type="module"` 和 token 均正确；
- 现有 Google Analytics 条件逻辑保持不变。
