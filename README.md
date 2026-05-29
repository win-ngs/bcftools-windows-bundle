# BCFtools Unofficial Windows Bundle

This repository publishes a small Windows x64 bundle of `bcftools.exe` copied
from the MSYS2 UCRT64 environment, together with the runtime DLLs needed to run
it from a single directory.

This is an unofficial Windows bundle. It is not published, endorsed, or
supported by the official BCFtools/HTSlib project.

Official BCFtools site: https://www.htslib.org/

## Included Version

- BCFtools: 1.23.1
- HTSlib: 1.23.1
- Source environment: MSYS2 UCRT64
- Target platform: Windows x64

## Usage

Download the release ZIP from:

https://github.com/win-ngs/bcftools-windows-bundle/releases/tag/v1.23.1-windows-ucrt64

Extract it, and run:

```powershell
.\bcftools.exe --version
```

The executable and DLLs are intended to stay in the same directory.

BCFtools plugins are included in the `plugins` directory. To use `bcftools +plugin`
commands from PowerShell, set the plugin path first:

```powershell
$env:BCFTOOLS_PLUGINS = "$PWD\plugins"
.\bcftools.exe plugin -l
```

You can add the extracted directory to `PATH` if you want to run `bcftools` from
any shell.

## License

BCFtools is distributed under the MIT/Expat license. See `LICENSE.md`.

This bundle also includes third-party DLLs from MSYS2 packages. See
`THIRD_PARTY_NOTICES.md` and the `licenses/` directory in the release archive.
