# Home Assistant integration

After GitHub Pages is enabled, your expected URL is `https://mcarahulsharma.github.io/AppHub/`.

## Dashboard Webpage card

```yaml
type: iframe
url: https://mcarahulsharma.github.io/AppHub/
aspect_ratio: 75%
```

## Sidebar panel

Merge under the top-level `panel_iframe:` key in Home Assistant `configuration.yaml`:

```yaml
panel_iframe:
  apphub:
    title: AppHub
    icon: mdi:apps
    url: https://mcarahulsharma.github.io/AppHub/
    require_admin: false
```

Validate configuration and restart Home Assistant. If your Home Assistant version does not support `panel_iframe`, use the dashboard Webpage card or a link card.
