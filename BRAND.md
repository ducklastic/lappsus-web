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
| Taronja accessible | — | `#b15200` |
| Blanc | 0C 0M 0Y 0K | `#ffffff` |

### Mode clar (light mode) — fons blanc `#ffffff`

| Rol | HEX | Contrast sobre blanc |
|---|---|---|
| Text principal | `#0d0d0d` | 19.44:1 ✅ AAA |
| Text secundari | `#555555` | 7.46:1 ✅ AAA |
| Fons subtil | `#f2f2f2` | — |
| Accent / links | `#b15200` | 5.15:1 ✅ AA |
| Decoració / icones | `#ff8012` | 2.5:1 ⚠️ només decoratiu |
| Separadors | `#e8e8e8` | — |

### Mode fosc (dark mode) — fons negre `#000000`

| Rol | HEX | Contrast sobre negre |
|---|---|---|
| Text principal | `#ffffff` | 21.00:1 ✅ AAA |
| Text secundari | `#f2f2f2` | 18.76:1 ✅ AAA |
| Accent / links | `#ff8012` | 8.35:1 ✅ AAA |
| Decoració / icones | `#ff8012` | 8.35:1 ✅ AAA |
| Separadors | `#333333` | — |

---

## Regles d'ús

- **`#ff8012`** — taronja pur: NOMÉS per a elements decoratius, icones i text sobre fons fosc. Mai com a text sobre blanc o gris clar (contrast insuficient).
- **`#b15200`** — taronja accessible: per a links i text sobre fons clar (mode light).
  Mateix to que `#ff8012` (27,8°), només més fosc. Passa AA **tant sobre blanc com sobre
  `#f2f2f2`**, que és la condició real: un accent que només aguanta sobre blanc falla el dia
  que es fa servir dins d'una secció de fons subtil.
- **`#0d0d0d`** — negre text: preferible al negre pur `#000000` per a text corrent (menys dur).
- **`#f2f2f2`** — gris clar: per a fons de seccions, cards o separació visual subtil.

---

## Contrastos validats (WCAG 2.1)

> Calculats amb la fórmula de luminància relativa de la WCAG i arrodonits **cap avall**.
> Un valor que arrodoneix cap amunt fins al llindar (4,47 → «4,5 ✅») no compleix: el
> llindar és un mínim, no una fita a la qual acostar-se.

| Combinació | Ratio | AA text | AA gran | AAA |
|---|---|---|---|---|
| `#0d0d0d` sobre `#ffffff` | 19.44:1 | ✅ | ✅ | ✅ |
| `#0d0d0d` sobre `#f2f2f2` | 17.36:1 | ✅ | ✅ | ✅ |
| `#b15200` sobre `#ffffff` | 5.15:1 | ✅ | ✅ | ❌ |
| `#b15200` sobre `#f2f2f2` | 4.60:1 | ✅ | ✅ | ❌ |
| `#ff8012` sobre `#000000` | 8.35:1 | ✅ | ✅ | ✅ |
| `#ff8012` sobre `#0d0d0d` | 7.73:1 | ✅ | ✅ | ✅ |
| `#ff8012` sobre `#ffffff` | 2.52:1 | ❌ | ❌ | ❌ |
| `#ffffff` sobre `#0d0d0d` | 19.44:1 | ✅ | ✅ | ✅ |
| `#f2f2f2` sobre `#000000` | 18.76:1 | ✅ | ✅ | ✅ |
