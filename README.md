# Bulakao

The central gateway for the Bulakao network, published at [bulakao.com](https://bulakao.com/).

The homepage gives visitors a concise introduction to two focused practices:

- [Bulakao Partner](https://partner.bulakao.com/) coordinates creator campaigns from matching through reporting.
- [Bulakao Solutions](https://solutions.bulakao.com/) replaces difficult manual workflows with custom software, automation, and applied AI.

## Site

The gateway is intentionally small:

1. A shared Bulakao introduction.
2. A Solutions section for operational software.
3. A Partner section for creator partnerships.

It uses one fixed, code-generated galaxy field with animated stars and comets. Jekyll builds the dependency-free site without a frontend framework or package manager.

## Local preview

```sh
jekyll serve --host 127.0.0.1 --port 4175
```

Open `http://localhost:4175/`.

## Deployment

Pushing `main` runs the Jekyll build and GitHub Pages deployment in `.github/workflows/static.yml`. The `CNAME` file maps the deployment to `bulakao.com`.

## Repository structure

- `index.html` — complete gateway, styles, and interactions
- `_config.yml` — Jekyll site and publishing configuration
- `og-image.png` — social sharing image
- `CNAME` — production custom domain
- `robots.txt` and `sitemap.xml` — search discovery metadata
- `design-qa.md` and `audits/` — visual review notes and evidence
