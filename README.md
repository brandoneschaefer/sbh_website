# sbh_website

Marketing homepage and policies pages for simplebusinesshelp.com.

## Local preview

1. From the project root, run:
	`python3 -m http.server 8000`
2. Open:
	`http://localhost:8000`

## Site structure

- Homepage: `/index.html`
- Policies: `/policies/` (Privacy Policy, Terms of Service, and contact details)
- Legacy legal routes (`/privacy-policy/`, `/terms/`) redirect to the policies page
- Legacy routes (`/contact.html`, `/thanks.html`) redirect back to the homepage

## Policies subdomain

GitHub Pages serves one custom domain. The policies page is published at
`https://simplebusinesshelp.com/policies/`.

To make `https://policies.simplebusinesshelp.com` open that page, add a
**subdomain forward** in GoDaddy (the current DNS host):

1. Open the `simplebusinesshelp.com` DNS / forwarding settings.
2. Add a subdomain forward for `policies`.
3. Destination: `https://simplebusinesshelp.com/policies/`
4. Use a permanent (301) redirect and **forward only** (do not mask).

## Custom domain (GitHub Pages)

1. In GitHub repo settings, open **Pages**.
2. Set deploy source to **Deploy from a branch** and choose `main` and `/ (root)`.
3. In **Custom domain**, set `simplebusinesshelp.com`.
4. In your DNS provider, add these records:
	- `A` for `@` to `185.199.108.153`
	- `A` for `@` to `185.199.109.153`
	- `A` for `@` to `185.199.110.153`
	- `A` for `@` to `185.199.111.153`
	- `CNAME` for `www` to `brandoneschaefer.github.io`
5. Wait for DNS propagation, then enable **Enforce HTTPS** in Pages.
