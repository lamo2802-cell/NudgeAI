# Nudge website

A small static site (no build step) for GitHub Pages.

## Before it goes live: replace the placeholders

Search all files for these and replace them:

| Placeholder | Replace with |
|---|---|
| `YOUR_EMAIL` | Your business email address (in `index.html` and `privacy.html`) |
| `YOUR_ADDRESS` | A contact address for the business (a sole trader must show name and address on business documents) |
| `[DATE]` | Date of the privacy notice (in `privacy.html`) |

Also read the About text in `index.html` and make sure you're happy with every claim.

## Publish on GitHub Pages

1. On GitHub, create a new repository (for example `nudge-site`), public.
2. Upload these files to the root of the repository (drag and drop works: **Add file > Upload files**), and commit.
3. Go to **Settings > Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the `main` branch and the `/ (root)` folder, then Save.
4. After a minute or two the site appears at `https://YOUR-USERNAME.github.io/nudge-site/`.

Note: the 404 page and its links assume the site sits at the root of a domain. That works once you add your custom domain. On the temporary `github.io/nudge-site/` address, the 404 page's styling may not load; the main pages work fine.

## Connect your own domain (after you buy it)

1. In **Settings > Pages > Custom domain**, enter your domain (for example `www.yourdomain.co.uk`) and Save. GitHub adds a `CNAME` file to the repo.
2. At your domain registrar, add DNS records:
   - For `www`: a **CNAME** record pointing to `YOUR-USERNAME.github.io`.
   - For the bare domain (`yourdomain.co.uk`): four **A** records pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and `185.199.111.153`.
3. Wait for DNS to update (from minutes to a day), then tick **Enforce HTTPS** in the Pages settings.

Check GitHub's current documentation for custom domains in case these values have changed: https://docs.github.com/en/pages

## Files

- `index.html`: the one-page site
- `privacy.html`: privacy notice (review it; it is general, not legal advice)
- `style.css`: all styling and colours (see `:root` at the top)
- `404.html`, `favicon.svg`, `.nojekyll`
