# Naga Varshini — Portfolio

A single-page, animated dark-tech portfolio built with plain HTML, CSS, and JavaScript — no build tools or frameworks required.

**Live file:** `index.html`


## Features

- **Animated hero** — typing terminal effect that types out a tagline character by character
- **Particle network background** — an HTML5 canvas animation with connected particles that react to mouse movement
- **Scroll-reveal animations** — sections fade and slide into view as you scroll, using `IntersectionObserver`
- **Hover micro-interactions** — glowing project cards, lifting skill tags, pulsing timeline dots
- **Fully responsive** — adapts down to mobile screen sizes
- **Respects reduced motion** — animations are disabled for users with `prefers-reduced-motion` enabled
- **Zero dependencies** — one HTML file, Google Fonts loaded via CDN, everything else is vanilla CSS/JS

## File Structure

```
index.html   → everything: markup, styles, and scripts in one file
```

## How to View It

Just double-click `index.html`, or open it directly in any modern browser. No server or install step needed.

## How to Deploy It

Any static hosting service works since there's no build step:

**Vercel**
1. Create a new project, drag and drop the folder containing `index.html`, or connect a GitHub repo.
2. Vercel auto-detects it as a static site and deploys it.

**GitHub Pages**
1. Push `index.html` to a GitHub repository.
2. In the repo settings, enable GitHub Pages and point it at the branch/folder containing the file.

**Netlify**
1. Drag and drop the folder onto [app.netlify.com/drop](https://app.netlify.com/drop).

## How to Customize

| What to change | Where to look |
|---|---|
| Name, tagline, hero text | `<section class="hero">` |
| Typing effect text | `const line = "..."` near the bottom `<script>` |
| About text & stats | `<section id="about">` |
| Skills | `<section id="skills">` — each `.skill-card` |
| Work experience | `<section id="experience">` — each `.tl-item` |
| Projects | `<section id="projects">` — each `.project-card` |
| Certifications & achievements | `<section id="more">` |
| Contact links / email | `<footer id="contact">` |
| Color palette | CSS variables at the top of `<style>` (`--bg`, `--cyan`, `--violet`, etc.) |
| Fonts | `<link>` tag in `<head>` and `--font-display` / `--font-body` / `--font-mono` variables |
| Particle animation behavior | `<script>` section — the `particles`, `initParticles()`, and `draw()` functions |

## Notes

- The particle count scales with screen size, so it stays smooth on smaller devices.
- All external links (GitHub, LinkedIn, email) are already wired to the details from the resume — update them if these change.
- To add a resume PDF download or profile photo, drop the file into the same folder and reference it with a relative path (e.g. `<img src="photo.jpg">` or `<a href="resume.pdf" download>`).
