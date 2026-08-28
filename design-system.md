# Design System — Site Denyse Albuquerque · Psiquiatria

> **Tom visual:** _Um espaço digital que abraça antes de informar — claro, sereno e profundamente humano._

---

## 🎨 Paleta de Cores

A paleta foi extraída das referências visuais: o azul profundo confiante da imagem 2, o turquesa acolhedor e os neutros cremosos da imagem 1, com o terracota/âmbar como acento energizante.

| Token | Hex | Uso |
|---|---|---|
| `--color-primary` | `#1A4A7A` | Azul noite — títulos, nav, âncoras de confiança |
| `--color-secondary` | `#3AACAA` | Turquesa suave — destaques, ícones, CTAs secundários |
| `--color-accent` | `#F28029` | Terracota âmbar — CTA principal, destaques em destaque |
| `--color-warm-rose` | `#D4848A` | Rosa envelhecido — gradientes sutis, elementos sensoriais |
| `--color-surface` | `#F7F1EA` | Creme areia — fundo geral, cards |
| `--color-text` | `#2D2D2D` | Quase-preto — corpo de texto, máxima legibilidade |

### Swatch visual

```
█████  #1A4A7A  Azul Noite (Primary)
█████  #3AACAA  Turquesa (Secondary)
█████  #F28029  Terracota (Accent)
█████  #D4848A  Rosa Envelhecido (Warm Rose)
█████  #F7F1EA  Creme Areia (Surface)
█████  #2D2D2D  Grafite (Text)
```

### Regras de uso

- **Fundos:** `--color-surface` para páginas; `--color-primary` para seções de destaque (hero escuro, footer).
- **Ações:** CTA principal em `--color-accent`; hover com 10% mais escuro (`#D96E1F`).
- **Acentos suaves:** `--color-secondary` para tags, badges e divisores decorativos.
- **Gradiente de marca:** de `--color-accent` (#F28029) até `--color-warm-rose` (#D4848A) — usar com moderação em ilustrações e separadores.
- **Nunca combinar:** `--color-accent` com `--color-warm-rose` em texto sobre fundo claro (baixo contraste).

---

## 🔤 Tipografia

Par escolhido para equilibrar autoridade científica com calor humano.

### Títulos — `Cormorant Garamond`

```css
font-family: 'Cormorant Garamond', serif;
```

- Serifada elegante, de origem humanista.
- Transmite confiança, delicadeza e profissionalismo sem frieza.
- Importar no peso **300 (Light)**, **400 (Regular)** e **600 (SemiBold)**.
- Link: `https://fonts.google.com/specimen/Cormorant+Garamond`

### Corpo — `DM Sans`

```css
font-family: 'DM Sans', sans-serif;
```

- Geométrica com traços humanistas — legível, moderna, calorosa.
- Ótima em telas pequenas e textos corridos.
- Importar nos pesos **300**, **400** e **500**.
- Link: `https://fonts.google.com/specimen/DM+Sans`

### Escala tipográfica

| Nível | Elemento | Fonte | Tamanho (rem) | Peso | Line-height |
|---|---|---|---|---|---|
| H1 | Título hero | Cormorant Garamond | 3.5 rem | 300 | 1.15 |
| H2 | Seções | Cormorant Garamond | 2.25 rem | 400 | 1.2 |
| H3 | Subtítulos | Cormorant Garamond | 1.5 rem | 600 | 1.3 |
| Body L | Lide / intro | DM Sans | 1.125 rem | 300 | 1.7 |
| Body M | Parágrafos | DM Sans | 1 rem | 400 | 1.7 |
| Caption | Labels, datas | DM Sans | 0.8125 rem | 500 | 1.5 |

> **Script pontual:** considere `Dancing Script` apenas em assinaturas ou frases de acolhimento, alinhado ao estilo manuscrito presente nas referências visuais.

---

## 📐 Espaçamento & Grid

### Grid

- **Layout base:** 12 colunas
- **Max-width do container:** `1160px`
- **Gutter (espaço entre colunas):** `24px`
- **Margin lateral do container:** `24px` mobile / `48px` tablet / `80px` desktop

```
Mobile  (≤ 640px):    4 colunas, gutter 16px
Tablet  (641–1024px): 8 colunas, gutter 24px
Desktop (≥ 1025px):  12 colunas, gutter 24px
```

### Escala de espaçamento (base 8 px)

| Token | Valor | Uso típico |
|---|---|---|
| `--space-1` | 4 px | Micro-espaços internos |
| `--space-2` | 8 px | Padding de tags, labels |
| `--space-3` | 16 px | Padding interno de cards |
| `--space-4` | 24 px | Gap entre elementos em linha |
| `--space-5` | 40 px | Espaçamento entre seções pequenas |
| `--space-6` | 64 px | Separação entre seções maiores |
| `--space-7` | 96 px | Padding hero / seções de impacto |

### Bordas & Cantos

- **Border-radius padrão:** `12px` (cards, botões)
- **Border-radius amplo:** `24px` (seções destacadas, imagens)
- **Border-radius total:** `9999px` (tags, pills, avatares)
- Preferir **sombras suaves** a bordas duras:
  `box-shadow: 0 4px 24px rgba(26, 74, 122, 0.08)`

---

## 🖼️ Princípios Visuais

1. **Respiração** — Seções com espaço amplo entre si. O creme e o branco fazem parte do conteúdo, não são ausência dele.
2. **Hierarquia com leveza** — Títulos grandes em peso leve (Cormorant 300) criam presença sem agressividade.
3. **Calor pontual** — O terracota e o rosa aparecem como acento, nunca como base de uma seção inteira.
4. **Fotografias humanizadas** — Preferir fotos com tonalidade levemente aquecida (creme/dourada), sem filtros frios.
5. **Consistência emocional** — Elementos decorativos orgânicos (folhas, traços curvilíneos) são bem-vindos com moderação, dentro da paleta definida.

---

## 🔗 Importação Google Fonts

Adicionar no `<head>` do HTML:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
```

---

## 📋 CSS Custom Properties

```css
:root {
  /* Cores */
  --color-primary:    #1A4A7A;
  --color-secondary:  #3AACAA;
  --color-accent:     #F28029;
  --color-warm-rose:  #D4848A;
  --color-surface:    #F7F1EA;
  --color-text:       #2D2D2D;

  /* Tipografia */
  --font-heading: 'Cormorant Garamond', serif;
  --font-body:    'DM Sans', sans-serif;

  /* Espaçamento */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 16px;
  --space-4: 24px;
  --space-5: 40px;
  --space-6: 64px;
  --space-7: 96px;

  /* Bordas */
  --radius-sm:   12px;
  --radius-lg:   24px;
  --radius-full: 9999px;

  /* Sombra */
  --shadow-card: 0 4px 24px rgba(26, 74, 122, 0.08);
}
```

---

_Design system criado em 27/08/2026 · Referências visuais: material de comunicação da Dra. Denyse Albuquerque._
