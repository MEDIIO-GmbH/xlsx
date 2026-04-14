# xlsx (MEDIIO mirror)

Unmodified mirror of the [SheetJS](https://sheetjs.com) `xlsx` package,
distributed via GitHub so it can be installed in environments where the
official SheetJS CDN (`cdn.sheetjs.com`) is not reachable — notably our
CI and the Claude Code sandbox, which both egress through host-allowlisted
proxies.

> **This is a distribution mirror, not a fork.** No source changes are made
> here. All development happens upstream at SheetJS. If you need a fix or a
> feature, file it with SheetJS.

## Current version

`v0.20.3` — mirrored from <https://cdn.sheetjs.com/xlsx-0.20.3/xlsx-0.20.3.tgz>

## Usage

In your `package.json`:

```jsonc
{
  "dependencies": {
    "xlsx": "github:MEDIIO-GmbH/xlsx#v0.20.3"
  }
}
