# sbh_website

Markdown-inspired redesign for simplebusinesshelp.com.

## Local preview

1. From the project root, run:
	`python3 -m http.server 8000`
2. Open:
	`http://localhost:8000`

## Contact form setup (Formspree)

1. Create a new form in Formspree and copy the endpoint URL (looks like `https://formspree.io/f/xxxxabcd`).
2. In `/contact.html`, replace:
	`https://formspree.io/f/REPLACE_WITH_YOUR_FORM_ID`
	with your real Formspree endpoint.
3. (Recommended) In Formspree settings, enable extra spam protection (reCAPTCHA/Turnstile).
4. Optional: update `_next` in `/contact.html` if your final domain changes.

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
