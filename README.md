# derekwietelman.github.io

Source for my academic website, https://derekwietelman.github.io.

The site is built with [Hugo](https://gohugo.io) and the [Hugo Blox](https://hugoblox.com) academic theme. **GitHub builds and publishes it automatically**: every change saved to the `main` branch rebuilds the site in about 1–3 minutes. Nothing needs to be built on your computer, and there is no `public` folder to copy.

## Where things live

| What you want to change | File |
| --- | --- |
| Name, title, affiliation, interests, education, profile links | `data/authors/me.yaml` |
| Biography text, homepage sections and their order | `content/_index.md` |
| A paper (title, authors, status, abstract, links) | `content/publications/<paper>/index.md` |
| Top menu links | `config/_default/menus.yaml` |
| PDFs (CV, papers) | `static/files/` (served at `/files/<name>.pdf`) |
| Profile photo | `assets/media/authors/me.jpg` |
| Site-wide settings (colors, footer, search) | `config/_default/params.yaml` |

## Making changes on github.com (no software needed)

1. Open the file on github.com and click the pencil icon (**Edit this file**).
2. Make your change.
3. Click **Commit changes…**, write a short note (e.g. "Update CV"), keep **Commit directly to the `main` branch** selected, and click **Commit changes**.
4. Wait 1–3 minutes, then reload the site (hard refresh: Ctrl+Shift+R on Windows, Cmd+Shift+R on Mac).
5. To check progress, open the **Actions** tab: a green check means the site is live; a red ✗ means the build failed and the previous version of the site stays up. Click the failed run to see the error, or ask Claude to fix it.

### Common tasks

**Update your CV.** In `static/files/`, click **Add file → Upload files**, upload the new PDF named exactly `cv.pdf` (it replaces the old one), and commit. The menu, Download CV button and CV icon all point to `/files/cv.pdf`.

**Change a paper's status** (e.g. a working paper gets accepted). Edit `content/publications/<paper>/index.md`:
- Working paper status line: `publication: Revise and Resubmit, *JAERE*` (text between `*` is italic).
- Once published, switch it to the Publications section by changing `publication_types` to `article-journal` and giving the journal details, e.g.
  ```yaml
  publication_types:
  - article-journal
  publication:
    name: Journal of the Association of Environmental and Resource Economists
    volume: 12
    issue: 3
  hugoblox:
    ids:
      doi: 10.1086/123456
  ```

**Add a new paper.**
1. Upload the PDF to `static/files/`.
2. In `content/publications/`, click **Add file → Create new file** and name it `<short-name>/index.md` (e.g. `lead/index.md`).
3. Copy the contents of an existing paper's `index.md` (e.g. `content/publications/bbr/index.md`), then edit the title, authors (use `me` for yourself), date, status, abstract and PDF link.
4. `publication_types: [article]` puts it under **Working Papers**; `[article-journal]` puts it under **Publications**. Papers are listed newest first by `date`.

**Edit your bio or interests.** Bio paragraphs are under `text:` in `content/_index.md`; interests, education and role are in `data/authors/me.yaml`. Keep the indentation (spaces) exactly as it is—YAML is sensitive to it.

## Previewing changes before they go live (optional)

For bigger changes, choose **Create a new branch … and start a pull request** in step 3 instead of committing to `main`. GitHub then builds the site as a check on the pull request (it does not publish it). If the check is green, click **Merge pull request** to publish.

## Working on your own computer (optional)

Requires [Hugo extended](https://gohugo.io/installation/) (version in `hugoblox.yaml`), [Go](https://go.dev/dl/) and [Node.js](https://nodejs.org) with pnpm.

```sh
pnpm install
hugo server   # preview at http://localhost:1313
```

Then commit and push to `main`. RStudio/blogdown is no longer needed.

## How publishing works

`.github/workflows/deploy.yml` runs on every push to `main`: it installs the Hugo version pinned in `hugoblox.yaml`, builds the site, and deploys it to GitHub Pages. This requires **Settings → Pages → Build and deployment → Source: GitHub Actions** in the repository settings.
