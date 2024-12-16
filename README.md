# My Alpine FoundryVTT package

## Preparing

See the [Alpine abuild instructions](https://wiki.alpinelinux.org/wiki/Creating_an_Alpine_package#)

## Building

1. Download a "timed url" zip from [foundryvtt.com](https://foundryvtt.com)
2. Edit `APKBUILD` and set `pkgversion=` to the foundry version (eg, 12.331), optionally reset `pkgrel=` to 0
3. Run `abuild checksum` to update the checksums
4. Run `abuild` to build the package

## Installing

Just use `apk add --allow-untrusted` on the built apk
