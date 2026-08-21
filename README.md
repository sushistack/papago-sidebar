# Papago Sidebar

Firefox sidebar panel for [Papago](https://papago.naver.com/). Loads Papago in
a sidebar iframe and strips `X-Frame-Options` / `Content-Security-Policy`
response headers (via `declarativeNetRequest`) so it can be framed.

## Install (development)

1. Open `about:debugging#/runtime/this-firefox`
2. **Load Temporary Add-on…** → select `manifest.json`
3. Open the sidebar: `View → Sidebar → Papago` (or `Ctrl+B` and pick Papago)

## Release

Push a `vX.Y.Z` tag matching `manifest.json`'s `version`. The
[release workflow](.github/workflows/release.yml) signs the add-on with AMO
(unlisted) and attaches the `.xpi` to a GitHub release. Requires repo secrets
`WEB_EXT_API_KEY` and `WEB_EXT_API_SECRET`.

## Icons

`icons/papago.png` is a transparent white monochrome variant derived from
Papago's official web app icon. The extension uses generated
`icons/icon-*.png` files for its toolbar and add-on icons.
