# 我的 CSS 主题库

**面向 Microsoft Edge + Stylus 的个人网页 CSS 主题集合。**

[English](README.md) | [简体中文](README.zh-CN.md)

用于收藏和开发各类网站的自定义主题，包括页面颜色、渐变、玻璃效果、自定义图片壁纸等。**不局限于 ChatGPT**，任何网站都可以独立创建主题文件夹。

> CSS 只改变本地浏览器中的显示效果，不修改网站的后端功能。网站更新后，部分选择器可能需要维护。

## 现有主题

| 网站 | 主题 | 说明 |
| --- | --- | --- |
| ChatGPT | [Warm Cream 奶油米色](themes/chatgpt/warm-cream.user.css) | 柔和、适合长时间阅读的暖色主题 |
| ChatGPT | [Dreamy Glass 梦幻渐变玻璃](themes/chatgpt/dreamy-glass.user.css) | 浅紫蓝渐变、玻璃面板，**支持自定义壁纸** |

**提示：** 同一个网站的多套完整主题不要同时启用，避免 CSS 规则互相覆盖。

## 默认壁纸（4 张）

仓库已经收录以下四张**默认壁纸**，均为 1672 × 941 分辨率的 WebP 文件，可直接供 Edge + Stylus 使用。

| 梦幻粉彩渐变 | 动漫月夜星空 |
|:---:|:---:|
| [![梦幻粉彩渐变](assets/wallpapers/pastel-gradient.webp)](assets/wallpapers/pastel-gradient.webp) | [![动漫月夜星空](assets/wallpapers/anime-night-sky.webp)](assets/wallpapers/anime-night-sky.webp) |
| [Pastel Gradient](assets/wallpapers/pastel-gradient.webp) | [Anime Night Sky](assets/wallpapers/anime-night-sky.webp) |

| 晨雾森林 | 紫蓝星云 |
|:---:|:---:|
| [![晨雾森林](assets/wallpapers/misty-forest.webp)](assets/wallpapers/misty-forest.webp) | [![紫蓝星云](assets/wallpapers/cosmic-nebula.webp)](assets/wallpapers/cosmic-nebula.webp) |
| [Misty Forest](assets/wallpapers/misty-forest.webp) | [Cosmic Nebula](assets/wallpapers/cosmic-nebula.webp) |

在 CSS 主题中使用图片的 **GitHub Raw 直链**，例如：

```css
--cg-wallpaper-image: url("https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/assets/wallpapers/pastel-gradient.webp");
```

查看 [完整四图预览与全部直链](assets/wallpapers/README.md)。

## 自定义背景图片

可以使用自己的图片、插画、摄影作品当作背景，也能叠加渐变、调整透明度和背景位置。

编辑 [Dreamy Glass](themes/chatgpt/dreamy-glass.user.css) 中的配置：

```css
--cg-wallpaper-image: none;
```

替换为：

```css
--cg-wallpaper-image: url("https://example.com/my-wallpaper.jpg");
```

把示例地址改成**浏览器能直接访问的图片地址**。使用 `none` 时仍显示默认渐变。

如果需要让仓库存储壁纸，可以把图片上传到 `assets/wallpapers/`，然后使用公开 GitHub Raw 图片地址。**当前仓库是公开的，不要上传私人照片、敏感图片或未经授权的作品。**

其他网站可复制 [自定义图片模板](templates/image-wallpaper.user.css)，将 `example.com` 改成实际域名，并按网站结构调整选择器。

完整说明：[自定义图片使用指南](docs/CUSTOM_WALLPAPERS.md)（英文）及 [Edge + Stylus 中文指南](docs/使用指南.md)。

## 仓库目录

```text
my-css-themes/
├── README.md                   # English (default)
├── README.zh-CN.md             # 中文
├── themes/
│   ├── chatgpt/
│   │   ├── warm-cream.user.css
│   │   └── dreamy-glass.user.css
│   └── universal/
│       └── README.md
├── templates/
│   ├── site-theme.user.css
│   └── image-wallpaper.user.css
├── assets/
│   └── wallpapers/
│       └── README.md
└── docs/
    ├── CUSTOM_WALLPAPERS.md
    └── 使用指南.md
```

以后可以增加 `themes/github/`、`themes/bilibili/` 等目录。通用主题目录暂为预留，尚无已验证的跨网站主题。

## 在 Edge 中安装

1. 安装 [Stylus 扩展](https://github.com/openstyles/stylus)。
2. 打开对应的 `.user.css` 文件，复制全部内容。
3. 在 Stylus 中创建 UserCSS 样式，粘贴并保存。
4. 刷新目标网站。
5. 可以在 Stylus 中单独切换、关闭、修改各个主题。

不同版本的 Stylus 操作界面可能略有区别。详见 [中文使用指南](docs/使用指南.md)。

## 开发规范

- 按网站建立目录，每个主题独立维护。
- 使用 `@-moz-document domain("example.com")` 将样式限定于目标域名。
- 保留并更新 UserStyle 元数据和版本号。
- 尽量避免影响所有按钮、输入框等的宽泛 CSS 规则。
- 测试文字可读性、菜单、弹窗、表单与网站交互。
- 适配所有网页是长期目标，但不同站点结构不同，无法保证一份 CSS 通用。
- GitHub 仓库更新不等于浏览器里已安装的样式自动更新。

## 隐私提醒

目前仓库为 **Public（公开）**。请勿提交密码、Token、私人链接和个人隐私图片。本项目为个人维护，与 Microsoft、OpenAI 或 Stylus 官方无关联。
