# CosmoVerse Architecture

## Vision

CosmoVerse is a comprehensive astronomy exploration and educational platform that combines curated educational content with structured astronomical data.

---

## Site Architecture

### Main Navigation (Level 1)

```
CosmoVerse
│
├── Home
├── Solar System
├── Stars
├── Black Holes
├── Galaxies
├── Nebulae
├── Exoplanets
├── Cosmic Events
├── Space Missions
├── Observatories
└── Universe
```

---

## Category Structure

### Solar System

```
solar-system/
│
├── Overview (index.html)
├── Sun/
│   └── index.html
├── Planets/
│   ├── index.html (Planet overview)
│   ├── mercury.html
│   ├── venus.html
│   ├── earth.html
│   ├── mars.html
│   ├── jupiter.html
│   ├── saturn.html
│   ├── uranus.html
│   └── neptune.html
├── Dwarf Planets/
│   ├── index.html
│   ├── pluto.html
│   ├── eris.html
│   ├── haumea.html
│   ├── makemake.html
│   └── ceres.html
├── Moons/
│   └── index.html
├── Asteroids/
│   └── index.html
├── Comets/
│   └── index.html
├── Kuiper Belt/
│   └── index.html
└── Oort Cloud/
    └── index.html
```

### Exoplanets

```
exoplanets/
│
├── Overview (index.html)
├── Discovery Methods/
│   └── index.html
├── Planet Types/
│   └── index.html
├── Habitable Worlds/
│   └── index.html
├── Notable Exoplanets/
│   └── index.html
└── Catalog/ (Future: database-driven)
    └── index.html
```

### Stars

```
stars/
│
├── Overview (index.html)
├── Classification/
│   └── index.html
├── Stellar Evolution/
│   └── index.html
├── Star Types/
│   ├── index.html
│   ├── red-dwarfs.html
│   ├── yellow-dwarfs.html
│   ├── red-giants.html
│   ├── blue-giants.html
│   ├── supergiants.html
│   ├── white-dwarfs.html
│   └── neutron-stars.html
├── Binary Stars/
│   └── index.html
├── Variable Stars/
│   └── index.html
├── Famous Stars/
│   └── index.html
└── Catalog/ (Future: database-driven)
    └── index.html
```

### Black Holes

```
black-holes/
│
├── Overview (index.html)
├── Formation/
│   └── index.html
├── Physics/
│   └── index.html
├── Types/
│   ├── index.html
│   ├── stellar-mass.html
│   ├── intermediate-mass.html
│   └── supermassive.html
├── Famous Black Holes/
│   └── index.html
└── Catalog/ (Future: database-driven)
    └── index.html
```

### Galaxies

```
galaxies/
│
├── Overview (index.html)
├── Formation/
│   └── index.html
├── Types/
│   ├── index.html
│   ├── spiral.html
│   ├── elliptical.html
│   ├── lenticular.html
│   └── irregular.html
├── Famous Galaxies/
│   └── index.html
└── Catalog/ (Future: database-driven)
    └── index.html
```

### Nebulae

```
nebulae/
│
├── Overview (index.html)
├── Types/
│   ├── index.html
│   ├── emission.html
│   ├── reflection.html
│   ├── dark.html
│   ├── planetary.html
│   └── supernova-remnants.html
└── Famous Nebulae/
    └── index.html
```

### Cosmic Events

```
cosmic-events/
│
├── Overview (index.html)
├── Supernovae/
│   └── index.html
├── Gamma-Ray Bursts/
│   └── index.html
├── Gravitational Waves/
│   └── index.html
└── Mergers/
    └── index.html
```

### Space Missions

```
missions/
│
├── Overview (index.html)
├── Human Spaceflight/
│   └── index.html
├── Robotic Missions/
│   └── index.html
├── Moon Missions/
│   └── index.html
├── Mars Missions/
│   └── index.html
├── Deep Space/
│   └── index.html
├── Space Telescopes/
│   └── index.html
└── Notable Missions/
    ├── voyager.html
    ├── hubble.html
    ├── james-webb.html
    └── ...
```

### Observatories

```
observatories/
│
├── Overview (index.html)
├── Space Telescopes/
│   └── index.html
├── Ground-Based/
│   └── index.html
└── Major Observatories/
    └── index.html
```

### Universe

Built as a single overview page carrying nine sections, in the same pattern as
the other eight regions. The subsections below are the planned Level 2 / Level 3
expansion, not the current file layout.

```
universe/
│
├── Overview (index.html) ← built
│     01 What is the universe      06 Cosmic web
│     02 The Big Bang              07 Composition
│     03 Cosmic expansion          08 How we know
│     04 Observable universe       09 Ultimate fate + misconceptions
│     05 Cosmic timeline
│
├── Big Bang/            (future)
├── Cosmic Timeline/     (future)
├── Dark Matter/         (future)
├── Dark Energy/         (future)
├── Relativity/          (future)
└── Cosmology/           (future)
```

Figures 01–08: cosmic evolution cone, comoving expansion grid, Hubble diagram,
observable-scale rail, two-band timeline, cosmic web, composition bar, fate
curves.

