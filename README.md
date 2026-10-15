# Driftwood Isle — public site

**Don't edit this repository by hand.** Every push to `main` in
[`idle-game`](https://github.com/Gerrit-van-Vliet/idle-game) rebuilds the game for the web and
force-pushes the result here as a single commit (`tools/publish_site.sh`).

- `public/` is the web root: the playable game (`index.html`), `privacy.html` and `support.html`.
- GitHub Pages serves it from this branch (Settings → Pages → Deploy from a branch → `main` / root) at https://gerrit-van-vliet.github.io/driftwood-isle-site/; the root `index.html` forwards to `public/`. Cleavr can serve it too: a **Static HTML** site with web directory **`public`** and **Push to Deploy** on.
- The game is a single-threaded Godot web export: no special COOP/COEP headers are needed.
  `*.gz` copies are included for NGINX `gzip_static` if you enable it.
