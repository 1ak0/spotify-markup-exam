# Spotify Home Page - Markup Exam

Spotify-inspired Home page built with semantic HTML5 and a modular SCSS architecture.
Individual project for the 10X Markup exam (HTML, CSS, Sass, Git/GitHub).

**Live demo:** _add your GitHub Pages link here_

## What is built

- **Sidebar** with 10 navigation items (icon + text) and an active state
- **Top header** with Home / Discover / Search and a group of action icons
- **Filter chips** row (All, Music, Podcasts, Audiobooks)
- **Made For You** section with 8 clickable cards in a horizontal row
- **Fixed bottom player** split into left (track info), center (controls + progress) and right (actions + volume)

## Tech

| Category   | Technology                                   |
| ---------- | -------------------------------------------- |
| Structure  | HTML5 (semantic markup)                      |
| Styling    | SCSS (Sass), CSS Grid, Flexbox               |
| Workflow   | Git, GitHub (step-by-step commits)           |

## Project structure

```plaintext
index.html
favicon.ico
src/scss
├── abstracts   # _variables.scss, _mixins.scss
├── base        # _reset.scss, _globals.scss, _typography.scss
├── components  # _buttons, _icon-button, _filter-chips, _cards
├── layout      # _page, _sidebar, _header, _player
├── pages       # _home
└── main.scss   # entry point, imports every partial
dist
├── css/style.css   # compiled output
└── assets          # img, icons, fonts
```

## SCSS highlights

- 50+ design tokens in `_variables.scss` (colors, spacing, radius, typography, layout sizes, breakpoints)
- Mixins: `flex-center`, `flex-between`, `truncate`, `tablet`, `laptop`, `focus-ring`
- Mobile-first breakpoints, BEM-style class names (`card__title`, `filter-chip--active`)
- Nesting never deeper than 3 levels

## Build

Install Sass once, then compile:

```bash
npm install -g sass
sass src/scss/main.scss dist/css/style.css --watch
```

Open `index.html` in a browser (or use Live Server).

## Responsive behavior

| Width      | Layout                                                              |
| ---------- | ------------------------------------------------------------------- |
| < 1200px   | One column, sidebar hidden, compact player (track info + play)      |
| >= 1200px  | Sidebar + main column, full three-zone fixed bottom player          |

## Git workflow

Work is committed in small, meaningful steps using the `feat:`, `fix:`, `refactor:`, `build:` and `docs:` prefixes.

## Notes

Educational project. Not affiliated with Spotify AB.