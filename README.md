# Lógos

A light theme for Omarchy Quattro inspired by Greek philosophy and the painted
architecture of Raphael's *School of Athens*. The Academia palette pairs
limestone and warm paper with ink, terracotta, mineral blue, and olive.

![Lógos with the Academia palette applied to Alacritty and Nautilus](preview.png)

The preview combines real Alacritty and Nautilus captures from an isolated
session with a sample folder and Raphael's fresco.

## Installation

Copy the theme folder to `~/.config/omarchy/themes/logos/`, then run:

```sh
omarchy theme set logos
```

Omarchy uses the palette for the shell, window borders, terminal, and other
supported apps. Use `omarchy theme bg next` to switch between the two wallpapers.

### Nautilus (GNOME Files)

The theme includes a separate GTK 4 stylesheet for Nautilus. From the Lógos
repository, register the theme hook and reapply the theme:

```sh
omarchy hook install theme-set ./hooks/logos-nautilus
omarchy theme set logos
```

Quit and reopen Files if it was running. The hook activates the stylesheet when
Lógos is selected and clears it on other themes. It adds one import to the GTK 4
user stylesheet and preserves existing CSS. The theme selects the
`Yaru-wartybrown` icon set included with Omarchy.

To remove the integration, delete the `logos-nautilus` hook from
`~/.config/omarchy/hooks/theme-set.d/`, remove the
`@import url("logos-nautilus.css");` line from the GTK 4 user stylesheet, and
remove its sibling `logos-nautilus.css`. Reopen Files to reload its styles.

## Design

See the [palette, surface mapping, and contrast review](DESIGN.md). The **ΛΟΓΟΣ**
wordmark in the preview uses **GFS Neohellenic Bold** by the Greek Font Society.
The [font](fonts/GFSNeohellenicBold.ttf) is included under the
[SIL Open Font License 1.1](fonts/OFL.txt). Interface and terminal fonts follow
the user's Omarchy settings.

## Artwork and inspiration

- [Pathos by Haflier](https://github.com/Haflier/omarchy-pathos-theme),
  inspiration for a desktop theme about philosophy.
- [*The School of Athens* by Raphael](https://commons.wikimedia.org/wiki/File:Raphael_School_of_Athens.jpg),
  a public-domain reproduction from Wikimedia Commons, 3697 × 2414.
- [*The Death of Socrates* by Jacques-Louis David](https://www.metmuseum.org/art/collection/search/436105),
  a public-domain reproduction from The Metropolitan Museum of Art, 4000 × 2663.
