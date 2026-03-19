# Gemini Watermark Remover

Gemini AI 图片去水印工具 — 100% 浏览器本地运行，免费、极速、无损。

## 功能

- ✅ 反向 Alpha 混合算法，无损去水印
- ✅ 拖拽 / 点击上传，支持 JPG、PNG、WebP
- ✅ 单图预览对比 + 批量处理
- ✅ 批量 ZIP 下载
- ✅ 中英文切换
- ✅ 暗色主题 + 响应式设计
- ✅ 零依赖单文件，无需安装

## 使用

直接用浏览器打开 `index.html`，或启动 HTTP 服务器：

```bash
python3 -m http.server 8080
# 访问 http://localhost:8080
```

## 技术原理

Gemini 添加水印公式：`watermarked = α × logo + (1-α) × original`

反向求解：`original = (watermarked - α × 255) / (1-α)`

通过预提取水印的 alpha 通道图，反向计算还原原始像素。

## 浏览器支持

所有现代浏览器（Chrome、Firefox、Safari、Edge）

## License

MIT
