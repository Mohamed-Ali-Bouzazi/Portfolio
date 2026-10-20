# Mohamed Ali Bouzazi | Portfolio (HTML + CSS only)

Personal portfolio of **Mohamed Ali Bouzazi**, embedded & mobile systems / IoT student.
This version is built with **plain HTML and CSS only: no JavaScript, no framework, no build step.**

🌐 Live site: [https://mohamed-ali-bouzazi.github.io](https://mohamed-ali-bouzazi.github.io/Portfolio/)

---

## ✨ Features

- **Single-page layout** with sections: Hero, About, Skills, Experience, Projects, Education & more, Contact
- **Bilingual (EN / FR)**: a toggle in the navbar switches the whole page between English and French
- **Responsive**: works on desktop, tablet and phone, with a hamburger menu on small screens
- **Automatic light / dark theme**: follows the visitor's system preference
- **Fade-in animation** on load (disabled for visitors who prefer reduced motion)
- **Zero dependencies** besides the Google Fonts stylesheet (Inter and JetBrains Mono)

## 📁 Project structure

```
.
├── index.html   # all page content (English + French)
├── style.css    # all styling, theming, responsiveness and the no-JS toggles
└── README.md
```

## 🧠 How it works without JavaScript

| Feature | CSS technique |
|---|---|
| **Language toggle** | A hidden checkbox (`#lang-toggle`) controlled by the `FR / EN` label. Every translatable element contains `<span class="en">` and `<span class="fr">`. When the checkbox is checked, `body:has(#lang-toggle:checked)` hides `.en` and shows `.fr`. |
| **Mobile menu** | A hidden checkbox (`#menu-toggle`) controlled by the hamburger label. `body:has(#menu-toggle:checked) .links` expands the menu. |
| **Fade-in** | A `@keyframes fadeUp` animation applied to `.reveal` sections. |
| **Light / dark theme** | CSS variables on `:root`, overridden in `@media (prefers-color-scheme: light)`. |
| **Smooth scrolling** | `scroll-behavior: smooth` plus `scroll-padding-top` for the fixed navbar. |

### Trade-offs compared with a JavaScript version

- The chosen language is **not remembered**; the page returns to English on reload.
- On phones the menu **stays open after tapping a link**; tap the hamburger again to close it.
- The fade-in plays **once at page load**, not as each section scrolls into view.
- The footer year is written directly in `index.html`.

## 🚀 Run locally

No installation needed. Open `index.html` in your browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## 🌍 Deploy on GitHub Pages

1. Create a **public** repository named `Mohamed-Ali-Bouzazi.github.io`.
2. Upload `index.html`, `style.css` and `README.md` to the repository root.
3. Go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. Your site will be live at `https://mohamed-ali-bouzazi.github.io` within a couple of minutes.

## 🛠️ Customize

- **Text and links**: edit `index.html`. Each translatable element has an English `<span class="en">` and a French `<span class="fr">`; update both.
- **Colors**: change the variables at the top of `style.css` (`--accent`, `--accent2`, `--bg`, `--card`, ...).
- **Add a project**: duplicate an `<article class="card project">` block in the Projects section.
- **Add a skill**: add a `<span>` inside the matching `.chips` container.

## 🌐 Browser support

Requires a browser that supports the CSS `:has()` selector (Chrome/Edge 105+, Safari 15.4+, Firefox 121+). In older browsers the page still displays in English, but the language toggle and mobile menu will not work.

## 📬 Contact

- GitHub: [Mohamed-Ali-Bouzazi](https://github.com/Mohamed-Ali-Bouzazi)
- LinkedIn: [mohamed-ali-bouzazi](https://www.linkedin.com/in/mohamed-ali-bouzazi-b42576317/)
- Email: bouzazimohamedali31@gmail.com
