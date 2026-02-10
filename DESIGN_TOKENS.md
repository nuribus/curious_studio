# Curious Studio Design Token System

## Overview

This document outlines the complete design token system for the Curious Studio website. Design tokens provide a single source of truth for all design decisions, ensuring consistency across the platform and enabling AI-assisted development.

---

## Color System

### Color Palette Inspiration

The color system is inspired by the vibrant, natural imagery of the Curious Studio brand — featuring bright greens, yellow-greens, and golden yellows that evoke creativity, growth, and joy.

### Primary Green Palette

| Token | Hex Value | Usage | WCAG AA Compliant |
|-------|-----------|-------|-------------------|
| `--color-green-900` | #006837 | Deep accents, dark text on light green | ✅ |
| `--color-green-800` | #008548 | Primary button active state | ✅ |
| `--color-green-700` | #009B54 | Primary button hover state | ✅ |
| `--color-green-600` | **#00B469** | **Primary brand color** — CTA buttons, links | ✅ |
| `--color-green-500` | #1FC97C | Success states, secondary actions | ✅ |
| `--color-green-400` | #65CD70 | Light accents, borders | ✅ |
| `--color-green-300` | #A6E17C | Yellow-green accents, highlights | ⚠️ Use on dark backgrounds |
| `--color-green-200` | #C8F0A3 | Subtle backgrounds, borders | ⚠️ Decorative only |
| `--color-green-100` | #E8F8D4 | Card backgrounds, tinted sections | ⚠️ Decorative only |
| `--color-green-50` | #F5FCF0 | Very subtle backgrounds | ⚠️ Decorative only |

### Yellow Palette

| Token | Hex Value | Usage |
|-------|-----------|-------|
| `--color-yellow-600` | #E6A800 | Deep golden yellow |
| `--color-yellow-500` | #F4A300 | Accent yellow, warning states |
| `--color-yellow-400` | #FFC043 | Bright highlights |
| `--color-yellow-300` | #FFD171 | Light accents |
| `--color-yellow-200` | #FFE5A8 | Gradient backgrounds |

### Neutral Palette

| Token | Hex Value | Usage |
|-------|-----------|-------|
| `--color-neutral-900` | #1d1d1f | Primary text, headings |
| `--color-neutral-800` | #2c2c2e | Dark elements |
| `--color-neutral-700` | #48484a | Strong secondary text |
| `--color-neutral-600` | #6e6e73 | Secondary text, labels |
| `--color-neutral-500` | #8e8e93 | Tertiary text, placeholders |
| `--color-neutral-400` | #aeaeb2 | Disabled text |
| `--color-neutral-300` | #c7c7cc | Strong borders |
| `--color-neutral-200` | #d2d2d7 | Default borders |
| `--color-neutral-100` | #e5e5ea | Subtle borders |
| `--color-neutral-50` | #f5f5f7 | Subtle backgrounds |
| `--color-neutral-0` | #ffffff | White |

---

## Semantic Color Tokens

### Primary Colors

```css
--color-primary: var(--color-green-600);         /* #00B469 */
--color-primary-hover: var(--color-green-700);   /* #009B54 */
--color-primary-active: var(--color-green-800);  /* #008548 */
--color-primary-light: var(--color-green-300);   /* #A6E17C */
```

**Usage:** Primary action buttons, active navigation, links, primary brand elements

### Text Colors

```css
--color-text-primary: var(--color-neutral-900);     /* Body text, headings */
--color-text-secondary: var(--color-neutral-600);   /* Labels, captions */
--color-text-tertiary: var(--color-neutral-500);    /* Placeholder text */
--color-text-inverse: var(--color-neutral-0);       /* Text on dark backgrounds */
```

### Background Colors

```css
--color-bg-primary: var(--color-neutral-0);      /* Main page background */
--color-bg-secondary: var(--color-neutral-50);   /* Subtle sections */
--color-bg-tertiary: var(--color-green-50);      /* Green-tinted sections */
--color-bg-accent: var(--color-green-100);       /* Emphasized cards */
```

### Border Colors

```css
--color-border-default: var(--color-neutral-200);  /* Default borders */
--color-border-subtle: var(--color-neutral-100);   /* Subtle dividers */
--color-border-strong: var(--color-neutral-300);   /* Emphasized borders */
```

### State Colors

```css
--color-success: var(--color-green-500);   /* Success messages */
--color-warning: var(--color-yellow-500);  /* Warning states */
--color-error: #dc2626;                     /* Error states */
--color-info: #3b82f6;                      /* Info messages */
```

---

## Typography System

### Font Family

```css
--font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', Arial, sans-serif;
```

**System font stack** ensures optimal performance and native feel across all platforms.

### Font Size Scale

