# Spotify Home Page - Markup Exam

Spotify-inspired Home page built with semantic HTML5 and a modular SCSS architecture.
Individual project for the 10X Markup exam (HTML, CSS, Sass, Git/GitHub).

## Structure

```plaintext
index.html
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

## Build

```bash
sass src/scss/main.scss dist/css/style.css --watch
```

## Layout

| Width      | Behavior                                                  |
| ---------- | --------------------------------------------------------- |
| < 1200px   | One column, sidebar hidden, compact player (track + play) |
| >= 1200px  | Sidebar + main column, full 3-zone fixed bottom player    |

Not affiliated with Spotify AB. Educational project.
