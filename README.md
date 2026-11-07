# Files for jdalbis.github.io (Plaid OAuth redirect)

Copy everything in this folder, including the hidden `.nojekyll` and `.well-known/`, to the
root of a **public** repo named exactly `jdalbis.github.io` (a GitHub *user* site; a project
site serves under `/<repo>/`, where Apple won't look). Then, in the copy, replace `TEAMID` in
`.well-known/apple-app-site-association` with the Apple Developer Team ID.

| File | Served at | Why |
|---|---|---|
| `.nojekyll` | (none) | Without it GitHub Pages skips `.well-known/` |
| `.well-known/apple-app-site-association` | `https://jdalbis.github.io/.well-known/apple-app-site-association` | Tells iOS the Ladder app owns `/plaid/oauth` |
| `plaid/oauth.html` | `https://jdalbis.github.io/plaid/oauth` (no redirect) | The redirect URI Plaid returns to; blank, no scripts |

Keep the repo to these files only: no other site, scripts or analytics (see the root
README, "Plaid OAuth", host rules). Nothing here is secret: a Team ID and bundle ID are public.
