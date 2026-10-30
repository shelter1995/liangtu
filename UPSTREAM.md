# Project origin

Liangtu (晾图) is independently maintained by shelter1995.

The original project is [Tendedero](https://github.com/alejandrobujan/tendedero), created by **Alejandro Buján**. The Windows port used **v1.6.0**, commit `32a3e47187fdea7b2fd43b3ab5a913f0ed33724a`, as its source baseline. The screenshot clothesline concept, ported interaction/layout rules, and retained localization resources originate there.

The original copyright notice and MIT license are preserved in [LICENSE](LICENSE) and `reference/tendedero/LICENSE`. The upstream name and icon are excluded from the code license. Liangtu has its own branding and does not imply endorsement by the upstream author.

## Independent repository

On 2026-10-30, Windows development moved from [shelter1995/tendedero](https://github.com/shelter1995/tendedero) to [shelter1995/liangtu](https://github.com/shelter1995/liangtu). This is a standalone repository rather than a GitHub fork.

The Windows subdirectory history was extracted with `git subtree split --prefix=windows`, placing the application at the repository root while retaining its Windows development commits. Historical tags refer to the corresponding extracted Windows trees:

| Release | Original fork commit | Extracted Windows commit |
| --- | --- | --- |
| `windows-v0.7.2` | `98418e1c716454c9183e7db9c5ef4451f83e872e` | `e2510c70202d4af82186127d15fd63fe2dbe7293` |
| `windows-v0.10.7` | `2f9e34e47229492931c8d9bc4f604a5b8b3bbf8e` | `746a88205bc565dffd442759dfb71b9208a3f5b6` |

Existing release binaries and SHA-256 files were copied unchanged. Source update endpoints on `main` now refer to the independent repository. Those source changes do not alter the migrated binaries: their built-in updater continues to use the earlier fork until users install a later build.
