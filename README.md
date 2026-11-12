# Sonic Unleashed Recompiled × Archipelago — Updates

Public update metadata and release-download repository for the Archipelago connector.

**No proprietary game assets, backups, or private saves should be distributed here.** Released client archives and APWorld packages are hosted under GitHub Releases.

## Original project, fork and source code

**Sonic Unleashed Recompiled × Archipelago is an unofficial, modified fork/derivative of [Unleashed Recompiled by hedge-dev](https://github.com/hedge-dev/UnleashedRecomp).** It adds Archipelago multiworld functionality and is not an official release or endorsement by the original developers.

- **Original Unleashed Recompiled:** https://github.com/hedge-dev/UnleashedRecomp
- **Archipelago modified source repository:** https://github.com/ZMGBZak/Sonic-Unleashed-Recompiled-Archipelago/tree/archipelago-prototype
- **License:** The original project is distributed under the [GNU General Public License version 3](https://www.gnu.org/licenses/gpl-3.0.en.html) (GPL-3.0). The corresponding-source and redistribution obligations continue to apply to modified builds.

Please credit the original authors and refer to the upstream repository for the base project. For source-code compliance, distributors must make the **complete corresponding source** for each released binary available, including any additional source files, modifications and applicable build/install scripts. A partial source snapshot is not sufficient by itself.

## AI-Assisted Development & Human Oversight

**Transparency about AI use:** The Archipelago-specific modifications in this project were developed through an ongoing collaboration between the project maintainer and ChatGPT (OpenAI), used as an AI-assisted programming and explanation tool.

The maintainer originated the ideas, gameplay goals, feature requests and many proposed improvements for the Archipelago integration. We discussed the intended behavior, technical approaches and trade-offs before and during implementation. ChatGPT assisted by proposing and generating code, helping investigate bugs, and explaining what functions did, why particular changes were suggested, and how the changes were expected to work.

**The maintainer remained actively involved throughout development.** They reviewed what was being added or corrected, challenged decisions, requested adjustments, suggested alternative approaches and further improvements, and compiled and tested successive changes in the game. Results from those tests informed subsequent fixes and iterations. AI-generated suggestions were not treated as automatically correct or accepted without human feedback.

**This is not described by the maintainer as “vibe coding.”** Their intent was an iterative, collaborative development process: a human developer directing and testing the project while working with an AI coding assistant as a close development partner—much like a small team discussing, implementing, reviewing and improving features together. This is a description of the workflow, not a claim that the AI is a legal co-author, repository maintainer, or independent rights holder.

The maintainer is responsible for decisions about what is published and for verifying the resulting software. **AI assistance does not replace code review, testing, security checks, attribution, or the license obligations of the upstream GPL-3.0 project.**


**V0.9 source and license notice:** The complete GPL-3.0 license text is available in [docs/GPL-3.0.txt](docs/GPL-3.0.txt). Refer to [V0.9 source status and redistribution checklist](docs/V0.9_SOURCE_STATUS.md) before redistributing the Windows/Linux binaries. **At the time of this update, the GitHub source branch has not yet been verified to contain the exact complete corresponding source for both V0.9 builds.** The binary release alone does not prove GPL compliance.

## How it works

The game checks [`updates/manifest.json`](updates/manifest.json) for the current client and APWorld versions. The latest published binary release is **V0.9 Beta**, with manual Windows, Linux and APWorld downloads on the [V0.9 release page](https://github.com/ZMGBZak/Sonic-Unleashed-Recompiled-Archipelago-Updates/releases/tag/V0.9). The [update manifest](updates/manifest.json) lists their exact published filenames, sizes and SHA-256 digests.

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
