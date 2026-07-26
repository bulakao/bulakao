# Bulakao

Static GitHub Pages gateway for [bulakao.com](https://bulakao.com/).

The site introduces Bulakao’s two focused practices:

- [Bulakao Partner](https://partner.bulakao.com/) — creator partnership coordination
- [Bulakao Solutions](https://solutions.bulakao.com/) — custom software, automation, and applied AI

## Local preview

No package manager or build step is required.

```sh
python3 -m http.server 4175 --bind 127.0.0.1
```

Open `http://localhost:4175/`.

## Deployment

Pushing `main` runs `.github/workflows/static.yml` and deploys the static repository to GitHub Pages. `CNAME` keeps the production domain at `bulakao.com`.
