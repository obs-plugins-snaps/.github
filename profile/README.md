# OBS Plugins snaps

Crowdsourced initiative to package [OBS Studio](https://obsproject.com)
plugins as snaps, so they can be installed with a single command and
connected to the [OBS Studio snap](https://snapcraft.io/obs-studio).

## Install a plugin

```shell
sudo snap install <plugin>-obs-studio-snap
sudo snap connect obs-studio:obs-plugins <plugin>-obs-studio-snap:obs-plugins
```

Browse the available plugins at
https://github.com/orgs/obs-plugins-snaps/repositories?q=topic:obs-plugin-snap.

## Repository map

| Repository | Purpose |
|---|---|
| [`meta`](https://github.com/obs-plugins-snaps/meta) | Automation (OpenTofu, CI), plugin records, and issue tracking |
| [`template`](https://github.com/obs-plugins-snaps/template) | Scaffold used to create each plugin repository |
| [`workflows`](https://github.com/obs-plugins-snaps/workflows) | Shared reusable CI workflows |
| `<plugin>-obs-studio-snap` | One repository per packaged plugin |

## Get involved

- **Request a plugin**: open a
  [plugin request](https://github.com/obs-plugins-snaps/meta/issues/new?template=plugin-request.yml)
  and 👍 vouch for the ones you want (reactions drive prioritization)
- **Test and report**: install the snaps, use them in your daily setup,
  and [report issues](https://github.com/obs-plugins-snaps/.github/blob/main/CONTRIBUTING.md#reporting-a-bug)
  — see [CONTRIBUTING.md](https://github.com/obs-plugins-snaps/.github/blob/main/CONTRIBUTING.md)
  for the details
- **Roadmap and plugin requests**: the
  [`meta` issue tracker](https://github.com/obs-plugins-snaps/meta/issues)
