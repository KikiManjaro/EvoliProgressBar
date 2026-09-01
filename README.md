# EvoliProgressBar — Eevee Progress Bar for JetBrains IDEs

[![CI](https://github.com/KikiManjaro/EvoliProgressBar/actions/workflows/ci.yml/badge.svg)](https://github.com/KikiManjaro/EvoliProgressBar/actions/workflows/ci.yml)
[![JetBrains Plugin](https://img.shields.io/badge/JetBrains-Plugin-000000?logo=intellij-idea)](https://plugins.jetbrains.com/)

An IntelliJ Platform plugin that replaces the default progress bar with a running **Eevee** (determinate) and random **Eeveelutions** (indeterminate) — based on the [Nyan Progress Bar](https://github.com/batkovitch/NyanProgressBar) by Dmitry Batkovitch.

## Demo

| Mode | Preview |
|------|---------|
| **Determinate** | ![Eevee determinate](https://i.imgur.com/EZUatq6.gif) |
| **Indeterminate** | ![Eevee indeterminate](https://i.imgur.com/Q3lXoYW.gif) |

- Determinate: Eevee runs across the filled portion with a grass texture.
- Indeterminate: a random Eeveelution bounces back and forth.

## Installation

### From JetBrains Marketplace (recommended)
1. Open **Settings → Plugins → Marketplace**
2. Search for **"Eevee Progress Bar"**
3. Click **Install** and restart the IDE

### From Source
```bash
git clone https://github.com/KikiManjaro/EvoliProgressBar.git
# Open the project in IntelliJ IDEA (Plugin SDK)
# Build → Prepare Plugin Module for Deployment
```

## Compatibility

| Plugin Version | IDE Since Build | Notes |
|----------------|-----------------|-------|
| 1.8            | 193 (2019.3)    | Supports IntelliJ 2023.3+ |

See `resources/META-INF/plugin.xml` for the `idea-version` declaration.

## Project Structure

```
src/
  ProgressBarUi.java                 # Custom BasicProgressBarUI
  Icons.java                         # Eeveelution GIF icons
  ProgressBarLafManagerListener.java # LafManager hook
resources/
  *.gif / grass.png                  # Sprites
  META-INF/plugin.xml
```

## Development

- JDK 17+ and IntelliJ IDEA with Plugin DevKit
- Open `EeveeProgressBar.iml` as a Plugin module
- Run the `plugin` run configuration to launch a sandboxed IDE

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## Credits

- Original idea: [NyanProgressBar](https://github.com/batkovitch/NyanProgressBar) by Dmitry Batkovitch
- Sprites: Eevee & Eeveelutions

## License

MIT — same as NyanProgressBar.
