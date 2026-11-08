# Lógos design review

Lógos uses the Academia palette as a hierarchy of materials. Limestone anchors
the desktop. The deeper stone shade groups navigation, and warm paper marks
areas where the user reads or works. Ink carries text. Terracotta identifies
the current location and active controls, while mineral blue and olive separate
commands and values in the terminal.

## Palette and surfaces

| Role | Color | Main uses |
| --- | --- | --- |
| Limestone | `#F1E9DA` | Terminal background, shell and window base |
| Stone | `#E7DDCC` | Files sidebar and breadcrumb surface |
| Warm paper | `#F9F3E8` | File canvas, cards, menus |
| Ink | `#282922` | Primary text and icons |
| Secondary ink | `#5D5549` | Muted terminal text |
| Terracotta | `#8B452F` | Active location, controls, focus color |
| Sand | `#DCCCB9` | File and terminal selections |
| Mineral blue | `#32536A` | Terminal blue and commands |
| Olive | `#446049` | Terminal green, values and success |

## Interface details

- **Files** uses a stone sidebar and a lighter file canvas to separate
  navigation from content. The breadcrumb names the current folder in
  terracotta. Selected files use a sand fill with ink text. Yaru Warty Brown
  ties the folder icons to the warm palette. Nautilus retains its own layout,
  controls, and keyboard interactions.
- **Terminal** keeps the limestone background and distinct ANSI hues for
  warnings, errors, success, links, and syntax. Secondary ink was deepened so
  small text remains readable against both the base and selection.
- **Shell and window borders** use Omarchy's templates from `colors.toml`.
  Terracotta marks the active window and controls. Neutral surfaces leave
  room for the artwork.
- **Typography and artwork** use GFS Neohellenic Bold for the Greek wordmark in
  the preview. The desktop typography follows the user's existing settings.
  Both original artworks are available as wallpapers.

The Files stylesheet scopes Adwaita's CSS variables to Nautilus windows.
See the [libadwaita CSS variable reference](https://gnome.pages.gitlab.gnome.org/libadwaita/doc/main/css-variables.html).
When adjusting the palette, update the corresponding values in
`nautilus.css` alongside `colors.toml`.

## Contrast checks

These are sRGB contrast ratios for solid colors, rounded to one decimal. They
describe the palette pairings used in the theme.

| Pair | Ratio |
| --- | ---: |
| Ink on limestone | 12.2:1 |
| Ink on warm paper | 13.3:1 |
| Ink on sand selection | 9.4:1 |
| Terracotta on warm paper | 6.4:1 |
| Terracotta on stone | 5.2:1 |
| Secondary ink on limestone | 6.1:1 |
| Secondary ink on sand selection | 4.7:1 |

The twelve normal and bright ANSI hues have a minimum contrast ratio of
5.0:1 on limestone.
