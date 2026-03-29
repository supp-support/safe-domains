# Safe Domains

Your phone's spacebar shrinks when you're in the URL bar. A period key shows up right next to it. You go to search "food delivery" and type `foof.delivery` instead. Your browser thinks that's a website and takes you there.

If a scammer owns that domain, you're on a phishing page. If we own it, you get a clean page that tells you what happened and sends you back to your search with one click.

That's what this is. We buy misspelled domains before scammers can, and we put this page on them.

## Live domains

- [foof.delivery](https://foof.delivery) -- "food delivery"
- [pancake.recipes](https://pancake.recipes) -- "pancake recipes"

More coming.

## How it works

One HTML file. No frameworks, no dependencies, no build step. 11KB total.

The page reads the domain it's being served on, splits it into words, checks each word against a typo correction dictionary, and shows the user what they meant to search. Search buttons link directly to Google, Bing, and DuckDuckGo with no tracking, no redirects, no affiliate parameters.

If JavaScript is blocked, the page shows a generic fallback: "You meant to type something else. This isn't it. Let us help get you back there."

Wildcard subdomains are supported. `easy.pancake.recipes` becomes "easy pancake recipes."

## Deploy your own

```
git clone https://github.com/supp-support/safe-domains.git
cd safe-domains
```

Host `index.html` anywhere. Point your domain at it. That's it.

If you own a misspelled domain and want to protect it instead of parking it, use this. Add your domain's typo corrections to the `corrections` object in the script tag, or don't -- the page works fine without corrections, it just shows the domain split into words.

## What's in here

```
index.html  -- the page (everything is in this one file)
LICENSE     -- MIT
README.md   -- you're reading it
```

Nothing else. No config files, no package.json, no node_modules, no build artifacts.

## Pull requests

We don't accept PRs. If you find a bug, open an issue.

The correction dictionary will grow as we add domains, but we maintain that ourselves. If you fork this and add your own corrections, that's fine -- MIT license, do what you want.

## Closed source versions

We may build specialized versions for advertisers and brands that include sponsored placements, analytics dashboards, and brand-specific features. Those won't be in this repo. This open source version will always be the clean, ad-free page you see on our domains today.

## Who we are

[Supp](https://supp.support) makes customer support software. We care about humans. We make support software, and protect people on the web.

More about why we do this: [supp.support/safe](https://supp.support/safe)

## License

MIT
