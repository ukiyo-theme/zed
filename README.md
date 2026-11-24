# Ukiyo for Zed

The [Ukiyo](https://github.com/ukiyo-theme/palette) color theme for Zed.

| Theme | Appearance | Background |
|---|---|---|
| Ukiyo Umi | dark | `#1A1A22` |
| Ukiyo Yoru | darker, muted | `#161514` |
| Ukiyo Kami | light, about 60% brightness | `#D2CCBC` |

Every text color meets a minimum WCAG contrast against the editor background. Comments are at least 4.5:1 and syntax colors at least 5:1.

## Install

The extension isn't in Zed's extension registry yet. To install it from source, clone this repo, run **zed: install dev extension** from the command palette and select the cloned folder. Then pick a Ukiyo theme with **theme selector: toggle**.

To follow the system appearance, set this in your Zed `settings.json`:

```json
"theme": {
  "mode": "system",
  "dark": "Ukiyo Umi",
  "light": "Ukiyo Kami"
}
```

## Changing the colors

Don't edit `themes/ukiyo.json` by hand. It is generated from `palette.json` in [ukiyo-theme/palette](https://github.com/ukiyo-theme/palette):

```sh
python3 ../palette/scripts/build.py zed --out .
```

The path assumes both repos are cloned side by side.

## License

MIT