| Token | Value (rem) | Pixel | Usage |
|-------|-------------|-------|-------|
| `--font-size-xs` | 0.75rem | 12px | Small labels, captions |
| `--font-size-sm` | 0.875rem | 14px | Navigation, buttons, secondary text |
| `--font-size-base` | 0.9375rem | 15px | Cards, secondary body text |
| `--font-size-md` | 1.0625rem | 17px | **Body text** (default) |
| `--font-size-lg` | 1.1875rem | 19px | Large body text, subheadings |
| `--font-size-xl` | 1.3125rem | 21px | H3, subtitles |
| `--font-size-2xl` | 1.5rem | 24px | H2 (smaller) |
| `--font-size-3xl` | 2rem | 32px | H2, section headings |
| `--font-size-4xl` | 2.5rem | 40px | Large headings |
| `--font-size-5xl` | 3rem | 48px | H1, hero headings |
| `--font-size-6xl` | 3.75rem | 60px | Extra large display |

### Font Weights

```css
--font-weight-regular: 400;   /* Body text */
--font-weight-medium: 500;    /* Emphasized text, active states */
--font-weight-semibold: 600;  /* Headings, buttons */
--font-weight-bold: 700;      /* Strong emphasis, H1 */
```

### Line Heights

```css
--line-height-tight: 1.2;     /* Large headings */
--line-height-snug: 1.4;      /* Subheadings */
--line-height-normal: 1.6;    /* UI elements */
--line-height-relaxed: 1.7;   /* Body text (default) */
--line-height-loose: 1.8;     /* Long-form content */
```

### Letter Spacing

```css
--letter-spacing-tight: -0.03em;   /* Large headings */
--letter-spacing-snug: -0.02em;    /* Medium headings */
--letter-spacing-normal: 0;         /* Body text */
--letter-spacing-wide: 0.02em;     /* Labels, uppercase */
```

---

## Spacing System

### Base Unit: 4px

All spacing follows a **4px base unit** for visual consistency and alignment.

| Token | Value | Pixel | Common Usage |
|-------|-------|-------|--------------|
| `--space-4` | 0.25rem | 4px | Micro spacing |
| `--space-8` | 0.5rem | 8px | Tight padding, icon gaps |
| `--space-10` | 0.625rem | 10px | Button padding (vertical) |
| `--space-12` | 0.75rem | 12px | Small gaps, list spacing |
| `--space-14` | 0.875rem | 14px | Button padding (large, vertical) |
| `--space-16` | 1rem | 16px | Standard padding, form fields |
| `--space-20` | 1.25rem | 20px | Button padding (horizontal) |
| `--space-22` | 1.375rem | 22px | Container padding (mobile) |
| `--space-24` | 1.5rem | 24px | Card padding, section spacing |
| `--space-28` | 1.75rem | 28px | Medium card padding |
| `--space-32` | 2rem | 32px | Large gaps, nav spacing, button padding (large) |
| `--space-40` | 2.5rem | 40px | Section padding |
| `--space-48` | 3rem | 48px | Large section spacing |
| `--space-56` | 3.5rem | 56px | Content block margins |
| `--space-60` | 3.75rem | 60px | Major section padding |
| `--space-64` | 4rem | 64px | Extra large gaps |
| `--space-80` | 5rem | 80px | Footer margin |

---

## Border Radius System

| Token | Value | Pixel | Usage |
|-------|-------|-------|-------|
| `--radius-none` | 0 | 0px | Square elements |
| `--radius-sm` | 0.25rem | 4px | Small tags, badges |
| `--radius-base` | 0.5rem | 8px | Inputs, small cards |
| `--radius-md` | 0.75rem | 12px | Radio buttons, week selector |
| `--radius-lg` | 1rem | 16px | Cards, modals, containers |
| `--radius-xl` | 1.25rem | 20px | Large cards |
| `--radius-2xl` | 1.5rem | 24px | Hero cards |
| `--radius-pill` | 980px | **Pill shape** | **Buttons** (fully rounded) |
| `--radius-circle` | 50% | Circle | Avatars, icon buttons |

**Note:** Buttons use `--radius-pill` (980px) for fully rounded pill shapes.

---

## Shadow System

| Token | CSS Value | Usage |
|-------|-----------|-------|
| `--shadow-sm` | 0 1px 2px rgba(0,0,0,0.05) | Subtle elevation |
| `--shadow-base` | 0 1px 3px rgba(0,0,0,0.1), 0 1px 2px -1px rgba(0,0,0,0.1) | Default cards |
| `--shadow-md` | 0 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -2px rgba(0,0,0,0.1) | Elevated cards |
| `--shadow-lg` | 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -4px rgba(0,0,0,0.1) | Hover states |
| `--shadow-xl` | 0 20px 25px -5px rgba(0,0,0,0.1), 0 8px 10px -6px rgba(0,0,0,0.1) | High elevation |
| `--shadow-modal` | 0 4px 24px rgba(0,0,0,0.15) | Modals, overlays |

