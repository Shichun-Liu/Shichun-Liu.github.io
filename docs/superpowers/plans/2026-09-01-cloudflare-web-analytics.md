# Cloudflare Web Analytics 全站接入实施计划

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 在网站所有正常页面的 `<body>` 末尾加载一次 Cloudflare Web Analytics beacon。

**Architecture:** 在现有 `_includes/analytics.html` 中集中管理 Cloudflare beacon。`_includes/scripts.html` 已被 `_layouts/default.html` 在 `</body>` 前引用，因此不需要修改布局或各页面正文；Cloudflare 标签放在 Google Analytics 条件块之外，确保独立启用。

**Tech Stack:** Jekyll、Liquid、HTML、Bundler、Cloudflare Web Analytics

## Global Constraints

- 使用站点 token `eaa0d5fe98d94ecb895702e614f49a68`。
- 使用 `type="module"` 和 `https://static.cloudflareinsights.com/beacon.min.js`。
- Cloudflare beacon 必须位于 `<body>` 内、`</body>` 之前。
- 每个正常页面只加载一次 Cloudflare beacon。
- 不新增依赖、配置项或自定义 JavaScript。
- 保持现有 Google Analytics 条件逻辑不变。

---

### Task 1: 添加并验证 Cloudflare Web Analytics beacon

**Files:**
- Modify: `_includes/analytics.html`
- Test: `_site/index.html`、`_site/blog/index.html`

**Interfaces:**
- Consumes: `_includes/scripts.html` 对 `analytics.html` 的现有引用，以及 `_layouts/default.html` 在 `</body>` 前对 `scripts.html` 的现有引用
- Produces: 每个使用站点布局的页面中唯一的 Cloudflare Web Analytics `<script>` 标签

- [x] **Step 1: 构建未修改的网站**

```bash
bundle exec jekyll build
```

Expected: 命令退出状态为 0，并生成尚未包含 Cloudflare beacon 的 `_site/index.html` 和 `_site/blog/index.html`。

- [x] **Step 2: 运行修改前行为断言并确认失败**

```bash
ruby -e 'files = %w[_site/index.html _site/blog/index.html]; marker = "https://static.cloudflareinsights.com/beacon.min.js"; files.each do |path| html = File.read(path); abort "#{path}: beacon 数量不正确" unless html.scan(marker).length == 1; body_start = html.index("<body"); beacon = html.index(marker); body_end = html.index("</body>"); abort "#{path}: beacon 不在 body 内" unless body_start && beacon && body_end && body_start < beacon && beacon < body_end; abort "#{path}: token 不正确" unless html.include?("eaa0d5fe98d94ecb895702e614f49a68"); end'
```

Expected: 命令以非零状态退出并输出 `_site/index.html: beacon 数量不正确`，证明测试能捕获缺失的功能。

- [x] **Step 3: 添加最小实现**

在 `_includes/analytics.html` 现有 `{% endif %}` 之后添加：

```html

<!-- Cloudflare Web Analytics -->
<script type="module" src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"token": "eaa0d5fe98d94ecb895702e614f49a68"}'></script>
<!-- End Cloudflare Web Analytics -->
```

不要修改现有 Google Analytics 条件块。

- [x] **Step 4: 构建网站**

```bash
bundle exec jekyll build
```

Expected: 命令退出状态为 0，并生成 `_site/index.html` 和 `_site/blog/index.html`。

- [x] **Step 5: 验证首页和博客页的生成结果**

```bash
ruby -e 'files = %w[_site/index.html _site/blog/index.html]; marker = "https://static.cloudflareinsights.com/beacon.min.js"; files.each do |path| html = File.read(path); abort "#{path}: beacon 数量不正确" unless html.scan(marker).length == 1; body_start = html.index("<body"); beacon = html.index(marker); body_end = html.index("</body>"); abort "#{path}: beacon 不在 body 内" unless body_start && beacon && body_end && body_start < beacon && beacon < body_end; abort "#{path}: token 不正确" unless html.include?("eaa0d5fe98d94ecb895702e614f49a68"); abort "#{path}: 缺少 module 类型" unless html.match?(%r{<script type="module" src="https://static\.cloudflareinsights\.com/beacon\.min\.js"}); end'
```

Expected: 命令退出状态为 0，无输出。

- [x] **Step 6: 检查差异并提交实现**

```bash
git diff --check
git diff -- _includes/analytics.html
git add _includes/analytics.html
git add -f docs/superpowers/plans/2026-09-01-cloudflare-web-analytics.md
git commit -m "feat: add Cloudflare Web Analytics"
```
