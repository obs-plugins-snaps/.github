# Contributing to OBS Plugins snaps

Thanks for your interest in this project! This organization packages
[OBS Studio](https://obsproject.com) plugins as snaps so they can be
installed with a single command and connected to the
[OBS Studio snap](https://snapcraft.io/obs-studio).

By participating in this project you agree to abide by our
[Code of Conduct](CODE_OF_CONDUCT.md).

Please read this document before opening an issue or a pull request.

## Requesting a plugin

Do you know a great OBS plugin that is not packaged here yet? We want to
hear about it.

1. Check [existing plugin requests](https://github.com/obs-plugins-snaps/meta/issues?q=is%3Aissue+label%3Aplugin-request)
   to make sure it has not been requested already.
2. Open a new issue in [meta](https://github.com/obs-plugins-snaps/meta/issues)
   using the **Plugin request** template. Fill in the plugin name, a link
   (the OBS forums thread or the upstream repository) and a brief
   description of what it does.
3. Once your issue is open, other users can **vouch for it by reacting
   with 👍**. The number of reactions is the main signal we use to
   prioritize what gets packaged next.

## Reporting a bug

- **Packaging bugs** (installation fails, the plugin does not show up in
  OBS Studio, it crashes on connect, ...): open an issue in the
  repository of the affected snap. Bug templates ask you to confirm that
  the problem does not happen when the plugin is installed natively
  (without the snap) — that check is what tells packaging problems and
  plugin bugs apart.
- **Plugin bugs** (wrong behavior inside OBS Studio once loaded): please
  report them to the plugin developers upstream. Check the `website` or
  `source-code` links on the snap page
  (https://snapcraft.io/search?category=obs-plugins) to find the upstream
  project.

## Testing plugins and reporting your findings

You don't need to write code to contribute! Installing the snaps,
exercising the plugins in your daily OBS Studio setup, and reporting
what you find is one of the most valuable contributions at this stage:

1. Install a plugin snap and connect it:

   ```shell
   sudo snap install <plugin>-obs-studio-snap
   sudo snap connect obs-studio:obs-plugins <plugin>-obs-studio-snap:obs-plugins
   ```

2. Use it in your regular streams and recordings, and watch for
   packaging problems: the plugin missing from OBS Studio, crashes on
   connect, missing libraries, wrong paths.
3. Report findings as bug reports in the plugin's repository (see
   *Reporting a bug* above). Do the native-install comparison — knowing
   whether a problem is snap-specific or upstream is half the diagnosis.

Findings from this Q&A effort feed directly into the packaging fixes and
are equally welcome for plugins already requested in `meta`.

## Code contributions

**Discuss first, then code.** Please open an issue (or comment on an
existing one) before sending a pull request. Pull requests that arrive
without a related discussion may be closed without review.

Right now this project is in its early stages: the scaffolding and
automation exist, but the actual snap packaging is still being set up.
For this reason, **all pull requests are handled by the maintainers at
the moment**. This includes:

- Packaging new plugins
- Changes to `meta` (OpenTofu automation, CI, plugin records)
- Changes to `template` (the repository scaffold)

Once the packaging pipeline is in place we will open up contribution of
new plugin records (a small, declarative JSON file plus a short
description). Until then, the best way to help is requesting plugins and
vouching for existing requests with 👍.
