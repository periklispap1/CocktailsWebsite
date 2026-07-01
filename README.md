# Velvet Pour Cocktails Website

Responsive cocktail bar website built with React, Vite, Tailwind CSS, and GSAP. The site uses scroll-based animation, split text reveals, a video-scrubbed hero, parallax leaves, an animated cocktail menu, and a polished contact section.


## Features

- Animated hero section with GSAP text reveals and scroll-scrubbed video
- Cocktail and mocktail list section with parallax leaf motion
- About section with animated heading and responsive image grid
- Art section with pinned ScrollTrigger mask reveal
- Interactive cocktail menu slider
- Responsive navigation and section spacing
- Contact/footer section with store details and social links

## Tech Stack

- React 19
- Vite 8
- Tailwind CSS 4
- GSAP 3 with ScrollTrigger and SplitText
- react-responsive
- Oxlint

## Getting Started

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Build for production:

```bash
npm run build
```

Preview the production build:

```bash
npm run preview
```

Run linting:

```bash
npm run lint
```

## Project Structure

```text
cocktails-website/
|-- constants/              # Navigation, menu, contact, and list data
|-- public/
|   |-- fonts/              # Custom display font
|   |-- images/             # Site imagery and UI assets
|   |-- readme/             # README preview images
|   `-- videos/             # Hero video assets
|-- src/
|   |-- components/         # Page sections and navigation
|   |-- App.jsx             # Main section composition
|   |-- index.css           # Tailwind theme and section styles
|   `-- main.jsx            # React entry point
`-- package.json
```

## Main Sections

The page is composed in `src/App.jsx`:

- `Navbar`
- `Hero`
- `Cocktails`
- `About`
- `Art`
- `Menu`
- `Contact`

## Animation Notes

GSAP plugins are registered in `src/App.jsx`:

```js
gsap.registerPlugin(ScrollTrigger, SplitText);
```

Most animation setup lives inside the relevant section component with `useGSAP`. Section-specific styles and layout rules live in `src/index.css`.

The hero video currently uses:

```text
public/videos/output-scroll.mp4
```

Local FFmpeg downloads or extracted binaries should stay out of git. The `tools/` directory is ignored for that reason.

## Deployment

The production build is generated into `dist/`:

```bash
npm run build
```

Deploy the generated `dist/` folder to any static hosting provider.
