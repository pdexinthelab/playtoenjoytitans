# PlayToEnjoy Titans website

Plain HTML and CSS, no JavaScript (except one line in 404.html). Every page is a file in this folder.

## Pages

| File | Page |
|---|---|
| index.html | Home: welcome, logo, game gallery |
| games.html | Games: every game as a text link with one line each |
| boujee-island.html and the other game files | One page per game |
| mods.html | Mods: every mod as a text link with one line each |
| mod-super-video-golf.html and other mod- files | One page per mod |
| news.html | News, newest first |
| help.html | Help: answers to common questions |
| sitemap.xml, robots.txt | For search engines: add a line to sitemap.xml for each new page |
| donate.html | Donate (PayPal link) |
| contact.html | Contact (email) |
| accessibility.html | Accessibility statement |
| about.html | About (bio) |
| 404.html | Shown for wrong addresses |
| css/style.css | Colours and layout for every page |
| images/ | Logo and game pictures |

## Add a new game

1. Copy a game page, for example `footy-racer.html`, and rename it, for example `new-game.html` (lower case, hyphens).
2. In the new file change: the `<title>`, the description, the sharing lines (`og:` and `canonical`, near the top), the `<h1>`, Available now or Coming soon, the picture and its
   alt text, the synopsis, Last updated, the download links (Dropbox links ending in `dl=1`) and System requirements.
   Leave out the Full Game or Trial heading and its links if the game does not have one yet.
   Also change the Controls table, the Accessibility features list and the game's name in the Send feedback link.
   For a Coming soon game copy `footy-27.html` instead (no downloads).
3. Put the game's picture in `images/` (16 by 9 shape, about 1280 by 720, saved as .jpg).
4. In `index.html` copy one `<li class="game-card">` block and change it. Its alt text must be the same as on the game page.
5. In `games.html` copy one `<li>` block and change it.
6. Commit and push: the site updates within a minute or two.

## Add a new mod

Mods work exactly like games, in their own section:
1. Copy `mod-super-video-golf.html` and rename it, starting with `mod-`, for example `mod-new-mod.html`.
2. Change the same things as for a game, plus What you need (the original game the mod needs). Mods use the
   PlayToEnjoy Titans logo as their picture (`images/mod-logo.jpg`), so keep the picture and its alt text as they are. Mod pages leave out
   the "every level of device" line, because a mod needs whatever its original game needs.
3. In `index.html` copy one `<li class="game-card">` block in the Mods list (under the Mods heading) and change it.
4. In `mods.html` copy one `<li>` block and change it.

## Add news

In `news.html` copy one `<li>` block, put it at the top of the list, and change the date (in both places), heading and text.

## Social media

In the footer of every page there is a commented-out list of social links. Copy the line you want above the comment
and put in your address. (Claude Code can do this for every page at once.)

## Your own domain

1. Buy the domain from any registrar (for example Namecheap, Cloudflare or GoDaddy).
2. In the registrar's DNS settings add these records:
   - Four `A` records for the bare domain (`@`): `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record for `www` pointing to `YOUR-GITHUB-NAME.github.io`
3. On GitHub: the repository, Settings, Pages, Custom domain: type the domain and Save. This adds a `CNAME` file.
4. When the check passes (DNS can take up to a day), tick Enforce HTTPS.
404.html works with either address.
