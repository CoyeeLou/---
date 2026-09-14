# 科目一 速记卡（源码与导出说明）

本仓库包含用于打印与导出的科目一速记卡源文件（HTML），方便你在本地导出为 PDF 或 PNG。

文件列表：

- `科目一_一页速记卡.html`：A4 单页速记卡 HTML（内嵌 SVG 标志），可直接在浏览器打开并打印为 A4 PDF。
- `科目一_便携卡_A6.html`：A6 便携卡 HTML（内嵌 SVG 标志），可直接在浏览器打开并打印为 A6 PDF 或导出为 PNG。

导出建议：

A. 在浏览器中打开 HTML → Ctrl/Cmd+P → 选择纸张大小（A4 或 A6）→ 页边距设为“无/最小”→ 勾选“背景图形/颜色”→ 另存为 PDF。

B. 将 A6 PDF 转 PNG（300 DPI）建议使用 ImageMagick：

```bash
# 转换为 300 DPI PNG
convert -density 300 "科目一_便携卡_A6.pdf" -quality 100 "科目一_便携卡_A6.png"
```

或使用 headless Chrome 截图：

```bash
# macOS 示例（替换为你的 chrome 路径与文件路径）
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --hide-scrollbars --screenshot="科目一_便携卡_A6.png" --window-size=1240,1748 "file:///完整/路径/科目一_便携卡_A6.html"
```

如需我替换为官方高清矢量标志并重新生成 PDF/PNG，可回复 "官方标志"。

---

制作：Copilot · 速记卡生成器