---

## Information Levels

### Level 1: Explore

- Simple explanations for beginners
- Accessible language
- Visual-first approach
- Example: "What is a black hole?"

### Level 2: Learn

- Detailed scientific explanations
- Technical accuracy
- References and sources
- Example: "How does a stellar-mass black hole form?"

### Level 3: Discover

- Individual object pages
- Structured data presentation
- Scientific properties
- Example: "Sagittarius A* - Supermassive black hole"

---

## Page Types

### Category Page

- Hero with category introduction
- Overview content
- Subcategory navigation
- Featured/notable objects

### Object Page

- Object header (name, type, visual)
- Quick facts panel
- Detailed sections
- Discovery/exploration history
- Scientific significance
- Sources/references

### Educational Page

- Concept introduction
- Detailed explanation
- Visual aids
- Related topics
- Further reading

---

## Visual Direction

CosmoVerse should read as **cinematic, scientific, mysterious and premium** — an
observatory, not a dashboard.

Four rules produce that, and everything else follows from them.

### 1. Two voices, never mixed

| Voice | Font | Used for |
| --- | --- | --- |
| **Display** | sans, light weight, tight tracking, large | Wonder. Headlines, ledes, body prose. |
| **Instrument** | monospace, uppercase, wide tracking, tiny | Fact. Labels, units, classifications, figure numbers, coordinates, indices. |

Every measurement on the site is spoken in the instrument voice; every statement of
meaning is spoken in the display voice. Keeping them strictly separated is what makes
the site read as scientific rather than merely decorated. One lit word per heading
(`<em>`) carries the domain accent — never more than one.

### 2. Sections are altitudes, not boxes

A page is one continuous sky. Sections differ by how much light reaches them
(`.shell--void`, `--abyss`, `--atmos`, `--lit`, `--rise`), and every join is a lit
horizon (`.shell--seam`) rather than a hard edge. Light cools as the reader travels
outward, which gives a category page a physical direction.

### 3. Geometry carries the subject

No stock iconography and no generic ornament. Each subject gets a **field texture**
whose geometry *is* its physics — orbits are concentric, spectra are linear, lensing is
warped, galaxies rotate, bursts are radial, missions are drafted on grid paper. The same
logic drives the emblems.

### 4. Sharp, not soft

Minimal border radius, hairline rules, corner ticks, tabular figures. Large rounded
rectangles are the single strongest signal of a template, so CosmoVerse avoids them.
Cards are replaced by **observation plates**: one top hairline, an accent segment that
runs the width on hover, one corner tick.

---

## CSS Architecture

### File Structure

```
css/
│
├── style.css        # Layer 1 — tokens, reset, shell, starfield, home hero
├── components.css   # Layer 2 — the reusable cosmic visual language
└── <page>.css       # Layer 3 — page-specific visuals (e.g. solar-system.css)
```

Load order matters and is always the same:

```html
<link rel="stylesheet" href="css/style.css">
<link rel="stylesheet" href="css/components.css">
<link rel="stylesheet" href="css/solar-system.css">
```

### The accent contract

This is the mechanism that lets nine different subjects each have their own
personality while remaining one product. **No component hard-codes a colour for a
subject.** Every component reads only these variables:

```
--accent  --accent-2  --accent-deep  --accent-ink
--accent-glow  --accent-wash  --mood-high  --mood-low
--field-line  --field-opacity
```

A section takes on a personality by doing two things:

```html
<body class="dm-nebulae">
    <section class="shell shell--lit shell--seam">
        <div class="field field--emission" aria-hidden="true"></div>
        ...
    </section>
</body>
```

Headings, plates, readouts, rails, ledgers, chips, orbs, seams and nav underlines all
retune themselves automatically.

### Domain themes

Each palette is anchored to a real physical cue, so the colour is never arbitrary.

| Class | Subject | Anchor | Field texture |
| --- | --- | --- | --- |
| `.dm-solar` | Solar System | photosphere amber | `.field--orbital` |
| `.dm-planets` | Planets | reflected daylight blue | `.field--banded` |
| `.dm-stars` | Stars | H–R diagram: hot blue-white ↔ cool amber | `.field--spectral` |
| `.dm-holes` | Black Holes | accretion orange + lensing violet on true black | `.field--lensing` |
| `.dm-galaxies` | Galaxies | old-population violet + young-arm magenta | `.field--spiral` |
| `.dm-nebulae` | Nebulae | OIII teal + H-alpha rose | `.field--emission` |
| `.dm-events` | Cosmic Events | shock-front crimson + detonation white | `.field--burst` |
| `.dm-missions` | Space Missions | instrument telemetry green on blueprint cyan | `.field--telemetry` |
| `.dm-universe` | Universe | CMB indigo cooling to aqua | `.field--web` |

Two hues are reserved across the whole site rather than per region. **Violet**
means *real but unobservable* — dark matter haloes in Galaxies, spacetime
geometry in Black Holes, gravitational waves in Cosmic Events, dark matter and
dark energy in Universe. The **CMB temperature pair** (blue cold, red hot) is
used only for microwave-background anisotropy, and nowhere else.

