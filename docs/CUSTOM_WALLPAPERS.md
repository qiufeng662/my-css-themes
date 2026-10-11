# Custom Wallpaper Guide / 自定义壁纸指南

[English](../README.md) | [简体中文](../README.zh-CN.md)

## Switch the four built-in wallpapers (no CSS editing)

With Microsoft Edge + Stylus installed, open the direct `.user.css` link:

| Wallpaper | Install |
| --- | --- |
| Pastel Gradient | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/wallpaper-pastel.user.css) |
| Anime Night Sky | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/wallpaper-anime.user.css) |
| Misty Forest | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/wallpaper-forest.user.css) |
| Cosmic Nebula | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/wallpaper-nebula.user.css) |

Switch by toggling **off** the current ChatGPT theme in the Stylus extension, then toggling **on** the desired theme. Only one should be enabled per site.

To use another image, clone a wallpaper theme and replace the `--lite-wallpaper` value with `url("https://your-domain.example/photo.webp")`. Adjust `--lite-overlay` to make foreground text readable. Links must point directly to an image and be browser-accessible.

The old `--cg-wallpaper-image` option belonged to an earlier heavy version of Dreamy Glass. In Lite v2 it has been superseded by standalone themes using `--lite-wallpaper`.

The lighter themes eliminate `backdrop-filter` and complex `:has()` selectors. They have **not** been visually or performance-tested on every ChatGPT build, and may require updates as the site changes.

## 中文：如何换壁纸

**不必写 CSS，也不必复制图片链接。**

1. 打开 [中文安装步骤](使用指南.md)，先关闭旧版紫色主题。
2. 点上表想使用的壁纸的 **Install** 链接，选择 **Install style / 安装样式**。
3. 在 ChatGPT 页面打开 Stylus，先关闭原主题，再打开新主题，刷新。
4. 四个壁纸主题可以全部安装，但**同一时间只开启一个**。

如需使用第五张自己提供的图片，请复制一份壁纸 CSS，把 `--lite-wallpaper` 的地址换成可直连的 JPG/PNG/WebP 图片。仓库公开时不要上传私人或敏感照片。

其他网页请使用 [专属域名壁纸模板](../templates/image-wallpaper.user.css)，网站布局需要单独适配。
