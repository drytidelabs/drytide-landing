# WIREFRAME: Drytide Labs (drytide.co) — v1.0

## 1. Sections

1. **Header** — Wordmark, tagline, statement
2. **Proof** — 4 project cards in a 2-col grid (desktop) / 1-col (mobile)
3. **Infrastructure Philosophy** — Sovereign Tech Foundation section
4. **Footer** — Bio text + external links

## 2. Global

- Container: `max-width: 800px; margin: 0 auto; padding: 0 1rem`
- Font: `ui-monospace, 'Cascadia Code', 'Source Code Pro', Menlo, Consolas, monospace`
- Colors: `--bg: #0A0A0A` / `--fg: #F2F2F2`
- All borders: `1px solid var(--fg)` or `2px solid var(--fg)`

## 3. Section Specs

### Header
| Element | Tag | Class |
|---|---|---|
| Wordmark | `span` | `.wordmark` |
| Tagline | `p` | `.tagline` |
| Statement | `p` | `.statement` |

### Proof
| Element | Tag | Class |
|---|---|---|
| Section wrapper | `section` | `.proof` |
| Grid wrapper | `div` | `.grid` |
| Card | `article` | `.card` |
| Project title | `h3` | `.project-name` |
| Links | `nav` | `.project-meta` |
| Description | `p` | `.project-desc` |
| In-dev badge | `span` | `.badge` |

### Philosophy
| Element | Tag | Class |
|---|---|---|
| Section wrapper | `section` | `.philosophy` |
| Heading | `h2` | — |
| Body | `p` | — |

### Footer
| Element | Tag | Class |
|---|---|---|
| Footer wrapper | `footer` | — |
| Status text | `p` | `.status` |
| Links wrapper | `nav` | `.external-links` |

## 4. Responsive

- Single breakpoint: `@media (max-width: 600px)`
- Above 600px: 2-col project grid
- Below 600px: all elements stack, single column

## 5. Interaction (CSS-Only)

```css
a:hover { background: var(--fg); color: var(--bg); text-decoration: none; }
.card:hover { outline: 1px solid var(--fg); outline-offset: 2px; }
```

## 6. Handoff Checklist

- [x] DESIGN.md committed to repo root
- [x] Zero image files in build
- [x] Zero JavaScript files or inline `<script>` tags
- [x] Zero external network requests
- [x] Responsive breakpoint at exactly 600px
- [x] CNAME contains `drytide.co`
- [ ] Verbatim copy verified against brief (placeholder copy in place — awaiting full brief)
- [x] Contrast ratio: #F2F2F2 on #0A0A0A ≈ 18.7:1 (WCAG AAA ✓)
