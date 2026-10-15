# mathbrown.com

Homepage for Mr. Brown's course websites. This repo is the account's
**user site** (`quarkzebra.github.io`), served by GitHub Pages at
https://mathbrown.com (DNS on Cloudflare).

Because the custom domain sits on the user site, every project site in the
account is served under it too: the course sites live in their own repos
(`mcr3u`, `mhf4u`, `mth1w`) and answer at `mathbrown.com/mcr3u/` etc.
GitHub itself 301-redirects the old `quarkzebra.github.io/<repo>/` URLs to
the same path on mathbrown.com.

- `index.html` — the whole homepage (styles + card physics inline).
  Cards dodge the cursor for 5 s, settle by 6 s. SPE4O never settles.
  Course cards link to `/mhf4u/`, `/mcr3u/`, `/mth1w/`.
- `MHF4U/`, `MCR3U/`, `MTH1W/` — forwarders for the old upper-case
  addresses (`quarkzebra.github.io/MCR3U/` → `mathbrown.com/MCR3U/` →
  `/mcr3u/`). Paths are case-sensitive on Pages, so these do not collide
  with the lowercase project sites.
- `404.html` — forwards any other capitalization of a course path.
- `CNAME` — tells GitHub Pages this repo answers for mathbrown.com.

To add a course site: name its repo in lowercase, add a card in
`index.html` (plus a `--ac` accent for its `data-c` in both color-scheme
blocks), an upper-case forwarder folder, and its code in the `404.html` map.
