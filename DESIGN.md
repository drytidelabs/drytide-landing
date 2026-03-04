# Drytide Labs: Design System (v1.0)

This document defines the visual and structural identity for **Drytide Labs** (drytide.co). The aesthetic is **Brutalist-Technical**: high contrast, zero fluff, and raw implementation.

---

## 1. Typography

All text must use a monospaced system font stack. No external requests to Google Fonts or CDNs.

- **Font Stack:** `ui-monospace, 'Cascadia Code', 'Source Code Pro', Menlo, Monaco, 'Consolas', 'DejaVu Sans Mono', monospace`
- **Scale:**
  - `H1`: 2.000rem (32px) / Bold (700) / Leading 1.1
  - `H2`: 1.500rem (24px) / Bold (700) / Leading 1.2
  - `H3`: 1.250rem (20px) / Bold (700) / Leading 1.2
  - `Body`: 1.000rem (16px) / Normal (400) / Leading 1.5
  - `Small / Caption`: 0.875rem (14px) / Normal (400) / Leading 1.4
  - `Nav / Label`: 1.000rem (16px) / Bold (700) / Uppercase
- **Rules:**
  - `letter-spacing`: -0.02em for headings; 0 for body.
  - No italics except for `<em>` tags within technical documentation.

---

## 2. Colour Palette

| Property | Value | Usage |
| :--- | :--- | :--- |
| `--bg` | `#0A0A0A` | Primary background |
| `--fg` | `#F2F2F2` | Primary text and borders |
| `--bg-alt` | `#111111` | Subtle section backgrounds (optional) |

**Rules:**
- Zero Gradients. Solid fills only.
- Zero Color Photography. Any images must be 1-bit, grayscale, or dithered.
- High Contrast. Text must always meet WCAG AAA contrast ratios against `--bg`.
- No third colour. If you're reaching for a colour, reach for a border instead.

---

## 3. Spacing System (8px base)

| Name | Value |
| :--- | :--- |
| `xs` | 0.25rem (4px) |
| `sm` | 0.5rem (8px) |
| `md` | 1.0rem (16px) |
| `lg` | 2.0rem (32px) |
| `xl` | 4.0rem (64px) |
| `2xl` | 8.0rem (128px) |

---

## 4. Component Patterns

### Wordmark
```css
.wordmark {
  font-size: 1.5rem;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  border-left: 4px solid var(--fg);
  padding-left: var(--space-sm);
}
```

### Project Card
```css
.card {
  border: 2px solid var(--fg);
  padding: var(--space-md);
  display: flex;
  flex-direction: column;
  gap: var(--space-sm);
  background: var(--bg);
}
```

### Footer
```css
footer {
  border-top: 2px solid var(--fg);
  padding: var(--space-lg) 0;
  margin-top: var(--space-2xl);
  font-size: 0.875rem;
}
```

### Links
```css
a {
  color: var(--fg);
  text-decoration: underline;
  text-underline-offset: 4px;
  text-decoration-thickness: 1px;
}
a:hover {
  background: var(--fg);
  color: var(--bg);
  text-decoration: none;
}
```

### Badge
```css
.badge {
  display: inline-block;
  border: 1px solid var(--fg);
  padding: 0 var(--space-xs);
  font-size: 0.75rem;
  letter-spacing: 0.1em;
  opacity: 0.6;
}
```

### HR / Divider
```css
hr {
  border: none;
  border-top: 1px solid var(--fg);
  opacity: 0.2;
  margin: var(--space-lg) 0;
}
```

---

## 5. Layout

- **Max Content Width:** `800px`
- **Responsive Breakpoint:** `600px` (single breakpoint)
- **Project Grid:** `grid-template-columns: repeat(auto-fill, minmax(300px, 1fr))`

---

## 6. Rules

1. **Dark background, always.** `--bg: #0A0A0A`. Never swap to light mode.
2. **Never use border-radius.** Every corner is a sharp 90-degree angle.
3. **No box-shadows.** Depth via 2px solid borders only.
4. **System fonts only.** No external font loading.
5. **No animations.** State changes are instant or capped at 100ms max.
6. **Content is signal.** If a design element has no function, remove it.
7. **Borders over backgrounds.** Use `2px solid var(--fg)` to define structure.
8. **Zero `<img>` tags.** CSS-only visuals. No SVG files without approval.
9. **Zero JavaScript.** No `<script>` tags, no external JS.
10. **Zero external network requests.** No CDN, no Google Fonts.
