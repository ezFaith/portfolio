# Dipankar Saha | Portfolio

Personal portfolio of an IT and cybersecurity professional: systems administration, networking, SIEM and machine-learning intrusion detection.

**Live site:** https://ezfaith.github.io/portfolio/

## What's on the site

- **Hero:** a typed role line and a live panel that switches between a simulated intrusion-detection log and a simulated infrastructure status board
- **About:** how IT operations and security work fit together
- **Experience:** IT Executive and Cybersecurity Intern
- **Projects:**
  - ML Network Intrusion Detection (autoencoder on CICIDS2017, Streamlit dashboard, live demo)
  - Windows Server and Active Directory homelab
  - Educational ransomware simulation
  - Image steganography tool
  - Mental health chatbot
- **Skills:** six groups, split evenly between IT (systems, networking, cloud and scripting) and security (detection, testing, frameworks)
- **Education and contact**

## Features

- Dark and light themes, following the system setting by default and remembered after the visitor switches
- 3D particle background (Three.js) that reacts to the mouse and scroll, with floating colour blobs and a cursor glow
- Scroll progress bar, staggered reveal animations and count-up metrics
- Fully responsive from 320px phones to ultrawide monitors, with no horizontal overflow
- Icons are inlined SVG, so nothing depends on an external icon library
- Accessible by default: skip link, visible focus states, semantic landmarks, and `prefers-reduced-motion` support
- Touch-friendly: hover effects only run on devices that have a pointer

## Tech

Plain HTML, CSS and JavaScript in a single file. There is no build step, framework or package manager.

| Part | Source |
|---|---|
| 3D particles | [Three.js](https://threejs.org/) r128 from cdnjs |
| Fonts | Chakra Petch, IBM Plex Sans and JetBrains Mono from Google Fonts |
| Icons | Hand-inlined SVG, drawn in the style of [Lucide](https://lucide.dev/) (ISC licence) |

If the CDN scripts or fonts fail to load, the page still works. It falls back to system fonts and a static background.

## Project structure

```
portfolio/
├── index.html   # the whole site: markup, styles and scripts
└── README.md
```

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

The site is hosted with GitHub Pages:

1. Push `index.html` to the `main` branch.
2. In the repo, go to **Settings → Pages**.
3. Set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. The site goes live at `https://<username>.github.io/<repo>/`.

## Customising

Everything lives in `index.html`:

- **Colours and fonts:** the CSS variables at the top of the `<style>` block (`--accent`, `--accent2`, `--bg`, `--display`, and so on). Dark and light values are set separately.
- **Content:** each section is plain HTML. Project cards are `<article class="glass proj">` blocks.
- **Hero typing line:** the `roles` array in the script.
- **Simulated panels:** the `rows` array (infrastructure) and the `line()` function (security log). Both are labelled as simulated on the page.
- **Icons:** add a `<symbol>` to the SVG sprite at the top of `<body>`, then use it with `<svg class="i"><use href="#i-name"/></svg>`.

## Browser support

Current versions of Chrome, Edge, Firefox and Safari, on desktop and mobile.

## Licence

The code is free to use as inspiration. The text, project descriptions and personal details are mine, so please don't republish them as your own.

## Contact

- Email: dsaha0427@gmail.com
- LinkedIn: https://linkedin.com/in/dipankarsaha2001
- GitHub: https://github.com/ezFaith
