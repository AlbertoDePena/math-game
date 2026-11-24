# Star Sums — standalone web bundle

This folder is a complete static site. There is nothing to install and no backend or database to configure.

## Run it

1. Unzip this archive into a folder.
2. Serve that folder over HTTP or HTTPS. For example:
   - macOS/Linux: `python3 -m http.server 8080` from inside the folder, then open `http://localhost:8080/`.
   - Windows: serve the folder with IIS, or use `npx serve .` if Node.js is available.
   - Internal hosting: drop the files into any nginx, Apache, or IIS virtual directory.
3. Open the site in a modern browser. Do not open `index.html` directly with `file://` — ES modules and service workers require HTTP(S).

The build uses relative paths, so a subfolder such as `https://intranet/apps/star-sums/` works as well as a domain root.

## What the machine needs

- A static web server and a current Chrome, Edge, Firefox, or Safari browser.
- Nothing else on the player machine: Node.js, npm, a database, and environment variables are only needed to build the bundle, not to run it.
- For PWA installation and offline play: use HTTPS or `localhost` and Chrome/Edge (or Add to Home Screen in Safari). Over plain internal HTTP the game still runs, but installation and offline caching are disabled.
- Google Fonts load from the internet; an air-gapped machine will use system fallback fonts.
- Profiles, scores, and settings live in that browser's `localStorage` on that device. Clearing site data erases them, so use **Grown-ups → Backup and move** before clearing browser data or moving to another machine. Each browser profile or device has its own separate progress; there is no account or server sync.

## Source and support

The project source is at https://github.com/65fastback2plus2/star-sums. See the repository README for game instructions, build commands, and Android build steps.
