# TrustTFM workshop website

A static, responsive website for the 1st Workshop on Trustworthiness of Tabular Foundation Models at IEEE SaTML 2027. Plain HTML, CSS, and SVG; no build tools or runtime dependencies. All navigation works without JavaScript. The design retains the original white background, Ubuntu Sans typography, brown headings, teal links, and workshop logo.

## Preview locally

Open `index.html` directly in your browser, or serve the folder:

```sh
python3 -m http.server 8000
```

Visit http://localhost:8000. Follow the navigation to preview each page.

## Publish with GitHub Pages

GitHub Pages is a good fit for this site. A public repository can use Pages on GitHub Free. A custom domain is optional.

1. Create a public repository on GitHub, for example `trusttfm-2027`.
2. Upload this folder's contents to the repository's `main` branch, including `.github/workflows/pages.yml`. Keep `index.html` at the repository root. If using a desktop file picker, enable hidden files so `.github` is included.
3. In **Settings → Pages → Build and deployment**, set **Source** to **GitHub Actions**.
4. Under **Actions**, select **Deploy website to GitHub Pages**, then **Run workflow** on `main`. Future pushes to `main` deploy automatically.
5. Once deployment completes, find the published link in **Settings → Pages** or the deployment job. For a project repository it is normally `https://YOUR-USERNAME.github.io/trusttfm-2027/`.

The included workflow uploads only HTML and site assets. It does not publish this README. If your default branch is not `main`, update `.github/workflows/pages.yml` accordingly.

For a shorter address, an organization named `trusttfm` could use a repository named `trusttfm.github.io`, giving `https://trusttfm.github.io/`, subject to the name being available. You can also attach a domain you own under **Settings → Pages → Custom domain** and configure its DNS using GitHub's guide.

Official guides: [creating a Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site), [configuring the publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site), [custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Editing the website

| File | Content |
| --- | --- |
| `index.html` | Overview, dates, workshop updates |
| `topics.html` | Research themes |
| `cfp.html` | Call for papers, requirements, submission status |
| `program.html` | Tentative schedule |
| `organization.html` | Committee and contact details |
| `css/custom.css` | Shared layouts with the original brown and teal color palette |
| `images/logo/trusttfm-logo.svg` | Original workshop logo |
| `images/logo/favicon.svg` | Original browser icon |
| `images/logo/trusttfm-visual.svg` | Homepage illustration using the original logo motif |
| `images/logo/trusttfm-logo-original.svg` | Original logo, kept for comparison |

Each page contains its own header and footer so it can be served directly. If changing the navigation or footer, update all five HTML files and preserve the appropriate `aria-current="page"` attribute. Asset and page URLs are relative, so both project and root-domain Pages deployments work.

The original Bulma stylesheet and SaTML logo are retained as assets. The current page layouts use `css/custom.css`.

## Content to finalize

- Confirm the exact workshop date, venue, and morning/afternoon time slot. The program currently uses the proposal's tentative 09:00–13:00 schedule.
- Add the submission portal URL to `cfp.html` when available.
- Add the applicable SaTML 2027 AI, Open Science, and Proactive Prevention of Harm policy links.
- Add confirmed invited speakers, accepted papers, and program committee members.
- Keep the submission and notification dates synchronized in `index.html` and `cfp.html`.

The dates and workshop information come from the supplied draft and proposal. The program remains tentative.
