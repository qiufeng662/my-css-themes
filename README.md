# My CSS Themes

**Personal CSS themes for the web — designed with Microsoft Edge and Stylus in mind.**

[English](README.md) | [简体中文](README.zh-CN.md)

A growing collection of website-specific themes, reusable CSS starters, and wallpaper customization notes. **Not limited to ChatGPT:** any website can have its own folder and styles.

> These styles change appearance in your browser only. They do not modify the website or its underlying functionality. Some selectors may need maintenance when a website changes.

## Install a theme in one click (Edge + Stylus)

**First:** Open ChatGPT in Edge, set Appearance to **Light**, and **disable the old ChatGPT theme** in Stylus (especially the previous Dreamy Glass v1). Do not enable multiple full-site themes at once.

With [Stylus installed](https://github.com/openstyles/stylus), open a **direct UserCSS link** below. Stylus should display an installation page; click **Install style**, return to ChatGPT, and refresh. If the installer does not open, see the [step-by-step instructions](docs/使用指南.md).

| Theme | Direct Stylus installation | Source |
| --- | --- | --- |
| Dreamy Gradient / 梦幻紫色渐变 | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/dreamy-glass.user.css) | [CSS](themes/chatgpt/dreamy-glass.user.css) |
| Pastel Gradient / 粉彩渐变壁纸 | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/wallpaper-pastel.user.css) | [CSS](themes/chatgpt/wallpaper-pastel.user.css) |
| Anime Night Sky / 月夜星空 | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/wallpaper-anime.user.css) | [CSS](themes/chatgpt/wallpaper-anime.user.css) |
| Misty Forest / 晨雾森林 | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/wallpaper-forest.user.css) | [CSS](themes/chatgpt/wallpaper-forest.user.css) |
| Cosmic Nebula / 紫蓝星云 | [Install](https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/themes/chatgpt/wallpaper-nebula.user.css) | [CSS](themes/chatgpt/wallpaper-nebula.user.css) |

**Switch wallpapers:** Click the Stylus extension icon on ChatGPT, turn the active ChatGPT theme **off**, then turn the theme you want **on**. You can install all five but keep **only one enabled at a time**.

**Performance fix:** The original purple Dreamy Glass theme was replaced with a **Lite** implementation. It removes large-area backdrop blur, expensive `:has()` selectors, generic button animations, and unnecessary styling overrides. The appearance may be simpler, and performance still depends on your Edge device and ChatGPT version. Browser-level testing has not been performed.

## Default wallpapers (4)

These four original wallpapers are included in the repository as **your default image collection**. All images are 1672 × 941 WebP files, ready for use in Edge + Stylus.

| Pastel Gradient | Anime Night Sky |
|:---:|:---:|
| [![Pastel Gradient](assets/wallpapers/pastel-gradient.webp)](assets/wallpapers/pastel-gradient.webp) | [![Anime Night Sky](assets/wallpapers/anime-night-sky.webp)](assets/wallpapers/anime-night-sky.webp) |
| [Pastel Gradient](assets/wallpapers/pastel-gradient.webp) | [Anime Night Sky](assets/wallpapers/anime-night-sky.webp) |

| Misty Forest | Cosmic Nebula |
|:---:|:---:|
| [![Misty Forest](assets/wallpapers/misty-forest.webp)](assets/wallpapers/misty-forest.webp) | [![Cosmic Nebula](assets/wallpapers/cosmic-nebula.webp)](assets/wallpapers/cosmic-nebula.webp) |
| [Misty Forest](assets/wallpapers/misty-forest.webp) | [Cosmic Nebula](assets/wallpapers/cosmic-nebula.webp) |

No CSS editing is necessary: choose one of the standalone [wallpaper themes](#install-a-theme-in-one-click-edge--stylus) above. The images remain available separately as [GitHub Raw files](assets/wallpapers/README.md), so they can also be reused on other websites.

## Custom wallpapers and images

Yes — you can replace the background with your own photo, illustration, or artwork. For ChatGPT, the four lightweight wallpaper themes above already include the image URL: just install one and switch it on.

For ChatGPT, simply install one of the four wallpaper themes above—**no manual URL replacement is required**. To use a different personal image in a custom theme, change `--lite-wallpaper` in a **copy** of one of the wallpaper CSS files to `url("https://example.com/my-wallpaper.jpg")`. The URL must point directly to a publicly accessible image. Since this repository is public, avoid committing sensitive photos.

For another website, start from [the reusable wallpaper template](templates/image-wallpaper.user.css), **change `example.com` to the intended domain**, and adapt the selectors to that site. There is no one-size-fits-all CSS for every website.

See the [full wallpaper guide](docs/CUSTOM_WALLPAPERS.md) for examples, opacity/readability tips, image hosting, and known limitations.

## Repository layout

```text
my-css-themes/
├── README.md
├── README.zh-CN.md
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

New websites can be added under `themes/github/`, `themes/bilibili/`, etc. The `universal` folder is reserved for carefully tested cross-site styles; **no universal theme has been verified yet**.

## Install in Microsoft Edge

1. Install [Stylus](https://github.com/openstyles/stylus) in Microsoft Edge.
2. Open a `.user.css` file in this repository and copy its **entire content**.
3. Create a new UserCSS style in Stylus, paste the CSS, and save.
4. Refresh the target website.
5. Use Stylus to enable, disable, or edit themes independently.

Depending on your Stylus version, the exact editor controls may differ. See [中文安装指南](docs/使用指南.md).

## Contributing and maintenance guidelines

- Keep one site per folder and one theme per `.user.css` file.
- Scope website-specific rules using `@-moz-document domain("example.com")`, and avoid broad selectors where possible.
- Maintain UserStyle metadata (`@name`, `@namespace`, `@version`, `@description`).
- Test accessibility, text readability, input controls, menus, and dialogs before considering a theme stable.
- CSS is site-dependent: visual consistency across **all** websites is not guaranteed.
- Committing changes to GitHub does **not** automatically update styles already installed in your browser.

## Privacy and attribution

This repository is **public**. Do not commit passwords, tokens, personal URLs, or private images. The project is independently maintained and is not affiliated with Microsoft, OpenAI, or Stylus.
