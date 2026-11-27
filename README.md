# karazuri for Zed

The [karazuri](https://github.com/karazuri/palette) color theme for Zed.

[View the palette](https://karazuri.github.io/palette/)

## Variants

| Theme | Appearance | Background | Description |
|---|---|---|---|
| karazuri Umi | Dark | `#1A1A22` | Sea. The cooler dark variant. |
| karazuri Yoru | Dark | `#161514` | Night. Darker and warmer than Umi. |
| karazuri Kami | Light | `#D2CCBC` | Paper. About 60% brightness. |

![karazuri Umi palette preview](https://raw.githubusercontent.com/karazuri/palette/main/assets/umi.svg)

![karazuri Yoru palette preview](https://raw.githubusercontent.com/karazuri/palette/main/assets/yoru.svg)

![karazuri Kami palette preview](https://raw.githubusercontent.com/karazuri/palette/main/assets/kami.svg)

Every text color meets a minimum WCAG contrast against the editor background. Comments are at least 4.5:1 and syntax colors at least 5:1.

## How to use

karazuri is currently available from this repository. Choose either installation method.

- **Development extension.** Clone this repository, run `zed: install dev extension` from Zed's command palette, and select the cloned repository folder.
- **Local theme file.** Copy [`themes/karazuri.json`](themes/karazuri.json) into `~/.config/zed/themes/` on macOS or Linux. Create the directory if needed, then restart Zed.

Run `theme selector: toggle` from the command palette and choose a karazuri variant.

To follow your system appearance, add the `theme` setting to your Zed `settings.json`.

```json
{
  "theme": {
    "mode": "system",
    "dark": "karazuri Umi",
    "light": "karazuri Kami"
  }
}
```

Use `theme_overrides` in `settings.json` to change colors for a named theme. This example changes the editor background for karazuri Umi. [Zed theme overrides](https://zed.dev/docs/themes#theme-overrides)

```json
{
  "theme_overrides": {
    "karazuri Umi": {
      "editor.background": "#202028"
    }
  }
}
```

## Regenerating the theme

`themes/karazuri.json` is generated from `palette.json`. Make source changes in the palette repository, then run the command below from the Zed repository. [karazuri/palette](https://github.com/karazuri/palette)

```sh
python3 ../palette/scripts/build.py zed --out .
```

The path assumes both repos are cloned side by side.

## License

MIT
