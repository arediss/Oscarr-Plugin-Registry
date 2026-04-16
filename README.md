# Oscarr Plugin Registry

Official plugin directory for [Oscarr](https://github.com/arediss/Oscarr). The Oscarr admin panel fetches `plugins.json` to discover community plugins.

## How it works

1. `plugins.json` lists approved plugin repositories
2. Oscarr fetches this file and reads each plugin's `manifest.json` from their GitHub repo
3. Users can browse available plugins in Admin > Plugins > Discover
4. Installation is manual: clone the plugin repo into `packages/plugins/` and restart Oscarr

## Submitting a plugin

Open a Pull Request adding your plugin to `plugins.json`:

```json
{
  "repository": "yourname/your-plugin-repo",
  "category": "utilities",
  "tags": ["plex"]
}
```

Your repo must have a valid `manifest.json` at the root following the [Oscarr plugin format](https://github.com/arediss/Oscarr/blob/main/docs/plugins.md).

### Available categories

Each plugin has exactly **one** category describing what it does.

| Category | Description |
|---|---|
| `bots` | Conversational bridges (Discord, Telegram, Matrix, Slack) |
| `notifications` | Additional notification providers |
| `automation` | Scheduled jobs, workflows, automated rules |
| `requests-workflow` | Extensions to the media request flow |
| `subscriptions` | Paid/timed access tiers and user lifecycle management |
| `ui-themes` | Visual customization |
| `analytics` | Statistics, dashboards, reporting |
| `utilities` | General-purpose tools |

### Tags (optional)

Tags are free-form labels describing the **context** a plugin targets — usually a third-party service it integrates with. A plugin can have multiple tags.

| Tag | Description |
|---|---|
| `plex` | Integrates with Plex (shared libraries, accounts, watch state) |
| `jellyfin` | Integrates with Jellyfin |
| `emby` | Integrates with Emby |
| `discord` | Integrates with Discord |
| `telegram` | Integrates with Telegram |
| `matrix` | Integrates with Matrix |
| `slack` | Integrates with Slack |
| `radarr` | Integrates with Radarr |
| `sonarr` | Integrates with Sonarr |

Need a new tag? Propose it in your PR.

## Registry URL

```
https://raw.githubusercontent.com/arediss/Oscarr-Plugin-Registry/main/plugins.json
```
