# NUS RIDGE Lab — Website

A clean, modern, static website for the NUS RIDGE Lab — Research in
Intelligence, Databases, Generation, and mEdia (NUS School of Computing).
No build step, no dependencies — just HTML + CSS + a tiny bit of JS.
Ready to deploy on GitHub Pages.

## Pages

| File                | Purpose                                              |
|---------------------|------------------------------------------------------|
| `index.html`        | Home — hero, about the PI, research highlights, news |
| `research.html`     | Research areas + current projects                    |
| `people.html`       | PI, postdoc, PhD/MSc students, visiting, alumni      |
| `publications.html` | Publications (placeholder entries to fill in)        |
| `news.html`         | News feed + "Join the lab" info                      |
| `contact.html`      | Contact details + map                                |

Shared assets: `css/style.css` (Academic Blue theme), `js/main.js` (mobile nav).

## Editing tips

- **Lab name:** search-and-replace `NUS RIDGE Lab` across the `.html` files.
- **Theme colors:** edit the `:root` variables at the top of `css/style.css`
  (e.g. `--accent` for the blue).
- **Photos:** add images to `assets/people/`, then replace the initials inside
  an `.avatar` / `.about-photo` div with `<img src="assets/people/NAME.jpg" alt="Name">`.
- **Publications:** replace the placeholder `<li class="pub-item">` entries.
- **News:** add/remove `<li class="news-item">` entries in `news.html` / `index.html`.

## Deploy to GitHub Pages

### Option A — project site (`username.github.io/repo`)
```bash
git init
git add .
git commit -m "Initial lab website"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```
Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
select `main` / `/ (root)`, save. Site appears at `https://USERNAME.github.io/REPO/`.

### Option B — user/org site (`username.github.io`)
Name the repo exactly `USERNAME.github.io` and push the same files; it serves at
`https://USERNAME.github.io/`.

> `.nojekyll` is included so GitHub Pages serves all files as-is without Jekyll processing.

## Local preview
```bash
python3 -m http.server 8000
# open http://localhost:8000
```
