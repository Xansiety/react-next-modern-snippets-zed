# React + Next Modern Snippets (Zed)

Modern snippets for React and Next.js 15+ development, ported from the
[VS Code extension](https://github.com/Xansiety/next-modern-snippets) to
Zed's extension format.

## Differences from the VS Code version

Zed's snippet engine does not document support for TextMate-style
filename-derived variables (`TM_FILENAME_BASE`) or regex/case transforms.
Because of that, the `$1` placeholder here is a plain text placeholder
(e.g. `ComponentName`) instead of auto-filling from the file name — you type
the name once and it mirrors everywhere `$1` is used, same as before.

## Snippets

See [snippets/snippets.json](./snippets/snippets.json) for the full list.
Prefixes match the original extension: `prc`, `prcm`, `prcfc`, `prca`,
`prch`, `lmrc`, `lrc`, `crc`, `mr`, `gmrf`, `gsp`, `ldc`, `err`, `ebc`,
`prcsp`, `rfc`, `rfce`, `rfcem`, `rmc`, `rnf`, `rnfs`, `rnfe`, `rnfes`.

## Local development

1. Open Zed → `zed: extensions` → **Install Dev Extension**.
2. Select this folder (`next-modern-snippets-zed`).
3. Open a `.tsx`/`.jsx` file and type a prefix, then press `Tab`.

## Publishing

Once verified locally, this repo is added as a git submodule to a fork of
[`zed-industries/extensions`](https://github.com/zed-industries/extensions)
and submitted as a PR to be listed in Zed's extension registry.

## License

MIT
