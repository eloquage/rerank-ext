# eloquage/rerank-ext

Optional TypePHP native accelerator for [eloquage/rerank](https://github.com/eloquage/rerank).

This repository is a PIE extension release shell. The runtime API and pure-PHP implementation remain in the regular package. The release workflow fetches the matching public source tag, compiles it with the shared Dockerized TypePHP builder, verifies the module, and uploads a PIE binary asset.

## Install

Use PIE with the Composer package name:

```sh
pie install eloquage/rerank-ext
```

The regular package remains the portable fallback:

```sh
composer require eloquage/rerank
```

## Release contract

The runtime package is tagged first, then this repository receives the identical `vX.Y.Z` tag and GitHub Release. The release contains a Linux x86_64/glibc/PHP 8.5/NTS asset named:

```
php_eloquage_rerank-X.Y.Z_php8.5-x86_64-Linux-glibc-N-debug-NTS.tar.gz
```

The archive contains `eloquage_rerank.so`. Windows, macOS, ZTS, and non-8.5 binaries are not currently published.

The companion package is optional and does not add a framework, `swoole/typephp`, or builder runtime dependency.

