# PizzaPulse

Simple, responsive landing page for PizzaPulse — a pizza delivery demo (HTML + CSS, client-side JS).

This repository contains a static landing page prototype you can open locally or host on GitHub Pages. It includes a hero, feature cards, a menu preview, how-it-works steps, contact form (client-side), and a clean footer.

## Preview
- Open `index.html` in your browser (double-click) to view the page.
- Or serve locally (recommended) to avoid issues with relative URLs:

PowerShell (from the project folder):
```powershell
Set-Location 'D:\Tasks\level1_task1'
# if you have Python installed
python -m http.server 8000
# then open http://localhost:8000 in your browser
```

## Project structure
- `index.html` — main landing page
- `style.css` — all page styles
- `images/` — hero and menu item images (add your images here)

## Quick edits
- Change hero image: replace file `images/pizzaImage.avif` (or update `style.css` hero `background-image` url).
- Change a menu image: replace `images/margherita.jpg`, `images/pepperoni.jpg`, `images/garden-veggie.jpg` or update the `src` attributes in `index.html`.
- Update copy: edit `index.html` directly (text is in clear sections with comments).

### Recommended image names & sizes
- Hero: `images/pizza-hero.jpg` or `pizzaImage.avif` — ~1600–2400px wide for best results.
- Menu items: `images/margherita.jpg`, `images/pepperoni.jpg`, `images/garden-veggie.jpg` — ~800px wide and compressed (< 300KB recommended).

## Git & GitHub (quick)
Initialize and push your project to GitHub (PowerShell):

```powershell
Set-Location 'D:\Tasks\level1_task1'
git init
git add .
git commit -m "Initial commit - PizzaPulse landing page"
# create repo on GitHub.com first, then:
git remote add origin https://github.com/YOURNAME/PizzaPulse.git
git branch -M main
git push -u origin main
```

If you use GitHub CLI (`gh`):

```powershell
Set-Location 'D:\Tasks\level1_task1'
gh auth login
gh repo create PizzaPulse --public --source=. --remote=origin --push
```

## Publish with GitHub Pages
1. In your GitHub repo, go to Settings → Pages.
2. Choose branch `main` and root `/` and save. The site will become available at `https://<AdinathJabade>.github.io/PizzaPulse/`.

Or create a `gh-pages` branch and push the built site (for static HTML this is not necessary).

## Contact form & ordering
- The contact form and order buttons are client-side demo handlers (no backend). Use the scripts in `index.html` to see how they work. If you want, I can help wire them to a simple Node/Express endpoint or a serverless function.

## Next steps / suggestions
- Replace emoji icons with SVGs for polish.
- Add a simple cart and backend to accept orders.
- Optimize images (WebP/AVIF) and add lazy-loading for menu images.

## License
This project is provided as-is for learning and prototyping. Add a LICENSE file to declare terms (MIT recommended).

---
If you want, tell me your GitHub username and I’ll paste the exact `git` commands with your repo URL filled in, or I can create a `README` commit for you and push (if you give me the remote URL and confirm you want me to edit files).
