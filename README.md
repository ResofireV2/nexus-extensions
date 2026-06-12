![Nexus](https://raw.githubusercontent.com/ResofireV2/nexus/master/priv/static/images/nexus-og.webp)

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

### [Gallery](https://github.com/ResofireV2/nexus-gallery)
**by ResofireV2** · `media` `community`

A community media gallery supporting images, videos, and embeds. Includes collections, ratings, comments, reactions, and subscriptions.

---

### [Nexus Awards](https://github.com/ResofireV2/nexus-awards)
**by ResofireV2** · `community` `events`

Run community awards and voting ceremonies. Create nomination categories, let members vote, and publish results with real-time counts.

---

### [Nexus Avatars](https://github.com/ResofireV2/nexus-avatars)
**by ResofireV2** · `community` `utilities`

Automatically generates unique avatars for every user. Six distinct styles: Mech, Orc, Zombie, Inkblot, Emblem, and Snowflake.

---

### [Wrapped](https://github.com/ResofireV2/nexus-wrapped)
**by ResofireV2** · `community` `analytics`

A personalised year-in-review for every member of your community.

---

### [Nexus Events](https://github.com/ResofireV2/nexus-events)
**by ResofireV2** · `community` `events`

Community event scheduling with RSVP, calendar views, and post-linked event cards.

---

### [Polls](https://github.com/ResofireV2/nexus-polls)
**by ResofireV2** · `community` `composer`

Attach polls to posts. Members vote inline from the post footer, with permission-controlled results and voter visibility.

---

### [Nexus Tickets](https://github.com/ResofireV2/nexus-tickets)
**by ResofireV2** · `community` `moderation`

Product support ticket system. Members open tickets, staff reply with internal notes, assign tickets to team members, and track status through a full helpdesk workflow. Includes web and email notifications, rate limiting, and a staff queue with status filters.

---

### [Table of Contents](https://github.com/ResofireV2/nexus-toc)
**by ResofireV2** · `navigation` `content`

Adds an opt-in Table of Contents sidebar widget to posts with H1 and H2 headings. Admins enable it per-post via the post menu.

---

### [Blog](https://github.com/ResofireV2/nexus-blog)
**by ResofireV2** · `content` `community`

A full-featured community blog with categories, hero images, rich Markdown articles, draft/publish workflow, right sidebar widgets, and digest integration.

---

### [Notification Hub](https://github.com/ResofireV2/nexus-notification)
**by ResofireV2** · `moderation` `utilities`

Send custom notifications to individual users or broadcast to all members and groups. Includes reusable notification type templates and a full admin panel.

---

## Available Themes

Themes are installed from Admin → Appearance → Themes. They apply structural CSS overrides to Nexus — colors remain under admin control via the Appearance panel.

### [Broadsheet](https://github.com/ResofireV2/nexus-broadsheet)
**by ResofireV2** · `light` `editorial` `grid` `minimal`

Newspaper broadsheet aesthetic. Black on cream, Playfair Display serif throughout, 2-column card grid feed, and a dateline injected into the sidebar masthead. Light mode only.

---

### [Brutalist](https://github.com/ResofireV2/nexus-brutalist)
**by ResofireV2** · `bold` `minimal` `dark` `light`

Raw concrete aesthetic. Zero border-radius on every surface, heavy 2–4px borders, Space Mono monospace throughout, numbered feed posts via CSS counter, and uppercase chrome everywhere. Works in both dark and light mode.

---

### [Focus](https://github.com/ResofireV2/nexus-focus)
**by ResofireV2** · `minimal` `reading` `light` `dark`

No sidebar. The sidebar hides by default and slides in as an overlay via a hamburger button. Centred reading column, Lora serif font, and a full-width feed. Admin colors apply untouched. Works in both dark and light mode.

---

### [Neon](https://github.com/ResofireV2/nexus-neon)
**by ResofireV2** · `dark` `bold` `minimal`

Acid green on near-black. A single hue — `#00ffa3` — at varying opacities across all surfaces, text, and borders. Space Mono monospace, zero border-radius, numbered thread counter. Dark mode only.

---

### [Outline](https://github.com/ResofireV2/nexus-outline)
**by ResofireV2** · `light` `minimal` `clean`

Everything defined by borders — no background fills on any structural surface. All depth and hierarchy communicated through borders alone, with the admin accent color as the sole chromatic element. DM Sans geometric sans. Light mode only.

---

### [Wanderer](https://github.com/ResofireV2/nexus-wanderer)
**by ResofireV2** · `rounded` `tactile`

A tactile theme with pill buttons, a floating sidebar card, and aggressive rounding throughout. Every interactive element has physical depth via bottom-shadow press animations. Works in both dark and light mode.

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

`games` `media` `composer` `community` `events` `integrations` `moderation` `analytics` `utilities` `navigation` `content`

---

## Submitting a Theme

Themes are submitted as pull requests that add an entry to `registry.json` with `"type": "theme"`.

### Requirements

1. **Public GitHub repository** — the source code must be publicly accessible.
2. **Valid `theme.json`** — served at a stable raw URL. Must include at minimum: `slug`, `name`, `version`.
3. **`theme.css`** — structural CSS overrides only. Color values must use Nexus CSS variables — do not hardcode colors that would conflict with the admin Appearance panel.
4. **Logo and banner images** — both at `priv/static/logo.webp` (200×200px) and `priv/static/banner.webp` (800×400px).
5. **Stable release** — the repo must have a published GitHub release for the installer to download.

### How to Submit

1. Fork this repository.
2. Add your theme to the `extensions` array in `registry.json` with `"type": "theme"`:

```json
{
  "slug":           "your-theme-slug",
  "name":           "Your Theme Name",
  "description":    "A clear one or two sentence description of what your theme looks like.",
  "author":         "your-github-username",
  "homepage":       "https://github.com/yourorg/your-theme",
  "theme_json_url": "https://raw.githubusercontent.com/yourorg/your-theme/main/theme.json",
  "logo_url":       "https://raw.githubusercontent.com/yourorg/your-theme/main/priv/static/logo.webp",
  "banner_url":     "https://raw.githubusercontent.com/yourorg/your-theme/main/priv/static/banner.webp",
  "categories":     ["your-category"],
  "type":           "theme",
  "installs":       0
}
```

3. Open a pull request with the title `Add theme: Your Theme Name`.
4. In the PR description, include a screenshot or preview of the theme.

### Categories

Use one or more of the following categories:

`light` `dark` `minimal` `bold` `editorial` `reading` `grid` `clean` `rounded` `tactile`

---

## License

This registry is MIT licensed. Individual extensions and themes are licensed under their own terms — check each repository for details.
