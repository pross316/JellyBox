# JellyBox

A Netflix-style frontend for [Jellyfin](https://jellyfin.org/), built as a single HTML file.

Drop it anywhere. Open it in a browser. Connect to your Jellyfin server.

![JellyBox screenshot — dark glassmorphism UI with Netflix-style browse rows](screenshot.png)

## Features

- **Netflix-style browse rows** — Continue Watching, New & Recent, Acclaimed, Edge of Seat, Scary, Hidden Gems, Classic Era, New Episodes, and more
- **Genre browser** — grid of genre tiles with counts, click to browse filtered content
- **Genre + rating filters** — filter the shelf by genre and minimum rating in real time
- **Per-row sorting** — sort any row by rating, year, title, or date added
- **Hero banner** — rotating top-rated unwatched content with backdrop images
- **Collections** — curated franchise playlists (MCU, Star Wars, LOTR, John Wick, and more) with custom order
- **Watchlist** — bookmark anything, persisted in localStorage
- **Lucky Reel** — spin wheel to pick something to watch
- **Mystery Box** — blind random pick with dramatic reveal
- **Fuzzy search** — search by title, director, or cast member
- **Trailer button** — plays trailers directly in the detail modal
- **Stats tab** — library stats, top genres, completion rate, and more
- **Multi-profile login** — saved profile switcher per browser
- **Fast loading** — two-phase init (resume/recent rows appear immediately), localStorage library cache with 15-min TTL

## Setup

1. Download `index.html`
2. Open it in any web browser (file://, a local server, or hosted anywhere)
3. Enter your Jellyfin server URL (e.g. `http://192.168.1.100:8096`)
4. Sign in with your Jellyfin credentials

That's it. No install, no build step, no dependencies.

## Hosting

Since it's a single file, you can serve it from anywhere:

- Drop it in your Jellyfin server's web root
- Serve it with Caddy, Nginx, or Apache
- Host it on GitHub Pages, Cloudflare Pages, or any static host
- Open it directly from your filesystem

> **Note:** Your Jellyfin server must allow CORS requests from wherever you're serving the file. If you're hosting on the same domain/IP as Jellyfin this is a non-issue.

## Customization

Open `index.html` in a text editor. At the very top of the `<script>` block you'll find the config section — that's the only thing you'd ever need to change.

Collections are hardcoded title-string matches near the top of the JS. Edit them to match your library's exact Jellyfin titles.

## Maintenance

Best-effort. PRs welcome. This is a side project — if something breaks I probably don't know yet and am going about my day unbothered.

## License

MIT
