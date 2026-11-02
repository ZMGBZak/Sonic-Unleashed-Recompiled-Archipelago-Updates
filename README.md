# Sonic Unleashed Recompiled × Archipelago — Updates

Public update metadata and release-download repository for the Archipelago connector.

**No proprietary game assets, backups, or private saves should be distributed here.** Released client archives and APWorld packages are hosted under GitHub Releases.

## Original project, fork and source code

**Sonic Unleashed Recompiled × Archipelago is an unofficial, modified fork/derivative of [Unleashed Recompiled by hedge-dev](https://github.com/hedge-dev/UnleashedRecomp).** It adds Archipelago multiworld functionality and is not an official release or endorsement by the original developers.

- **Original Unleashed Recompiled:** https://github.com/hedge-dev/UnleashedRecomp
- **Archipelago modified source repository:** https://github.com/ZMGBZak/Sonic-Unleashed-Recompiled-Archipelago/tree/archipelago-prototype
- **License:** The original project is distributed under the [GNU General Public License version 3](https://www.gnu.org/licenses/gpl-3.0.en.html) (GPL-3.0). The corresponding-source and redistribution obligations continue to apply to modified builds.

Please credit the original authors and refer to the upstream repository for the base project. For source-code compliance, distributors must make the **complete corresponding source** for each released binary available, including any additional source files, modifications and applicable build/install scripts. A partial source snapshot is not sufficient by itself.

## How it works

The game checks [`updates/manifest.json`](updates/manifest.json) for the current client and APWorld versions. The current published version is `0.8.2`, with manual downloads available on the [V0.8.2 release page](https://github.com/ZMGBZak/Sonic-Unleashed-Recompiled-Archipelago-Updates/releases/tag/V0.8.2).

The modified source repository is separate. Never upload a development/build/game directory wholesale.

## Publication rules

- Publish only release metadata and separately reviewed distributable files.
- Never include game dumps, proprietary game assets, extracted textures/models/music/video, local backups or patch scripts with private data.
- Review source licenses and redistribution conditions before offering compiled binaries.
- For releases, use an allowlist of approved files and verify each artifact before upload.
- Keep checksums and download links explicit. Do not claim an update is available before publishing an actual release.
- Do not store GitHub tokens in the client.

## Updater behavior

- **Client:** notify about a newer version, then a separate updater will install approved client files after the game exits.
- **APWorld:** notify users and point them to an approved GitHub download page. It is not automatically installed.