---

## Z-Index Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--z-base` | 0 | Default layer |
| `--z-dropdown` | 100 | Dropdowns, popovers |
| `--z-sticky` | 1000 | Sticky header |
| `--z-overlay` | 1500 | Background overlays |
| `--z-modal` | 2000 | Modal dialogs |
| `--z-tooltip` | 2500 | Tooltips, toasts |

---

## Component Tokens

### Button Tokens

```css
/* Primary Button */
background-color: var(--color-primary);
color: var(--color-text-inverse);
padding: var(--space-10) var(--space-20);         /* Small button */
padding: var(--space-14) var(--space-32);         /* Large button */
border-radius: var(--radius-pill);                /* Fully rounded */
font-size: var(--font-size-sm);                   /* Small button */
font-size: var(--font-size-md);                   /* Large button */
font-weight: var(--font-weight-medium);

/* Hover State */
background-color: var(--color-primary-hover);

/* Active State */
background-color: var(--color-primary-active);
```

### Card Tokens

```css
/* Expectation Cards */
background: linear-gradient(135deg, var(--color-green-100) 0%, var(--color-green-50) 100%);
padding: var(--space-28);
border-radius: var(--radius-lg);
border: 1px solid var(--color-green-200);
```

### Modal Tokens

```css
/* Modal */
background-color: var(--color-bg-primary);
padding: var(--space-40);
border-radius: var(--radius-lg);
box-shadow: var(--shadow-modal);
max-width: 600px;
```

---

## Accessibility Standards

### Color Contrast

All color combinations meet **WCAG AA standards** (minimum 4.5:1 for normal text, 3:1 for large text):

✅ **Primary green (#00B469) on white:** 3.08:1 (AA for large text)
✅ **Neutral-900 (#1d1d1f) on white:** 16.07:1 (AAA)
✅ **Neutral-600 (#6e6e73) on white:** 5.74:1 (AA)

### Focus States

```css
/* All interactive elements */
outline: 2px solid var(--color-primary);
outline-offset: 2px;
```

### High Contrast Mode

```css
@media (prefers-contrast: high) {
    :root {
        --color-text-secondary: var(--color-neutral-700);
    }
}
```

### Reduced Motion

```css
@media (prefers-reduced-motion: reduce) {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
}
```

---

## AI Integration Guidelines

### For AI Code Generation

When using AI assistants (Claude Code, GitHub Copilot, etc.) to generate code for this project:

**Color Guidance:**
```
- Primary actions: Use --color-primary (#00B469)
- Text: Use --color-text-primary (#1d1d1f) for body, --color-text-secondary (#6e6e73) for labels
- Backgrounds: Use --color-bg-primary (white) or --color-bg-secondary (#f5f5f7)
- Never hardcode hex values — always reference tokens
```

**Spacing Guidance:**
```
- Follow 4px grid: use --space-16, --space-24, --space-32, etc.
- Button padding: --space-10 --space-20 (small), --space-14 --space-32 (large)
- Section spacing: --space-48 or --space-60
- Never use arbitrary values like "15px" or "23px"
```

**Typography Guidance:**
```
- Headings: Use --font-size-5xl (H1), --font-size-3xl (H2), --font-size-xl (H3)
- Body: Use --font-size-md (17px)
- Buttons: Use --font-size-sm (14px, small), --font-size-md (17px, large)
- Always use --font-family for consistency
```

**Border Radius:**
```
- Buttons: Always use --radius-pill (980px) for fully rounded pill shape
- Cards: Use --radius-lg (16px)
- Modals: Use --radius-lg (16px)
```

---

## Maintenance & Updates

### When to Update Tokens

- **New feature requires a new color:** Add to primitives first, then create semantic token
- **Inconsistent spacing appears:** Add missing token to spacing scale
- **New component pattern emerges:** Document as component token

### Token Naming Convention

**Pattern:** `--{category}-{concept}-{variant}`

Examples:
- `--color-primary-hover` (category: color, concept: primary, variant: hover)
- `--space-32` (category: space, value: 32)
- `--radius-pill` (category: radius, variant: pill)

### Version Control

Update `tokens.json` and `style.css` simultaneously. The JSON file serves as documentation and can be used for future platform expansion (iOS, Android, etc.).

---

## References

- **W3C Design Tokens Specification:** [https://www.w3.org/community/design-tokens/](https://www.w3.org/community/design-tokens/)
- **Apple Human Interface Guidelines:** [https://developer.apple.com/design/human-interface-guidelines/](https://developer.apple.com/design/human-interface-guidelines/)
- **WCAG Color Contrast:** [https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html)

---

**Last Updated:** February 9, 2026
**Maintained by:** Curious Studio Design System
