# nexus-extensions

The official extension registry for [Nexus](https://github.com/ResofireV2/nexus) forum software. Extensions listed here appear in the one-click install store inside every Nexus admin panel.

---

## Available Extensions

### [Gamepedia](https://github.com/ResofireV2/nexus-gamepedia)
**by ResofireV2** · `games` `integrations`

A game database powered by IGDB. Browse games, link forum threads to games, and let members track their gamelog. Adds a full Gamepedia page to the sidebar and a game-linking tool to the post composer.

---

### [GIFs](https://github.com/ResofireV2/nexus-gifs)
**by ResofireV2** · `media` `composer`

Insert GIFs and stickers from KLIPY directly into posts. Adds a GIF picker button to the composer toolbar.

---

### [Nexus Awards](https://github.com/ResofireV2/nexus-awards)
**by billyrayfoss** · `community` `events`

Run community awards and voting ceremonies. Create nomination categories, let members vote, and publish results with real-time counts.

---

## Submitting an Extension

Extensions are submitted as pull requests that add an entry to `registry.json`.

### Requirements

Before submitting, your extension must meet the following requirements:

1. **Public GitHub repository** — the source code must be publicly accessible.
2. **Valid `manifest.json`** — served at a stable raw URL (e.g. `https://raw.githubusercontent.com/yourorg/your-extension/main/manifest.json`). The manifest must include at minimum: `slug`, `name`, `description`, `version`, `author`, `homepage`, `webhook_url`, `js_bundle_url`.
3. **Logo and banner images** — both served at stable raw URLs. Logo should be square (recommended 200×200px). Banner should be 800×400px in WebP format.
4. **Stable release** — your extension should be on a tagged release and working against the current version of Nexus core.
5. **No malicious code** — extensions are reviewed before inclusion. Any extension that exfiltrates data, injects unauthorized content, or violates user privacy will be rejected and removed.

### How to Submit

1. Fork this repository.
2. Add your extension to the `extensions` array in `registry.json`:

```json
{
  "slug":         "your-extension-slug",
  "name":         "Your Extension Name",
  "description":  "A clear one or two sentence description of what your extension does.",
  "author":       "your-github-username",
  "homepage":     "https://github.com/yourorg/your-extension",
  "manifest_url": "https://raw.githubusercontent.com/yourorg/your-extension/main/manifest.json",
  "logo_url":     "https://raw.githubusercontent.com/yourorg/your-extension/main/priv/static/logo.webp",
  "banner_url":   "https://raw.githubusercontent.com/yourorg/your-extension/main/priv/static/banner.webp",
  "categories":   ["your-category"],
  "installs":     0
}
```

3. Open a pull request with the title `Add extension: Your Extension Name`.
4. In the PR description, briefly describe what your extension does and link to any relevant documentation or screenshots.

### Categories

Use one or more of the following categories. If none fit, propose a new one in your PR:

`games` `media` `composer` `community` `events` `integrations` `moderation` `analytics` `utilities`

---

## License

This registry is MIT licensed. Individual extensions are licensed under their own terms — check each extension's repository for details.
