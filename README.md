# Boing Systems Limited Website

Public company website for Boing Systems Limited, hosted with GitHub Pages.

## Live Website

- Website: https://boing.nz
- Privacy policy: https://boing.nz/privacy.html
- GitHub repository: https://github.com/dannycash-dev/boing-website

The site is also available through the default GitHub Pages address:

https://dannycash-dev.github.io/boing-website/

## Website Files

- `index.html` - company homepage
- `privacy.html` - privacy policy page
- `assets/Boing_Logo.png` - Boing logo
- `CNAME` - GitHub Pages custom domain configuration
- `.github/workflows/pages.yml` - automatic GitHub Pages deployment

## Local Preview

From this repository directory, run:

```bash
python3 -m http.server 8080
```

Then open:

- http://localhost:8080
- http://localhost:8080/privacy.html

## GitHub Pages Deployment

The repository is configured to deploy automatically when changes are pushed to `main`.

The current deployment workflow runs from `main` but checks out the `public-site` branch before uploading the Pages artifact. This allows the original website version to remain available on `main` while the reduced public version is displayed on the live site.

To deploy a change to the live site:

1. Make the change on `public-site`.
2. Push `public-site` to GitHub.
3. Update or trigger the Pages workflow from `main` if required.
4. Check the deployment under the repository's **Actions** tab.

GitHub Pages settings should use **GitHub Actions** as the deployment source.

## Custom Domains

`boing.nz` is the primary custom domain and is configured in `CNAME`.

At the DNS provider, configure the root domain with GitHub Pages A records:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Configure `www.boing.nz` as a CNAME pointing to:

```text
dannycash-dev.github.io
```

`boing.co.nz` can be configured at 1st Domains as a permanent URL redirect to:

```text
https://boing.nz
```

After DNS is configured, GitHub Pages provisions HTTPS for `boing.nz`. Enable **Enforce HTTPS** in the repository's Pages settings once the certificate is available.

## Contacts

- Danny: danny.cash@boing.nz
- Aidan: aidan.clark@boing.nz
- Larry: larry.eade@boing.nz

The privacy policy currently directs privacy enquiries to `danny.cash@boing.nz`.
