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
  "category": "utilities"
}
```

Your repo must have a valid `manifest.json` at the root following the [Oscarr plugin format](https://github.com/arediss/Oscarr/blob/main/docs/plugins.md).

### Available categories

| Category | Description |
|---|---|
| `bots` | Conversational bridges (Discord, Telegram, Matrix, Slack) |
| `notifications` | Additional notification providers |
| `automation` | Scheduled jobs, workflows, automated rules |
| `requests-workflow` | Extensions to the media request flow |
| `ui-themes` | Visual customization |
| `analytics` | Statistics, dashboards, reporting |
| `utilities` | General-purpose tools |

## Registry URL

```
https://raw.githubusercontent.com/arediss/Oscarr-Plugin-Registry/main/plugins.json
```
