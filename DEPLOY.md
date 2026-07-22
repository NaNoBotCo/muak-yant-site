# Putting hongdam.net live

The whole site is one file — `index.html` — plus `CNAME`, `robots.txt`, `sitemap.xml`.
No build step, no framework. You just need to get these files onto a host and point
the domain at them. Two easy paths below; **Path A (Cloudflare Pages) is the one I recommend.**

> I can't log into Namecheap or Cloudflare for you (entering your passwords is something
> only you should do), but I can sit with you and tell you exactly what to click.

---

## Path A — Cloudflare Pages (free, fast, automatic HTTPS)  ← recommended

1. Go to **dash.cloudflare.com** and make a free account (or sign in).
2. Left menu → **Workers & Pages** → **Create** → **Pages** → **Upload assets**.
3. Name the project `muak-yant`. Drag the **contents** of this folder
   (`index.html`, `robots.txt`, `sitemap.xml` — you can skip `CNAME` and `DEPLOY.md`)
   into the upload box → **Deploy**. It goes live at `muak-yant.pages.dev` in seconds.
4. In the project → **Custom domains** → **Set up a domain** → type `hongdam.net`.
   Cloudflare shows you either a one-click option or two DNS records to add.
5. In **Namecheap** → Domain List → `hongdam.net` → **Manage** → **Nameservers** →
   choose **Custom DNS** and paste the two Cloudflare nameservers it gave you.
   (Cloudflare walks you through this — it's the "change your nameservers" step.)
6. Wait 10 min–2 hrs. `https://hongdam.net` is live, HTTPS included, free.

To update the site later: edit `index.html`, then repeat step 2–3 (re-upload). Done.

---

## Path B — Namecheap's own hosting (if you already pay for their cPanel hosting)

1. Namecheap → **Hosting List** → **cPanel** → **File Manager**.
2. Open the `public_html` folder.
3. **Upload** `index.html`, `robots.txt`, `sitemap.xml` into it.
   (Delete or ignore any placeholder `default.html` Namecheap put there.)
4. Namecheap serves `hongdam.net` from that folder automatically. Turn on their
   free **AutoSSL** (cPanel → SSL/TLS Status → Run AutoSSL) so it's `https://`.

Skip this path if you don't already have Namecheap hosting — don't buy it just for this;
Path A is free and better.

---

## Before you go live — fill in the blanks

`index.html` has three placeholder contact slots near the bottom (the "Inquire" section):

- `[ LINE ]` — your LINE ID
- `[ E-mail ]` — your contact email
- `[ Studio address · Chiang Mai ]` — as much or as little as you want to show

Search the file for `class="slot"` to find them. Tell me the real values and I'll drop them in.

---

## What's in this folder

| File | What it is |
|------|-----------|
| `index.html` | the entire website |
| `CNAME` | tells GitHub/Cloudflare Pages the domain is `hongdam.net` (harmless elsewhere) |
| `robots.txt` | lets search engines in |
| `sitemap.xml` | one-line map for search engines |
| `DEPLOY.md` | this file — not uploaded |
