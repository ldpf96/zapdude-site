# zapdude-site

Download site for [Zapdude](https://github.com/ldpf96/zapdude), the
multi-account WhatsApp Web desktop client. Static, dependency-free,
vanilla HTML/CSS/JS.

Live at: https://ldpf96.github.io/zapdude-site/

## How it works

- GitHub Pages serves `index.html` from this repository root
  (branch `main`, folder `/`).
- Download buttons resolve at runtime through the GitHub API
  (`/repos/ldpf96/zapdude/releases/latest`), so they always point at the
  current release assets (`x64-setup.exe`, `aarch64.dmg`, `x64.dmg`).
  The visitor's platform gets a "recommended" outline; if the API is
  unreachable the buttons fall back to the Releases page.
- Two languages (Spanish default, English toggle) switch client side
  and persist in `localStorage`.
- macOS install notes on the page cover the one-time Gatekeeper
  confirmation for directly distributed apps (no paid Apple signing).

## Local preview

Open `index.html` in a browser, or serve the folder:

```powershell
python -m http.server 8000
```

## Publishing

Pushes to `main` rebuild the Pages site automatically. Pages is enabled
via the repository settings (source: main branch, root folder).
