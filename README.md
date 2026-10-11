# My CSS Themes · 个人网页主题库

面向 **Microsoft Edge + Stylus** 的个人网页 CSS 主题收藏与开发仓库。不限于 ChatGPT：可以针对任意网站创建独立样式，也可以创建适用于大多数网站的通用配色方案。

> CSS 主题只改变网页在本机浏览器中的视觉效果，不改变网站后端。建议优先使用站点专用主题；通用主题应保持保守，避免误伤复杂网页功能。

## 已有主题

| 适用网站 | 主题 | 文件 | 简介 |
|---|---|---|---|
| ChatGPT | Warm Cream 奶油米色 | [查看 CSS](themes/chatgpt/warm-cream.user.css) | 温暖浅色、柔和阅读体验 |
| ChatGPT | Dreamy Glass 梦幻渐变 | [查看 CSS](themes/chatgpt/dreamy-glass.user.css) | 浅粉紫蓝渐变、磨砂玻璃效果 |

**注意：** 两款 ChatGPT 主题不要同时启用，否则可能互相覆盖。

## 目录结构

```text
my-css-themes/
├── README.md
├── themes/
│   ├── chatgpt/
│   │   ├── warm-cream.user.css
│   │   └── dreamy-glass.user.css
│   └── universal/
│       └── README.md
├── templates/
│   └── site-theme.user.css
└── docs/
    └── 使用指南.md
```

未来可按网站域名继续扩展，例如 `themes/github/`、`themes/google/`、`themes/bilibili/`；每个文件夹可存多套不同风格。

## 安装

1. 使用 Microsoft Edge 安装 [Stylus 扩展](https://github.com/openstyles/stylus)。
2. 在本仓库打开想安装的 `.user.css` 文件。
3. 在 Stylus 中新建 UserCSS 样式，并粘贴完整内容后保存（不同 Stylus 版本的菜单可能稍有不同）。
4. 刷新对应网站；在 Stylus 扩展中单独启用、禁用或编辑样式。

参见 [使用指南](docs/使用指南.md)。

## 开发约定

- 每个网站一个目录；每个主题一个 `.user.css` 文件。
- 使用 `@-moz-document domain("example.com")` 等域名限制来避免影响不相关网站。
- 统一保留 UserStyle 元数据，维护 `@version`、`@name` 和 `@description`。
- 避免通配符 `*`、覆盖所有按钮、输入框等过宽规则。
- 保持文本对比度、可点击性、键盘焦点和网页原有功能。
- 对于新网站，复制 [站点主题模板](templates/site-theme.user.css) 后修改域名和 CSS。
- 主题是否适配需在目标网站实际测试；网站更新后可能需要维护。
- GitHub 只存代码，不自动确保浏览器已安装样式随仓库同步更新。

## 关于公开仓库

本仓库当前为公开仓库。请勿提交账号凭据、Token、私人网址或其他敏感内容。此项目是个人主题收藏库，不属于 Microsoft、OpenAI 或 Stylus 官方项目。
