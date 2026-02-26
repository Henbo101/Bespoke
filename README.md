# BESPOKE Garden Play — Master Brand Guidelines

A single-page brand guidelines document for Bespoke Garden Play. Built with semantic HTML and CSS custom properties. No build tools required.

## Quick Start

```
git clone <your-repo-url>
cd bespoke-brand-guidelines
open index.html
```

Or deploy directly to Netlify / GitHub Pages — the site is static with no dependencies beyond Google Fonts (loaded via CDN).

## Folder Structure

```
/
├── index.html
├── README.md
└── assets/
    ├── playhouse-imagery/       ← Real photography
    │   ├── hero-structure.jpg
    │   ├── interior-plywood-detail.jpg
    │   ├── cedar-shingle-closeup.jpg
    │   └── workshop-craftsmanship.jpg
    │
    └── ai-imagery/              ← AI-generated lifestyle shots
        ├── garden-golden-hour-atmosphere.jpg
        ├── playhouse-in-landscaped-garden.jpg
        ├── child-hands-on-timber-faceless.jpg
        ├── overcast-british-daylight-exterior.jpg
        └── dappled-canopy-light-play.jpg
```

## How to Update Images

1. Place your image files in the correct subfolder (`playhouse-imagery` or `ai-imagery`).
2. Rename each file to match the filenames listed above — or update the corresponding CSS class in `index.html`.

The image classes live in the `/* --- 06. PHOTOGRAPHY & IMAGE SYSTEM --- */` section of the `<style>` block. Each class maps to one file:

| CSS Class | File Path | Usage |
|---|---|---|
| `.img-hero` | `assets/playhouse-imagery/hero-structure.jpg` | Main hero — wide shot of a playhouse |
| `.img-detail` | `assets/playhouse-imagery/interior-plywood-detail.jpg` | Tight crop of ply-lined interior |
| `.img-cedar-shingles` | `assets/playhouse-imagery/cedar-shingle-closeup.jpg` | Cedar roof texture |
| `.img-workshop` | `assets/playhouse-imagery/workshop-craftsmanship.jpg` | Workshop / build process |
| `.img-lifestyle` | `assets/ai-imagery/garden-golden-hour-atmosphere.jpg` | AI golden-hour garden scene |
| `.img-garden-wide` | `assets/ai-imagery/playhouse-in-landscaped-garden.jpg` | AI wide garden landscape |
| `.img-child-texture` | `assets/ai-imagery/child-hands-on-timber-faceless.jpg` | AI faceless child + timber |
| `.img-overcast-exterior` | `assets/ai-imagery/overcast-british-daylight-exterior.jpg` | AI overcast exterior |
| `.img-dappled-canopy` | `assets/ai-imagery/dappled-canopy-light-play.jpg` | AI dappled light scene |

### Image Specs

- Format: JPG (optimised for web)
- Minimum width: 1200px
- Target file size: under 500KB
- Colour treatment: the CSS applies `filter: sepia(20%) saturate(70%) contrast(90%)` automatically — shoot/generate in natural colour

## Design System Reference

### The Heritage Palette

| Name | Hex | Usage |
|---|---|---|
| Alabaster | `#F7F6F2` | Background, negative space |
| Charcoal | `#232323` | Primary text, headings |
| Smoked Sage | `#7A8B7C` | Accent, labels, metadata |
| Portland Stone | `#D1CEC5` | Borders, dividers, placeholders |

### Typography

- **Primary:** Playfair Display (serif) — headlines, brand mark
- **Secondary:** Inter (sans-serif, light 300 / regular 400) — body, navigation, labels

### Spacing Scale (Alabaster Space)

| Token | Value | Use |
|---|---|---|
| `--space-sm` | 2rem | Tight gaps, paragraph spacing |
| `--space-md` | 4rem | Section padding, grid gaps |
| `--space-lg` | 8rem | Major separations |
| `--space-xl` | 12rem | Top-of-section breathing room |

## Deployment

### Netlify
Drag the entire project folder into the Netlify dashboard, or connect the GitHub repo. No build command needed — set publish directory to `/`.

### GitHub Pages
Push to a repo, go to Settings → Pages, set source to the `main` branch root.

## Notes

- All CSS is inline within `index.html` for zero-dependency deployment.
- Google Fonts are loaded via CDN — requires internet access.
- The sidebar navigation uses a vanilla JS scroll spy (no libraries).
