# sbh_website

Single-page marketing homepage for simplebusinesshelp.com.

## Local preview

1. From the project root, run:
	`python3 -m http.server 8000`
2. Open:
	`http://localhost:8000`

## Site structure

- Homepage: `/index.html`
- Legacy routes (`/contact.html`, `/thanks.html`) redirect back to the homepage.

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
