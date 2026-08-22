# renjieshao.com — personal site

Plain HTML + CSS, no build step. Edit the files, commit, push — GitHub Pages
redeploys in about 30 seconds.

## What's where

| File | What it holds |
|---|---|
| `index.html` | Everything on the front page: bio, experience, publications |
| `xiuxiu.html` | Xiuxiu's page |
| `styles.css` | All the styling (colors, fonts, spacing, dark mode) |
| `assets/` | Photos |
| `CNAME` | Your custom domain (add this once you buy the domain) |
| `.nojekyll` | Tells GitHub not to run Jekyll on the files. Leave it alone. |

## Common edits

**Add your first paper.** Open `index.html`, find the big commented-out
`PUBLICATIONS` block, delete the `<!--` and `-->` around it, and fill in the
details. Copy the `<li>...</li>` once per paper.

**Add a photo of Xiuxiu.** Put the file in `assets/`, then in `xiuxiu.html`
copy the commented `<figure>` block, uncomment it, and point `src` at your file.

**Add an experience entry.** In `index.html`, copy an existing `<li>` inside
`<ul class="entries">` and change the date and text.

**Change a color or font.** Everything lives in the `:root` block at the top of
`styles.css`. The second block, `@media (prefers-color-scheme: dark)`, is the
dark-mode version of the same colors.

## Preview locally before pushing

```bash
cd path/to/this/folder
python3 -m http.server 8000
```

Then open http://localhost:8000 in a browser. Ctrl+C to stop.

## Publish a change

```bash
git add .
git commit -m "describe what changed"
git push
```
