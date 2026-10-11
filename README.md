# My CSS Themes

**Personal CSS themes for the web — designed with Microsoft Edge and Stylus in mind.**

[English](README.md) | [简体中文](README.zh-CN.md)

A growing collection of website-specific themes, reusable CSS starters, and wallpaper customization notes. **Not limited to ChatGPT:** any website can have its own folder and styles.

> These styles change appearance in your browser only. They do not modify the website or its underlying functionality. Some selectors may need maintenance when a website changes.

## Themes

| Website | Theme | Description |
| --- | --- | --- |
| ChatGPT | [Warm Cream](themes/chatgpt/warm-cream.user.css) | Calm cream-colored reading environment. |
| ChatGPT | [Dreamy Glass](themes/chatgpt/dreamy-glass.user.css) | Soft lavender–blue gradients and glass-like panels. **Custom wallpaper supported.** |

**Tip:** Enable only one full-page theme per website at a time to prevent conflicting styles.

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

Use their **GitHub Raw** URLs as CSS background images, for example:

```css
--cg-wallpaper-image: url("https://raw.githubusercontent.com/qiufeng662/my-css-themes/main/assets/wallpapers/pastel-gradient.webp");
```

See the [wallpaper gallery and all four URLs](assets/wallpapers/README.md).

## Custom wallpapers and images

Yes — you can replace the background with your own photo, illustration, or artwork. The Dreamy Glass theme includes an optional `--cg-wallpaper-image` setting.

Edit this line in [Dreamy Glass](themes/chatgpt/dreamy-glass.user.css):

```css
--cg-wallpaper-image: none;
```

Replace it with:

```css
--cg-wallpaper-image: url("https://example.com/my-wallpaper.jpg");
```

Use an actual, directly accessible image URL (JPG, PNG, WebP, etc.). The default `none` keeps the original gradient. For your own image, you may also upload it to `assets/wallpapers/` in this **public** repository and use its GitHub Raw URL. Do **not** upload private photos or sensitive images to a public repository.

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
