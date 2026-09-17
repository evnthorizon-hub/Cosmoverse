# CosmoVerse Navigation Structure

## Main Navigation (Current Implementation)

All ten links ship on every page, in this order. The order is the region order
used by the homepage index — outward by distance — with Exoplanets kept next to
Missions in the bar because the bar is chrome and reads better with the two
shortest labels adjacent.

```
Home          → index.html
Solar System  → solar-system/index.html
Stars         → stars/index.html
Black Holes   → black-holes/index.html
Galaxies      → galaxies/index.html
Nebulae       → nebulae/index.html
Cosmic Events → cosmic-events/index.html
Missions      → missions/index.html
Exoplanets    → exoplanets/index.html
Universe      → universe/index.html
```

### Width budget

Ten links is 86 characters of label, which needs roughly 930px of the 1084px
gutter next to a 182px logo. That leaves no room for the old 2rem gap or 0.1em
tracking, so `style.css` sets the gap to `clamp(0.55rem, 1.15vw, 1.05rem)`,
tracking to `0.06em`, and `white-space: nowrap` on `.nav-link` — a label that
breaks the budget then overflows visibly instead of silently stacking onto a
second line.

Below **1120px** the bar becomes the drawer. That breakpoint moved up from 860px
when the tenth link was added; it lives in `style.css` and covers nav chrome
only, so the 860px breakpoints in `components.css` and the page stylesheets —
which are about figures and photographs — are unaffected.

### Not yet built

```
Observatories → observatories/index.html (future — not in the bar)
```

## Navigation Linking Strategy

### From Homepage (root level)

```html
<a href="index.html">Home</a>
<a href="solar-system/">Solar System</a>
<a href="stars/">Stars</a>
<a href="black-holes/">Black Holes</a>
<a href="galaxies/">Galaxies</a>
```

### From Category Pages (one level deep)

```html
<a href="../index.html">Home</a>
<a href="../solar-system/index.html">Solar System</a>
<a href="../stars/index.html">Stars</a>
<a href="../black-holes/index.html">Black Holes</a>
<a href="../galaxies/index.html">Galaxies</a>
<a href="../universe/index.html">Universe</a>
```

The page's own entry drops the relative prefix and takes the active state:

```html
<a href="index.html" class="nav-link active" aria-current="page">Universe</a>
```

### From Subcategory Pages (two levels deep)

```html
<a href="../../index.html">Home</a>
<a href="../../solar-system/">Solar System</a>
<a href="../../stars/">Stars</a>
<a href="../../black-holes/">Black Holes</a>
<a href="../../galaxies/">Galaxies</a>
```

### From Object Pages (three levels deep)

```html
<a href="../../../index.html">Home</a>
<a href="../../../solar-system/">Solar System</a>
<a href="../../../stars/">Stars</a>
<a href="../../../black-holes/">Black Holes</a>
<a href="../../../galaxies/">Galaxies</a>
```

## CSS Class Convention

### Active States

Each page should have its corresponding nav link marked with `.active` **and**
`aria-current="page"`. The active state is signalled two ways — a full-width accent
underline and a small tick above the label — so it is never communicated by colour
alone.

The accent colour of the underline, the tick and the hairline beneath the header all
come from the page's domain theme (see ARCHITECTURE.md → *The accent contract*), so
site chrome shifts hue to match whichever region the reader is inside.

```html
<!-- On home page -->
<a href="index.html" class="nav-link active">Home</a>

<!-- On solar-system pages -->
<a href="solar-system/" class="nav-link active">Solar System</a>

<!-- On stars pages -->
<a href="stars/" class="nav-link active">Stars</a>
```

## Breadcrumb Structure

### Category Page

```
Home > Solar System
```

### Subcategory Page

```
Home > Solar System > Planets
```

### Object Page

```
Home > Solar System > Planets > Jupiter
```

## Mobile Navigation

The mobile navigation uses the CSS checkbox hack:

```html
<input type="checkbox" id="mobile-menu-checkbox" class="mobile-menu-checkbox">
<label for="mobile-menu-checkbox" class="mobile-menu-toggle" aria-label="Toggle navigation menu">
    <span class="hamburger-line"></span>
    <span class="hamburger-line"></span>
    <span class="hamburger-line"></span>
</label>
```

Each page must have unique checkbox ID if multiple navigations exist on the same page.
