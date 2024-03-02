[![CI](https://github.com/tj-actions/cargo-bump/workflows/CI/badge.svg)](https://github.com/tj-actions/cargo-bump/actions?query=workflow%3ACI)
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->
[![Update release version.](https://github.com/tj-actions/cargo-bump/workflows/Update%20release%20version./badge.svg)](https://github.com/tj-actions/cargo-bump/actions?query=workflow%3A%22Update+release+version.%22)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/d02fea7e1446463789182186c74b7f40)](https://app.codacy.com/gh/tj-actions/cargo-bump/dashboard?utm_source=gh\&utm_medium=referral\&utm_content=\&utm_campaign=Badge_grade)
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
        uses: tj-actions/cargo-bump@v3
      # Commit and Push changes to the Cargo.toml
```

See working example [here](https://github.com/tj-actions/cargo-bump/blob/main/.github/workflows/test.yml)

## Inputs

<!-- AUTO-DOC-INPUT:START - Do not remove or modify this section -->

|                                        INPUT                                        |  TYPE  | REQUIRED | DEFAULT |                                                DESCRIPTION                                                |
|-------------------------------------------------------------------------------------|--------|----------|---------|-----------------------------------------------------------------------------------------------------------|
|        <a name="input_release_type"></a>[release\_type](#input_release_type)         | string |  false   |         | The release type (major, minor, patch). (Default: the diff between the current tag and the previous tag)  |
| <a name="input_working-directory"></a>[working-directory](#input_working-directory) | string |  false   |  `"."`  |                                             Working directory                                             |

<!-- AUTO-DOC-INPUT:END -->

## Outputs

<!-- AUTO-DOC-OUTPUT:START - Do not remove or modify this section -->

|                                 OUTPUT                                 |  TYPE  |                                    DESCRIPTION                                     |
|------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------|
|  <a name="output_new_version"></a>[new\_version](#output_new_version)   | string |                            The current project version                             |
|  <a name="output_old_version"></a>[old\_version](#output_old_version)   | string |                            The previous project version                            |
| <a name="output_release_type"></a>[release\_type](#output_release_type) | string | The difference between two versions <br>by the release type (major, minor, patch)  |

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

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://home.boidol.dev/"><img src="https://avatars.githubusercontent.com/u/652404?v=4?s=100" width="100px;" alt="Raphael Boidol"/><br /><sub><b>Raphael Boidol</b></sub></a><br /><a href="https://github.com/tj-actions/cargo-bump/commits?author=boidolr" title="Documentation">📖</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!