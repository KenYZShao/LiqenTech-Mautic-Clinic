# 简单的 Mautic Landing Page（用于 GitHub Pages）

这是一个最基础的 `index.html` 示例，可以直接部署到 GitHub Pages，展示并嵌入你的 Mautic 表单。

## 使用方法（简短）

1. 在 Mautic 后台创建一个表单，记下表单的 `FORM_ID`（通常是数字或嵌入代码里提供的 id）。
2. 在 Mautic 找到表单的 "分享/嵌入"（Share / Publish）选项，复制 JavaScript 嵌入或 Standalone 链接以确认 `FORM_ID` 与 `MAUTIC_BASE_URL`。
3. 编辑 `index.html`：替换 `MAUTIC_BASE_URL` 和 `FORM_ID` 为你自己的值。例如：

```html
<script src="https://mautic.example.com/form/generate.js?id=2"></script>
```

4. 本地测试：直接在浏览器打开 `index.html` 即可（注意 CORS 或 iframe 限制，推荐使用 generate.js 嵌入）。

5. 部署到 GitHub Pages：

```bash
git init
ngit add index.html README.md
ngit commit -m "Add simple Mautic landing page"
ngit branch -M main
ngit remote add origin https://github.com/<your-username>/<your-repo>.git
ngit push -u origin main
```

然后在 GitHub 仓库的 Settings -> Pages 中启用 `main` 分支，根目录（/）作为 Pages 源，等待几分钟即可访问 `https://<your-username>.github.io/<your-repo>/`。

## 额外提示
- 如果你的 Mautic 部署使用 HTTPS，请确保 `MAUTIC_BASE_URL` 使用 `https`，否则浏览器可能阻止加载。
- 如需自定义样式或文案，直接修改 `index.html` 中的 HTML/CSS 即可。
- 若要使用 Mautic 的完整跟踪（tracking），可以在 `<head>` 中加入 Mautic 的跟踪脚本（`mtc.js`）。

---
文件：`index.html`（示例页面）
