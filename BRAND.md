# Lappsus — Identitat Corporativa

## Tipografia
- **Helvetica Neue Regular** (12px cos de text)
- Web fallback: `"Helvetica Neue", Helvetica, Arial, sans-serif`

---

## Logo
Text CSS pur — no usar imatge PNG.

```
[lappsus]
```

- Font: Helvetica Neue Light (`font-weight: 300`)
- Tot en minúscules
- CSS:
  ```css
  .logo { font-size: 20px; font-weight: 300; letter-spacing: -0.5px; color: #000; text-decoration: none; }
  .logo::before { content: "["; }
  .logo::after  { content: "]"; }
  ```

---

## Colors

### Paleta base (CMYK → HEX)

| Nom | CMYK | HEX |
|---|---|---|
| Negre pur | 0C 0M 0Y 100K | `#000000` |
| Negre text | 0C 0M 0Y 95K | `#0d0d0d` |
| Gris clar | 0C 0M 0Y 5K | `#f2f2f2` |
| Taronja corporatiu | 0C 50M 93Y 0K | `#ff8012` |
| Blanc | 0C 0M 0Y 0K | `#ffffff` |

### Mode clar (light mode) — fons blanc `#ffffff`

| Rol | HEX | Contrast sobre blanc |
|---|---|---|
| Text principal | `#0d0d0d` | 19.4:1 ✅ AAA |
| Text secundari | `#555555` | 7.4:1 ✅ AAA |
| Fons subtil | `#f2f2f2` | — |
| Accent / links | `#b85c0d` | 4.6:1 ✅ AA |
| Decoració / icones | `#ff8012` | 2.5:1 ⚠️ només decoratiu |
| Separadors | `#e8e8e8` | — |

### Mode fosc (dark mode) — fons negre `#000000`

| Rol | HEX | Contrast sobre negre |
|---|---|---|
| Text principal | `#ffffff` | 21:1 ✅ AAA |
| Text secundari | `#f2f2f2` | 18.8:1 ✅ AAA |
| Accent / links | `#ff8012` | 8.4:1 ✅ AAA |
| Decoració / icones | `#ff8012` | 8.4:1 ✅ AAA |
| Separadors | `#333333` | — |

---

## Regles d'ús

- **`#ff8012`** — taronja pur: NOMÉS per a elements decoratius, icones i text sobre fons fosc. Mai com a text sobre blanc o gris clar (contrast insuficient).
- **`#b85c0d`** — taronja accessible: per a links i text sobre fons clar (mode light).
- **`#0d0d0d`** — negre text: preferible al negre pur `#000000` per a text corrent (menys dur).
- **`#f2f2f2`** — gris clar: per a fons de seccions, cards o separació visual subtil.

---

## Contrastos validats (WCAG 2.1)

| Combinació | Ratio | AA text | AA gran | AAA |
|---|---|---|---|---|
| `#0d0d0d` sobre `#ffffff` | 19.4:1 | ✅ | ✅ | ✅ |
| `#0d0d0d` sobre `#f2f2f2` | 17.4:1 | ✅ | ✅ | ✅ |
| `#b85c0d` sobre `#ffffff` | 4.6:1 | ✅ | ✅ | ❌ |
| `#b85c0d` sobre `#f2f2f2` | 4.9:1 | ✅ | ✅ | ❌ |
| `#ff8012` sobre `#000000` | 8.4:1 | ✅ | ✅ | ✅ |
| `#ff8012` sobre `#0d0d0d` | 7.7:1 | ✅ | ✅ | ✅ |
| `#ff8012` sobre `#ffffff` | 2.5:1 | ❌ | ❌ | ❌ |
| `#ffffff` sobre `#0d0d0d` | 19.4:1 | ✅ | ✅ | ✅ |
| `#f2f2f2` sobre `#000000` | 18.8:1 | ✅ | ✅ | ✅ |
