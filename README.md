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

### React

| Prefix  | Name                           | Description                                 |
| ------- | ------------------------------ | -------------------------------------------- |
| `prc`   | Page Component                 | Simple page component                        |
| `prcfc` | Functional Component (FC)      | Arrow function with `React.FC<Props>`        |
| `prca`  | Async Server Component         | Server component with async data fetching   |
| `prch`  | Custom Hook                    | Hook with `useState` and `useEffect`         |
| `crc`   | Client Component               | Component with `"use client"` directive      |
| `rfc`   | Arrow Function Component       | Arrow function with named export             |
| `rfce`  | Arrow Function Component (DE)  | Arrow function with default export           |
| `rmc`   | Memo Component                 | Component wrapped with `memo()`              |
| `ebc`   | Error Boundary                 | React 19 `ErrorBoundary` wrapper component   |

### Next.js

| Prefix  | Name                            | Description                                           |
| ------- | -------------------------------- | ------------------------------------------------------ |
| `lmrc`  | Layout with Metadata             | Layout component with `Metadata` export               |
| `lrc`   | Layout without Metadata          | Layout component without metadata                     |
| `mr`    | Static Metadata                  | Static `Metadata` export                               |
| `gmrf`  | Generate Metadata                | `generateMetadata` function for dynamic SEO            |
| `gsp`   | Generate Static Params           | `generateStaticParams` function                        |
| `ldc`   | Loading Component                | Loading UI component                                   |
| `err`   | Error Component                  | Error segment with reset functionality                 |
| `prcsp` | Page with searchParams           | Async page with params and searchParams (Next.js 15+)  |
| `prcm`  | Page Component with Metadata     | Page component with `Metadata` export                  |
| `rfcem` | Arrow Function + Metadata (DE)   | Arrow function with default export and `Metadata`       |

### React Native

| Prefix  | Name                         | Description                                      |
| ------- | ----------------------------- | -------------------------------------------------- |
| `rnf`   | Function Component            | React Native function component                   |
| `rnfs`  | Function Component + Styles   | React Native function with `StyleSheet`            |
| `rnfe`  | Arrow Function Component      | React Native arrow function with default export    |
| `rnfes` | Arrow Function + Styles       | React Native arrow function with `StyleSheet`       |

Full snippet bodies live in [snippets/snippets.json](./snippets/snippets.json).

## Usage

Type a snippet prefix (e.g. `prc`) in a `.tsx` or `.jsx` file and press `Tab` to expand.

### Tab Stops

- **`$1`** — Component name. Type it once; every mirrored occurrence (declaration,
  JSX, export) updates together, same linking behavior as VS Code.
- **`$2`, `$3`** — Secondary fields like Props type contents, destructured params,
  metadata values.
- **`$0`** — Final cursor position after all tab stops are filled.

## Local development

1. Open Zed → `zed: extensions` → **Install Dev Extension**.
2. Select this folder (`react-next-modern-snippets-zed`).
3. Open a `.tsx`/`.jsx` file and type a prefix, then press `Tab`.

## Publishing

Once verified locally, this repo is added as a git submodule to a fork of
[`zed-industries/extensions`](https://github.com/zed-industries/extensions)
and submitted as a PR to be listed in Zed's extension registry.

## License

MIT
