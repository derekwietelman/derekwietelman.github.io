# derekwietelman.github.io

Source for my academic website, https://derekwietelman.github.io.

The site is built with [Hugo](https://gohugo.io) and the [Hugo Blox](https://hugoblox.com) academic theme. **GitHub builds and publishes it automatically**: every change saved to the `main` branch rebuilds the site in about 1–3 minutes. Nothing needs to be built on your computer, and there is no `public` folder to copy.

## Where things live

The site has four pages plus a page for each paper. The top menu is Home · Bio · CV · Research · Contact.

| What you want to change | File |
| --- | --- |
| Homepage: short bio and its footnote | `content/_index.md` (under `text:`) |
| Bio page: longer bio and its photos | `content/bio.md`; photos in `assets/media/bio/` |
| Research page: the two paper lists (headings, which papers go where) | `content/research.md` |
| Contact page: address, email, profile links, photo and caption | `content/contact.md`; photo in `assets/media/contact/` |
| A paper (title, authors, date, status, abstract, links) | `content/publications/<paper>/index.md` |
| Name and the role under it ("Economist") | `data/authors/me.yaml` |
| Profile photo | `assets/media/authors/me.jpg` |
| Top menu links | `config/_default/menus.yaml` |
| PDFs (CV, papers) | `static/files/` (served at `/files/<name>.pdf`) |
| Labels such as "Working Paper" and "Peer-Reviewed Publication" | `i18n/en.yaml` |
| Colors (navy with CU Gold accents), text sizes and spacing | `assets/css/custom.css` |
| Site name, description for search engines, footer | `config/_default/params.yaml` |

Files under `layouts/` change how the theme builds pages (for example, paper pages without share buttons or an author card). Each one has a comment at the top saying what it changes.

## Making changes on github.com (no software needed)

1. Open the file on github.com and click the pencil icon (**Edit this file**).
2. Make your change.
3. Click **Commit changes…**, write a short note (e.g. "Update CV"), keep **Commit directly to the `main` branch** selected, and click **Commit changes**.
4. Wait 1–3 minutes, then reload the site (hard refresh: Ctrl+Shift+R on Windows, Cmd+Shift+R on Mac).
5. To check progress, open the **Actions** tab: a green check means the site is live; a red ✗ means the build failed and the previous version of the site stays up. Click the failed run to see the error, or ask Claude to fix it.

### Common tasks

**Update your CV.** In `static/files/`, click **Add file → Upload files**, upload the new PDF named exactly `cv.pdf` (it replaces the old one), and commit. The menu's CV link and the homepage's Download CV button both point to `/files/cv.pdf`.

**Change a paper's status** (e.g. a working paper gets accepted). Edit `content/publications/<paper>/index.md`:
- Working paper status line: `publication: R&R, *Journal of the Association of Environmental and Resource Economists*` (text between `*` is italic).
- Once published, move it to the Peer-Reviewed Publications list by changing `publication_types` to `article-journal`, setting `date` to the issue's month, and giving the journal details, e.g.
  ```yaml
  date: '2026-03-01T00:00:00Z'
  publication_types:
  - article-journal
  publication:
    name: Journal of the Association of Environmental and Resource Economists
    volume: 'Vol. 13'
    issue: 2
    pages: '345–378'
  hugoblox:
    ids:
      doi: 10.1086/123456
  ```

**Add a new paper.**
1. Upload the PDF to `static/files/`.
2. In `content/publications/`, click **Add file → Create new file** and name it `<short-name>/index.md` (e.g. `lead/index.md`).
3. Copy the contents of an existing paper's `index.md` (e.g. `content/publications/bbr/index.md`), then edit the title, authors (use `me` for yourself), date, status, abstract and PDF link.
4. `publication_types: [article]` puts it under **Working Papers**; `[article-journal]` puts it under **Peer-Reviewed Publications**. Both lists are on the Research page, newest first by `date`.

**Edit your bio.** The homepage bio is under `text:` in `content/_index.md`; the Bio page's longer bio is under `text:` in `content/bio.md` (its opening comment explains where photos go). Keep the indentation (spaces) exactly as it is—YAML is sensitive to it.

## Previewing changes before they go live (optional)

For bigger changes, choose **Create a new branch … and start a pull request** in step 3 instead of committing to `main`. GitHub then builds the site as a check on the pull request (it does not publish it). If the check is green, click **Merge pull request** to publish.

## Working on your own computer (optional)

Requires [Hugo extended](https://gohugo.io/installation/) (version in `hugoblox.yaml`), [Go](https://go.dev/dl/) and [Node.js](https://nodejs.org) with pnpm.

```sh
pnpm install
hugo server   # preview at http://localhost:1313
```

Then commit and push to `main`.

## How publishing works

`.github/workflows/deploy.yml` runs on every push to `main`: it installs the Hugo version pinned in `hugoblox.yaml`, builds the site, and deploys it to GitHub Pages. This requires **Settings → Pages → Build and deployment → Source: GitHub Actions** in the repository settings.