`.dm-holes` additionally darkens `--void`/`--abyss` to absolute black. It is the one
region allowed to do that.

### Component inventory (components.css)

| Component | Purpose |
| --- | --- |
| `.shell` + tone modifiers | Section as an altitude in one continuous sky |
| `.field--*` | Per-subject backdrop geometry |
| `.eyebrow`, `.chip`, `.caption` | The instrument voice |
| `.head` | Section heading with index, rule and lede |
| `.page-hero` | Category arrival: left-aligned, bottom-anchored, readout docked |
| `.readout` | Instrument panel; grid gaps double as hairlines so it wraps cleanly |
| `.spec` | Hairline key/value rows, tabular figures |
| `.orb` | **The celestial-body primitive** — every sphere on the site |
| `.plate` / `.plate-grid` | Observation plate; the alternative to a card |
| `.ledger` | Proportional comparison rows (`--reach` per row) |
| `.rail` | Labelled axis beneath any diagram that compresses reality |
| `.note` | Field callout |
| `.domain-grid` / `.tile` / `.emblem` | The nine-region contact sheet |
| `.roadmap` | Honest in-development panel |

### The `.orb` primitive

One primitive renders every sphere: planets, moons, dwarf planets, stars, exoplanets.
A body is described only by custom properties, so a new world costs a few lines:

```css
.orb--kepler-22b {
    --orb-d:    72px;
    --orb-skin: radial-gradient(...);   /* may be layered */
    --orb-halo: rgba(...);              /* light cast into vacuum */
    --orb-air:  rgba(...);              /* atmospheric limb */
    --orb-shine: 0.24;                  /* specular strength */
}
```

```html
<span class="orb orb--kepler-22b" aria-hidden="true">
    <span class="orb__limb"></span>
    <span class="orb__body"><span class="orb__mark"></span></span>
</span>
```

Optional parts: `.orb__limb` (atmosphere), `.orb__mark` (a storm or basin),
`.orb__ring--back` / `--front` (ring halves with real occlusion), and
`--far-side` / `--near-side` for ring planes seen close to edge-on.

Band skins must use **interpolated** colour stops, never hard stops — hard stops
stair-step against the antialiased edge of the globe and read as printed stripes.

### Honesty rules for figures

These are design rules, not just content rules, because they change the markup.

1. Any diagram that compresses distance or size must say so in its caption.
2. Any diagram that compresses distance should be paired with a `.rail` or `.ledger`
   stating the real numbers.
3. Give at least one figure per page a true, uncompressed scale.
4. Spans over four orders of magnitude use a base-10 axis, and the caption says so.
5. Figures are numbered (`Fig 01`, `Fig 02`…) and referenced in the footer.

### Motion

Motion is always decorative and always removable. Orbital periods are compressed but
correctly *ordered*. Under `prefers-reduced-motion` the orrery does not snap every
planet to conjunction — it freezes at a scattered, physically plausible set of
longitudes (`--frozen` per orbit).

### Accessibility notes

- Decorative layers carry `aria-hidden="true"`; data figures carry
  `role="img"` with an `aria-label` that states what the figure shows.
- Nav state is never colour-only — the active link also gets a tick.
- `.skip-link` on every page; `:focus-visible` uses the domain accent.
- `<dl>` is used for all key/value data (`.readout`, `.spec`).

---

## Development Phases

### Phase 1: Foundation (Current)

- HTML + CSS only
- Homepage
- Navigation system
- Visual design system
- Responsive layouts
- Category structure

### Phase 2: Content Expansion

- Detailed category pages
- Object pages
- Educational content
- Reusable page patterns

### Phase 3: JavaScript Enhancement

- Search functionality
- Filtering and sorting
- Interactive UI
- Navigation improvements
- Dynamic content loading

### Phase 4: Backend Integration

- Flask/Python backend
- Database integration
- API development
- User authentication
- Content management

### Phase 5: Advanced Features

- Astronomical catalogs
- Advanced search
- Data visualization
- Real-time data
- Community features

---

## Design Principles

1. **Coherence**: Every page feels like part of one product
2. **Consistency**: Reusable components and patterns
3. **Accessibility**: Semantic HTML, keyboard navigation, ARIA
4. **Performance**: Lightweight CSS, no unnecessary dependencies
5. **Scalability**: Architecture supports future expansion
6. **Education-First**: Clear, accurate, accessible content

---

## Content Principles

1. **Accuracy**: All astronomical facts must be scientifically accurate
2. **Attribution**: Cite sources for scientific data
3. **Accessibility**: Content understandable for various knowledge levels
4. **Depth**: Support multiple information levels
5. **Curation**: Focus on quality over quantity

---

## Future Considerations

- Internationalization support
- Dark/light theme toggle (CSS custom properties ready)
- Print styles for educational content
- Search indexing structure
- Structured data (JSON-LD) for SEO
- API endpoints for catalog data
