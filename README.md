# Shadrack Kpani Odametey – Personal Website

One-page bilingual (English / Arabic) site for recruiters.
Live address once published: https://shadlabs.github.io/

## Files

| File | What it is |
|---|---|
| `index.html` | The whole website |
| `headshot.jpg` | Photo in the hero |
| `og-image.jpg` | Preview image shown when the link is shared on LinkedIn |
| `Shadrack-Odametey-CV.pdf` | English CV (Download CV button) |
| `Shadrack-Odametey-CV-Arabic.pdf` | Arabic CV |

## Publish on GitHub Pages (one time, about 10 minutes)

1. Sign in to GitHub as **ShadLabs**.
2. Click **+ → New repository**. Name it exactly `shadlabs.github.io`, set it to **Public**, and click **Create repository**.
3. On the new repository page, click **uploading an existing file**.
4. Drag in all five files above (not the folder), then click **Commit changes**.
5. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, Branch to **main** and folder **/ (root)**, then **Save**.
6. Wait 1–2 minutes and open https://shadlabs.github.io/

Your existing project links (for example `shadlabs.github.io/labor-planning-calculator`) keep working.

## Check the LinkedIn preview

Paste your site address into https://www.linkedin.com/post-inspector/ and click **Inspect**.
You should see the banner image, your name and the description. Run it again after any change to the image, because LinkedIn caches previews.

## Edit your content (no design changes needed)

Open `index.html` on GitHub, click the pencil icon, and scroll to the block that starts with:

```
EDIT HERE — everything you'll update lives in SITE below.
```

Everything is listed there: links, strengths, experience, education, projects and certifications. Each item has an English (`en`) and Arabic (`ar`) version.

**Add a certification:** copy one `{ ... }` block inside `certifications`, paste it after the last one, put a comma between them, and change the text. Use `status: "in-progress"` to show the "In progress" badge, or `status: "done"` with a Credly link in `url`.

**When PL-300 is complete:** change its `status` to `"done"`, set the `date`, and paste the Credly verification link into `url`.

**Add a project:** copy one block inside `projects` the same way.

**Replace a CV:** upload a new PDF with exactly the same file name. Keep the phone number off the versions you put here.

Click **Commit changes**. The site updates within about a minute.

Tip: keep the quotes, commas and brackets exactly as they are. If the page goes blank after an edit, a missing comma or quote is the usual cause; open the file's **History** on GitHub to restore the previous version.

## Connect a custom domain later (for example shadrackodametey.com)

1. Buy the domain from a registrar (Namecheap, Cloudflare, Porkbun; about USD 10–15 a year).
2. In the repository, go to **Settings → Pages → Custom domain**, enter the domain, and save.
3. At your registrar, add the DNS records GitHub shows on that page (four `A` records for the root domain and a `CNAME` for `www` pointing to `shadlabs.github.io`).
4. When the check passes, tick **Enforce HTTPS**.
5. In `index.html`, replace `https://shadlabs.github.io/` with your new domain in the `og:image`, `og:url`, `canonical` and JSON-LD lines near the top, so the LinkedIn preview keeps working.
