# Publish Serendipity to JetBrains Marketplace

This repository includes a ready-to-build IntelliJ Platform plugin with bundled editor color schemes.

## What is included

- Gradle plugin project (build with `./gradlew buildPlugin`)
- Bundled schemes: Serendipity Midnight, Serendipity Morning, Serendipity Sunset
- Marketplace screenshots in `screenshots/` (1280×800 previews)
- GitHub Actions workflow that uploads a `.zip` artifact on every push to `main`

## You do not need a JetBrains IDE locally

1. Push this repo (or download the **plugin-distribution** artifact from the latest GitHub Actions run).
2. Unzip the artifact — it is the file you upload to Marketplace.

Screenshots in `screenshots/` are generated previews showing each scheme's syntax colors. You can replace them later with real IDE captures if you install IntelliJ.

## Create a JetBrains account (one time)

1. Go to [plugins.jetbrains.com](https://plugins.jetbrains.com).
2. Sign in with GitHub or create a JetBrains Account.
3. Open your profile menu → **Upload plugin**.
4. Accept the **Marketplace Developer Agreement** and create a **Vendor profile** (your name or `Serendipity-Theme`).

## Upload Serendipity Theme

1. Download the plugin ZIP from GitHub Actions (**Actions → Build Plugin → plugin-distribution**).
2. On [plugins.jetbrains.com/author/me](https://plugins.jetbrains.com/author/me), click **Upload plugin**.
3. Select the ZIP file.
4. Fill in the listing:
   - **Name**: Serendipity Theme
   - **Tags**: Theme, Color Scheme
   - **License**: MIT — link `https://github.com/Serendipity-Theme/jetbrains`
   - **Description**: copy from README; mention Serendipity variants
5. Upload screenshots from `screenshots/`:

- `Serendipity Midnight` → `screenshots/serendipity-midnight.png`
- `Serendipity Morning` → `screenshots/serendipity-morning.png`
- `Serendipity Sunset` → `screenshots/serendipity-sunset.png`

6. Submit for review ([upload guide](https://plugins.jetbrains.com/docs/marketplace/uploading-a-new-plugin.html)).

Approval usually takes a few business days. After approval, users install via **Settings → Plugins → Marketplace**.

## Manual scheme import (no plugin)

See `INSTALL.md` to import `.icls` files directly.

## Rebuild locally (optional)

Requires Java 21+:

```bash
./gradlew buildPlugin
open build/distributions/
```
