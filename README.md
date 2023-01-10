[![CI](https://github.com/tj-actions/cargo-bump/workflows/CI/badge.svg)](https://github.com/tj-actions/cargo-bump/actions?query=workflow%3ACI)
[![Update release version.](https://github.com/tj-actions/cargo-bump/workflows/Update%20release%20version./badge.svg)](https://github.com/tj-actions/cargo-bump/actions?query=workflow%3A%22Update+release+version.%22)
[![Public workflows that use this action.](https://img.shields.io/endpoint?url=https%3A%2F%2Fused-by.vercel.app%2Fapi%2Fgithub-actions%2Fused-by%3Faction%3Dtj-actions%2Fcargo-bump%26badge%3Dtrue)](https://github.com/search?o=desc\&q=tj-actions+cargo-bump+path%3A.github%2Fworkflows+language%3AYAML\&s=\&type=Code)

## cargo-bump

Github action that bumps the current version in your `Cargo.toml`.

```yaml
on:
  push:
    tags:
      - v*

jobs:
  bump-version:
    runs-on: ubuntu-latest
    name: Test cargo-bump
    steps:
      - uses: actions/checkout@v2
      - name: Bump version
        uses: tj-actions/cargo-bump@v1
      # Commit and Push changes to the Cargo.toml
```

## Inputs

<!-- AUTO-DOC-INPUT:START - Do not remove or modify this section -->

|       INPUT       |  TYPE  | REQUIRED | DEFAULT |                                                   DESCRIPTION                                                   |
|-------------------|--------|----------|---------|-----------------------------------------------------------------------------------------------------------------|
|   release\_type    | string |  false   |         | The release type (major, minor, patch).<br> (Default: the diff between the current<br>tag and the previous tag) |
| working-directory | string |  false   |  `"."`  |                                                Working directory                                                |

<!-- AUTO-DOC-INPUT:END -->

## Outputs

<!-- AUTO-DOC-OUTPUT:START - Do not remove or modify this section -->

|    OUTPUT    |  TYPE  |                                   DESCRIPTION                                    |
|--------------|--------|----------------------------------------------------------------------------------|
| new\_version  | string |                           The current project version                            |
| old\_version  | string |                           The previous project version                           |
| release\_type | string | The difference between two versions by<br>the release type (major, minor, patch) |

<!-- AUTO-DOC-OUTPUT:END -->

*   Free software: [MIT license](LICENSE)

If you feel generous and want to show some extra appreciation:

[![Buy me a coffee][buymeacoffee-shield]][buymeacoffee]

[buymeacoffee]: https://www.buymeacoffee.com/jackton1

[buymeacoffee-shield]: https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png

## Credits

This package was created with [Cookiecutter](https://github.com/cookiecutter/cookiecutter) using [cookiecutter-action](https://github.com/tj-actions/cookiecutter-action)

## Report Bugs

Report bugs at https://github.com/tj-actions/cargo-bump/issues.

If you are reporting a bug, please include:

*   Your operating system name and version.
*   Any details about your workflow that might be helpful in troubleshooting.
*   Detailed steps to reproduce the bug.
