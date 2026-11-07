# Zhenglan (Tank) Jiang

A compact academic homepage with three sections: Home, Selected Work, and Education. Contact information is in the footer.

- Website: https://tankkkjiang.github.io/
- Google Scholar: https://scholar.google.com/citations?user=oLE5jScAAAAJ&hl=en
- GitHub: https://github.com/tankkkJiang
- Email: jiangzhlan@mail2.sysu.edu.cn

## Project Structure

```text
index.html    Biography, profile links, publications, education, and email
styles.css    Responsive layout, typography, and colors
site.js       Mobile navigation and citation copying
media/        Portrait, publication media, and favicon
.nojekyll     Serve the site directly without a Jekyll build
```

This site has no build step, package installation, external fonts, or tracking scripts. All content is in English. Publications and citations remain accessible without JavaScript.

## Local Preview

From the repository directory:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000/ and press Ctrl+C in the terminal to stop the preview.

## Edit Content and Media

Edit `index.html` to update the biography, profile links, publications, or education.

The homepage uses `media/portrait.jpg`. Each publication uses one representative image, GIF, or video. The current paper uses `media/counter-uav.png`. See [media/README.md](media/README.md) for the media interface and examples.

To add another publication, duplicate the `<article class="publication-card">` block and update its content, media, and BibTeX. The citation copy button is initialized automatically for each publication.

## Commit and Publish

The original `origin` remote points to `tankkkJiang/tankkkJiang.github.io`. In GitHub, Pages should use **Deploy from a branch → main → / (root)**.

```sh
git status
git diff
git add index.html styles.css site.js media README.md .nojekyll .gitignore
git commit -m "Update academic homepage"
git push origin main
```

If authentication is required, use [GitHub CLI](https://cli.github.com/) with a browser login:

```sh
gh auth login --hostname github.com --git-protocol https --web
gh auth setup-git --hostname github.com
gh auth status
```

## Publication Sources

The paper's title and author order were checked against the [official ICASSP 2026 program](https://www.cmsworkshops.com/ICASSP2026/view_paper.php?PaperNum=13692&bare=1). The DOI and pages were checked against the [publisher-deposited Crossref record](https://api.crossref.org/works/10.1109/ICASSP55912.2026.11461509).

The portrait and paper framework figure were supplied by the site owner.
