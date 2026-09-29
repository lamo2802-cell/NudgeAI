# Nudge website

A small static site (no build step) for GitHub Pages.

## Before it goes live

Contact details are filled in. Re-read the About text in `index.html` and the privacy notice in `privacy.html`, and make sure you are happy with every claim.

## Publish on GitHub Pages

1. On GitHub, create a new repository (for example `nudge-site`), public.
2. Upload these files to the root of the repository (drag and drop works: **Add file > Upload files**), and commit.
3. Go to **Settings > Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the `main` branch and the `/ (root)` folder, then Save.
4. After a minute or two the site appears at `https://YOUR-USERNAME.github.io/nudge-site/`.

Note: the 404 page and its links assume the site sits at the root of a domain. That works once you add your custom domain. On the temporary `github.io/nudge-site/` address, the 404 page's styling may not load; the main pages work fine.

## Custom domain: thisisnudge.co.uk

The repo already contains a `CNAME` file for `thisisnudge.co.uk`. At your domain registrar, add these DNS records:

| Type | Host / name | Value |
|---|---|---|
| A | `@` (the bare domain) | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `lamo2802-cell.github.io` |

Then in **Settings > Pages**, confirm the custom domain shows `thisisnudge.co.uk` and wait for the DNS check to pass (minutes to a day). Once it does, tick **Enforce HTTPS**. Remove any parking-page or default records your registrar added for `@` or `www` first.

GitHub's docs, in case these values change: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## Files

- `index.html`, `services.html`, `about.html`, `contact.html`: the site pages
- `privacy.html`: privacy notice (review it; it is general, not legal advice)
- `style.css`: all styling and colours (see `:root` at the top)
- `404.html`, `favicon.svg`, `.nojekyll`, `CNAME`, `robots.txt`, `sitemap.xml`
