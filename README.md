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
# PizzaPulse

PizzaPulse is a small, responsive static landing page prototype for a pizza delivery app. It's built with plain HTML, CSS, and a bit of client-side JavaScript (no backend). Use it as a visual prototype, experiment with layouts, or wire the forms and order buttons to a backend later.

Quick highlights
- Responsive header with mobile hamburger menu
- Hero section with hero image (in `images/`)
- Features, Menu preview, How it works, CTA banner, Contact form, and Footer
- Small client-side scripts: mobile nav toggle, smooth scrolling, contact form demo handler

---

## Preview (local)

Recommended: serve locally so relative URLs and images behave correctly.

PowerShell (from the project folder):

```powershell
Set-Location 'D:\Tasks\level1_task1'
# If you have Python 3 installed
python -m http.server 8000
# Open http://localhost:8000 in your browser
```

Or simply open `index.html` in a browser for a quick look (some features like relative image loading or anchors work better when served).

---

## What is in this repo

- `index.html` — main landing page markup. Sections are commented (hero, features, menu, how, cta, contact, footer).
- `style.css` — main stylesheet with responsive rules and component styles.
- `images/` — image assets used by the hero and menu preview.

Images currently included (file names exactly as in the project):

- `images/pizzaImage.avif` (hero background)
- `images/Margherita.jpg`
- `images/Pepperoni Classic.jpg`
- `images/Garden Veggie.jpg`

Note: the menu item `src` attributes in `index.html` reference these exact filenames. If you replace images, keep the names or update the `src` in `index.html`/`style.css`.

---

## Important behaviors (what the code does)

- Mobile navigation: the hamburger toggles a `nav-open` class on the header and updates `aria-expanded`. CSS controls the dropdown layout.
- Smooth scrolling: `document.documentElement.classList.add('smooth-scroll')` enables CSS `scroll-behavior`. Anchor clicks close the mobile nav and use `scrollIntoView({behavior:'smooth'})` as a fallback.
- Contact form: demo handler intercepts the submit event, shows an alert and resets the form. There is no server-side processing.
- Prices in the menu preview are shown in INR (₹) in `index.html` as static values.

---

## Quick customizations

- Change the hero image: replace `images/pizzaImage.avif` or update the `background-image` URL in `style.css` (look for `.hero` rules).
- Replace a menu image: swap the files in `images/` (e.g. replace `Margherita.jpg`) or update the `src` attributes in `index.html`.
- Edit copy: open `index.html` and modify the section you want — sections are separated with HTML comments for convenience.

If you want to wire the contact form to a backend or turn the 'Add' buttons into a working cart, I can add a small Node/Express example or a serverless function.

---

## Git & GitHub (quick commands)

If you haven't already created a remote repository, you can create one manually on GitHub or use the `gh` CLI. This repo's suggested remote URL (based on the repo owner in the workspace) is:

`https://github.com/AdinathJabade/PizzaPulse.git`

PowerShell example to push (replace remote URL if different):

```powershell
Set-Location 'D:\Tasks\level1_task1'
git init            # only if the repo isn't already initialized
git add .
git commit -m "Add PizzaPulse landing page"
git remote add origin https://github.com/AdinathJabade/PizzaPulse.git
git branch -M main
git push -u origin main
```

Using `gh` (GitHub CLI):

```powershell
Set-Location 'D:\Tasks\level1_task1'
gh auth login
gh repo create PizzaPulse --public --source=. --remote=origin --push
```

---

## Publish via GitHub Pages

1. Push your `main` branch to GitHub.
2. On GitHub, go to Settings → Pages and select branch `main` and folder `/ (root)` and save.
3. Your site will be available at `https://AdinathJabade.github.io/PizzaPulse/` (it may take a minute to publish).

---

## Next steps / suggestions

- Replace emoji icons with small SVG icons for a more polished look.
- Add a simple client-side cart and persist to localStorage; then add a small API (Node/Express or serverless) to accept orders.
- Optimize images (WebP/AVIF) and add `loading="lazy"` for menu item `<img>` tags.

If you want, I can make any of the above changes and commit them for you.

---

## License

Add a LICENSE file to declare terms (MIT recommended for open source). This repo currently contains no explicit license — add one if you plan to publish.

---

If you'd like, tell me which short project description you prefer for the GitHub repository metadata and I will insert it at the top of this README or prepare a commit with that short blurb.
