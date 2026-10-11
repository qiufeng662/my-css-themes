# Custom image wallpapers / 自定义背景图片

[English README](../README.md) · [中文 README](../README.zh-CN.md)

## English

You can apply your own image, artwork, or wallpaper using **CSS + Microsoft Edge + Stylus**.

### ChatGPT Dreamy Glass

1. Open [Dreamy Glass](../themes/chatgpt/dreamy-glass.user.css) in Stylus.
2. Find `--cg-wallpaper-image: none;`.
3. Change it to `--cg-wallpaper-image: url("https://your-host.example/wallpaper.webp");`.
4. Refresh ChatGPT. Keep the default `none` to use the original gradient.
5. Use `--cg-wallpaper-position`, `--cg-wallpaper-size`, and `--cg-wallpaper-overlay` to tune appearance. The overlay alpha (the final number from 0 to 1) adjusts readability.

Use a directly accessible image URL, not an HTML gallery/share page. The link must load in your browser, and browser privacy/CSP policies may affect particular image hosts.

### Other websites

Start from [image-wallpaper.user.css](../templates/image-wallpaper.user.css), replace `example.com` with the site's domain, then adjust its page/container CSS. A generic body background cannot always penetrate opaque application layers.

### Hosting options

- Public URL from an image host you control.
- Upload non-sensitive, appropriately licensed image files to `assets/wallpapers/` on GitHub, then use the file's `raw.githubusercontent.com` URL.
- Data URL embedded in CSS for small images (increases file size).
- Local `file://` images may be blocked by browser security restrictions and are less portable.

**Privacy:** This repository is public. Do not upload personal or sensitive photos. Respect the original image's license.

## 简体中文

通过 **Edge + Stylus + CSS**，可以将自己的图片设为网页背景。

### ChatGPT 梦幻玻璃主题

1. 在 Stylus 中打开 [Dreamy Glass](../themes/chatgpt/dreamy-glass.user.css)。
2. 找到 `--cg-wallpaper-image: none;`。
3. 修改为 `--cg-wallpaper-image: url("https://图片直链地址/wallpaper.webp");`。
4. 刷新 ChatGPT。改回 `none` 即恢复默认渐变。
5. 调节 `--cg-wallpaper-position`（图片位置）、`--cg-wallpaper-size`（缩放）和 `--cg-wallpaper-overlay`（遮罩透明度）。

链接应直接指向 JPG/PNG/WebP 等图片，不能只是图片分享网页。某些图片网站可能禁止外部引用或限制浏览器加载。

### 其他网站

使用 [通用壁纸开发模板](../templates/image-wallpaper.user.css)，先替换 `example.com`，再按目标网站的具体结构调整。**不是所有网站只改一个 CSS 属性就能透明显示背景**，某些网站还需要修改页面容器样式。

### 如何存储图片

可以使用已有的公共图片直链，或者将非隐私、已获授权的图片上传到仓库 `assets/wallpapers/` 后获取 GitHub Raw 链接。较小的图片也可以使用 data URL 嵌入 CSS；本机 file URL 受安全限制，不一定能用。

**提醒：仓库为公开状态，切勿上传私人照片、敏感信息或无授权作品。**
