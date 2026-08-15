# zola-debian

Debian packaging for [Zola](https://github.com/getzola/zola), published to
the [pkg.haus](https://pkg.haus) APT archive.

## Install

Follow the installation instructions on [pkg.haus](https://pkg.haus), then run:

```bash
sudo apt install zola
```

## Building locally

```bash
docker run --rm -v "$PWD:/target" -w /target ghcr.io/pkghaus/deb-builder:trixie
```

Packages land in `debs/`. Build for another suite by swapping the image
tag (`testing` or `unstable`).

## Release

* add a new entry in `debian/changelog`
* update `VERSION` in `package.conf` to the upstream tag
* create a tag matching the Debian package version (`vX.Y.Z-N`) - CI
  validates the build on every suite and architecture; the pkg.haus
  archive ingest builds and publishes it

## License

```
Copyright (c) 2021-2026 pkg.haus

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Buy us a coffee?

If you feel like buying us a coffee (or a beer?), donations are welcome:

```
BTC : bc1qq04jnuqqavpccfptmddqjkg7cuspy3new4sxq9
DOGE: DRBkryyau5CMxpBzVmrBAjK6dVdMZSBsuS
ETH : 0x2238A11856428b72E80D70Be8666729497059d95
LTC : MQwXsBrArLRHQzwQZAjJPNrxGS1uNDDKX6
```
