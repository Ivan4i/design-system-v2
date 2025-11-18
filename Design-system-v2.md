# Design System Documentation

## 📋 Содержание

1. [Основы](#основы)
2. [Цветовая палитра](#цветовая-палитра)
3. [Типографика](#типографика)
4. [Spacing & Layout](#spacing--layout)
5. [Компоненты](#компоненты)
6. [Паттерны](#паттерны)
7. [Состояния](#состояния)
8. [Иконки](#иконки)

---

## Основы

### Принципы дизайна

- **Консистентность**: Единообразное использование компонентов, цветов и типографики во всех частях интерфейса
- **Читаемость**: Четкая визуальная иерархия и оптимальная контрастность текста
- **Эффективность**: Минималистичный подход к дизайну с фокусом на пользовательские задачи
- **Адаптивность**: Гибкие компоненты, работающие в светлой и темной темах

### Философия

> Дизайн-система создана для построения современных, функциональных интерфейсов с акцентом на визуализацию данных, аналитику и удобство работы пользователей. Мы используем мягкие скругления, тонкие обводки и градиенты для создания глубины и современного внешнего вида.

---

## Цветовая палитра

### Primary Colors

```css
/* Основной цвет бренда */
--color-primary: var(--Primary-primary03); /* Используется для focus states */
--color-primary-hover: var(--Primary-primary03);
--color-primary-active: var(--Primary-primary03);
--color-primary-light: rgba(147, 51, 234, 0.1); /* purple-500 с opacity */
--color-primary-dark: #7c3aed; /* purple-600 */

/* Вторичный цвет */
--color-secondary: #9333ea; /* purple-500 */
--color-secondary-hover: #a855f7; /* purple-400 */
--color-secondary-active: #7c3aed; /* purple-600 */
```

### Semantic Colors

```css
/* Success / Trend Up */
--color-success: var(--Primary-primary02); /* Зеленый для success */
--color-success-bg: rgba(22, 163, 74, 0.05); /* green-600/5 */
--color-success-border: rgba(22, 163, 74, 0.20); /* green-600/20 */

/* Error / Trend Down */
--color-error: #f87171; /* red-400 */
--color-error-bg: rgba(248, 113, 113, 0.05); /* red-400/5 */
--color-error-border: rgba(248, 113, 113, 0.20); /* red-400/20 */

/* Warning / Hot */
--color-warning: #fb923c; /* orange-400 */
--color-warning-bg: rgba(251, 146, 60, 0.05); /* orange-400/5 */
--color-warning-border: rgba(251, 146, 60, 0.20); /* orange-400/20 */

/* Info */
--color-info: #22d3ee; /* cyan-400 */
--color-info-bg: rgba(34, 211, 238, 0.05); /* cyan-400/5 */
--color-info-border: rgba(34, 211, 238, 0.20); /* cyan-400/20 */
```

### Neutral Colors

```css
/* Text */
--color-text-primary: var(--Text-Primary); /* Основной текст */
--color-text-secondary: var(--Text-Secondary); /* Вторичный текст */
--color-text-tertiary: var(--Text-Tertiary); /* Tertiary текст, placeholder */
--color-text-disabled: rgba(var(--Text-Secondary), 0.4);
--color-text-inverse: var(--Text-Light); /* Светлый текст на темном фоне */
--color-text-blue: var(--Text-Blue); /* Синий для каретки и акцентов */

/* Backgrounds */
--color-bg-primary: var(--Backgrounds-surface1); /* Основной фон */
--color-bg-secondary: var(--Backgrounds-surface2); /* Вторичный фон */
--color-bg-tertiary: var(--Stroke-Subtle); /* Третичный фон */
--color-bg-elevated: var(--Backgrounds-surface2);
--color-bg-overlay: var(--Backgrounds-dark1); /* Для tooltips/overlays */
--color-bg-neutral-800: #262626; /* neutral-800 */

/* Stroke / Borders */
--color-border-primary: var(--Stroke-Stroke2);
--color-border-secondary: var(--Stroke-Subtle);
--color-border-focus: var(--Primary-primary03);
--color-border-disabled: rgba(var(--Stroke-Stroke2), 0.5);

/* Shades */
--color-shade07-40: rgba(var(--shade07-40), 0.4); /* 40% opacity */
--color-shade07-50: rgba(var(--shade07-50), 0.5); /* 50% opacity */
--color-shade07-60: rgba(var(--shade07-60), 0.6); /* 60% opacity */
--color-shade08-100: var(--shade08-100);
--color-shade09-100: var(--shade09-100);

/* Tailwind equivalents */
--color-gray-50: #fafafa;
--color-gray-100: #f5f5f5;
--color-gray-200: #e5e5e5; /* neutral-200 */
--color-gray-300: #d4d4d4;
--color-gray-400: #a3a3a3;
--color-gray-500: #737373;
--color-gray-600: #525252;
--color-gray-700: #404040;
--color-gray-800: #262626; /* zinc-800, neutral-800 */
--color-gray-900: #171717;
```

### Chart Colors

```css
/* Для графиков и визуализации данных */
--color-chart-1: #8b5cf6; /* purple-500 - primary chart color */
--color-chart-2: #22d3ee; /* cyan-400 - secondary */
--color-chart-3: #fb923c; /* orange-400 - tertiary */
--color-chart-4: #16a34a; /* green-600 - positive */
--color-chart-5: #f87171; /* red-400 - negative */
--color-chart-6: #a855f7; /* purple-400 - accent */
--color-chart-7: #06b6d4; /* cyan-500 - cool accent */
--color-chart-8: #ea580c; /* orange-600 - warm accent */
```

### Gradients

```css
/* Градиенты для специальных элементов */
--gradient-primary-light: linear-gradient(to bottom, #ffffff, #e5e5e5); /* from-white to-neutral-200 */
--gradient-primary-dark: linear-gradient(to bottom, #262626, #262626); /* from-zinc-800 to-zinc-800 */
--gradient-secondary-dark: linear-gradient(to bottom, #262626, #171717); /* from-zinc-800 to-neutral-800 */
--gradient-progress: linear-gradient(to right, var(--shade08-100), var(--shade09-100)); /* Для progress bars */
```

### Brand Icon Colors

```css
/* Цвета для иконок брендов и социальных сетей */
--color-brand-facebook: #1877f2; /* Facebook blue */
--color-brand-twitter: #1da1f2; /* Twitter/X blue */
--color-brand-instagram: #e4405f; /* Instagram gradient primary */
--color-brand-linkedin: #0a66c2; /* LinkedIn blue */
--color-brand-youtube: #ff0000; /* YouTube red */
--color-brand-github: #181717; /* GitHub dark */
```

---

## Типографика

### Font Family

```css
--font-primary: 'Inter Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-secondary: 'ES Build', 'Inter Display', monospace; /* Для password fields */
--font-mono: 'SF Mono', 'Monaco', 'Inconsolata', 'Fira Code', monospace;
```

### Font Sizes

```css
--font-size-overline: 0.625rem; /* 10px - overline text */
--font-size-xs: 0.75rem;    /* 12px - caption */
--font-size-sm: 0.875rem;   /* 14px - body 2, buttons */
--font-size-base: 1rem;     /* 16px - body 1, subtitle 1 */
--font-size-lg: 1.25rem;    /* 20px - H6 */
--font-size-xl: 1.5rem;     /* 24px - H5 */
--font-size-2xl: 1.875rem;  /* 30px - H4 */
--font-size-3xl: 2rem;      /* 32px */
--font-size-4xl: 2.5rem;    /* 40px */
--font-size-5xl: 3rem;      /* 48px - H3 */
--font-size-6xl: 3.75rem;   /* 60px - H2 */
--font-size-7xl: 4.5rem;    /* 72px */
--font-size-8xl: 6rem;      /* 96px - H1 */
```

### Font Weights

```css
--font-weight-thin: 100;
--font-weight-light: 300;    /* H1 */
--font-weight-normal: 400;   /* Body text, Caption */
--font-weight-medium: 500;   /* H2, H3, H5, Overline */
--font-weight-semibold: 600; /* H4, H6, Subtitle 1, Button */
--font-weight-bold: 700;     /* Subtitle 2 */
--font-weight-extrabold: 800;
--font-weight-black: 900;
```

### Line Heights

```css
--line-height-overline: 0.625rem;  /* 10px - leading-[10px] for overline */
--line-height-tight: 1rem;         /* 16px - leading-4 for buttons */
--line-height-snug: 1.25rem;       /* 20px - leading-5 for body 2, caption */
--line-height-normal: 1.5rem;      /* 24px - leading-6 for body 1 */
--line-height-relaxed: 1.75rem;    /* 28px - leading-7 for H6 */
--line-height-loose: 2.25rem;      /* 36px - leading-9 for H5 */
--line-height-heading: 2.5rem;     /* 40px - leading-10 for H4 */
--line-height-h3: 3.75rem;         /* 60px - leading-[60px] for H3 */
--line-height-h2: 4.6875rem;       /* 75px - leading-[75px] for H2 */
--line-height-h1: 6.9rem;          /* 110.40px - leading-[110.40px] for H1 */
```

### Text Styles

#### Headings

**H1 - Hero / Display:**
- Font size: `text-8xl` (96px / 6rem)
- Font weight: `font-light` (300)
- Line height: `leading-[110.40px]` (110.40px)
- Font family: `font-['Inter_Display']`
- Usage: Hero sections, landing pages, main display text
- Tailwind: `text-8xl font-light leading-[110.40px] font-['Inter_Display']`

**H2 - Main Heading:**
- Font size: `text-6xl` (60px / 3.75rem)
- Font weight: `font-medium` (500)
- Line height: `leading-[75px]` (75px)
- Font family: `font-['Inter_Display']`
- Usage: Page titles, major section headers
- Tailwind: `text-6xl font-medium leading-[75px] font-['Inter_Display']`

**H3 - Section Heading:**
- Font size: `text-5xl` (48px / 3rem)
- Font weight: `font-medium` (500)
- Line height: `leading-[60px]` (60px)
- Font family: `font-['Inter_Display']`
- Usage: Section headers, content divisions
- Tailwind: `text-5xl font-medium leading-[60px] font-['Inter_Display']`

**H4 - Subsection Heading:**
- Font size: `text-3xl` (30px / 1.875rem)
- Font weight: `font-semibold` (600)
- Line height: `leading-10` (40px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: Subsections, card titles
- Tailwind: `text-3xl font-semibold leading-10 tracking-tight font-['Inter_Display']`

**H5 - Minor Heading:**
- Font size: `text-2xl` (24px / 1.5rem)
- Font weight: `font-medium` (500)
- Line height: `leading-9` (36px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: Small sections, list titles
- Tailwind: `text-2xl font-medium leading-9 tracking-tight font-['Inter_Display']`

**H6 - Smallest Heading:**
- Font size: `text-xl` (20px / 1.25rem)
- Font weight: `font-semibold` (600)
- Line height: `leading-7` (28px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: Component headers, inline titles, toolbar counters
- Tailwind: `text-xl font-semibold leading-7 tracking-tight font-['Inter_Display']`

#### Subtitles

**Subtitle 1:**
- Font size: `text-base` (16px / 1rem)
- Font weight: `font-semibold` (600)
- Line height: `leading-6` (24px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: Product names, table headers, important labels
- Tailwind: `text-base font-semibold leading-6 tracking-tight font-['Inter_Display']`

**Subtitle 2:**
- Font size: `text-sm` (14px / 0.875rem)
- Font weight: `font-bold` (700)
- Line height: `leading-5` (20px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: Small labels, emphasized text, form labels
- Tailwind: `text-sm font-bold leading-5 tracking-tight font-['Inter_Display']`

#### Body Text

**Body 1 - Default:**
- Font size: `text-base` (16px / 1rem)
- Font weight: `font-normal` (400)
- Line height: `leading-6` (24px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: Main content, descriptions, paragraphs
- Tailwind: `text-base font-normal leading-6 tracking-tight font-['Inter_Display']`

**Body 2 - Small:**
- Font size: `text-sm` (14px / 0.875rem)
- Font weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: Secondary content, URLs, dates, metadata
- Tailwind: `text-sm font-normal leading-5 tracking-tight font-['Inter_Display']`

#### Specialized Text

**Button Text:**
- Font size: `text-sm` (14px / 0.875rem)
- Font weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: All button labels, action text
- Tailwind: `text-sm font-semibold leading-4 tracking-tight font-['Inter_Display']`

**Caption:**
- Font size: `text-xs` (12px / 0.75rem)
- Font weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Letter spacing: `tracking-tight`
- Font family: `font-['Inter_Display']`
- Usage: Image captions, help text, footnotes, tertiary labels
- Tailwind: `text-xs font-normal leading-5 tracking-tight font-['Inter_Display']`

**Overline:**
- Font size: `text-[10px]` (10px / 0.625rem)
- Font weight: `font-medium` (500)
- Line height: `leading-[10px]` (10px)
- Letter spacing: `tracking-tight`
- Text transform: `uppercase`
- Font family: `font-['Inter_Display']`
- Usage: Category labels, small headers, kickers
- Tailwind: `text-[10px] font-medium uppercase leading-[10px] tracking-tight font-['Inter_Display']`

#### Tracking (Letter Spacing)

```css
--letter-spacing-tight: -0.01em;  /* tracking-tight - используется повсеместно */
--letter-spacing-normal: 0;
--letter-spacing-wide: 0.025em;
--letter-spacing-wider: 0.05em;
```

### Typography Examples

```jsx
// Typography Showcase Component
<div className="w-[1303px] p-20 bg-shade02-100 rounded-[32px] inline-flex flex-col justify-start items-start gap-16">
  {/* H1 - Hero / Display */}
  <div className="self-stretch justify-start text-white text-8xl font-light font-['Inter_Display'] leading-[110.40px]">
    H1 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* H2 - Main Heading */}
  <div className="justify-start text-white text-6xl font-medium font-['Inter_Display'] leading-[75px]">
    H2 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* H3 - Section Heading */}
  <div className="justify-start text-white text-5xl font-medium font-['Inter_Display'] leading-[60px]">
    H3 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* H4 - Subsection Heading */}
  <div className="justify-start text-white text-3xl font-semibold font-['Inter_Display'] leading-10 tracking-tight">
    H4 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* H5 - Minor Heading */}
  <div className="justify-start text-white text-2xl font-medium font-['Inter_Display'] leading-9 tracking-tight">
    H5 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* H6 - Smallest Heading */}
  <div className="justify-start text-white text-xl font-semibold font-['Inter_Display'] leading-7 tracking-tight">
    H6 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* Subtitle 1 */}
  <div className="justify-start text-white text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight">
    Sub Title 1 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* Subtitle 2 */}
  <div className="justify-start text-white text-sm font-bold font-['Inter_Display'] leading-5 tracking-tight">
    Sub Title 2 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* Body 1 */}
  <div className="justify-start text-white text-base font-normal font-['Inter_Display'] leading-6 tracking-tight">
    Body 1 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* Body 2 */}
  <div className="justify-start text-white text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
    Body 2 - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* Button Text */}
  <div className="self-stretch justify-start text-white text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
    Button - Purchase Now
  </div>

  {/* Caption */}
  <div className="justify-start text-white text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">
    Caption - Going to put a<br/>
    couple lines of text<br/>
    right here.
  </div>

  {/* Overline */}
  <div className="self-stretch justify-start text-white text-[10px] font-medium font-['Inter_Display'] uppercase leading-[10px] tracking-tight">
    Overline - This is an overline
  </div>
</div>
```

### Typography Usage Notes

**When to Use Each Style:**

- **H1 (text-8xl)**: Only for hero sections, landing pages, and major marketing pages. One per page maximum.
- **H2 (text-6xl)**: Main page titles, feature section headers. Typically one per major section.
- **H3 (text-5xl)**: Large content divisions, blog post titles, product showcase headers.
- **H4 (text-3xl)**: Subsection headers, card titles, modal headers.
- **H5 (text-2xl)**: Small section headers, sidebar titles.
- **H6 (text-xl)**: Inline section headers, toolbar counters ("8 new comments"), component titles.
- **Subtitle 1 (text-base semibold)**: Product names in lists, table cell headers, important metadata.
- **Subtitle 2 (text-sm bold)**: Form labels, emphasized secondary text, small headers.
- **Body 1 (text-base)**: Main content, paragraph text, descriptions.
- **Body 2 (text-sm)**: Secondary text, URLs, timestamps, metadata, helper text.
- **Button (text-sm semibold)**: All button labels, CTAs, action links.
- **Caption (text-xs)**: Image captions, footnotes, tertiary information.
- **Overline (text-[10px] uppercase)**: Category labels, tags, small identifiers.

**Accessibility Notes:**
- Maintain proper heading hierarchy (H1 → H2 → H3, etc.)
- Ensure sufficient color contrast (minimum 4.5:1 for body text, 3:1 for large text)
- Use semantic HTML tags (`<h1>`, `<h2>`, etc.) with Tailwind classes
- Don't skip heading levels for visual styling
- Provide adequate line height for readability (already built into text styles)

**Color Usage:**
- Primary text: `text-Text-Primary` (default for headings and body)
- Secondary text: `text-Text-Secondary` (for metadata, helper text)
- Tertiary text: `text-Text-Tertiary` (for placeholders, disabled text)
- Light text: `text-Text-Light` or `text-white` (for dark backgrounds)

---

## Spacing & Layout

### Spacing Scale

```css
--space-0: 0;
--space-0-5: 0.125rem;  /* 2px */
--space-1: 0.25rem;     /* 4px - gap-1, gap-px */
--space-1-5: 0.375rem;  /* 6px */
--space-2: 0.5rem;      /* 8px - gap-2 */
--space-2-5: 0.625rem;  /* 10px - gap-2.5 */
--space-3: 0.75rem;     /* 12px - p-3, gap-3 */
--space-4: 1rem;        /* 16px - p-4, gap-4 */
--space-5: 1.25rem;     /* 20px */
--space-6: 1.5rem;      /* 24px - px-6 */
--space-7: 1.75rem;     /* 28px - px-7 */
--space-8: 2rem;        /* 32px */
--space-10: 2.5rem;     /* 40px */
--space-12: 3rem;       /* 48px */
--space-14: 3.5rem;     /* 56px - py-3.5 */
--space-16: 4rem;       /* 64px */
--space-20: 5rem;       /* 80px */
--space-24: 6rem;       /* 96px */
```

### Border Radius

```css
--radius-none: 0;
--radius-sm: 0.125rem;   /* 2px - rounded-sm */
--radius-xs: 0.25rem;    /* 4px - rounded-[1px] approximately */
--radius-base: 0.313rem; /* 5px - rounded-[5px] для контейнеров */
--radius-md: 0.5rem;     /* 8px - rounded-md */
--radius-lg: 0.75rem;    /* 12px */
--radius-xl: 1rem;       /* 16px */
--radius-2xl: 2rem;      /* 32px - rounded-[32px] для buttons */
--radius-3xl: 3rem;      /* 48px - rounded-[48px] для inputs */
--radius-pill: 5.625rem; /* 90px - rounded-[90px] для круглых элементов */
--radius-full: 9999px;   /* rounded-full для аватаров и точек */
```

### Shadows

#### Card Shadows

```css
--shadow-xs: 0px 1px 2px 0px rgba(0,0,0,0.05); /* Minimal elevation */
--shadow-sm: 0px 1px 4px 0px rgba(0,0,0,0.05); /* Small cards, buttons */
--shadow-base: 0px 2px 4px 0px rgba(0,0,0,0.08), 0px 1px 2px 0px rgba(0,0,0,0.04); /* Default cards */
--shadow-md: 0px 4px 8px -2px rgba(0,0,0,0.1), 0px 2px 4px -2px rgba(0,0,0,0.06); /* Elevated cards */
--shadow-lg: 0px 12px 16px -4px rgba(0,0,0,0.08), 0px 4px 6px -2px rgba(0,0,0,0.03); /* Modals, dropdowns */
--shadow-xl: 0px 24px 32px -12px rgba(18,18,18,0.10), 0px 8px 16px -4px rgba(0,0,0,0.08); /* Large modals, overlays */

/* Popup/Dropdown Shadows (Light Mode) */
--shadow-popup-light: 0px 5px 1.5px -4px rgba(8,8,8,0.09),
                      0px 6px 4px -4px rgba(8,8,8,0.05),
                      0px 6px 13px 0px rgba(8,8,8,0.03),
                      0px 24px 24px -16px rgba(8,8,8,0.04),
                      0px 2.15px 0.5px -2px rgba(0,0,0,0.25),
                      0px 0px 10px 0px rgba(0,0,0,0.05);

/* Popup/Dropdown Shadows (Dark Mode) */
--shadow-popup-dark: 0px 5px 1.5px -4px rgba(8,8,8,0.09),
                     0px 6px 4px -4px rgba(8,8,8,0.05),
                     0px 6px 13px 0px rgba(8,8,8,0.03),
                     0px 24px 24px -16px rgba(8,8,8,0.04),
                     0px 2.15px 0.5px -2px rgba(0,0,0,0.80),
                     0px 0px 10px 0px rgba(0,0,0,1.00);

/* Toggle Knob Shadows (3D effect) */
--shadow-knob: 0px 2px 4px 0px rgba(0,0,0,0.20),
               inset 0px -1px 1px 0px rgba(0,0,0,0.10),
               inset 0px 2px 2px 0px rgba(255,255,255,1.00);
```

#### Button Shadows

```css
--shadow-button-light: inset 2px 0px 8px 2px rgba(24, 24, 24, 0.20); /* Dark mode button */
--shadow-button-dark: inset 2px 0px 8px 2px rgba(248, 248, 248, 0.20); /* Light mode button */
--shadow-button-hover: 0px 4px 8px -2px rgba(0,0,0,0.15), inset 2px 0px 8px 2px rgba(248, 248, 248, 0.25); /* Elevated on hover */
--shadow-button-active: inset 0px 2px 4px 0px rgba(0,0,0,0.15), inset 2px 0px 6px 1px rgba(248, 248, 248, 0.15); /* Pressed state */
```

#### Hover Shadows

```css
--shadow-hover-sm: 0px 2px 8px 0px rgba(0,0,0,0.08); /* Small elements hover */
--shadow-hover-md: 0px 6px 16px -4px rgba(0,0,0,0.12); /* Card hover */
--shadow-hover-lg: 0px 12px 24px -8px rgba(0,0,0,0.15); /* Large card hover */

/* List Item Hover Shadow (Light Mode) */
--shadow-list-hover-light: 0px 1px 4px 0px rgba(0,0,0,0.05),
                           0px 8px 8px -2px rgba(0,0,0,0.08),
                           inset 0px 0px 0px 3px rgba(255,255,255,1.00);

/* Active/Selected Item Shadow */
--shadow-item-active: 0px 1px 4px 0px rgba(0,0,0,0.05),
                      0px 8px 8px -2px rgba(0,0,0,0.08),
                      inset 0px 0px 0px 3px rgba(255,255,255,1.00);
```

### Borders

#### Border Width

```css
--border-width-0: 0;
--border-width-0-5: 0.5px;   /* 0.5px для тонких линий */
--border-width-0-75: 0.75px; /* 0.75px для outline-offset */
--border-width-1: 1px;       /* border */
--border-width-1-5: 1.5px;   /* outline-[1.50px] - основная толщина обводки */
--border-width-2: 2px;
--border-width-4: 4px;
```

#### Border Offset

```css
--border-offset-0: 0;
--border-offset-negative-0-75: -0.75px; /* outline-offset-[-0.75px] для иконок */
--border-offset-negative-1: -1px;
--border-offset-negative-1-5: -1.5px;   /* outline-offset-[-1.50px] - основной offset */
--border-offset-1: 1px;
--border-offset-2: 2px;
```

### Opacity Scale

```css
--opacity-0: 0;        /* opacity-0 для скрытых элементов */
--opacity-10: 0.1;     /* /10 для subtle borders */
--opacity-20: 0.2;
--opacity-30: 0.3;
--opacity-40: 0.4;     /* /40 для shades */
--opacity-50: 0.5;     /* /50 для borders */
--opacity-60: 0.6;     /* /60 для элементов */
--opacity-70: 0.7;
--opacity-80: 0.8;
--opacity-90: 0.9;
--opacity-100: 1;
```

---

## Компоненты

### 1. Cards

#### Basic Card

- **Padding**:
- **Border Radius**:
- **Background**:
- **Shadow**:
- **Border**:

**Варианты:**
-
-
-

#### Пример использования

```css

```

---

### 2. Buttons

#### Primary Button (Gradient)

- **Size**:
  - Small: px-6 py-3 (24px horizontal, 12px vertical), height: 48px
  - Medium: px-7 py-4 (28px horizontal, 16px vertical)
  - Large: px-7 py-4
- **Radius**: 32px (rounded-[32px])
- **Font**: font-semibold, text-sm (14px), leading-4, tracking-tight
- **States**:
  - Default (Light Mode): bg-gradient from-white to-neutral-200, shadow-[inset 2px 0px 8px 2px rgba(24,24,24,0.20)], outline-[1.50px] white/60
  - Default (Dark Mode): bg-gradient from-zinc-800 to-zinc-800, shadow-[inset 2px 0px 8px 2px rgba(248,248,248,0.20)], outline-[1.50px] white/40
  - Hover: (to be defined)
  - Active: (to be defined)
  - Disabled: (to be defined)

##### Primary Button with Icon (Chevron)

Вариант primary button с иконкой справа (обычно chevron для action buttons).

- **Padding**: pl-7 pr-3 py-3 (28px left, 12px right, 12px vertical)
- **Radius**: rounded-[32px]
- **Layout**: inline-flex justify-center items-center gap-3
- **Overflow**: overflow-hidden
- **Text**:
  - Font: text-sm, font-semibold, leading-4, tracking-tight
  - Color: text-Text-Light
- **Icon**:
  - Container: w-6 h-6, relative overflow-hidden
  - Chevron: w-1 h-2, positioned [16px, 10px], origin-top-left rotate-90
  - Outline: outline-[1.50px] outline-offset-[-0.75px] outline-Text-Light
  - Direction: pointing right (rotate-90)

**Light Mode Variant**:
- Background: bg-gradient-to-b from-white to-neutral-200
- Shadow: shadow-[inset_2px_0px_8px_2px_rgba(24,24,24,0.20)]
- Border: outline-[1.50px] outline-offset-[-1.50px] outline-white/60
- Text: text-Text-Light (может быть темный текст)
- Icon: outline-Text-Light

**Dark Mode Variant**:
- Background: bg-gradient-to-b from-zinc-800 to-zinc-800
- Shadow: shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)]
- Border: outline-[1.50px] outline-offset-[-1.50px] outline-white/40
- Text: text-Text-Light
- Icon: outline-Text-Light

**Common Labels**: "Publish now", "Continue", "Next", "Submit"

##### Пример использования

```jsx
// Dark mode variant
<div className="pl-7 pr-3 py-3 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/40 inline-flex justify-center items-center gap-3 overflow-hidden">
  <div className="justify-start text-Text-Light text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Publish now</div>
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-1 h-2 left-[16px] top-[10px] absolute origin-top-left rotate-90 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Light" />
  </div>
</div>

// Light mode variant
<div className="pl-7 pr-3 py-3 bg-gradient-to-b from-white to-neutral-200 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(24,24,24,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/60 inline-flex justify-center items-center gap-3 overflow-hidden">
  <div className="justify-start text-Text-Light text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Publish now</div>
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-1 h-2 left-[16px] top-[10px] absolute origin-top-left rotate-90 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Light" />
  </div>
</div>
```

#### Icon Button (Round)

- **Size**: w-12 h-12 (48x48px)
- **Radius**: 90px (rounded-[90px]) - pill shape
- **Background**:
  - Light mode: Backgrounds-surface2
  - Dark mode: gradient from-zinc-800 to-neutral-800
- **Icon Size**: 24x24px (w-6 h-6)
- **States**:
  - Default: (описано выше)
  - Hover: (to be defined)
  - Active: (to be defined)

#### Icon Button (Small)

Компактная кнопка только с иконкой, без фона по умолчанию.

- **Size**: p-3 (12px padding), total size варьируется
- **Radius**: rounded-[48px]
- **Icon Size**: w-6 h-6 (24x24px container)
  - Inner icon: w-4 h-4 (16x16px)
  - Positioning: left-[3.75px] top-[3.75px] или similar
- **Layout**: inline-flex flex-col justify-center items-center gap-2.5
- **Overflow**: overflow-hidden

##### States

**Default (Inactive)**:
- Background: transparent
- Border: none
- Icon: outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary
- Opacity: может быть normal

**Active/Selected**:
- Background: transparent или slight highlight
- Border: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
- Icon: outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary
- Radius: rounded-[48px]

**Hover**:
- Background: может добавиться subtle background
- Border: может появиться outline-Stroke-Stroke2
- Icon: может измениться на Text-Primary

**Disabled**:
- Opacity: opacity-50
- Cursor: not-allowed
- Icon: Text-Secondary

##### Пример использования

```jsx
// Default state
<div className="p-3 rounded-[48px] inline-flex flex-col justify-center items-center gap-2.5 overflow-hidden">
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-4 h-4 left-[3.75px] top-[3.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
  </div>
</div>

// Active/Selected state
<div className="p-3 rounded-[48px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex flex-col justify-center items-center gap-2.5 overflow-hidden">
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-4 h-4 left-[3.75px] top-[3.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
  </div>
</div>
```

#### Segment Control Button (Tabs)

- **Size**: px-6 py-3 (24px horizontal, 12px vertical), height: 48px
- **Radius**: 48px (rounded-[48px])
- **Font**: font-semibold, text-sm (14px), leading-4, tracking-tight
- **States**:
  - Default: transparent, text-Text-Secondary
  - Active: outline-[1.50px] Stroke-Stroke2, text-Text-Primary
  - Hover: (to be defined)

#### Secondary Button

Простая кнопка с фоном без градиента, используется для менее важных действий.

- **Size**: px-7 py-3.5 (28px horizontal, 14px vertical), height: h-12 (48px)
- **Radius**: rounded-[32px]
- **Font**: font-semibold, text-sm (14px), leading-4, text-center, tracking-tight
- **Layout**: flex justify-center items-center gap-2
- **States**:
  - **Default (Light Mode)**:
    - Background: bg-Backgrounds-pop
    - Border: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
    - Text: text-Text-Secondary
    - Shadow: может иметь subtle shadow
  - **Default (Dark Mode)**:
    - Background: bg-Backgrounds-pop
    - Border: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
    - Text: text-Text-Secondary
  - **Hover**:
    - Background: может стать lighter/darker
    - Border: outline-Stroke-Stroke2 (более выраженная)
    - Text: text-Text-Primary
    - Shadow: может увеличиться
  - **Active/Pressed**:
    - Background: может быть darker
    - Inset shadow: может иметь inset shadow для pressed эффекта
  - **Disabled**:
    - Opacity: opacity-50
    - Cursor: not-allowed
    - Background: bg-Backgrounds-pop
    - Text: text-Text-Secondary
- **Usage**: Используется для второстепенных действий (Cancel, Deselect), как альтернатива primary gradient button
- **Common Labels**: "Cancel", "Deselect", "Back", "Close"

#### Пример использования

```jsx
// Secondary button (Light Mode)
<div className="h-12 px-7 py-3.5 bg-Backgrounds-pop rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-center items-center gap-2">
  <div className="text-center text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Cancel</div>
</div>

// Secondary button (Dark Mode) - similar structure
<div className="h-12 px-7 py-3.5 bg-Backgrounds-pop rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-center items-center gap-2">
  <div className="text-center text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Deselect</div>
</div>

// In a button group (e.g., modal actions)
<div className="self-stretch inline-flex justify-start items-start gap-3">
  <div className="flex-1 h-12 px-7 py-3.5 bg-Backgrounds-pop rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-center items-center">
    <div className="text-center text-Text-Secondary text-sm font-semibold leading-4 tracking-tight">Cancel</div>
  </div>
  <div className="flex-1 px-7 py-4 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px] flex justify-center items-center">
    <div className="text-center text-Text-Primary text-sm font-semibold leading-4 tracking-tight">Confirm</div>
  </div>
</div>
```

---

### 3. Inputs

#### Password Input

- **Height**: 48px (h-12)
- **Padding**: px-28 (horizontal 28px for text area)
- **Radius**: 48px (rounded-[48px])
- **Border**: outline-[1.50px] outline-offset-[-1.50px]
- **Font**:
  - Placeholder dots: 6px dots (w-1.5 h-1.5), gap-1, bg-Text-Tertiary
  - Text: font-medium text-sm 'ES Build', bg-Text-Primary
- **Label**:
  - Position: floating label, px-1 py-0.5, bg-Backgrounds-surface2
  - Font: text-xs, text-Text-Primary, leading-5, tracking-tight
  - Offset: left-[24px], top-0
- **Helper Text**:
  - Position: right side, data-state="default"
  - Font: text-xs, text-Text-Secondary
  - Example: "Forgot password?"
- **Cursor**: w-0.5 h-4 bg-Text-Blue rounded-sm (мигающая каретка)
- **States**:
  - Default: outline-Stroke-Stroke2
  - Hover: outline-shade07-50/50
  - Focus: outline-shade07-50/50, cursor visible
  - Error: outline-Primary-primary03
  - Disabled: (to be defined)
- **Icons**:
  - Eye icon (show/hide): w-6 h-6, right-[12px], top-[12px]

#### Search Input

- **Size**: w-60 pl-3 pr-5 py-3 (240px width default, можно w-72 или w-80)
- **Height**: 48px (h-12)
- **Radius**: 90px (rounded-[90px]) - pill shape
- **Layout**: flex justify-start items-center gap-2
- **Border**: outline-[1.50px] outline-offset-[-1.50px]
- **Overflow**: overflow-hidden
- **Icon**: Search icon w-6 h-6 (24x24px), left aligned, gap-2 от текста
- **Placeholder/Text**: text-sm, font-normal, leading-5, tracking-tight
- **Cursor**: w-0 h-4 (0.5px width, 16px height) rounded-sm, bg-Primary-primary01 (синий)

**States**:

##### Default (Light Mode)
- **Background**: bg-Backgrounds-surface1
- **Border**: none или outline-Stroke-Subtle/10 (very subtle)
- **Placeholder**: text-Text-Secondary
- **Icon**: outline-[1.50px] outline-Text-Secondary

##### Default (Dark Mode)
- **Background**: bg-Backgrounds-surface1
- **Border**: none
- **Placeholder**: text-Text-Secondary
- **Icon**: outline-[1.50px] outline-Text-Secondary

##### Hover (Light Mode)
- **Background**: bg-Backgrounds-surface2
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Shadow**: shadow-[0px_5px_1.5px_-4px_...] (popup shadows)
- **Placeholder**: text-Text-Secondary
- **Icon**: без изменений

##### Focus/Active (Light Mode)
- **Background**: bg-Backgrounds-surface2
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Shadow**: может быть subtle shadow
- **Text**: text-Text-Primary
- **Icon**: outline-[1.50px] outline-Text-Blue (синий accent)
- **Cursor**: visible, мигающий
- **Clear Button**: w-6 h-6, opacity-50 или visible (опционально)

##### Focus/Active (Pressed/Dark Mode)
- **Background**: bg-Backgrounds-surface2
- **Shadow**:
  - shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)] (light)
  - shadow-[inset_0px_4px_4px_0px_rgba(157,157,157,0.10)] (light)
  - shadow-[inset_0px_0px_0px_3px_rgba(40,40,40,0.10)] (dark)
  - shadow-[inset_0px_4px_4px_0px_rgba(18,18,18,0.81)] (dark)
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Icon**: outline-[1.50px] outline-Text-Blue
- **Cursor**: visible

##### Disabled
- **Background**: bg-Backgrounds-surface1
- **Opacity**: opacity-50 на всем input
- **Cursor**: not-allowed
- **Border**: может быть более прозрачным

##### With Clear Button
- **Layout**: justify-between вместо justify-start
- **Left Section**: icon + text/placeholder
- **Right Section**: clear button (x icon)
- **Clear Button**: w-6 h-6, opacity-50 (default), можно hover для full opacity
- **Padding Right**: p-3 для размещения clear button

#### Пример использования

```jsx
// Default state (Light Mode)
<div className="w-60 pl-3 pr-5 py-3 bg-Backgrounds-surface1 rounded-[90px] inline-flex justify-start items-center gap-2 overflow-hidden">
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
    <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
  </div>
  <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Search products</div>
</div>

// Hover state (Light Mode)
<div className="w-60 pl-3 pr-5 py-3 bg-Backgrounds-surface2 rounded-[90px] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-start items-center gap-2 overflow-hidden">
  {/* Same content */}
</div>

// Focus/Active state with cursor
<div className="w-60 p-3 bg-Backgrounds-surface2 rounded-[90px] shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-between items-center overflow-hidden">
  <div className="flex justify-start items-center gap-2">
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Blue" />
      {/* Search icon in blue */}
    </div>
    <div className="h-6 py-1 flex justify-start items-center gap-1">
      <div className="justify-start text-Text-Primary text-sm font-normal leading-5 tracking-tight">Search products</div>
      <div className="w-0 h-4 outline outline-[1.50px] outline-offset-[-0.75px] outline-Primary-primary01" />
    </div>
  </div>
  <div className="w-6 h-6 relative overflow-hidden">
    {/* Clear button (optional) */}
  </div>
</div>
```

#### Select / Dropdown

- **Size**: max-w-44 pl-5 pr-3 py-3, height: 48px
- **Radius**: 90px (rounded-[90px])
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Text**: text-sm, text-Text-Secondary, leading-5, tracking-tight
- **Icon**: Chevron down, w-6 h-6, right aligned
- **Example**: "Last 7 days"

#### Text Input with Floating Label

Текстовый input с плавающей меткой (label), которая располагается над полем ввода.

- **Container**: inline-flex flex-col justify-start items-start
- **Input Field**:
  - Height: h-12 (48px)
  - Padding: pl-[28px] (horizontal padding for text)
  - Radius: rounded-[48px]
  - Border: outline-[1.50px] outline-offset-[-1.50px]
  - Overflow: overflow-hidden
  - Font: text-sm, font-normal, leading-5, tracking-tight

##### Floating Label
- **Container**: h-3 px-6, positioned над input
- **Label Badge**:
  - Padding: px-1 py-0.5
  - Background: bg-Backgrounds-surface2 или bg-Backgrounds-surface1
  - Font: text-xs, font-normal, leading-5, tracking-tight
  - Color: text-Text-Primary
  - Layout: inline-flex justify-center items-center gap-0.5
- **Positioning**: Label "плавает" над верхней границей input

##### Input States

**Default (Empty)**:
- Border: outline-Stroke-Stroke2
- Placeholder: opacity-50, text-Text-Secondary
- Label background: bg-Backgrounds-surface2

**Hover**:
- Border: outline-shade07-50/50
- Placeholder: text-Text-Secondary
- Label background: bg-Backgrounds-surface1

**Focus/Active**:
- Border: outline-shade07-50/50
- Cursor: w-0.5 h-4 bg-Text-Blue visible
- Placeholder: может скрыться
- Text: text-Text-Primary (при вводе)
- Label background: bg-Backgrounds-surface2

**Filled (Success)**:
- Border: outline-shade07-50/50 или outline-Stroke-Stroke2
- Text: text-Text-Primary
- Success Icon: w-6 h-6 checkmark icon справа
  - Icon color: outline-Primary-primary02 (зеленый)
  - Position: absolute, right side
- Label visible

**Error**:
- Border: outline-Primary-primary03 (красная обводка)
- Text: text-Text-Primary
- Cursor: w-0.5 h-4 bg-Text-Blue visible
- Error Message: под input
  - Font: text-xs, font-normal, leading-5, tracking-tight
  - Color: text-Primary-primary03
  - Gap: gap-2 от input
  - Example: "Please enter an email address."

**Disabled**:
- Opacity: opacity-50
- Cursor: not-allowed
- Border: может быть более прозрачным

##### Пример использования

```jsx
// Default state with floating label
<div className="w-80 inline-flex flex-col justify-start items-start">
  <div className="self-stretch h-3 px-6 flex flex-col justify-center items-start gap-2">
    <div className="h-5 px-1 py-0.5 bg-Backgrounds-surface2 inline-flex justify-center items-center gap-0.5">
      <div className="justify-start text-Text-Primary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Component name</div>
    </div>
  </div>
  <div className="self-stretch h-12 relative rounded-[48px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 overflow-hidden">
    <div className="left-[28px] top-[14px] absolute opacity-50 justify-center text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">ie. Bento Cards: User Interface</div>
  </div>
</div>

// Error state
<div className="w-80 inline-flex flex-col justify-start items-center gap-2">
  <div className="self-stretch flex flex-col justify-start items-start">
    <div className="self-stretch h-3 px-6 flex flex-col justify-center items-start gap-2">
      <div className="h-5 px-1 py-0.5 bg-Backgrounds-surface1 inline-flex justify-center items-center gap-0.5">
        <div className="justify-start text-Text-Primary text-xs font-normal leading-5 tracking-tight">Component name</div>
      </div>
    </div>
    <div className="self-stretch h-12 relative rounded-[48px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Primary-primary03 overflow-hidden">
      <div className="left-[26px] top-[15px] absolute inline-flex justify-start items-center">
        <div className="justify-center text-Text-Primary text-sm font-normal leading-5 tracking-tight">adkahdfl</div>
        <div className="w-0.5 h-4 bg-Text-Blue rounded-sm" />
      </div>
    </div>
  </div>
  <div className="self-stretch justify-start text-Primary-primary03 text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Please enter an email address.</div>
</div>
```

#### Tags Input (Multi-select Input)

Компонент для ввода множественных тегов/значений с возможностью добавления и удаления.

- **Container**:
  - Padding: p-2 или p-2.5 (8px или 10px)
  - Radius: rounded-[32px] (Light) или rounded-[20px] (некоторые варианты)
  - Border: outline-[1.50px] outline-offset-[-1.50px]
  - Layout: inline-flex justify-start items-center gap-1.5 flex-wrap content-center
  - Overflow: overflow-hidden

##### Container States

**Default (Empty)**:
- Border: outline-Stroke-Stroke2
- Placeholder: opacity-50, text-Text-Secondary
- Font: text-sm, font-normal, leading-5, tracking-tight
- Placeholder position: left-[10px] top-[4px]
- Example: "i.e. Dashboard, Light, Responsive"

**Hover**:
- Border: outline-shade07-50/50
- Placeholder: text-Text-Secondary

**Focus/Active (Empty)**:
- Border: outline-shade07-50/50
- Cursor: w-0.5 h-4 bg-Text-Blue visible
- Cursor positioned с placeholder text

**Focus with Text**:
- Border: outline-shade07-50/50
- Cursor: visible после текста
- Может показывать частично введенный текст
- Highlight введенного текста: text-Text-Primary
- Остаток placeholder: text-Text-Secondary, opacity-50

**With Tags (Filled)**:
- Border: outline-Stroke-Stroke2 или outline-Stroke-BorderBorder
- Contains multiple tag chips
- Tags layout: flex-wrap
- Gap: gap-1.5 между тегами
- Может содержать cursor или новый placeholder

##### Content Layout

**Empty State**:
- w-72 h-7 relative container с placeholder

**With Single Tag + Cursor**:
- Tag chip (см. Tag/Chip specs)
- Cursor: w-0.5 h-4 bg-Text-Blue

**With Multiple Tags**:
- Multiple tag chips wrapped
- Each tag: h-8 px-3 bg-Backgrounds-surface1 rounded-[32px]
- Gap: gap-1.5 между элементами
- Может показывать частично введенный текст

##### Input Field Inside

- **Placeholder**: opacity-50, text-Text-Secondary
- **Input Text**: text-Text-Primary (при вводе)
- **Cursor**: w-0.5 h-4 bg-Text-Blue rounded-sm
- **Font**: text-sm, font-normal, leading-5, tracking-tight

##### Пример использования

```jsx
// Empty state
<div className="self-stretch p-2.5 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-start items-center gap-1.5 flex-wrap content-center overflow-hidden">
  <div className="w-72 h-7 relative">
    <div className="left-[10px] top-[4px] absolute opacity-50 justify-center text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">i.e. Dashboard, Light, Responsive</div>
  </div>
</div>

// Focus with cursor
<div className="self-stretch p-2.5 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-shade07-50/50 inline-flex justify-start items-center gap-1.5 flex-wrap content-center overflow-hidden">
  <div className="w-72 h-7 relative">
    <div className="h-5 py-0.5 left-[10px] top-[4px] absolute inline-flex justify-start items-center">
      <div className="w-0.5 h-4 bg-Text-Blue rounded-sm" />
      <div className="opacity-50 justify-center text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">i.e. Dashboard, Light, Responsive</div>
    </div>
  </div>
</div>

// With single tag and cursor
<div className="self-stretch p-2 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-shade07-50/50 inline-flex justify-start items-center gap-1.5 flex-wrap content-center overflow-hidden">
  <div className="h-8 px-3 bg-Backgrounds-surface1 rounded-[32px] flex justify-start items-center gap-1.5 overflow-hidden">
    <div className="justify-center text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Dashboard</div>
    <div className="w-3 h-3 relative overflow-hidden">
      <div className="w-2 h-2 left-[2.38px] top-[2.38px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Tertiary" />
    </div>
  </div>
  <div className="w-0.5 h-4 bg-Text-Blue rounded-sm" />
</div>

// Typing with partial text
<div className="self-stretch p-2 relative rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-shade07-50/50 inline-flex justify-start items-center gap-1.5 flex-wrap content-center overflow-hidden">
  <div className="h-8 px-3 bg-Backgrounds-surface1 rounded-[32px] flex justify-start items-center gap-1.5 overflow-hidden">
    <div className="justify-center text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Dashboard</div>
    <div className="w-3 h-3 relative overflow-hidden">
      <div className="w-2 h-2 left-[2.38px] top-[2.38px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Tertiary" />
    </div>
  </div>
  <div className="opacity-50 justify-center">
    <span className="text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Res</span>
    <span className="text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">ponsive</span>
  </div>
  <div className="w-0.5 h-4 left-[142px] top-[16px] absolute bg-Text-Blue rounded-sm" />
</div>

// With multiple tags
<div className="self-stretch p-2 rounded-[20px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-start items-center gap-1.5 flex-wrap content-center overflow-hidden">
  <div className="h-8 px-3 bg-Backgrounds-surface1 rounded-[32px] flex justify-start items-center gap-1.5 overflow-hidden">
    <div className="justify-center text-Text-Primary text-sm font-normal">Dashboard</div>
    <div className="w-3 h-3 relative overflow-hidden">
      <div className="w-2 h-2 left-[2.38px] top-[2.38px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Tertiary" />
    </div>
  </div>
  <div className="h-8 px-3 bg-Backgrounds-surface1 rounded-[32px] flex justify-start items-center gap-1.5 overflow-hidden">
    <div className="justify-center text-Text-Primary text-sm font-normal">Light</div>
    <div className="w-3 h-3 relative overflow-hidden">
      <div className="w-2 h-2 left-[2.38px] top-[2.38px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Tertiary" />
    </div>
  </div>
  <div className="h-8 px-3 bg-Backgrounds-surface1 rounded-[32px] flex justify-start items-center gap-1.5 overflow-hidden">
    <div className="justify-center text-Text-Primary text-sm font-normal">Responsive</div>
    <div className="w-3 h-3 relative overflow-hidden">
      <div className="w-2 h-2 left-[2.38px] top-[2.38px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Tertiary" />
    </div>
  </div>
  {/* More tags... */}
</div>
```

---

### 4. Badges & Tags

#### Status Badge (Small)

Компактный badge для отображения статуса элементов.

- **Padding**: px-2 py-1.5 (8px horizontal, 6px vertical)
- **Height**: auto (определяется padding)
- **Radius**: rounded-lg (12px)
- **Border**: outline-[1.50px] outline-offset-[-1.50px]
- **Layout**: inline-flex justify-center items-center gap-2
- **Overflow**: overflow-hidden
- **Font**: text-sm, font-semibold, leading-4, tracking-tight
- **Variants**:
  - **Success/Active**:
    - Background: bg-green-600/5
    - Border: outline-green-600/20
    - Text: text-Primary-primary02
    - Label: "Active"
  - **Error/Offline**:
    - Background: bg-red-600/5 (или bg-red-400/5)
    - Border: outline-red-600/20 (или outline-red-400/20)
    - Text: text-Primary-primary03
    - Label: "Offline"
  - **Warning**: (to be defined)
  - **Info**: (to be defined)
  - **Neutral**: (to be defined)
- **Usage**: в таблицах, карточках, списках для отображения статуса

#### Пример использования

```jsx
// Active badge
<div className="px-2 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 inline-flex justify-center items-center gap-2 overflow-hidden">
  <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Active</div>
</div>

// Offline badge
<div className="px-2 py-1.5 bg-red-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-red-600/20 inline-flex justify-center items-center gap-2 overflow-hidden">
  <div className="justify-start text-Primary-primary03 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Offline</div>
</div>
```

#### Trend Badge (с иконкой)

- **Padding**: px-2 py-1.5 (8px horizontal, 6px vertical)
- **Radius**: rounded-lg (12px)
- **Border**: outline-[1.50px] outline-offset-[-1.50px]
- **Font**: text-sm, font-semibold, leading-4, tracking-tight
- **Icon**: w-4 h-4, arrow up/down
- **Gap**: gap-1 между icon и text
- **Variants**:
  - **Trend Up**: bg-green-600/5, outline-green-600/20, text-Primary-primary02, arrow up
  - **Trend Down**: bg-red-400/5, outline-red-400/20, text-red-400, arrow down
- **Example**: "36.8%" с стрелкой

#### Tag / Chip

Компактный компонент для отображения меток, тегов или выбранных элементов с возможностью удаления.

- **Size**: h-8 px-3 (32px height, 12px horizontal padding)
- **Radius**: rounded-[32px] (полностью скругленный)
- **Background**: bg-Backgrounds-surface1
- **Layout**: flex justify-start items-center gap-1.5
- **Overflow**: overflow-hidden
- **Font**: text-sm, font-normal, leading-5, tracking-tight
- **Color**: text-Text-Primary

##### Close Icon (X)
- **Container**: w-3 h-3 (12x12px)
- **Icon**: w-2 h-2 (8x8px), positioned [2.38px, 2.38px]
- **Outline**: outline-[1.50px] outline-offset-[-0.75px]
- **States**:
  - **Default**: outline-Text-Tertiary (серый)
  - **Hover/Active**: outline-Text-Primary (темный/активный)

##### Tag States

**Default**:
- Background: bg-Backgrounds-surface1
- Text: text-Text-Primary
- Close icon: outline-Text-Tertiary

**Hover**:
- Close icon может измениться на Text-Primary
- Может появиться subtle shadow
- Background: может слегка подсветиться

**Active/Interactive**:
- Close icon: outline-Text-Primary
- Может быть более выраженная обводка

**Disabled**:
- Opacity: opacity-50
- Close icon: может быть скрыт
- Cursor: not-allowed

##### Пример использования

```jsx
// Default tag
<div className="h-8 px-3 bg-Backgrounds-surface1 rounded-[32px] flex justify-start items-center gap-1.5 overflow-hidden">
  <div className="justify-center text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Dashboard</div>
  <div className="w-3 h-3 relative overflow-hidden">
    <div className="w-2 h-2 left-[2.38px] top-[2.38px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Tertiary" />
  </div>
</div>

// Active/Hover tag
<div className="h-8 px-3 bg-Backgrounds-surface1 rounded-[32px] flex justify-start items-center gap-1.5 overflow-hidden">
  <div className="justify-center text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Dashboard</div>
  <div className="w-3 h-3 relative overflow-hidden">
    <div className="w-2 h-2 left-[2.38px] top-[2.38px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
  </div>
</div>
```

---

### 5. Forms

#### Form Layout

- **Label**:
  - Margin Bottom:
  - Font Weight:
  - Font Size:
- **Field Group**:
  - Margin Bottom:
- **Helper Text**:
  - Margin Top:
  - Font Size:
  - Color:
- **Error Message**:
  - Color:
  - Font Size:

#### Label with Info Icon

Label с иконкой информации и tooltip для дополнительных пояснений.

- **Container**: inline-flex justify-start items-center gap-1.5
- **Label Text**:
  - Font: text-sm, font-semibold, leading-4, tracking-tight
  - Color: text-Text-Primary
  - Example: "Product title"
- **Info Icon**:
  - Size: w-4 h-4 (16x16px container)
  - Icon: circle with 'i' или question mark
  - Outline: outline-[1.50px] outline-offset-[-0.75px]
- **Tooltip** (при hover/click):
  - Position: data-position="right" (или top, bottom, left)
  - Container: px-2 py-1.5, bg-Backgrounds-dark1, rounded-md
  - Font: text-xs, font-normal, leading-5, tracking-tight
  - Color: text-Text-Light
  - Arrow: w-2 h-1, rotate-90, bg-Backgrounds-dark1
  - Max Width: может быть ограничена
  - Example: "Maximum 100 characters. No HTML or emoji allowed"

##### States

**Default**:
- Icon opacity: opacity-50
- Icon color: outline-Text-Tertiary
- Tooltip: hidden

**Hover/Active**:
- Icon opacity: 1 (full opacity)
- Icon color: outline-Text-Blue (синий accent)
- Tooltip: visible
- Может быть дополнительный info icon w-8 h-8

##### Пример использования

```jsx
// Default state
<div className="inline-flex justify-start items-center gap-1.5">
  <div className="justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Product title</div>
  <div className="w-4 h-4 relative opacity-50">
    <div className="w-3 h-3 left-[2px] top-[2px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Tertiary" />
    <div className="w-[1.50px] h-[1.50px] left-[7.25px] top-[10.40px] absolute bg-Text-Tertiary" />
    <div className="w-1 h-1 left-[6.35px] top-[4.40px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Tertiary" />
  </div>
</div>

// Hover/Active with tooltip
<div className="inline-flex justify-start items-center gap-1.5">
  <div className="justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Product title</div>
  <div className="w-4 h-4 relative">
    <div className="w-3 h-3 left-[2px] top-[2px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Blue" />
    <div className="w-[1.50px] h-[1.50px] left-[7.25px] top-[10.40px] absolute bg-Text-Blue" />
    <div className="w-1 h-1 left-[6.35px] top-[4.40px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Blue" />
  </div>
  <div data-position="right" className="flex justify-start items-center">
    <div className="w-2 h-1 origin-top-left rotate-90 bg-Backgrounds-dark1" />
    <div className="h-5 px-2 py-1.5 bg-Backgrounds-dark1 rounded-md flex justify-center items-center gap-2">
      <div className="justify-start text-Text-Light text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Maximum 100 characters. No HTML or emoji allowed</div>
    </div>
  </div>
</div>
```

---

### 6. Tables

#### Table Structure

- **Row Height**:
  - Default: h-16 (64px) с p-4 (16px padding)
  - Header: h-12 (48px) с p-4
  - Compact: (to be defined)
  - Comfortable: (to be defined)
- **Cell Padding**: p-4 (16px all sides)
- **Layout**: inline-flex justify-start items-start gap-6
- **Border Radius**: округлые углы не применяются к строкам
- **Overflow**: overflow-hidden на контейнере

#### Table Header Row

- **Padding**: p-4 (16px)
- **Height**: auto (определяется содержимым)
- **Border Bottom**: border-b-[1.50px] border-Stroke-Subtle/10 или border-Stroke-Subtle
- **Layout**: inline-flex justify-start items-center gap-6
- **Checkbox**: w-6 h-6 с gap-5 от следующего элемента
- **Font**: text-xs, font-normal, leading-5, tracking-tight
- **Color**: text-Text-Tertiary (80% opacity)
- **Column Labels**: aligned по содержимому (Product, Status, Price, Sales, Views, Like)
- **Column Widths**:
  - Product column: w-96 (384px)
  - Status: w-20 (80px)
  - Price: w-14 (56px)
  - Sales: w-36 (144px)
  - Views/Like: w-24 (96px each)

#### Table Row (Default)

- **Padding**: p-4 (16px)
- **Layout**: inline-flex justify-start items-start gap-6
- **Border Bottom**: border-b-[1.50px] border-Stroke-Subtle/10 (light) или border-Stroke-Subtle (dark)
- **Background**: transparent
- **Components**:
  - Checkbox: w-6 h-6
  - Image: w-16 h-16 (64x64px), rounded-xl (16px)
  - Content sections с gap-6 между ними

#### Table Row States

##### Default State
- **Background**: transparent
- **Border Bottom**: border-b-[1.50px] border-Stroke-Subtle/10
- **Text**: text-Text-Primary
- **Transition**: none

##### Hover State (Light Mode)
- **Background**: bg-Backgrounds-highlight, rounded-2xl (16px)
- **Shadow**:
  - shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)]
  - shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)]
  - shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)]
- **Border**: outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100
- **Action Buttons**: появляются Edit, Delete, Share кнопки
- **Checkbox Border**: может измениться на border-Stroke-Stroke2 или border-Stroke-Highlight/50

##### Hover State (Dark Mode)
- **Background**: bg-Backgrounds-highlight, rounded-2xl (16px)
- **Border**: outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100
- **No inset shadow**: только внешний outline
- **Action Buttons**: появляются
- **Checkbox Border**: border-Stroke-Highlight/50

##### Selected/Active State
- Аналогичен Hover State, но остается после снятия курсора
- Checkbox: checked состояние

##### Loading/Skeleton State
- **Background**: bg-Backgrounds-surface1 (light) или bg-Backgrounds-pop (dark)
- **Skeleton elements**:
  - Image placeholder: w-16 h-16, bg-Backgrounds-surface1/pop, rounded-xl
  - Text placeholders: h-2, различные ширины (w-44, w-20, w-14, w-32), bg-Backgrounds-surface1/pop, rounded-sm
  - Positioned: left-0 top-[8px] или top-[10px] для vertical centering
- **Animation**: pulse или shimmer effect

#### Row Content Layout

##### Product Column (w-96)
- **Layout**: flex justify-start items-center gap-5
- **Checkbox**: w-6 h-6
- **Image**: w-16 h-16, rounded-xl
- **Content**: flex-1 flex-col
  - Title: text-base, font-semibold, leading-6, tracking-tight, line-clamp-1
  - Subtitle: text-sm, font-normal, leading-5, tracking-tight, text-Text-Secondary, opacity-80

##### Product Column (with actions on hover)
- **Layout**: flex-1 relative
- **Title**: positioned at top
- **Action Buttons Row**: positioned at bottom (top-[34px])
  - Layout: inline-flex gap-2
  - Button: pl-1 pr-1.5 py-1, rounded-md
  - States: default (no outline), hover (outline-[1.50px] outline-Stroke-Stroke2)

##### Metadata Columns
- **Layout**: flex-1 py-2 flex justify-between items-center
- **Each column**: inline-flex flex-col gap-2.5
- **Column types**:
  - Status: w-20, contains badge
  - Price: w-14, text-sm text-Text-Primary
  - Sales: w-36, includes price + trend badge
  - Views/Like: w-24, mini progress indicator

#### Table Row Variants

##### Simple Row (without image)
- Checkbox + Text content
- Layout: flex gap-5

##### Row with Image & Metadata
- Checkbox + Image + Title/Subtitle + Multiple metadata columns
- Most common variant

##### Row with Date Range
- Checkbox + Image + Title + Date range (subtitle) + Sales + Progress bar
- Subtitle: "25 Sep - 4 Oct" format

##### Row with Action Buttons
- Shows Edit, Delete, Share on hover
- Buttons appear below title in product column

---

### 7. Action Buttons (Small)

#### Small Action Button (Inline)

Используется для действий в строках таблиц (Edit, Delete, Share) или других компактных интерфейсах.

- **Padding**: pl-1 pr-1.5 py-1 (4px left, 6px right, 4px top/bottom)
- **Radius**: rounded-md (8px)
- **Layout**: flex justify-start items-center gap-1
- **Border**: none по умолчанию
- **Height**: auto (определяется padding, ~24px)
- **Components**:
  - Icon: w-4 h-4 (16x16px)
  - Text: text-sm, font-semibold, leading-4, tracking-tight
- **States**:
  - **Default**:
    - Background: transparent
    - Border: none
    - Text: text-Text-Secondary, opacity-80
    - Icon: outline-[1.50px] outline-Text-Secondary
  - **Hover**:
    - Background: transparent или subtle
    - Border: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
    - Text: text-Text-Primary, opacity-80
    - Icon: outline-[1.50px] outline-Text-Primary
  - **Active/Pressed**:
    - Background: может быть подсвечен
    - Border: outline-[1.50px] outline-Stroke-Stroke2
  - **Disabled**:
    - Opacity: opacity-50
    - Cursor: not-allowed

#### Common Action Button Variants

##### Edit Button
- Icon: pen/edit icon, w-4 h-4
- Text: "Edit"
- Color: text-Text-Secondary (default), text-Text-Primary (hover)

##### Delete Button
- Icon: trash/delete icon, w-4 h-4
- Text: "Delete"
- Color: text-Text-Secondary (default), можно использовать text-Primary-primary03 для delete warning

##### Share Button
- Icon: share icon, w-4 h-4
- Text: "Share"
- Color: text-Text-Secondary (default), text-Text-Primary (hover)

#### Пример использования

```jsx
// Default state
<div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
  <div className="w-4 h-4 relative overflow-hidden">
    <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
  </div>
  <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Edit</div>
</div>

// Hover state
<div className="pl-1 pr-1.5 py-1 rounded-md outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-start items-center gap-1">
  <div className="w-4 h-4 relative overflow-hidden">
    <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
  </div>
  <div className="opacity-80 justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Edit</div>
</div>
```

---

### 8. Progress Indicators

#### Mini Progress Bar (Time Indicator)

Компактный индикатор прогресса с текстовой меткой, используется для отображения времени или небольших значений.

- **Container**:
  - Padding: py-0.5 (2px vertical)
  - Radius: rounded-lg (12px)
  - Layout: inline-flex justify-center items-center gap-2
  - Width: auto (определяется содержимым)
- **Label**:
  - Width: w-8 (32px) - фиксированная ширина для выравнивания
  - Font: text-sm, font-normal, leading-5, tracking-tight
  - Color: text-Text-Primary
  - Example: "48m", "2h", "15s"
- **Progress Bar**:
  - Container: w-8 h-1.5 (32px width, 6px height), bg-shade07-40/40, rounded-sm
  - Fill: absolute positioned, various widths (w-1, w-3, w-5, w-6 из w-8 max)
  - Fill Color: bg-Chart-Green (или другие цвета для различных статусов)
  - Fill Radius: rounded-sm
- **Variants**:
  - Multiple states: разная ширина заполнения для отображения прогресса
  - Color variants: Chart-Green (success), можно добавить warning, error цвета

#### Full Progress Bar

Используется для отображения прогресса задач, загрузки и других процессов.

- **Container**: h-3 (12px height), relative
- **Background Sections**:
  - Base section: w-24 (или другая ширина), bg-shade07-40/40, rounded-[1px]
  - Separator dots: w-0.5 h-3, bg-shade07-60/60, rounded-[0.50px], gap-px между точками
  - Progress section: variable width, gradient или solid color
- **Progress Fill**:
  - Gradient variant: bg-gradient-to-r from-shade08-100 to-shade09-100, rounded-[1px]
  - Solid variant: bg-Chart-Green, rounded-[1px]
  - Border: border border-Stroke-Stroke2 (опционально)
- **Layout**: inline-flex gap-0.5 между секциями
- **Usage**: показывает completion percentage с визуальными разделителями

#### Пример использования

```jsx
// Mini progress indicator
<div className="py-0.5 rounded-lg inline-flex justify-center items-center gap-2">
  <div className="w-8 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">48m</div>
  <div className="w-8 h-1.5 relative bg-shade07-40/40 rounded-sm">
    <div className="w-6 h-1.5 left-0 top-0 absolute bg-Chart-Green rounded-sm" />
  </div>
</div>

// Full progress bar with sections
<div className="h-3 relative">
  <div className="left-0 top-0 absolute inline-flex justify-start items-start gap-0.5">
    <div className="w-24 h-3 bg-shade07-40/40 rounded-[1px]" />
    <div className="flex justify-start items-center gap-px">
      <div className="w-0.5 h-3 bg-shade07-60/60 rounded-[0.50px]" />
      <!-- More separator dots -->
    </div>
    <div className="w-60 h-3 bg-gradient-to-r from-shade08-100 to-shade09-100 rounded-[1px] border border-Stroke-Stroke2" />
  </div>
</div>
```

---

### 9. Navigation

#### Main Navigation / Header

- **Height**: 176px (container)
- **Background**: transparent
- **Spacing**: px-16 py-20 (80px top/bottom, 80px left/right from edges)
- **Layout**: flex justify-between items-center
- **Components**:
  - Title: text-3xl font-semibold text-Text-Primary leading-10 tracking-tight
  - Search: w-80 search input
  - Create Button: primary gradient button
  - Icon Buttons: gap-3 между элементами
  - Avatar: последний элемент справа

#### Pagination Navigation

- **Button Size**: w-12 h-12 (48x48px)
- **Radius**: rounded-[90px]
- **Border**: outline-[1.50px] outline-Stroke-Stroke2 (active)
- **Icon Size**: w-6 h-6 (24x24px)
- **Layout**: inline-flex gap-1
- **States**:
  - Default: transparent, text-Text-Secondary
  - Active: outline-Stroke-Stroke2, text-Text-Primary
  - Disabled: (to be defined)
- **Icons**: Arrow left/right icons

#### Sidebar Navigation

##### Navigation Menu Item

Основной элемент бокового меню навигации.

- **Padding**: p-3 (12px all sides)
- **Height**: h-11 (44px)
- **Radius**: rounded-xl (16px)
- **Layout**: inline-flex justify-start items-center gap-3
- **Overflow**: overflow-hidden
- **Font**: text-sm, font-semibold, leading-4, tracking-tight

##### Menu Item Components

- **Icon Container**: w-6 h-6, relative overflow-hidden
  - Icon: w-4 h-4 (или другие размеры), positioned left-[3px] top-[3px]
  - Outline: outline-[1.50px] outline-offset-[-0.75px]
- **Text**: flex-1 justify-start
  - Opacity: opacity-80 для secondary text
- **Chevron Icon** (опционально): w-6 h-6, right aligned
  - Down: rotate-90
  - Right: -rotate-90
- **Number Badge** (опционально): w-6 h-6 px-2 py-1

##### Menu Item States

**Default State**:
- **Background**: transparent
- **Text**: text-Text-Secondary, opacity-80
- **Icon**: outline-Text-Secondary

**Active/Selected State (Light Mode)**:
- **Background**: bg-Backgrounds-pop
- **Radius**: rounded-xl
- **Shadow**:
  - shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)]
  - shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)]
  - shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)]
  - shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)]
  - shadow-[0px_2.15px_0.5px_-2px_rgba(0,0,0,0.25)]
- **Border**: outline-1 outline-offset-[-1px] outline-neutral-200/50
- **Text**: text-Text-Primary (no opacity)
- **Icon**: outline-Text-Primary

**Active/Selected State (Dark Mode)**:
- Same as Light Mode but может иметь другие shadow значения

**Hover State**:
- Similar to Active but less prominent
- Can use lighter background or subtle shadow

##### Tree Navigation (Nested Items)

Для вложенных пунктов меню с визуальными соединительными линиями.

- **Container**: w-9 h-11 (или h-7 для top position), relative
- **Tree Line**: w-3, variable height (h-7, h-12), positioned left-[24px]
  - Radius: rounded-[10px]
  - Border: outline-[1.50px] outline-offset-[-0.75px] outline-Stroke-Stroke2
  - Positioning: top offset для соединения (top-[-6px], top-[-30px])
- **Layout**: inline-flex с tree line container слева и content справа

**Tree Line Positions**:
- **Top item**: h-7 (28px), top-[-6px] - короткая линия сверху
- **Middle items**: h-12 (48px), top-[-30px] - полная линия соединения
- **Last item**: может иметь другую высоту для завершения

##### Menu Group (with Dropdown)

Группа меню с возможностью сворачивания/разворачивания.

- **Header**: p-3, rounded-xl
  - Layout: inline-flex justify-start items-center gap-3
  - Icon + Title + Chevron
- **States**:
  - **Collapsed**: chevron pointing right (-rotate-90)
  - **Expanded**: chevron pointing down (default или rotate-90)
- **Children**: nested items with tree lines
- **Active Group**: bg-Backgrounds-pop with shadow

##### Number Badge (Notification)

- **Size**: w-6 h-6 px-2 py-1
- **Radius**: rounded-lg (12px)
- **Layout**: inline-flex flex-col justify-center items-center gap-2
- **Font**: text-sm, font-semibold, text-center
- **Colors**:
  - **Default (Secondary-01)**: bg-Secondary-secondary01, text-shade01-100
  - **Alternate (Secondary-04)**: bg-Secondary-secondary04, text-shade01-100
- **Usage**: показывает количество непрочитанных элементов, уведомлений
- **Examples**: "2", "3", "8"

#### Пример использования

```jsx
// Simple menu item (default)
<div className="self-stretch p-3 rounded-xl inline-flex justify-start items-center gap-3 overflow-hidden">
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-4 h-4 left-[3px] top-[3px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
  </div>
  <div className="flex-1 opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Dashboard</div>
</div>

// Active menu item
<div className="self-stretch p-3 bg-Backgrounds-pop rounded-xl shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] outline outline-1 outline-offset-[-1px] outline-neutral-200/50 inline-flex justify-start items-center gap-3 overflow-hidden">
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-4 h-4 left-[3px] top-[3px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
  </div>
  <div className="flex-1 justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Dashboard</div>
</div>

// Menu item with number badge
<div className="self-stretch p-3 rounded-xl inline-flex justify-start items-center gap-3 overflow-hidden">
  <div className="flex-1 opacity-80 justify-start text-Text-Secondary text-sm font-semibold">Drafts</div>
  <div className="w-6 h-6 px-2 py-1 bg-Secondary-secondary01 rounded-lg inline-flex flex-col justify-center items-center">
    <div className="text-center text-shade01-100 text-sm font-semibold">3</div>
  </div>
</div>

// Tree navigation item
<div className="self-stretch inline-flex justify-start items-center">
  <div className="w-9 h-11 relative">
    <div className="w-3 h-12 left-[24px] top-[-30px] absolute rounded-[10px] outline outline-[1.50px] outline-offset-[-0.75px] outline-Stroke-Stroke2" />
  </div>
  <div className="flex-1 h-11 px-3 rounded-xl flex justify-start items-center gap-3">
    <div className="flex-1 opacity-80 text-Text-Secondary text-sm font-semibold">Drafts</div>
  </div>
</div>

// Menu group header (expandable)
<div className="self-stretch p-3 rounded-xl inline-flex justify-start items-center gap-3 overflow-hidden">
  <div className="w-6 h-6 relative overflow-hidden">
    {/* Icon */}
  </div>
  <div className="flex-1 justify-start text-Text-Primary text-sm font-semibold">Product</div>
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-1 h-2 left-[8px] top-[14px] absolute origin-top-left -rotate-90 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
  </div>
</div>
```

---

### 8. Charts

#### Line Chart

- **Line Width**:
- **Point Radius**:
- **Grid Lines**:
- **Colors**:

#### Bar Chart

- **Bar Spacing**:
- **Border Radius**:
- **Colors**:

#### Pie/Donut Chart

- **Border Width**:
- **Spacing**:
- **Colors**:

---

### 9. Avatars

#### Sizes

- **XS**: 24x24px
- **Small**: 32x32px
- **Medium**: 40x40px (w-10 h-10)
- **Large**: 48x48px (container w-12 h-12 с px-4 py-3.5)
- **List Item**: 64x64px (w-16 h-16) для list items
- **XL**: 56x56px
- **2XL**: 64x64px

#### Styles

- **Border Radius**:
  - Default: rounded-full (полностью круглый)
  - List Item: rounded-xl (16px) для квадратных, rounded-[64px] для круглых
- **Border**:
  - Default: outline-[1.50px] outline-Stroke-Subtle/10 (светлый режим)
  - Active/Selected: outline-[1.50px] outline-Text-Blue (синяя обводка)
  - Dark Mode: outline-[1.50px] outline-Stroke-Subtle
- **Container**: px-4 py-3.5, bg-Backgrounds-surface2, rounded-[90px]
- **Placeholder**: img placeholder (placehold.co)
- **Status Indicator**: (to be defined)

#### Avatar Selection State

- **Selected**: outline-[1.50px] outline-offset-[-1.50px] outline-Text-Blue
- **Default**: без outline или subtle outline
- **Container остается**: bg-Backgrounds-surface2, rounded-[90px]

---

### 10. List Items

#### List Item (Simple with Icon)

- **Padding**: p-3 (12px all sides)
- **Radius**: rounded-2xl (16px) или rounded-[20px] (20px)
- **Layout**: flex justify-start items-center gap-4
- **Icon**: w-6 h-6
- **Text**: text-sm, font-semibold, leading-4, tracking-tight
- **States**:
  - Default: transparent, text-Text-Secondary
  - Hover: (background change)
  - Active: bg-Backgrounds-pop, shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)] shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)] shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)], outline-1 outline-zinc-100, text-Text-Primary
  - Selected: (same as active)

#### List Item (with Image & Price)

- **Padding**: p-3 (12px)
- **Radius**: rounded-[20px]
- **Layout**: flex justify-start items-center gap-8
- **Image**: w-16 h-16 (64x64px), rounded-xl (16px)
- **Content Layout**: flex-1 flex gap-5
- **Title**: text-base, font-semibold, leading-6, tracking-tight, text-Text-Primary
- **Price/Value**: text-base, font-semibold, leading-6, text-right
- **Badge**: status badge в правой части (gap-1 от price)
- **States**:
  - Default: transparent
  - Hover (Light Mode): bg-Backgrounds-highlight, shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)], shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)], shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)], outline-[1.50px] outline-zinc-100
  - Hover (Dark Mode): bg-Backgrounds-highlight, outline-[1.50px] outline-zinc-100

#### List Item (User Card with Subtitle)

- **Padding**: p-3 (12px)
- **Radius**: rounded-[20px]
- **Layout**: flex justify-start items-center gap-8
- **Avatar**: w-16 h-16, rounded-xl (или rounded-[64px] для круглого)
- **Content**: flex-col gap-1
  - Name: text-base, font-semibold, leading-6, tracking-tight
  - Subtitle: text-xs, font-normal, leading-5, tracking-tight, text-Text-Secondary
- **Action Button**: w-12 h-12, p-5, rounded-[96px], outline-[1.50px] Stroke-Stroke2
- **Gap**: gap-5 между avatar и content

---

### 11. Messages / Notifications

#### Tooltip

- **Padding**: px-2 py-1.5 (8px horizontal, 6px vertical)
- **Radius**: rounded-md (8px)
- **Background**: Backgrounds-dark1
- **Font**: text-xs, text-Text-Light, leading-5, tracking-tight
- **Position**: data-position="right" (или другие направления)
- **Arrow**: w-2 h-1 треугольник, bg-Backgrounds-dark1, rotate-90
- **Example**: "Forgot password?"
- **Offset**: left-[26px] top-[1px] от родителя

#### Toast Notification

- **Width**: (to be defined)
- **Padding**: (to be defined)
- **Radius**: (to be defined)
- **Shadow**: (to be defined)
- **Position**: (to be defined)
- **Variants**: (to be defined)
- **Auto-dismiss**: (to be defined)

#### Alert Banner

- **Padding**: (to be defined)
- **Border Left**: (to be defined)
- **Background**: (to be defined)
- **Close Button**: (to be defined)

---

### 12. Panels & Cards

#### Dropdown Menu / Popup Panel

- **Width**: w-96 (384px)
- **Padding**: p-3 (12px)
- **Background**: Backgrounds-surface2
- **Radius**: rounded-[32px]
- **Border**: outline-1 outline-offset-[-1px]
- **Shadows (Light Mode)**:
  - shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)]
  - shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)]
  - shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)]
  - shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)]
  - shadow-[0px_2.15px_0.5px_-2px_rgba(0,0,0,0.25)]
  - shadow-[0px_0px_10px_0px_rgba(0,0,0,0.05)]
  - outline-Stroke-Subtle/10
- **Shadows (Dark Mode)**:
  - (same as light +)
  - shadow-[0px_2.15px_0.5px_-2px_rgba(0,0,0,0.80)]
  - shadow-[0px_0px_10px_0px_rgba(0,0,0,1.00)]
  - shadow-[inset_0px_0px_12px_4px_rgba(250,250,250,0.05)]
  - outline-Stroke-Stroke2
- **Section Header**: p-3, text-sm, font-normal, text-Text-Secondary
- **Gap**: gap-3 между секциями, gap-1.5 внутри секций
- **Content**: flex-col для vertical layout

#### Side Panel

- **Width**: (to be defined)
- **Background**: (to be defined)
- **Shadow**: (to be defined)
- **Padding**: (to be defined)
- **Header**:
  - Padding Bottom: (to be defined)
  - Border Bottom: (to be defined)

#### Modal / Dialog

##### Modal Container

- **Max Width**: w-[573px] (573px)
- **Padding**: p-12 (48px all sides)
- **Background**: bg-Backgrounds-surface1
- **Border Radius**: rounded-[32px]
- **Border**: outline-1 outline-offset-[-1px]
- **Layout**: flex-col justify-center items-start gap-8
- **Overlay**: backdrop blur с затемнением (implementation specific)

##### Modal Shadows

**Light Mode**:
- shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)]
- shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)]
- shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)]
- shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)]
- shadow-[0px_2.15px_0.5px_-2px_rgba(0,0,0,0.25)]
- outline-1, backdrop-blur-[32px]

**Dark Mode**:
- shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.08)]
- shadow-[0px_6px_13px_0px_rgba(8,8,8,0.12)]
- shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.16)]
- shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.20)]
- shadow-[0px_2.15px_0.5px_-2px_rgba(0,0,0,0.25)]
- shadow-[inset_2px_4px_16px_0px_rgba(253,253,253,0.05)]
- outline-1 outline-white/40, backdrop-blur-[32px]

##### Modal Icon

- **Size**: w-16 h-16 (64x64px)
- **Radius**: rounded-[80px] (круглая)
- **Layout**: flex justify-center items-center
- **Overflow**: overflow-hidden
- **Icon размер**: w-6 h-6 (24x24px) внутри
- **Варианты**:
  - Error/Delete: bg-red-600/20, icon color Primary-primary03
  - Success/Info: bg-shade08-100, icon color Text-Primary или Backgrounds-surface1

##### Modal Content

- **Title**:
  - Font: text-3xl, font-semibold, leading-10, tracking-tight
  - Color: text-Text-Primary
  - Example: "Are you sure?", "Set products status", "Share this product"
- **Description**:
  - Font: text-base, font-normal, leading-6, tracking-tight
  - Color: text-Text-Tertiary
  - Margin Top: gap-4 от title
  - Max Width: self-stretch
  - Can contain mixed colors: Text-Tertiary + Primary-primary02 для акцентов
- **Gap**: gap-8 между icon, content section и actions

##### Modal Actions

- **Container**:
  - Layout: inline-flex gap-3
  - Width: self-stretch (full width)
- **Button Layout**: flex-1 для равной ширины кнопок
- **Common Actions**:
  - Cancel button (secondary): outline button
  - Confirm/Primary button: gradient button
  - Example: "Cancel" + "Delete", "Cancel" + "Copy link"

#### Modal Variants

##### Confirmation Modal (Delete)
- **Icon**: bg-red-600/20 с alert icon
- **Title**: "Are you sure?"
- **Description**: предупреждение об удалении
- **Actions**: "Cancel" + "Delete" (primary destructive)

##### Status Change Modal
- **Icon**: bg-shade08-100 с status icon
- **Title**: "Set products status"
- **Description**: описание изменения с акцентом на новый статус
- **Content**: Segmented Control для выбора статуса
- **Actions**: может не иметь, или иметь "Cancel" + "Apply"

##### Share Modal
- **Icon**: отсутствует или используется product image
- **Title**: "Share this product"
- **Product Preview**:
  - Layout: inline-flex gap-6
  - Image: w-20 h-20, rounded-2xl
  - Info: title + subtitle
- **Share Options**:
  - Social buttons grid: flex-wrap gap-3
  - Each button: flex-1 min-w-48
- **Actions**: "Copy link" primary button

##### Social Share Buttons

- **Size**: flex-1 min-w-48 px-7 py-3
- **Radius**: rounded-[32px]
- **Border**: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
- **Layout**: flex justify-center items-center gap-2
- **Icon**: w-6 h-6, bg-Text-Secondary (default)
- **Variants**:
  - Instagram (ig): соответствующая иконка
  - Twitter/X (x): соответствующая иконка
  - Facebook (fb): соответствующая иконка
  - Telegram (tr): соответствующая иконка
- **States**:
  - Default: outline-Stroke-Stroke2
  - Hover: может измениться background или border
- **Grid Layout**: flex-wrap для адаптивности

#### Пример использования

```jsx
// Delete Confirmation Modal
<div className="w-[573px] p-12 bg-Backgrounds-surface1 rounded-[32px] shadow-[...] outline-1 backdrop-blur-[32px] inline-flex flex-col justify-center items-start gap-8">
  <div className="w-16 h-16 relative bg-red-600/20 rounded-[80px] overflow-hidden">
    <div className="w-6 h-6 left-[20px] top-[20px] absolute overflow-hidden">
      {/* Alert Icon */}
    </div>
  </div>
  <div className="self-stretch flex flex-col justify-start items-start gap-4">
    <div className="justify-start text-Text-Primary text-3xl font-semibold leading-10 tracking-tight">Are you sure?</div>
    <div className="self-stretch justify-start text-Text-Tertiary text-base font-normal leading-6 tracking-tight">
      This will definitely delete 4 products, and all data will be removed. This action cannot be undone.
    </div>
  </div>
  <div className="self-stretch inline-flex justify-start items-start gap-3">
    <div className="flex-1 h-12 px-7 py-3.5 rounded-[32px] outline-Stroke-Stroke2">Cancel</div>
    <div className="flex-1 px-7 py-4 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px]">Delete</div>
  </div>
</div>
```

---

### 13. Accordion / FAQ

#### Accordion Item

- **Padding**:
- **Border**:
- **Border Radius**:
- **Margin Bottom**:
- **States**:
  - Collapsed:
  - Expanded:
  - Hover:

---

### 14. Loading States

#### Skeleton Loader / Progress Bar

- **Background**:
  - Base: shade07-40/40 (40% opacity)
  - Separator: shade07-60/60 dots, w-0.5 h-3, gap-px
  - Progress: gradient from-shade08-100 to-shade09-100
- **Border**: border border-Stroke-Stroke2 (на заполненной части)
- **Border Radius**: rounded-[1px], rounded-[0.50px] для маленьких элементов
- **Sizes**:
  - Height: 12px (h-3)
  - Width: variable (w-24, w-40, w-60, w-80, etc.)
  - Full width: w-full для адаптивности
- **Animation**: (gradient animation or shimmer)
- **Pattern**: dots/dashes между base и progress для визуального разделения

#### Spinner

- **Size**: (to be defined)
- **Color**: (to be defined)
- **Animation**: (to be defined)

---

### 15. Empty States

#### Empty State Layout

- **Icon**:
- **Heading**:
- **Description**:
- **Action Button**:
- **Spacing**:
  - Icon → Heading:
  - Heading → Description:
  - Description → Button:

---

### 16. Special Effects

#### Focus Ring

```css
--focus-ring: 0 0 0 3px rgba(147, 51, 234, 0.15); /* Purple focus ring with 3px offset */
--focus-ring-offset: 2px; /* Offset from element */
--focus-ring-color: var(--Primary-primary03); /* Purple-500 */
```

#### Backdrop Blur

```css
--backdrop-blur-sm: blur(8px); /* Subtle blur for overlays */
--backdrop-blur-base: blur(16px); /* Default blur */
--backdrop-blur-md: blur(32px); /* Medium blur for modals */
--backdrop-blur-lg: blur(50px); /* Strong blur for emphasis */
```

---

### 17. Checkbox

#### Checkbox

- **Size**: w-6 h-6 (24x24px)
- **Radius**: rounded-md (8px)
- **Border**: border-2
- **Container**: relative overflow-hidden
- **States**:
  - **Unchecked**:
    - Border: border-2 border-Stroke-Stroke2
    - Background: transparent
    - Icon: none
  - **Checked**:
    - Border: border-2 border-Primary-primary01, opacity-30
    - Checkmark: w-4 h-4, bg-Primary-primary01, rounded-sm
    - Position: left-[4px] top-[4px] (centered within 24px container)
  - **Hover (Unchecked)**:
    - Border: border-2 border-shade07-50/50
  - **Hover (Checked)**:
    - Border opacity может увеличиться
  - **Disabled**:
    - Opacity: opacity-50
    - Cursor: not-allowed
  - **Indeterminate**:
    - Checkmark: horizontal line instead of checkmark
- **Animation**: smooth transition для checked state

#### Пример использования

```jsx
// Unchecked
<div className="w-6 h-6 relative overflow-hidden">
  <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
</div>

// Checked
<div className="w-6 h-6 relative overflow-hidden">
  <div className="w-6 h-6 left-0 top-0 absolute opacity-30 rounded-md border-2 border-Primary-primary01" />
  <div className="w-4 h-4 left-[4px] top-[4px] absolute bg-Primary-primary01 rounded-sm" />
</div>
```

---

### 18. Toggle Switch

#### Toggle Switch

- **Size**: w-11 h-6 (44x24px)
- **Padding**: p-0.5 (2px внутренний отступ)
- **Radius**: rounded-[32px] (pill shape)
- **Border**: outline-[1.50px] outline-offset-[-1.50px]
- **Knob**: w-5 h-5 (20x20px), rounded-3xl (почти полный круг)
- **Layout**: inline-flex justify-end (ON) или justify-start (OFF)
- **States**:
  - **ON (Light Mode)**:
    - Track: bg-gradient from-zinc-800 to-zinc-800, shadow-[inset 2px 0px 8px 2px rgba(248,248,248,0.20)], outline white/40
    - Knob: bg-neutral-50, positioned right (justify-end)
  - **ON (Dark Mode)**:
    - Track: bg-gradient from-zinc-300 to-gray-200, shadow-[inset 2px 0px 8px 1px rgba(248,248,248,0.19)], outline white/40
    - Knob: bg-shade02-100
  - **OFF**:
    - Track: bg-Backgrounds-surface2, shadow-[inset 2px 0px 8px 2px rgba(248,248,248,0.05)], outline-Stroke-Stroke2
    - Knob: bg-neutral-50, positioned left (justify-start)
- **Knob Shadows** (3D effect):
  - shadow-[0px_2px_4px_0px_rgba(0,0,0,0.20)]
  - shadow-[inset_0px_-1px_1px_0px_rgba(0,0,0,0.10)]
  - shadow-[inset_0px_2px_2px_0px_rgba(255,255,255,1.00)] (OFF) или 0.05-0.12 (ON)
- **Transition**: smooth transition для knob position и colors

#### Segmented Control (Status Toggle)

Используется для переключения между двумя опциями (например, Active/Deactive).

- **Container**:
  - Padding: p-1 (4px внутренний отступ)
  - Radius: rounded-[36px]
  - Border: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
  - Layout: inline-flex gap-2
- **Segment**:
  - Size: flex-1 px-6 py-4 (равная ширина для всех сегментов)
  - Radius: rounded-[32px]
  - Font: text-sm, font-semibold, leading-4, tracking-tight
  - Min Height: 48px total (with padding)
- **States**:
  - **Active (Success variant)**:
    - Background: bg-green-600/10
    - Border: outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20
    - Text: text-Primary-primary02
  - **Active (Error variant)**:
    - Background: bg-red-600/10
    - Border: outline-[1.50px] outline-offset-[-1.50px] outline-red-600/20
    - Text: text-Primary-primary03
  - **Inactive**:
    - Background: transparent
    - Border: none
    - Text: text-Text-Secondary
    - Padding: py-3.5 (slightly less для visual alignment)

#### Пример использования

```jsx
// Active state
<div className="self-stretch p-1 rounded-[36px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-start items-start gap-2">
  <div className="flex-1 px-6 py-4 bg-green-600/10 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 flex justify-center items-center gap-2">
    <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Active</div>
  </div>
  <div className="flex-1 px-6 py-3.5 rounded-[32px] flex justify-center items-center gap-2">
    <div className="justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Deactive</div>
  </div>
</div>
```

---

### 19. Page Headers

#### Section Header with Dropdown

- **Container**: inline-flex justify-between items-center
- **Title**:
  - Padding: px-5 (h-12 container с p-3 gap-2)
  - Font: text-xl, font-semibold, leading-7, tracking-tight
  - Color: text-Text-Primary
- **Dropdown**: w-40 max-w-44, positioned на правой стороне
- **Layout**: flex между title и dropdown
- **Example**: "Overview" + "Last 7 days" dropdown

#### Page Header with Search & Filters

- **Container**: w-full px-4 py-3 (или p-3)
- **Layout**: inline-flex justify-between items-center
- **Left Section**:
  - Title: text-xl, font-semibold, leading-7, tracking-tight, text-Text-Primary
  - Search Input: w-72 (288px), pill-shaped search
  - Gap: gap-6 между элементами
  - Container: h-12 pl-5 flex items-center
- **Right Section (Filters)**:
  - Tab Filter buttons: Segment Control style
  - Layout: flex gap-1
  - Example: "Market", "Traffic sources", "Viewers"

#### Bulk Actions Header

Появляется когда выбраны элементы в таблице, заменяет обычный header.

- **Container**: w-full px-4 py-3 (или p-3)
- **Layout**: inline-flex justify-between items-center
- **Height**: h-12 min
- **Left Section**:
  - Container: pl-5 flex items-center gap-6
  - Selection Text: text-xl, font-semibold, leading-7, tracking-tight, text-Text-Primary
    - Example: "4 products selected"
  - Deselect Button: px-7 py-3.5, rounded-[32px], outline-[1.50px] outline-Stroke-Stroke2
    - Text: text-sm, font-semibold, text-Text-Secondary, "Deselect"
- **Right Section (Actions)**:
  - Layout: flex gap-3
  - Action Buttons: px-7 py-3, rounded-[32px], outline-[1.50px] outline-Stroke-Stroke2
    - Common actions: "Delete", "Set status", "Export", etc.
    - Text: text-sm, font-semibold, text-Text-Secondary
- **State**:
  - Appears: when items are selected (checkbox checked)
  - Replaces: normal page header
  - Transition: smooth fade in/out

#### Пример использования

```jsx
// Normal header with search & filters
<div className="w-full p-3 inline-flex justify-between items-center">
  <div className="h-12 pl-5 flex justify-center items-center gap-6">
    <div className="justify-start text-Text-Primary text-xl font-semibold leading-7 tracking-tight">Products</div>
    <div className="w-72 pl-3 pr-5 py-3 bg-Backgrounds-surface1 rounded-[90px] flex items-center gap-2">
      {/* Search input */}
    </div>
  </div>
  <div className="flex justify-start items-start gap-1">
    {/* Filter tabs */}
  </div>
</div>

// Bulk actions header
<div className="w-full p-3 inline-flex justify-between items-center">
  <div className="h-12 pl-5 flex justify-center items-center gap-6">
    <div className="justify-start text-Text-Primary text-xl font-semibold leading-7 tracking-tight">4 products selected</div>
    <div className="px-7 py-3.5 rounded-[32px] outline outline-[1.50px] outline-Stroke-Stroke2">
      <div className="text-center text-Text-Secondary text-sm font-semibold leading-4 tracking-tight">Deselect</div>
    </div>
  </div>
  <div className="flex items-center gap-3">
    <div className="px-7 py-3 rounded-[32px] outline outline-[1.50px] outline-Stroke-Stroke2">
      <div className="text-center text-Text-Secondary text-sm font-semibold leading-4 tracking-tight">Delete</div>
    </div>
    <div className="px-7 py-3 rounded-[32px] outline outline-[1.50px] outline-Stroke-Stroke2">
      <div className="text-center text-Text-Secondary text-sm font-semibold leading-4 tracking-tight">Set status</div>
    </div>
  </div>
</div>
```

---

### 20. File Upload (Drag & Drop)

#### File Upload Area

Компонент для загрузки файлов с поддержкой drag & drop.

- **Container**:
  - Size: w-96 h-56 (384px x 224px)
  - Padding: px-8 py-16 (32px horizontal, 64px vertical)
  - Radius: rounded-[32px]
  - Border: outline-2 outline-offset-[-2px] (активное состояние)
  - Layout: flex-col justify-center items-center gap-4
  - Overflow: overflow-hidden

##### Empty State (Light Mode)
- **Background**: bg-Backgrounds-surface3/50 (50% opacity)
- **Border**: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
- **Icon Container**: w-12 h-12, bg-Backgrounds-surface2, rounded-xl
  - Icon: w-6 h-6 upload icon, outline-[1.50px] outline-Text-Secondary
- **Text**:
  - Primary: text-base, font-semibold, leading-6, tracking-tight, text-Text-Primary
  - Secondary: text-sm, font-normal, leading-5, tracking-tight, text-Text-Secondary
  - Content: "Drag and drop an image, or Browse"
  - "Browse" highlighted with text-Primary-primary01 (синий)

##### Empty State (Dark Mode)
- **Background**: bg-shade04-100
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Icon & Text**: same as Light Mode

##### Active Drag State
- **Border**: outline-2 outline-offset-[-2px] outline-Primary-primary01
- **Background**: может быть слегка подсвечен
- **Visual feedback**: показывает что область готова принять файл

##### With Uploaded Image State
- **Container**: same sizing (w-96 h-56)
- **Background**: bg-Backgrounds-surface3/50 (Light) or bg-shade04-100 (Dark)
- **Image**: positioned fill container, rounded-[32px] to match container
- **Success Indicator**:
  - Container: w-12 h-12, bg-Backgrounds-pop, rounded-xl (positioned top-right or center)
  - Icon: w-6 h-6 checkmark, bg-Primary-primary02 (зеленый)
  - Shadow: может иметь subtle shadow
- **Positioning**: relative для размещения success indicator overlay

#### File Upload States

**Default State**:
- Show icon + text
- Border: outline-[1.50px] outline-Stroke-Stroke2
- Cursor: pointer
- Hover: может подсветить border или background

**Dragging Over (Active Drop Zone)**:
- Border: outline-2 outline-Primary-primary01 (синяя, более толстая обводка)
- Background: может быть слегка подсвечен
- Visual feedback: показывает готовность к drop

**Uploading State**:
- Progress indicator (to be defined)
- Может показывать spinner или progress bar

**Success State (Uploaded)**:
- Shows image preview
- Success checkmark overlay
- Border: может вернуться к default или убраться

**Error State**:
- Border: outline-Primary-primary03 (красный)
- Error message под компонентом
- Icon: может измениться на error icon

#### Пример использования

```jsx
// Empty state (Light Mode)
<div className="w-96 h-56 px-8 py-16 bg-Backgrounds-surface3/50 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex-col justify-center items-center gap-4 inline-flex overflow-hidden">
  <div className="w-12 h-12 p-3 bg-Backgrounds-surface2 rounded-xl inline-flex justify-center items-center overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-4 h-4 left-[3px] top-[4.50px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      {/* Upload icon arrows */}
    </div>
  </div>
  <div className="flex-col justify-start items-center gap-1 flex">
    <div className="justify-start text-center">
      <span className="text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight">Drag and drop an image, or </span>
      <span className="text-Primary-primary01 text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight">Browse</span>
    </div>
    <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Supports: JPG, PNG, SVG</div>
  </div>
</div>

// Active drag state
<div className="w-96 h-56 px-8 py-16 bg-Backgrounds-surface3/50 rounded-[32px] outline outline-2 outline-offset-[-2px] outline-Primary-primary01 flex-col justify-center items-center gap-4 inline-flex overflow-hidden">
  {/* Same content */}
</div>

// With uploaded image
<div className="w-96 h-56 relative bg-Backgrounds-surface3/50 rounded-[32px] overflow-hidden">
  <img className="w-full h-full object-cover rounded-[32px]" src="..." alt="Uploaded" />
  <div className="absolute top-4 right-4 w-12 h-12 p-3 bg-Backgrounds-pop rounded-xl flex justify-center items-center">
    <div className="w-6 h-6 relative">
      <div className="w-4 h-4 left-[4px] top-[4px] absolute bg-Primary-primary02 rounded-sm" />
      {/* Checkmark icon */}
    </div>
  </div>
</div>
```

---

### 21. Uploaded File Card

#### File Card Component

Карточка для отображения загруженного файла с информацией и действиями.

- **Container**:
  - Padding: p-6 (24px all sides)
  - Radius: rounded-3xl (24px)
  - Border: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
  - Layout: flex justify-between items-center
  - Gap: gap-6 между элементами

##### Left Section (File Info)
- **Layout**: flex items-center gap-4
- **Icon Container**: w-12 h-12, bg-Backgrounds-surface3, rounded-xl
  - Icon: w-6 h-6 file/document icon с upload arrows
  - Color: outline-[1.50px] outline-Text-Secondary
- **File Details**: flex-col gap-1
  - Filename: text-base, font-semibold, leading-6, tracking-tight, text-Text-Primary
  - File size: text-sm, font-normal, leading-5, tracking-tight, text-Text-Secondary
  - Example: "product-image.png", "2.4 MB"

##### Right Section (Delete Button)
- **Button (Light Mode)**:
  - Size: w-12 h-12 p-3
  - Radius: rounded-xl
  - Background: bg-gradient-to-b from-white to-neutral-200
  - Shadow: shadow-[inset_2px_0px_8px_2px_rgba(24,24,24,0.20)]
  - Border: outline-[1.50px] outline-offset-[-1.50px] outline-white/60
  - Icon: w-6 h-6 trash/delete icon, outline-Text-Primary
- **Button (Dark Mode)**:
  - Background: bg-gradient-to-b from-zinc-800 to-zinc-800
  - Shadow: shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)]
  - Border: outline-[1.50px] outline-white/40
  - Icon: outline-Text-Primary

#### States

**Default**:
- Border: outline-Stroke-Stroke2
- Background: transparent or bg-Backgrounds-surface2
- Icon: Text-Secondary

**Hover**:
- Delete button hover: может подсветиться
- Card hover: может иметь subtle shadow

**Uploading**:
- Progress bar под filename (опционально)
- Percentage indicator

**Error**:
- Border: outline-Primary-primary03
- Error icon вместо file icon

#### Пример использования

```jsx
// Light mode
<div className="self-stretch p-6 rounded-3xl outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-between items-center">
  <div className="flex justify-start items-center gap-4">
    <div className="w-12 h-12 p-3 bg-Backgrounds-surface3 rounded-xl inline-flex justify-center items-center overflow-hidden">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-4 h-4 left-[3px] top-[4.50px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        {/* File upload icon */}
      </div>
    </div>
    <div className="flex-col justify-start items-start gap-1 inline-flex">
      <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight">product-image.png</div>
      <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">2.4 MB</div>
    </div>
  </div>
  <div className="w-12 h-12 p-3 bg-gradient-to-b from-white to-neutral-200 rounded-xl shadow-[inset_2px_0px_8px_2px_rgba(24,24,24,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/60 inline-flex justify-center items-center overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden">
      {/* Delete icon */}
    </div>
  </div>
</div>
```

---

### 22. Text Editor / Rich Text

#### Text Editor Container

Компонент для редактирования текста с форматированием (bold, italic, underline, etc.).

- **Container**:
  - Width: w-full или fixed (например w-96)
  - Padding: p-6 (24px)
  - Radius: rounded-3xl (24px)
  - Border: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
  - Background: bg-Backgrounds-surface1 or bg-Backgrounds-surface2
  - Layout: flex-col gap-4

##### Toolbar
- **Container**:
  - Layout: inline-flex items-center gap-2
  - Border Bottom: может иметь border-b separator
  - Padding Bottom: pb-4 (если есть separator)
- **Button Groups**: разделены вертикальными линиями
  - Separator: w-px h-6 bg-Stroke-Stroke2 между группами

##### Toolbar Buttons
- **Size**: w-10 h-10 p-3 (40x40px container, 12px padding)
- **Radius**: rounded-lg (12px)
- **Layout**: flex justify-center items-center
- **Icon**: w-4 h-4 (16x16px)
- **Gap**: gap-1 между кнопками в группе
- **States**:
  - **Default (Inactive)**:
    - Background: transparent
    - Border: none
    - Icon: outline-[1.50px] outline-Text-Secondary
  - **Active (Light Mode)**:
    - Background: bg-shade08-80/80
    - Radius: rounded-lg
    - Icon: outline-[1.50px] outline-Text-Primary
  - **Active (Dark Mode)**:
    - Background: bg-shade05-50/50
    - Radius: rounded-lg
    - Icon: outline-[1.50px] outline-Text-Primary
  - **Hover**:
    - Background: bg-shade08-80/40 (Light) or bg-shade05-50/25 (Dark)
    - Icon: может стать Text-Primary

##### Common Toolbar Buttons
- **Text Formatting**:
  - Bold (B): text-sm font-semibold или icon
  - Italic (I): text-sm italic или icon
  - Underline (U): text-sm underline или icon
  - Strikethrough: icon
- **Alignment**:
  - Align Left
  - Align Center
  - Align Right
  - Justify
- **Lists**:
  - Bullet List
  - Numbered List
  - Checklist
- **Insert**:
  - Link
  - Image
  - Code block
  - Quote

##### Text Area
- **Container**: flex-1 или min-h-40
- **Padding**: p-4
- **Font**: text-base, font-normal, leading-6
- **Placeholder**: text-Text-Tertiary
- **Cursor**: text cursor visible при focus
- **Content**: contenteditable или textarea

##### Resize Handle
- **Position**: absolute, bottom-right corner (bottom-0 right-0)
- **Size**: w-4 h-4
- **Icon**: resize grip lines
  - Two diagonal lines: w-px h-3, bg-Text-Secondary, gap-1
  - Positioned: right-[4px] bottom-[4px]
  - Rotation: может быть повернут на 45deg для diagonal lines
- **Cursor**: cursor-nwse-resize

#### Editor States

**Default**:
- Border: outline-Stroke-Stroke2
- Background: bg-Backgrounds-surface2
- Toolbar visible

**Focus**:
- Border: может стать outline-Primary-primary01 или shade07-50/50
- Cursor visible в text area

**Disabled**:
- Opacity: opacity-50
- Cursor: not-allowed
- Toolbar buttons disabled

**Read-only**:
- No toolbar
- No cursor
- No editing allowed

#### Пример использования

```jsx
<div className="w-96 p-6 bg-Backgrounds-surface2 rounded-3xl outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex-col justify-start items-start gap-4 inline-flex">
  {/* Toolbar */}
  <div className="self-stretch inline-flex justify-start items-center gap-2">
    {/* Format buttons group */}
    <div className="inline-flex justify-start items-center gap-1">
      <div className="w-10 h-10 p-3 bg-shade08-80/80 rounded-lg flex justify-center items-center">
        <div className="w-4 h-4 relative overflow-hidden">
          {/* Bold icon - active state */}
        </div>
      </div>
      <div className="w-10 h-10 p-3 rounded-lg flex justify-center items-center">
        <div className="w-4 h-4 relative overflow-hidden">
          {/* Italic icon - inactive state */}
        </div>
      </div>
      <div className="w-10 h-10 p-3 rounded-lg flex justify-center items-center">
        <div className="w-4 h-4 relative overflow-hidden">
          {/* Underline icon */}
        </div>
      </div>
    </div>

    {/* Separator */}
    <div className="w-px h-6 bg-Stroke-Stroke2" />

    {/* Alignment buttons group */}
    <div className="inline-flex justify-start items-center gap-1">
      <div className="w-10 h-10 p-3 rounded-lg flex justify-center items-center">
        {/* Align left icon */}
      </div>
      <div className="w-10 h-10 p-3 rounded-lg flex justify-center items-center">
        {/* Align center icon */}
      </div>
    </div>

    {/* More button groups... */}
  </div>

  {/* Text area */}
  <div className="self-stretch min-h-40 p-4 relative">
    <div className="text-Text-Primary text-base font-normal leading-6 tracking-tight">
      {/* Editable content */}
    </div>

    {/* Resize handle */}
    <div className="absolute bottom-0 right-0 w-4 h-4 cursor-nwse-resize">
      <div className="flex gap-1">
        <div className="w-px h-3 bg-Text-Secondary rotate-45" />
        <div className="w-px h-3 bg-Text-Secondary rotate-45" />
      </div>
    </div>
  </div>
</div>
```

---

### 23. Product Card (Bento Card)

#### Product Card Component

Карточка продукта с изображением, метаданными и интерактивными элементами.

- **Container**:
  - Width: w-96 min-w-72 (384px, minimum 288px)
  - Layout: inline-flex flex-col justify-start items-start gap-3
  - Spacing: gap-3 между image и content

##### Card Image
- **Size**: h-56 (224px height), full width
- **Radius**: rounded-3xl (24px)
- **Background**: bg-gray-200 (placeholder)
- **Image**: w-96 h-56, absolute positioned, object-cover
- **Overflow**: overflow-hidden

##### Card Content
- **Layout**: flex-col justify-center items-start gap-1
- **Components**:
  - Title row (с ценой или действиями)
  - Metadata row (дата, рейтинг и т.д.)

##### Title Row
- **Layout**: inline-flex justify-between items-center
- **Title**:
  - Font: text-base, font-semibold, leading-6, tracking-tight
  - Color: text-Text-Primary
  - Truncation: line-clamp-1
  - Example: "Bento Design System"
- **Price Badge**: positioned справа (see Status Badge specs)

##### Metadata Components
- **Date/Time**:
  - Layout: inline-flex justify-start items-center gap-2
  - Icon: w-6 h-6 clock icon
  - Text: text-xs, font-normal, leading-5, tracking-tight
  - Opacity: opacity-80
  - Color: text-Text-Secondary
  - Example: "Apr 9, 2044 at 3:55 PM"
- **Rating** (if applicable):
  - Layout: inline-flex gap-2.5
  - Star icon: w-5 h-5
  - Score: text-sm, font-semibold, text-Text-Primary
  - Count: text-sm, font-normal, text-Text-Secondary в скобках
  - Example: "4.8 (88)"

#### Card States

##### Default State
- Image: full visibility
- Content: full opacity
- No overlay
- No checkbox
- No action buttons

##### Hover State (with Checkbox)
- Image: может иметь slight overlay (opacity-30 bg-Backgrounds-dark1)
- Checkbox: появляется в left-top corner
  - Position: absolute, left-[16px] top-[16px]
  - Unchecked: bg-Backgrounds-surface2, border-2 border-Stroke-Stroke2
  - Size: w-6 h-6
- Action Buttons: появляются под title
  - Layout: inline-flex gap-2, positioned absolute или relative
  - Buttons: Edit, Delete, Schedule/Unpublish
  - See Action Buttons (Small) specs

##### Selected State
- Image overlay: opacity-10 bg-shade10-100
- Checkbox: checked state
  - Container: bg-shade10-100, border-2 border-Primary-primary01
  - Checkmark: w-4 h-4 bg-Primary-primary01 rounded-sm, positioned [4px, 4px]
- Content: opacity-50 на всем content section
- Title, price, metadata: все с opacity-50

##### With Action Buttons (Hover Variant)
- Image: opacity-30 bg-Backgrounds-dark1 overlay
- Checkbox: unchecked, visible
- Action Buttons Row:
  - Position: может быть absolute overlay на content или ниже title
  - Layout: inline-flex gap-2
  - Buttons show default and hover states
  - Common actions: Edit, Delete, Schedule, Unpublish
- Info tooltip: может появиться w-8 h-8 icon с tooltip

#### Rating Component

Компонент отображения рейтинга со звездочкой.

- **Container**: inline-flex justify-start items-start gap-2.5
- **Layout**: flex justify-start items-center gap-2
- **Star Icon**:
  - Container: w-5 h-5 (20x20px), relative overflow-hidden
  - Star shape: w-4 h-4, positioned [1.25px, 0.83px]
  - Color: bg-Text-Secondary
- **Score and Count**:
  - Layout: flex justify-start items-center gap-1
  - Score: text-sm, font-semibold, leading-4, tracking-tight, text-Text-Primary
  - Count: text-sm, font-normal, leading-5, tracking-tight, text-Text-Secondary
  - Format: "4.8 (88)" - score + count in parentheses

##### Пример использования

```jsx
// Default card
<div className="w-96 min-w-72 inline-flex flex-col justify-start items-start gap-3">
  <div className="self-stretch h-56 relative bg-gray-200 rounded-3xl overflow-hidden">
    <img className="w-96 h-56 left-0 top-0 absolute" src="https://placehold.co/356x230" />
  </div>
  <div className="self-stretch flex flex-col justify-center items-start gap-1">
    <div className="self-stretch inline-flex justify-between items-center">
      <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">Bento Design System</div>
      <div className="w-12 px-3 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 flex justify-center items-center gap-1">
        <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">$98</div>
      </div>
    </div>
    <div className="self-stretch inline-flex justify-start items-center gap-2">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-5 h-5 left-[2.75px] top-[2.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      </div>
      <div className="flex-1 opacity-80 justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Apr 9, 2044 at 3:55 PM</div>
    </div>
  </div>
</div>

// Selected card with checkbox
<div className="w-96 min-w-72 inline-flex flex-col justify-start items-start gap-3">
  <div className="self-stretch h-56 relative bg-gray-200 rounded-3xl overflow-hidden">
    <img className="w-96 h-56 left-0 top-0 absolute" src="https://placehold.co/356x230" />
    <div className="w-96 h-56 left-0 top-0 absolute opacity-10 bg-shade10-100" />
    <div className="w-6 h-6 left-[16px] top-[16px] absolute overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute bg-shade10-100 rounded-md border-2 border-Primary-primary01" />
      <div className="w-4 h-4 left-[4px] top-[4px] absolute bg-Primary-primary01 rounded-sm" />
    </div>
  </div>
  <div className="self-stretch opacity-50 flex flex-col justify-center items-start gap-1">
    {/* Same content structure */}
  </div>
</div>

// Card with rating
<div className="w-96 min-w-72 inline-flex flex-col justify-start items-start gap-3">
  <div className="self-stretch h-56 relative bg-gray-200 rounded-3xl overflow-hidden">
    <img className="w-96 h-56 left-0 top-0 absolute" src="..." />
  </div>
  <div className="self-stretch flex flex-col justify-center items-start gap-1">
    <div className="self-stretch inline-flex justify-between items-center">
      <div className="justify-start text-Text-Primary text-base font-semibold leading-6 tracking-tight line-clamp-1">Bento Design System</div>
      <div className="w-12 px-3 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 flex justify-center items-center gap-1">
        <div className="justify-start text-Primary-primary02 text-sm font-semibold leading-4 tracking-tight">$98</div>
      </div>
    </div>
    <div className="w-20 inline-flex justify-start items-start gap-2.5">
      <div className="flex justify-start items-center gap-2">
        <div className="w-5 h-5 relative overflow-hidden">
          <div className="w-4 h-4 left-[1.25px] top-[0.83px] absolute bg-Text-Secondary" />
        </div>
        <div className="flex justify-start items-center gap-1">
          <div className="justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">4.8</div>
          <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">(88)</div>
        </div>
      </div>
    </div>
  </div>
</div>

// Hover card with action buttons
<div className="w-96 min-w-72 inline-flex flex-col justify-start items-start gap-3">
  <div className="self-stretch h-56 relative bg-gray-200 rounded-3xl overflow-hidden">
    <img className="w-96 h-56 left-0 top-0 absolute" src="..." />
    <div className="w-96 h-56 left-0 top-0 absolute opacity-30 bg-Backgrounds-dark1" />
    <div data-status="placeholder" className="w-6 h-6 left-[16px] top-[16px] absolute overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute bg-Backgrounds-surface2 rounded-md border-2 border-Stroke-Stroke2" />
    </div>
  </div>
  <div className="self-stretch relative flex flex-col justify-center items-start gap-1">
    <div className="self-stretch inline-flex justify-between items-center">
      <div className="justify-start text-Text-Primary text-base font-semibold leading-6 tracking-tight line-clamp-1">Bento Design System</div>
      <div className="w-12 px-3 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 flex justify-center items-center gap-1">
        <div className="justify-start text-Primary-primary02 text-sm font-semibold leading-4 tracking-tight">$98</div>
      </div>
    </div>
    <div className="w-56 h-6 relative">
      <div className="left-[-4px] top-0 absolute inline-flex justify-start items-start gap-2">
        <div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold leading-4 tracking-tight">Edit</div>
        </div>
        <div className="pl-1 pr-1.5 py-1 rounded-md outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[1.83px] top-[1.83px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Primary text-sm font-semibold leading-4 tracking-tight">Delete</div>
        </div>
        <div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative">
            <div className="w-3 h-3 left-[2px] top-[2px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold leading-4 tracking-tight">Schedule</div>
        </div>
      </div>
    </div>
  </div>
</div>
```

---

### 24. Emoji Picker

#### Emoji Picker Component

Всплывающий выборщик эмодзи с поиском и сеточной раскладкой.

- **Container**:
  - Width: w-96 max-w-96 min-w-60 (384px max, 240px min)
  - Height: max-h-48 min-h-48 (192px fixed height)
  - Padding: p-2
  - Background: bg-Backgrounds-surface2
  - Radius: rounded-[32px]
  - Shadow:
    - Drop shadow: shadow-[0px_24px_32px_-12px_rgba(18,18,18,0.10)]
    - Inset glow: shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)]
  - Border: outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
  - Layout: inline-flex flex-col justify-start items-start gap-2

##### Search Bar
- **Container**: self-stretch p-3 bg-Backgrounds-surface1 rounded-[90px]
- **Layout**: inline-flex justify-start items-center gap-2
- **Icon**:
  - Size: w-6 h-6
  - Search icon with magnifying glass shape
  - Circle: w-3 h-3 at [6.75px, 4.48px], outline-[1.50px] outline-Text-Secondary
  - Handle: w-1 h-1 at [4.87px, 15.60px], rounded-sm outline-[1.50px] outline-Text-Secondary
- **Placeholder Text**:
  - Text: "Search emoji"
  - Color: text-Text-Secondary
  - Font: text-sm font-normal

##### Emoji Grid
- **Container**:
  - Size: self-stretch h-32 max-h-32 (128px height)
  - Layout: w-96 h-32 rounded-3xl
  - Display: inline-flex flex-wrap content-start
  - Overflow: overflow-hidden
- **Emoji Item**:
  - Size: w-11 h-11 (44x44px)
  - Radius: rounded-[44px]
  - Shadow: shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)]
  - Backdrop: backdrop-blur-[50px]
  - Image: w-11 h-11 positioned absolute
  - States:
    - Default: no background
    - Hover: slight bg-Backgrounds-surface1
    - Selected: bg-shade08-70/70

#### Light/Dark Mode Variants

##### Light Mode
- Container: bg-Backgrounds-surface2
- Search bar: bg-Backgrounds-surface1
- Text: text-Text-Secondary
- Border: outline-Stroke-Stroke2

##### Dark Mode
- Container: bg-Backgrounds-surface2 (dark variant)
- Search bar: bg-Backgrounds-surface1 (dark variant)
- Text: text-Text-Secondary
- Border: outline-Stroke-Stroke2
- Shadows более заметные в темном режиме

##### Пример использования

```jsx
// Light mode emoji picker
<div data-light-mode="True" className="w-96 max-w-96 min-w-60 max-h-48 min-h-48 p-2 bg-Backgrounds-surface2 rounded-[32px] shadow-[0px_24px_32px_-12px_rgba(18,18,18,0.10)] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex flex-col justify-start items-start gap-2">
  <div data-state="Default" className="self-stretch p-3 bg-Backgrounds-surface1 rounded-[90px] inline-flex justify-start items-center gap-2 overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
    </div>
    <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Search emoji</div>
  </div>
  <div className="self-stretch h-32 max-h-32 relative">
    <div className="w-96 h-32 left-0 top-0 absolute rounded-3xl inline-flex justify-start items-start flex-wrap content-start overflow-hidden">
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
      <div data-state="default" className="w-11 h-11 relative rounded-[44px] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] backdrop-blur-[50px] overflow-hidden">
        <div className="w-11 h-11 left-0 top-0 absolute">
          <img className="w-11 h-11 left-0 top-0 absolute" src="https://placehold.co/44x44" />
        </div>
      </div>
    </div>
  </div>
</div>

// Dark mode emoji picker
<div data-light-mode="False" className="w-96 max-w-96 min-w-60 max-h-48 min-h-48 p-2 bg-Backgrounds-surface2 rounded-[32px] shadow-[0px_24px_32px_-12px_rgba(18,18,18,0.10)] shadow-[inset_2px_4px_16px_0px_rgba(248,248,248,0.06)] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex flex-col justify-start items-start gap-2">
  <div data-state="Default" className="self-stretch p-3 bg-Backgrounds-surface1 rounded-[90px] inline-flex justify-start items-center gap-2 overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
    </div>
    <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Search emoji</div>
  </div>
  <div className="self-stretch h-32 max-h-32 relative">
    <div className="w-96 h-32 left-0 top-0 absolute rounded-3xl inline-flex justify-start items-start flex-wrap content-start overflow-hidden">
      {/* Same grid structure as light mode */}
    </div>
  </div>
</div>
```

---

### 25. Date/Time Picker Inputs

#### Date and Time Inputs with Floating Labels

Поля ввода для даты и времени с плавающей меткой сверху.

- **Container**:
  - Width: w-52 (208px)
  - Layout: inline-flex flex-col justify-start items-start
  - Gap between label and input

##### Floating Label
- **Container**:
  - Position: self-stretch px-4 (positioned above input)
  - Layout: flex flex-col justify-start items-start gap-2
- **Label Badge**:
  - Size: h-5 px-1 py-0.5
  - Background: bg-Backgrounds-surface1 (acts as mask over input border)
  - Layout: inline-flex justify-center items-center gap-0.5
  - Text:
    - Opacity: opacity-80
    - Color: text-Text-Secondary
    - Font: text-xs font-normal
    - Examples: "Date", "Time"

##### Input Field
- **Container**:
  - Size: self-stretch h-12 (48px height)
  - Padding: px-5 py-3
  - Radius: rounded-[32px]
  - Border: outline outline-[1.50px] outline-offset-[-1.50px]
  - Layout: flex flex-col justify-center items-start
  - Overflow: overflow-hidden

##### Input States

**Default State**:
- Border: outline-Stroke-Stroke2
- Text: text-Text-Primary text-sm font-normal
- Truncation: line-clamp-1
- Example values: "May 28, 2044", "05:00 PM"

**Focus State**:
- Border: outline-Stroke-Focus
- Label: remains text-Text-Secondary opacity-80
- Text input: активный курсор, text-Text-Primary

##### Date Input Specifics
- **Format**: "Month Day, Year" (e.g., "May 28, 2044")
- **Icon**: может иметь календарь справа (optional)
- **Picker**: открывает calendar picker при клике

##### Time Input Specifics
- **Format**: "HH:MM AM/PM" (e.g., "05:00 PM")
- **Icon**: может иметь часы справа (optional)
- **Picker**: открывает time picker dropdown при клике

##### Пример использования

```jsx
// Date input - default state
<div className="w-52 inline-flex flex-col justify-start items-start">
  <div className="self-stretch px-4 flex flex-col justify-start items-start gap-2">
    <div className="h-5 px-1 py-0.5 bg-Backgrounds-surface1 inline-flex justify-center items-center gap-0.5">
      <div className="opacity-80 justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Date</div>
    </div>
  </div>
  <div className="self-stretch h-12 px-5 py-3 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex flex-col justify-center items-start overflow-hidden">
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">May 28, 2044</div>
  </div>
</div>

// Time input - default state
<div className="w-52 inline-flex flex-col justify-start items-start">
  <div className="self-stretch px-4 flex flex-col justify-start items-start gap-2">
    <div className="h-5 px-1 py-0.5 bg-Backgrounds-surface1 inline-flex justify-center items-center gap-0.5">
      <div className="opacity-80 justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Time</div>
    </div>
  </div>
  <div className="self-stretch h-12 px-5 py-3 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex flex-col justify-center items-start overflow-hidden">
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">05:00 PM</div>
  </div>
</div>

// Date input - focus state
<div className="w-52 inline-flex flex-col justify-start items-start">
  <div className="self-stretch px-4 flex flex-col justify-start items-start gap-2">
    <div className="h-5 px-1 py-0.5 bg-Backgrounds-surface1 inline-flex justify-center items-center gap-0.5">
      <div className="opacity-80 justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Date</div>
    </div>
  </div>
  <div data-state="focus" className="self-stretch h-12 px-5 py-3 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Focus flex flex-col justify-center items-start overflow-hidden">
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">May 28, 2044</div>
  </div>
</div>

// Time input - focus state
<div className="w-52 inline-flex flex-col justify-start items-start">
  <div className="self-stretch px-4 flex flex-col justify-start items-start gap-2">
    <div className="h-5 px-1 py-0.5 bg-Backgrounds-surface1 inline-flex justify-center items-center gap-0.5">
      <div className="opacity-80 justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Time</div>
    </div>
  </div>
  <div data-state="focus" className="self-stretch h-12 px-5 py-3 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Focus flex flex-col justify-center items-start overflow-hidden">
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">05:00 PM</div>
  </div>
</div>
```

---

### 26. Time Picker List

#### Time Selection Dropdown List

Выпадающий список для выбора времени с галочкой для выбранного элемента.

- **Container**:
  - Width: w-60 (240px)
  - Layout: может быть частью dropdown menu
  - Background: обычно bg-Backgrounds-surface2 с border
  - Max height с overflow-y-auto для прокрутки

##### List Item (Unselected)
- **Container**:
  - Width: w-60 (240px)
  - Padding: p-3
  - Layout: inline-flex justify-start items-center gap-3
  - Overflow: overflow-hidden
  - Background: transparent
  - Radius: нет (или небольшой при hover)
- **Icon Space**: w-6 h-6 (пустое пространство для галочки)
- **Text**:
  - Color: text-Text-Primary
  - Font: text-sm font-normal
  - Examples: "12:00 PM", "12:30 PM", "01:00 PM"
  - Opacity: может быть opacity-80 для unselected

##### List Item (Selected)
- **Container**:
  - Width: w-60 (240px)
  - Padding: p-3
  - Background: bg-shade08-70/70 (или bg-shade08-70 opacity-70)
  - Radius: rounded-xl
  - Layout: inline-flex justify-start items-center gap-3
  - Overflow: overflow-hidden
- **Checkmark Icon**:
  - Container: w-6 h-6 relative overflow-hidden
  - Checkmark shape: w-3.5 h-3 positioned at [5px, 6px]
  - Border: outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary
- **Text**:
  - Color: text-Text-Primary
  - Font: text-sm font-normal
  - Full opacity (no opacity reduction)

##### Hover State
- Background: bg-Backgrounds-surface1 или slight shade
- Cursor: pointer
- Transition: smooth

##### List Layout
- **Gap**: небольшой gap между items (gap-1 или gap-0.5)
- **Scrolling**: max-h-64 или max-h-80 с overflow-y-auto
- **Padding**: p-2 для всего списка

##### Пример использования

```jsx
// Time list container with items
<div className="w-60 p-2 bg-Backgrounds-surface2 rounded-2xl flex flex-col gap-1">
  {/* Unselected item */}
  <div className="w-60 p-3 inline-flex justify-start items-center gap-3 overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden" />
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">12:00 PM</div>
  </div>

  {/* Selected item */}
  <div className="w-60 p-3 bg-shade08-70/70 rounded-xl inline-flex justify-start items-center gap-3 overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-3.5 h-3 left-[5px] top-[6px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
    </div>
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">12:30 PM</div>
  </div>

  {/* Unselected item */}
  <div className="w-60 p-3 inline-flex justify-start items-center gap-3 overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden" />
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">01:00 PM</div>
  </div>

  {/* Unselected item */}
  <div className="w-60 p-3 inline-flex justify-start items-center gap-3 overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden" />
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">01:30 PM</div>
  </div>

  {/* Unselected item */}
  <div className="w-60 p-3 inline-flex justify-start items-center gap-3 overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden" />
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">02:00 PM</div>
  </div>

  {/* Unselected item */}
  <div className="w-60 p-3 inline-flex justify-start items-center gap-3 overflow-hidden">
    <div className="w-6 h-6 relative overflow-hidden" />
    <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">02:30 PM</div>
  </div>
</div>

// Individual selected item variant
<div className="w-60 p-3 bg-shade08-70/70 rounded-xl inline-flex justify-start items-center gap-3 overflow-hidden">
  <div className="w-6 h-6 relative overflow-hidden">
    <div className="w-3.5 h-3 left-[5px] top-[6px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
  </div>
  <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">03:00 PM</div>
</div>

// Individual unselected item variant
<div className="w-60 p-3 inline-flex justify-start items-center gap-3 overflow-hidden hover:bg-Backgrounds-surface1 rounded-xl transition-colors cursor-pointer">
  <div className="w-6 h-6 relative overflow-hidden" />
  <div className="opacity-80 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">03:30 PM</div>
</div>
```

---

### 27. Connect Button (Integration Button)

#### Integration Connection Button

Кнопка для подключения к внешним сервисам и интеграциям.

- **Container**:
  - Width: w-52 min-w-52 (208px minimum)
  - Padding: p-3
  - Radius: rounded-[48px]
  - Layout: inline-flex justify-center items-center gap-2
  - Overflow: overflow-hidden

##### Default State (Inactive)
- **Background**: bg-Backgrounds-surface2
- **Shadow Stack**:
  - shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)]
  - shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)]
  - shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)]
  - shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)]
  - shadow-[0px_2.1500000953674316px_0.5px_-2px_rgba(0,0,0,0.25)]
- **Border**: outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
- **Backdrop**: backdrop-blur-[32px]

##### Focus/Active State
- **Border**: outline outline-2 outline-offset-[-2px] outline-Stroke-Focus
- **Background**: transparent (no bg-Backgrounds-surface2)
- **No shadow stack**
- **No backdrop-blur**

##### Icon + Text Variant
- **Icon Container**: w-6 h-6 relative
  - Inner container: w-5 h-5 at [2px, 2px] overflow-hidden
  - Icon: w-4 h-4 at [1.67px, 1.38px] bg-Text-Primary
- **Text**: flex-1 text-Text-Primary text-sm font-semibold leading-4 tracking-tight
- **Gap**: gap-2

##### Icon Only Variant
- **Same sizing**: w-52 min-w-52 p-3
- **No text element**
- **Centered icon**: justify-center items-center

##### Пример использования

```jsx
// Default state with icon and text
<div className="w-52 min-w-52 p-3 bg-Backgrounds-surface2 rounded-[48px] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)] shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)] shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)] shadow-[0px_2.1500000953674316px_0.5px_-2px_rgba(0,0,0,0.25)] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 backdrop-blur-[32px] inline-flex justify-center items-center gap-2 overflow-hidden">
  <div className="w-6 h-6 relative">
    <div className="w-5 h-5 left-[2px] top-[2px] absolute overflow-hidden">
      <div className="w-4 h-4 left-[1.67px] top-[1.38px] absolute bg-Text-Primary" />
    </div>
  </div>
  <div className="flex-1 justify-center text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Notion</div>
</div>

// Focus/Active state with icon and text
<div className="w-52 min-w-52 p-3 rounded-[48px] outline outline-2 outline-offset-[-2px] outline-Stroke-Focus inline-flex justify-center items-center gap-2 overflow-hidden">
  <div className="w-6 h-6 relative">
    <div className="w-5 h-5 left-[2px] top-[2px] absolute overflow-hidden">
      <div className="w-4 h-4 left-[1.67px] top-[1.38px] absolute bg-Text-Primary" />
    </div>
  </div>
  <div className="flex-1 justify-center text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Notion</div>
</div>

// Icon only - default state
<div className="w-52 min-w-52 p-3 bg-Backgrounds-surface2 rounded-[48px] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)] shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)] shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)] shadow-[0px_2.1500000953674316px_0.5px_-2px_rgba(0,0,0,0.25)] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 backdrop-blur-[32px] inline-flex justify-center items-center gap-2 overflow-hidden">
  <div className="w-6 h-6 relative">
    <div className="w-5 h-5 left-[2px] top-[2px] absolute overflow-hidden">
      <div className="w-4 h-4 left-[1.67px] top-[1.38px] absolute bg-Text-Primary" />
    </div>
  </div>
</div>

// Icon only - focus state
<div className="w-52 min-w-52 p-3 rounded-[48px] outline outline-2 outline-offset-[-2px] outline-Stroke-Focus inline-flex justify-center items-center gap-2 overflow-hidden">
  <div className="w-6 h-6 relative">
    <div className="w-5 h-5 left-[2px] top-[2px] absolute overflow-hidden">
      <div className="w-4 h-4 left-[1.67px] top-[1.38px] absolute bg-Text-Primary" />
    </div>
  </div>
</div>
```

---

### 28. Toolbar / Action Bar

#### Product Management Toolbar

Панель управления с заголовком, поиском, переключателями вида и bulk actions.

- **Container**:
  - Width: w-[1180px] (1180px)
  - Padding: p-3
  - Layout: inline-flex justify-between items-center

##### Default Toolbar State

**Left Section**:
- **Title Container**: h-12 pl-5 flex justify-center items-center gap-6
- **Title**: text-Text-Primary text-2xl font-medium leading-9 tracking-tight
  - Example: "Products"
- **Search Bar**:
  - Width: w-72 (288px)
  - Padding: pl-3 pr-5 py-3
  - Background: bg-Backgrounds-surface1
  - Radius: rounded-[90px]
  - Layout: flex justify-start items-center gap-2
  - Icon: w-6 h-6 search icon (magnifying glass)
  - Placeholder: "Search products" text-Text-Secondary text-sm font-normal

**Right Section**:
- **Layout**: flex justify-start items-center gap-2
- **View Toggle Buttons**:
  - Grid button: p-3 rounded-[48px] (no outline when default)
    - Icon: w-4 h-4 grid icon, outline-Text-Secondary
  - List button: p-3 rounded-[48px] outline outline-[1.50px] outline-Stroke-Stroke2 (active)
    - Icon: w-4 h-3.5 list icon, outline-Text-Primary

##### Selection State (Bulk Actions)

**Left Section**:
- **Selection Count**: "2 products selected" text-Text-Primary text-2xl font-medium
- **Deselect Button**:
  - Padding: px-7 py-3.5
  - Radius: rounded-[32px]
  - Border: outline outline-[1.50px] outline-Stroke-Stroke2
  - Text: text-Text-Secondary text-sm font-semibold
  - Label: "Deselect"

**Right Section** (Action Buttons):
- **Delete Button**:
  - Size: h-12 px-7 py-3.5
  - Radius: rounded-[32px]
  - Border: outline outline-[1.50px] outline-Stroke-Stroke2
  - Text: text-Text-Secondary text-sm font-semibold "Delete"
- **Publish Button** (Primary Dark):
  - Padding: px-7 py-4
  - Background: bg-gradient-to-b from-zinc-800 to-zinc-800
  - Radius: rounded-[32px]
  - Shadow: shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)]
  - Border: outline outline-[1.50px] outline-white/40
  - Text: text-Text-Light text-sm font-semibold "Publish"

##### Пример использования

```jsx
// Default toolbar (no selection)
<div className="w-[1180px] p-3 inline-flex justify-between items-center">
  <div className="h-12 pl-5 flex justify-center items-center gap-6">
    <div className="justify-start text-Text-Primary text-2xl font-medium font-['Inter_Display'] leading-9 tracking-tight">Products</div>
    <div data-state="default" className="w-72 pl-3 pr-5 py-3 bg-Backgrounds-surface1 rounded-[90px] flex justify-start items-center gap-2 overflow-hidden">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      </div>
      <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">Search products</div>
    </div>
  </div>
  <div className="flex justify-start items-center gap-2">
    <div data-property-1="grid" data-property-2="default" className="p-3 rounded-[48px] inline-flex flex-col justify-center items-center gap-2.5 overflow-hidden">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-4 h-4 left-[3.75px] top-[3.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      </div>
    </div>
    <div data-property-1="list" data-property-2="active" className="p-3 rounded-[48px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex flex-col justify-center items-center gap-2.5 overflow-hidden">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-4 h-3.5 left-[3.75px] top-[5.25px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
      </div>
    </div>
  </div>
</div>

// Selection state with bulk actions
<div className="w-[1180px] p-3 inline-flex justify-between items-center">
  <div className="h-12 pl-5 flex justify-center items-center gap-6">
    <div className="justify-start text-Text-Primary text-2xl font-medium font-['Inter_Display'] leading-9 tracking-tight">2 products selected</div>
    <div className="self-stretch px-7 py-3.5 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-center items-center gap-2 overflow-hidden">
      <div className="text-center justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Deselect</div>
    </div>
  </div>
  <div className="flex justify-start items-start gap-2">
    <div className="h-12 px-7 py-3.5 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-center items-center gap-2 overflow-hidden">
      <div className="text-center justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Delete</div>
    </div>
    <div data-light-mode="True" data-state="Default" data-style="Button" className="px-7 py-4 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/40 flex justify-center items-center gap-2.5 overflow-hidden">
      <div className="justify-start text-Text-Light text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Publish</div>
    </div>
  </div>
</div>
```

---

### 29. Calendar / Date Picker

#### Calendar Component

Полноценный календарь для выбора даты с навигацией по месяцам.

- **Container**:
  - Padding: p-4
  - Background: bg-Backgrounds-surface1
  - Radius: rounded-[32px]
  - Shadow Stack (same as Connect Button):
    - shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)]
    - shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)]
    - shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)]
    - shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)]
    - shadow-[0px_2.1500000953674316px_0.5px_-2px_rgba(0,0,0,0.25)]
  - Border: outline outline-[1.50px] outline-offset-[-1.50px] outline-white
  - Backdrop: backdrop-blur-[32px]
  - Layout: inline-flex flex-col justify-start items-start gap-2

##### Calendar Header
- **Container**: self-stretch inline-flex justify-between items-center
- **Month/Year Display**:
  - Text: "February 2025"
  - Font: text-Text-Primary text-base font-semibold leading-6 tracking-tight
  - Centered

**Navigation Buttons**:
- **Previous Button** (left arrow, disabled in example):
  - Size: w-12 h-12
  - Radius: rounded-[90px]
  - No outline (disabled state)
  - Icon: rotated-180 arrow (w-1 h-2 + w-2.5 h-0 lines)
  - Color: outline-Text-Secondary

- **Next Button** (right arrow, active):
  - Size: w-12 h-12
  - Radius: rounded-[90px]
  - Border: outline outline-[1.50px] outline-Stroke-Stroke2
  - Icon: arrow pointing right
  - Color: outline-Text-Primary

##### Week Days Header
- **Container**: w-80 flex-wrap
- **Day Cell**: w-11 h-11 p-2 rounded-[40px]
- **Text**:
  - opacity-50
  - text-Text-Secondary text-xs font-normal
  - text-center line-clamp-1
  - Labels: "Su", "Mo", "Tu", "We", "Th", "Fr", "Sa"

##### Date Grid
- **Container**: w-80 relative inline-flex flex-wrap content-start
- **Date Cell**: w-11 h-11 p-2.5 rounded-[40px]

**Cell States**:

1. **Disabled (other month)**:
   - opacity-50 (visible)
   - opacity-0 (invisible placeholders)
   - text-Text-Secondary

2. **Default (current month)**:
   - No background
   - text-Text-Primary text-sm font-normal
   - text-center line-clamp-1

3. **Today**:
   - Background: bg-Backgrounds-dark1
   - Text: text-Text-Light text-sm font-normal
   - Radius: rounded-[40px]

4. **Hover**:
   - Border: outline outline-[1.50px] outline-Backgrounds-dark1
   - Text: text-Text-Primary

##### Пример использования

```jsx
// Full calendar component
<div className="p-4 bg-Backgrounds-surface1 rounded-[32px] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)] shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)] shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)] shadow-[0px_2.1500000953674316px_0.5px_-2px_rgba(0,0,0,0.25)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white backdrop-blur-[32px] inline-flex flex-col justify-start items-start gap-2 overflow-hidden">
  {/* Header */}
  <div className="self-stretch inline-flex justify-between items-center">
    <div data-property-1="default" className="w-12 h-12 relative rounded-[90px] overflow-hidden">
      <div className="w-6 h-6 left-[12px] top-[12px] absolute overflow-hidden">
        <div className="w-1 h-2 left-[10px] top-[16px] absolute origin-top-left rotate-180 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        <div className="w-2.5 h-0 left-[18px] top-[12px] absolute origin-top-left rotate-180 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      </div>
    </div>
    <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight">February 2025</div>
    <div data-property-1="default" className="w-12 h-12 relative rounded-[90px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 overflow-hidden">
      <div className="w-6 h-6 left-[12px] top-[12px] absolute overflow-hidden">
        <div className="w-1 h-2 left-[14px] top-[8px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
        <div className="w-2.5 h-0 left-[6px] top-[12px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
      </div>
    </div>
  </div>

  {/* Week days and dates grid */}
  <div className="w-80 relative inline-flex justify-start items-start flex-wrap content-start">
    {/* Week days */}
    <div data-state="week day" className="w-11 h-11 p-2 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">Su</div>
    </div>
    <div data-state="week day" className="w-11 h-11 p-2 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">Mo</div>
    </div>
    <div data-state="week day" className="w-11 h-11 p-2 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">Tu</div>
    </div>
    <div data-state="week day" className="w-11 h-11 p-2 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">We</div>
    </div>
    <div data-state="week day" className="w-11 h-11 p-2 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">Th</div>
    </div>
    <div data-state="week day" className="w-11 h-11 p-2 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">Fr</div>
    </div>
    <div data-state="week day" className="w-11 h-11 p-2 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">Sa</div>
    </div>

    {/* Disabled dates (previous month, invisible) */}
    <div data-state="disable" className="w-11 h-11 p-2.5 opacity-0 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">8</div>
    </div>

    {/* Disabled dates (previous month, visible) */}
    <div data-state="disable" className="w-11 h-11 p-2.5 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch opacity-50 text-center justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">1</div>
    </div>

    {/* Today */}
    <div data-state="today" className="w-11 h-11 p-2.5 bg-Backgrounds-dark1 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch text-center justify-start text-Text-Light text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">7</div>
    </div>

    {/* Default date */}
    <div data-state="default" className="w-11 h-11 p-2.5 rounded-[40px] inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch text-center justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">8</div>
    </div>

    {/* Hover state */}
    <div data-state="hover" className="w-11 h-11 p-2.5 rounded-[40px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Backgrounds-dark1 inline-flex flex-col justify-center items-center gap-2 overflow-hidden">
      <div className="self-stretch text-center justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">12</div>
    </div>
  </div>
</div>
```

---

### 30. Modal / Dialog

#### Reschedule Product Modal

Модальное окно для переноса публикации продукта.

- **Container**:
  - Width: w-[480px] (480px)
  - Padding: p-3
  - Background: bg-Backgrounds-surface1
  - Radius: rounded-[32px]
  - Shadow Stack: (same as Calendar)
  - Border: outline outline-1 outline-offset-[-1px]
  - Backdrop: backdrop-blur-[32px]
  - Layout: inline-flex flex-col justify-center items-start gap-3

##### Product Preview Section
- **Container**:
  - self-stretch p-4
  - Background: bg-Backgrounds-surface2
  - Radius: rounded-[20px]
  - Border: outline outline-[1.50px] outline-Stroke-Subtle/10
  - Layout: inline-flex justify-start items-center gap-5

**Image**:
- Size: w-16 h-16
- Radius: rounded-xl

**Content**:
- **Layout**: flex-1 inline-flex flex-col justify-center items-start
- **Title Row**: inline-flex justify-between items-center
  - Title: text-Text-Primary text-lg font-medium leading-7 line-clamp-1
  - Price Badge: w-16 px-2 py-1.5 bg-green-600/5 rounded-lg outline-green-600/20
    - Text: text-Primary-primary02 text-sm font-semibold "$98.00"
- **Subtitle**: opacity-80 text-Text-Secondary text-sm font-normal
  - Example: "UI Design Kit"

##### Modal Content Section
- **Container**: self-stretch p-5 flex flex-col gap-8

**Header**:
- **Title**: text-Text-Primary text-3xl font-semibold leading-10 tracking-tight
  - "Reschedule product"
- **Description**: text-Text-Tertiary text-base font-normal leading-6
  - "Choose a day and time in the future you want your product to be published."

**Form Fields**:
- **Layout**: inline-flex justify-start items-start gap-3
- **Date Input**: flex-1 (см. section 25)
- **Time Input**: flex-1 (см. section 25)

**Action Buttons**:
- **Layout**: inline-flex justify-end items-center gap-3
- **Cancel Button**:
  - Size: h-12 px-7 py-3.5
  - Radius: rounded-[32px]
  - Border: outline outline-[1.50px] outline-Stroke-Stroke2
  - Text: text-Text-Secondary text-sm font-semibold "Cancel"
- **Reschedule Button** (Primary Dark):
  - Padding: px-7 py-4
  - Background: bg-gradient-to-b from-zinc-800 to-zinc-800
  - Shadow: shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)]
  - Border: outline outline-[1.50px] outline-white/40
  - Text: text-Text-Light text-sm font-semibold "Reschedule"

##### Пример использования

```jsx
<div className="w-[480px] p-3 bg-Backgrounds-surface1 rounded-[32px] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)] shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)] shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)] shadow-[0px_2.1500000953674316px_0.5px_-2px_rgba(0,0,0,0.25)] outline outline-1 outline-offset-[-1px] backdrop-blur-[32px] inline-flex flex-col justify-center items-start gap-3">
  {/* Product preview */}
  <div className="self-stretch p-4 bg-Backgrounds-surface2 rounded-[20px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Subtle/10 inline-flex justify-start items-center gap-5 overflow-hidden">
    <img className="w-16 h-16 relative rounded-xl" src="https://placehold.co/64x64" />
    <div className="flex-1 self-stretch inline-flex flex-col justify-center items-start">
      <div className="self-stretch inline-flex justify-between items-center">
        <div className="justify-start text-Text-Primary text-lg font-medium font-['Inter_Display'] leading-7 line-clamp-1">Fleet Travel UI Kit</div>
        <div data-property-1="True" className="w-16 px-2 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 flex justify-center items-center gap-2 overflow-hidden">
          <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">$98.00</div>
        </div>
      </div>
      <div className="self-stretch opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">UI Design Kit</div>
    </div>
  </div>

  {/* Modal content */}
  <div className="self-stretch p-5 flex flex-col justify-start items-start gap-8">
    <div className="self-stretch flex flex-col justify-start items-start gap-2">
      <div className="self-stretch justify-start text-Text-Primary text-3xl font-semibold font-['Inter_Display'] leading-10 tracking-tight">Reschedule product</div>
      <div className="self-stretch justify-start text-Text-Tertiary text-base font-normal font-['Inter_Display'] leading-6 tracking-tight">Choose a day and time in the future you want your product to be published.</div>
    </div>

    {/* Date/Time inputs */}
    <div className="self-stretch inline-flex justify-start items-start gap-3">
      <div data-input="Date" data-state="default" className="flex-1 inline-flex flex-col justify-start items-start">
        <div className="self-stretch px-4 flex flex-col justify-start items-start gap-2">
          <div className="h-5 px-1 py-0.5 bg-Backgrounds-surface1 inline-flex justify-center items-center gap-0.5">
            <div className="opacity-80 justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Date</div>
          </div>
        </div>
        <div className="self-stretch h-12 px-5 py-3 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex flex-col justify-center items-start overflow-hidden">
          <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">May 28, 2044</div>
        </div>
      </div>
      <div data-input="Time" data-state="default" className="flex-1 inline-flex flex-col justify-start items-start">
        <div className="self-stretch px-4 flex flex-col justify-start items-start gap-2">
          <div className="h-5 px-1 py-0.5 bg-Backgrounds-surface1 inline-flex justify-center items-center gap-0.5">
            <div className="opacity-80 justify-start text-Text-Secondary text-xs font-normal font-['Inter_Display'] leading-5 tracking-tight">Time</div>
          </div>
        </div>
        <div className="self-stretch h-12 px-5 py-3 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex flex-col justify-center items-start overflow-hidden">
          <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">05:00 PM</div>
        </div>
      </div>
    </div>

    {/* Action buttons */}
    <div className="self-stretch inline-flex justify-end items-center gap-3">
      <div className="h-12 px-7 py-3.5 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-center items-center gap-2 overflow-hidden">
        <div className="text-center justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Cancel</div>
      </div>
      <div data-light-mode="True" data-state="Default" data-style="Button" className="px-7 py-4 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/40 flex justify-center items-center gap-2.5 overflow-hidden">
        <div className="justify-start text-Text-Light text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Reschedule</div>
      </div>
    </div>
  </div>
</div>
```

---

### 31. Time Picker Panel

#### Time Selection Panel with Header

Панель выбора времени с отображением выбранного времени в заголовке.

- **Container**:
  - Width: w-72 (288px)
  - Height: h-96 (384px)
  - Padding: p-4
  - Background: bg-Backgrounds-surface1
  - Radius: rounded-[32px]
  - Shadow Stack (same as Calendar/Modal)
  - Border: outline outline-1 outline-offset-[-1px]
  - Backdrop: backdrop-blur-[32px]
  - Layout: inline-flex flex-col justify-start items-start gap-2

##### Header Section
- **Container**: self-stretch h-12 inline-flex justify-between items-center
- **Selected Time Display**:
  - Layout: px-3 py-2.5 flex justify-start items-center gap-3
  - **Icon**: w-6 h-6 relative overflow-hidden
    - Clock icon: w-4 h-5 at [3.75px, 2.75px] outline-Text-Primary
  - **Time Text**: text-Text-Primary text-base font-semibold leading-6 tracking-tight
    - Example: "12:00 PM"
- **Action Button** (placeholder, hidden in this design):
  - Size: w-12 h-12 opacity-0
  - Radius: rounded-[90px]

##### Time List Section
- **Container**: self-stretch flex flex-col justify-start items-start
- **List Items**: self-stretch p-3

**Item States**:

1. **Default (Unselected)**:
   - Padding: p-3
   - Layout: inline-flex justify-start items-center gap-3
   - Icon: w-6 h-6 opacity-0 (empty space)
   - Text: text-Text-Secondary text-sm font-normal
   - Examples: "11:30 AM", "12:30 PM", "01:30 PM"

2. **Selected**:
   - Padding: p-3
   - Layout: inline-flex justify-start items-center gap-3
   - **Checkmark Icon**: w-6 h-6 visible
     - Checkmark: w-3.5 h-3 at [5px, 6px] outline-Text-Primary
   - Text: text-Text-Primary text-sm font-normal
   - Example: "12:00 PM"

3. **Hover**:
   - Padding: p-3
   - Background: bg-shade08-70/70
   - Radius: rounded-xl
   - Layout: inline-flex justify-start items-center gap-3
   - Icon: w-6 h-6 opacity-0
   - Text: text-Text-Primary text-sm font-normal
   - Example: "01:00 PM"

4. **Placeholder** (bottom, hidden):
   - opacity-0

##### Пример использования

```jsx
<div className="w-72 h-96 p-4 bg-Backgrounds-surface1 rounded-[32px] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)] shadow-[0px_6px_13px_0px_rgba(8,8,8,0.03)] shadow-[0px_24px_24px_-16px_rgba(8,8,8,0.04)] shadow-[0px_2.1500000953674316px_0.5px_-2px_rgba(0,0,0,0.25)] outline outline-1 outline-offset-[-1px] backdrop-blur-[32px] inline-flex flex-col justify-start items-start gap-2 overflow-hidden">
  {/* Header with selected time */}
  <div className="self-stretch h-12 inline-flex justify-between items-center">
    <div className="px-3 py-2.5 flex justify-start items-center gap-3">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-4 h-5 left-[3.75px] top-[2.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
      </div>
      <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight">12:00 PM</div>
    </div>
    <div data-property-1="default" className="w-12 h-12 relative opacity-0 rounded-[90px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 overflow-hidden">
      <div className="w-6 h-6 left-[12px] top-[12px] absolute overflow-hidden" />
    </div>
  </div>

  {/* Time list */}
  <div className="self-stretch flex flex-col justify-start items-start">
    {/* Unselected item */}
    <div data-property-1="default" className="self-stretch p-3 inline-flex justify-start items-center gap-3">
      <div className="w-6 h-6 relative opacity-0 overflow-hidden">
        <div className="w-3.5 h-3 left-[5px] top-[6px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
      </div>
      <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">11:30 AM</div>
    </div>

    {/* Selected item */}
    <div data-property-1="selected" className="self-stretch p-3 inline-flex justify-start items-center gap-3">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-3.5 h-3 left-[5px] top-[6px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
      </div>
      <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">12:00 PM</div>
    </div>

    {/* Unselected item */}
    <div data-property-1="default" className="self-stretch p-3 inline-flex justify-start items-center gap-3">
      <div className="w-6 h-6 relative opacity-0 overflow-hidden">
        <div className="w-3.5 h-3 left-[5px] top-[6px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
      </div>
      <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">12:30 PM</div>
    </div>

    {/* Hover item */}
    <div data-property-1="hover" className="self-stretch p-3 relative bg-shade08-70/70 rounded-xl inline-flex justify-start items-center gap-3 overflow-hidden">
      <div className="w-6 h-6 relative opacity-0 overflow-hidden">
        <div className="w-3.5 h-3 left-[5px] top-[6px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
      </div>
      <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">01:00 PM</div>
    </div>

    {/* More items... */}
    <div data-property-1="default" className="self-stretch p-3 inline-flex justify-start items-center gap-3">
      <div className="w-6 h-6 relative opacity-0 overflow-hidden">
        <div className="w-3.5 h-3 left-[5px] top-[6px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
      </div>
      <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">01:30 PM</div>
    </div>
  </div>
</div>
```

---

### 32. Reaction Button / Like Counter

#### Like Counter Button

Кнопка для лайков/реакций с иконкой и счетчиком.

- **Container**:
  - Width: w-48 (192px)
  - Padding: p-1
  - Radius: rounded-[48px]
  - Border: outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2
  - Layout: inline-flex justify-center items-center gap-2
  - Overflow: overflow-hidden

##### Icon Container
- **Size**: w-10 h-10 (40x40px)
- **Background**: bg-Secondary-secondary04
- **Radius**: rounded-[40px]
- **Icon**:
  - Container: w-6 h-6 at [8px, 8px]
  - Inner: w-5 h-5 at [2.75px, 2.75px]
  - Border: outline outline-[1.50px] outline-offset-[-0.75px] outline-black
  - Может быть heart, thumbs-up, или другая иконка реакции

##### Counter Text
- **Layout**: flex-1
- **Font**: text-sm font-normal leading-5 tracking-tight
- **States**:
  - Inactive: opacity-50 text-Text-Secondary
  - Active: text-Text-Primary (no opacity)

##### Button States

**Inactive (Not Liked)**:
- Counter: opacity-50 text-Text-Secondary
- Icon: outline-black (or theme color)
- Example: "98" with 50% opacity

**Active (Liked)**:
- Counter: text-Text-Primary (full opacity)
- Icon: может быть filled вариант
- Example: "98" with full opacity

**Hover**:
- Slight background change on container
- Cursor: pointer

##### Пример использования

```jsx
// Inactive state
<div className="w-48 p-1 rounded-[48px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-center items-center gap-2 overflow-hidden">
  <div className="w-10 h-10 relative bg-Secondary-secondary04 rounded-[40px] overflow-hidden">
    <div className="w-6 h-6 left-[8px] top-[8px] absolute overflow-hidden">
      <div className="w-5 h-5 left-[2.75px] top-[2.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-black" />
    </div>
  </div>
  <div className="flex-1 opacity-50 justify-center text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">98</div>
</div>

// Active state
<div className="w-48 p-1 rounded-[48px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-center items-center gap-2 overflow-hidden">
  <div className="w-10 h-10 relative bg-Secondary-secondary04 rounded-[40px] overflow-hidden">
    <div className="w-6 h-6 left-[8px] top-[8px] absolute overflow-hidden">
      <div className="w-5 h-5 left-[2.75px] top-[2.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-black" />
    </div>
  </div>
  <div className="flex-1 justify-center text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">98</div>
</div>
```

---

### 33. Table Row / Product List Item

#### Product List Row Component

Строка таблицы продуктов с полной информацией и интерактивными элементами.

- **Container**:
  - Width: w-[1148px] (1148px)
  - Padding: p-4
  - Layout: inline-flex justify-start items-start gap-6
  - Overflow: overflow-hidden

##### Row States

**Default State**:
- No background
- Border bottom: border-b-[1.50px] border-Stroke-Subtle/10
- No shadows
- Checkbox visible but no action buttons

**Hover/Selected State**:
- Background: bg-Backgrounds-highlight
- Radius: rounded-2xl
- Border: outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100
- Shadows:
  - shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)]
  - shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)]
  - shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)]
- Action buttons visible (Edit, Delete, Unpublish)

**Bottom Row Variant**:
- Border: border-b-[1.50px] border-Stroke-Subtle (более заметный)

##### Left Section (Product Info)
- **Container**: w-96 h-16 flex justify-start items-start gap-5

**Checkbox**:
- Size: w-6 h-6
- Border: border-2 border-Stroke-Stroke2
- Radius: rounded-md
- Hover variant: border-Stroke-Highlight/50

**Product Image**:
- Size: w-16 h-16 (64x64px)
- Radius: rounded-xl
- Source: product thumbnail

**Product Info**:
- Layout: flex-1 inline-flex flex-col justify-center items-start
- **Title**: text-Text-Primary text-base font-semibold leading-6 line-clamp-1
  - Example: "Bento Pro v.2"
- **Subtitle**: opacity-80 text-Text-Secondary text-sm font-normal
  - Example: "UI Design Kit"

**Action Buttons** (visible on hover):
- Layout: inline-flex justify-start items-start gap-2
- Button structure: pl-1 pr-1.5 py-1 rounded-md
- Buttons:
  - Edit: pencil icon + "Edit" text
  - Delete: trash icon + "Delete" text
  - Unpublish: eye-off icon + "Unpublish" text
- Icon: w-4 h-4 with w-3 h-3 inner outline-Text-Secondary
- Text: opacity-80 text-Text-Secondary text-sm font-semibold

##### Right Section (Metrics)
- **Container**: flex-1 py-2 flex justify-between items-center

**Status Badge**:
- Width: w-20
- Badge: px-2 py-1.5 bg-green-600/5 rounded-lg
- Border: outline outline-[1.50px] outline-green-600/20
- Text: text-Primary-primary02 text-sm font-semibold "Active"

**Price**:
- Width: w-14
- Text: text-Text-Primary text-sm font-normal "$98"

**Revenue with Trend**:
- Container: w-36 inline-flex items-center gap-2
- **Revenue**: w-12 text-Text-Primary text-sm "$3,200"
- **Trend Badge**:
  - Padding: px-2 py-1.5
  - Background: bg-green-600/5 (для роста) или bg-red-600/5 (для падения)
  - Border: outline outline-[1.50px] outline-green-600/20
  - Layout: flex items-center gap-1
  - **Arrow Icon**: w-4 h-4
    - Up arrow: -rotate-180 для роста
    - Down arrow: normal для падения
    - Color: outline-Primary-primary02 (green) or outline-red-600
  - **Percentage**: text-Primary-primary02 text-sm font-semibold "+36.8%"

**Rating**:
- Container: w-20 flex items-center gap-2
- **Star Icon**: w-5 h-5
  - Inner: w-4 h-4 at [1.25px, 0.83px] bg-Text-Secondary
- **Score + Count**: flex items-center gap-1
  - Score: text-Text-Primary text-sm "4.8"
  - Count: text-Text-Secondary text-sm "(88)"

**Time Progress**:
- Container: w-24
- Layout: py-0.5 rounded-lg flex items-center gap-2
- **Time Text**: w-8 text-Text-Primary text-sm "48m"
- **Progress Bar**:
  - Container: w-8 h-1.5 bg-shade07-40/40 rounded-sm
  - Fill: w-3 h-1.5 bg-Chart-Green rounded-sm (positioned left-0)

##### Пример использования

```jsx
// Default row state
<div className="w-[1148px] p-4 inline-flex justify-start items-start gap-6 overflow-hidden">
  {/* Left section */}
  <div className="w-96 h-16 flex justify-start items-start gap-5">
    <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
    </div>
    <img className="w-16 h-16 relative rounded-xl" src="https://placehold.co/64x64" />
    <div className="flex-1 self-stretch inline-flex flex-col justify-center items-start">
      <div className="self-stretch justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">Bento Pro v.2</div>
      <div className="self-stretch opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">UI Design Kit</div>
    </div>
  </div>

  {/* Right section with metrics */}
  <div className="flex-1 py-2 flex justify-between items-center">
    {/* Status */}
    <div className="w-20 inline-flex flex-col justify-start items-start gap-2.5">
      <div data-property-1="True" className="px-2 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 inline-flex justify-center items-center gap-2 overflow-hidden">
        <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Active</div>
      </div>
    </div>

    {/* Price */}
    <div className="inline-flex flex-col justify-start items-start gap-2.5">
      <div className="w-14 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">$98</div>
    </div>

    {/* Revenue with trend */}
    <div className="w-36 inline-flex flex-col justify-start items-start gap-2.5">
      <div className="inline-flex justify-start items-center gap-2">
        <div className="w-12 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">$3,200</div>
        <div data-trend="up" className="px-2 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 flex justify-center items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-[2.67px] h-1.5 left-[5.33px] top-[6.67px] absolute origin-top-left -rotate-180 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Primary-primary02" />
            <div className="w-2 h-0 left-[8px] top-[12px] absolute origin-top-left rotate-180 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Primary-primary02" />
          </div>
          <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">36.8%</div>
        </div>
      </div>
    </div>

    {/* Rating */}
    <div className="w-20 flex justify-start items-start gap-2.5">
      <div className="flex justify-start items-center gap-2">
        <div className="w-5 h-5 relative overflow-hidden">
          <div className="w-4 h-4 left-[1.25px] top-[0.83px] absolute bg-Text-Secondary" />
        </div>
        <div className="flex justify-start items-center gap-1">
          <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">4.8</div>
          <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">(88)</div>
        </div>
      </div>
    </div>

    {/* Time progress */}
    <div className="w-24 inline-flex flex-col justify-start items-start gap-2.5">
      <div data-property-1="03" className="py-0.5 rounded-lg inline-flex justify-center items-center gap-2">
        <div className="w-8 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">48m</div>
        <div className="w-8 h-1.5 relative bg-shade07-40/40 rounded-sm">
          <div className="w-3 h-1.5 left-0 top-0 absolute bg-Chart-Green rounded-sm" />
        </div>
      </div>
    </div>
  </div>
</div>

// Hover/Selected state with action buttons
<div className="w-[1148px] p-4 bg-Backgrounds-highlight rounded-2xl shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)] shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)] shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)] outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100 inline-flex justify-start items-start gap-6 overflow-hidden">
  <div className="w-96 h-16 flex justify-start items-start gap-5">
    <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
    </div>
    <img className="w-16 h-16 relative rounded-xl" src="https://placehold.co/64x64" />
    <div className="flex-1 self-stretch inline-flex flex-col justify-center items-start">
      <div className="self-stretch justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">Bento Pro v.2</div>
      {/* Action buttons visible on hover */}
      <div className="inline-flex justify-start items-start gap-2">
        <div data-property-1="default" className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Edit</div>
        </div>
        <div data-property-1="default" className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[1.83px] top-[1.83px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Delete</div>
        </div>
        <div data-property-1="default" className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3.5 h-3 left-[1.49px] top-[1.83px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">Unpublish</div>
        </div>
      </div>
    </div>
  </div>
  {/* Same metrics section as above */}
  <div className="flex-1 py-2 flex justify-between items-center">
    {/* ... */}
  </div>
</div>

// Row with bottom border (last in section)
<div className="w-[1148px] p-4 border-b-[1.50px] border-Stroke-Subtle inline-flex justify-start items-start gap-6 overflow-hidden">
  {/* Same structure as default */}
</div>
```

---

## Паттерны

### Dashboard Layouts

#### Grid Dashboard

- **Grid**:
- **Card Spacing**:
- **Responsive**:

#### Sidebar + Content

- **Sidebar Width**:
- **Content Area**:
- **Gap**:
- **Responsive**:

---

### Form Patterns

#### Single Column Form

- **Max Width**:
- **Field Spacing**:
- **Button Group**:
- **Layout**:

#### Multi Column Form

- **Grid**:
- **Full Width Fields**:
- **Responsive**:

#### Wizard / Stepper Form

- **Steps Indicator**:
- **Content Area**:
- **Navigation**:
- **Progress**:

---

### Data Visualization

#### Dashboard Card with Chart

- **Header**:
  - Title:
  - Subtitle:
  - Actions:
- **Chart Area**:
- **Footer**:

#### Table with Filters

- **Filter Bar**:
  - Height:
  - Background:
  - Padding:
  - Border Bottom:
- **Table**:
- **Pagination**:

---

## Состояния

### Interactive States

#### Default
- Border: outline-[1.50px] Stroke-Stroke2
- Background: соответствует компоненту
- Text: Text-Primary или Text-Secondary
- Cursor: default или pointer

#### Hover
- Border: outline-shade07-50/50
- Background: может измениться (to be defined для каждого компонента)
- Text: может измениться на Text-Primary
- Cursor: pointer
- Transition: smooth transitions

#### Active/Focus
- Border: outline-[1.50px] Stroke-Stroke2 или Primary-primary03
- Cursor: visible для inputs (w-0.5 h-4 bg-Text-Blue)
- Background: может быть подсвечен
- Text: Text-Primary
- Ring/Outline: более выраженная обводка

#### Disabled
- Border: rgba(Stroke-Stroke2, 0.5)
- Background: приглушенный
- Text: Text-Tertiary или rgba(Text-Secondary, 0.4)
- Cursor: not-allowed
- Opacity: может использоваться opacity-50

#### Loading
- Skeleton: shade07-40/40 background
- Animation: shimmer или pulse
- Dots separator: shade07-60/60
- Progress: gradient from-shade08-100 to-shade09-100

#### Error
- Border: outline-Primary-primary03 (красный/primary цвет для ошибок)
- Text: может быть красным
- Icon: alert или error icon
- Message: отображается под полем

#### Success
- Border: может быть зеленым (to be defined)
- Text: может быть зеленым
- Icon: checkmark icon
- Message: отображается под полем

---

## Иконки

### Icon System

- **Library**: Custom icons (возможно Lucide, Heroicons или custom)
- **Sizes**:
  - XS: 12x12px
  - SM: 14x14px (w-3.5 h-3.5)
  - Base: 16x16px (w-4 h-4) - основной размер
  - MD: 20x20px (w-5 h-5)
  - LG: 24x24px (w-6 h-6) - для buttons и навигации
  - XL: 32x32px
- **Stroke Width**: 1.50px (outline-[1.50px]), 0.75px (outline-offset-[-0.75px])
- **Style**: Outline/stroke style (не заливка)
- **Color**:
  - Primary: Text-Primary
  - Secondary: Text-Secondary
  - Tertiary: Text-Tertiary
  - Inverse: Text-Light

### Common Icons

| Название | Использование | Размер по умолчанию |
|----------|---------------|---------------------|
| Search | Search inputs | 24x24px (w-6 h-6) |
| Close / X | Tooltips, modals | 16x16px (w-4 h-4) |
| Chevron Down | Dropdowns, selects | 24x24px (w-6 h-6) |
| Chevron Right | Tree navigation, expandable menus | 24x24px (w-6 h-6) |
| Arrow Right | Navigation, pagination | 24x24px (w-6 h-6) |
| Arrow Left | Navigation, pagination | 24x24px (w-6 h-6) |
| Arrow Up | Trends, sorting | 16x16px (w-4 h-4) |
| Arrow Down | Trends, sorting | 16x16px (w-4 h-4) |
| Eye / Eye Off | Password visibility toggle | 16x16px (w-4 h-4) |
| Bell | Notifications | 24x24px (w-6 h-6) |
| Mail | Messages | 24x24px (w-6 h-6) |
| User | Profile, avatar placeholder | 24x24px (w-6 h-6) |
| Settings | Settings button | 16x16px (w-4 h-4) |

#### Chevron/Arrow Icon Details

Chevron иконки используются для навигации и раскрывающихся элементов.

**Chevron Structure**:
- **Container**: w-6 h-6, relative overflow-hidden
- **Inner Element**: w-1 h-2 (4px width, 8px height), rounded-sm
- **Positioning**: positioned left-[8px] top-[14px] or similar
- **Outline**: outline-[1.50px] outline-offset-[-0.75px]
- **Rotation** для направления:
  - **Right**: origin-top-left -rotate-90 (collapsed state)
  - **Down**: origin-top-left rotate-90 или default (expanded state)
  - **Left**: origin-top-left rotate-180
  - **Up**: no rotation or custom

**Usage Examples**:

```jsx
// Chevron Right (collapsed menu)
<div className="w-6 h-6 relative overflow-hidden">
  <div className="w-1 h-2 left-[8px] top-[14px] absolute origin-top-left -rotate-90 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
</div>

// Chevron Down (expanded menu)
<div className="w-6 h-6 relative overflow-hidden">
  <div className="w-1 h-2 left-[8px] top-[14px] absolute origin-top-left rotate-90 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
</div>

// Chevron Left
<div className="w-6 h-6 relative overflow-hidden">
  <div className="w-1 h-2 left-[16px] top-[10px] absolute origin-top-left rotate-90 rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
</div>
```

**Arrow Icons** (for trends):
- Used in trend badges
- Smaller size: typically part of w-4 h-4 container
- Can point up (positive trend) or down (negative trend)
- Colors: Primary-primary02 (green, up), Primary-primary03 (red, down)

**Иконки в компонентах:**
- Icons имеют вложенную структуру: контейнер (w-6 h-6) → overflow-hidden → внутренний icon (w-4 h-4 или w-3.5)
- Offset позиционирование: left-[3px] top-[3px] или left-[4px] top-[4px] внутри контейнера
- Для иконок используется outline style с offset для создания эффекта обводки
- Rotation применяется с origin-top-left для правильного вращения

### Brand Icons / Social Icons

Коллекция цветных иконок для брендов, социальных сетей и популярных сервисов.

- **Size**: w-4 h-4 (16x16px) - стандартный размер
- **Style**: filled/colored icons с градиентами и фирменными цветами
- **Usage**: для отображения социальных ссылок, интеграций, платформ

#### Common Brand Icons

**Filled Icons** (простые заливки):
- **Star** (filled): w-3.5 h-3.5, bg-Text-Primary
- **Heart** (filled): w-4 h-3.5, bg-Text-Primary
- **Generic Icon**: w-4 h-4, bg-Text-Primary

**Colored Brand Icons**:

##### Instagram
- w-4 h-4, gradient background
- Outer: bg-orange-500 или gradient
- Inner ring: bg-stone-900
- Center circle: bg-orange-500
- Pattern: nested circles with brand colors

##### Facebook
- w-4 h-4
- Background: bg-gradient-to-b from-blue-600 to-blue-800
- 'f' letter: bg-white

##### Twitter/X
- w-4 h-4
- Background: bg-cyan-400
- Inner: bg-emerald-950
- X shape: bg-cyan-400

##### Windows
- w-4 h-4 разделен на 4 квадрата
- Градиенты: from-sky-300 to-sky-400, from-cyan-400 to-sky-500, from-blue-600 to-sky-500
- Pattern: 4 separated squares forming window

##### YouTube
- w-4 h-4
- Background: bg-orange-700
- Play button: bg-white

##### Figma
- w-4 h-4 из 5 цветных кругов
- Colors: emerald-500, purple-500, orange-600, red-400, cyan-400
- Pattern: 5 circles in specific positions

##### Crown (Premium)
- w-4 h-4
- Colors: amber-600, amber-500, amber-400, yellow-100
- Complex shape с градиентами

##### Generic/Placeholder
- img placeholders: placehold.co/16x16

##### Monochrome Icons
- w-4 h-4 простые фигуры
- bg-Text-Primary
- Различные shapes (filled squares, circles, etc.)

#### Icon with Badge
- w-4 h-4 base icon
- Small badge/dot positioned: w-1 h-1, bg-sky-800
- Example: notification badge on icon

#### Purple Variant
- w-4 h-4
- Background: bg-purple-300
- Inner: bg-slate-900
- Center: bg-purple-300

#### Usage Notes

- Brand icons должны использовать официальные цвета брендов
- Для placeholder используйте generic monochrome icons
- Размер 16x16px оптимален для inline использования
- Для больших размеров используйте пропорциональное масштабирование
- Соблюдайте brand guidelines при использовании логотипов

#### Пример использования

```jsx
// Generic filled icon
<div className="w-4 h-4 relative overflow-hidden">
  <div className="w-3.5 h-3.5 left-[1.33px] top-[1.10px] absolute bg-Text-Primary" />
</div>

// Instagram icon
<div className="w-4 h-4 relative">
  <div className="w-4 h-4 left-0 top-0 absolute bg-orange-500" />
  <div className="w-3.5 h-3.5 left-[1px] top-[1px] absolute bg-stone-900" />
  <div className="w-2 h-2 left-[4.09px] top-[4.33px] absolute bg-orange-500" />
</div>

// Facebook icon
<div className="w-4 h-4 relative">
  <div className="w-4 h-4 left-0 top-0 absolute bg-gradient-to-b from-blue-600 to-blue-800" />
  <div className="w-2.5 h-1.5 left-[2.50px] top-[4.93px] absolute bg-white" />
</div>

// Figma icon (5 circles)
<div className="w-4 h-4 relative">
  <div className="w-1.5 h-1.5 left-[3px] top-[10.67px] absolute bg-emerald-500" />
  <div className="w-1.5 h-1.5 left-[3px] top-[5.33px] absolute bg-purple-500" />
  <div className="w-1.5 h-1.5 left-[3px] top-0 absolute bg-orange-600" />
  <div className="w-1.5 h-1.5 left-[8.33px] top-0 absolute bg-red-400" />
  <div className="w-1.5 h-1.5 left-[8.33px] top-[5.33px] absolute bg-cyan-400" />
</div>

// Image placeholder
<div className="w-4 h-4 relative overflow-hidden">
  <img className="w-4 h-4 left-0 top-0 absolute" src="https://placehold.co/16x16" />
</div>
```

---

## 34. Simplified Table Row / Simple Product Row

### Описание / Description

Упрощенная версия строки таблицы продуктов с базовой информацией: категория с иконкой, цена и дата. Более компактная альтернатива полной строке с метриками.

Simplified version of product table row with basic info: category with icon, price, and date. More compact alternative to full metrics row.

### Спецификация / Specification

#### Базовая структура / Base Structure

```
Container (w-[1148px] p-4)
├── Left Section (w-96 h-16)
│   ├── Checkbox (w-6 h-6)
│   ├── Product Image (w-16 h-16)
│   └── Product Info
│       ├── Title (text-base font-semibold)
│       └── URL (text-sm opacity-80)
└── Right Section (flex-1 py-2)
    ├── Category (icon + text)
    ├── Price Badge (bg-green-600/5)
    └── Date/Time (text-sm)
```

#### Dimensions

- Container width: `w-[1148px]`
- Container padding: `p-4` (16px all sides)
- Row height: `h-16` (64px)
- Product image: `w-16 h-16` (64x64px)
- Checkbox: `w-6 h-6` (24x24px)
- Category icon: `w-6 h-6`
- Price badge: `w-12 h-7` (48x28px)
- Spacing between sections: `gap-6` (24px)
- Spacing within sections: `gap-5` (20px)

#### Typography

**Product Title:**
- Font: `font-['Inter_Display']`
- Size: `text-base` (16px)
- Weight: `font-semibold` (600)
- Line height: `leading-6` (24px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Primary`
- Truncation: `line-clamp-1`

**Product URL:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Secondary`
- Opacity: `opacity-80`

**Category Text:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Color: `text-Text-Primary`
- Width: `w-32` (128px)

**Price:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Color: `text-Primary-primary02` (green)

**Date/Time:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Color: `text-Text-Secondary`
- Width: `w-40` (160px)

#### Colors

**Checkbox (placeholder):**
- Border: `border-2 border-Stroke-Stroke2`
- Border radius: `rounded-md`

**Product Image:**
- Border radius: `rounded-xl`

**Price Badge:**
- Background: `bg-green-600/5` (5% opacity green)
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20`
- Border radius: `rounded-lg`
- Padding: `px-3 py-1.5`

**Category Icon:**
- Outline: `outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary`

#### Layout

**Left Section:**
- Display: `flex justify-start items-center`
- Gap: `gap-5` (20px)
- Contains: checkbox, image, product info

**Right Section:**
- Display: `flex justify-start items-center`
- Gap: `gap-12` (48px)
- Padding: `py-2`
- Contains: category, price, date

**Product Info Column:**
- Display: `inline-flex flex-col justify-center items-start`
- Flex: `flex-1` (takes remaining space)

#### States

##### Default State
- Checkbox: placeholder state с `data-status="placeholder"`
- Image: loaded с placeholder fallback
- Text: полная видимость
- Price badge: зеленый фон с outline

##### Hover State (optional)
- Background: легкое выделение строки
- Cursor: pointer при наведении на интерактивные элементы

##### Selected State (via checkbox)
- Checkbox: checked appearance
- Возможно выделение всей строки

##### Highlighted/Active Row State

**Purpose:**
- Показывает активную/выбранную строку с prominent выделением
- Используется для drag-and-drop preview, active editing, или focused item

**Visual Appearance (Light Mode):**
- Background: `bg-Backgrounds-highlight`
- Border radius: `rounded-2xl` (вместо без border radius)
- Multiple shadow layers:
  - Layer 1: `shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)]` - soft shadow
  - Layer 2: `shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)]` - depth shadow
  - Layer 3: `shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)]` - white inset border effect
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100`
- Padding: `p-4` (same as default)

**Visual Appearance (Dark Mode):**
- Background: `bg-Backgrounds-highlight` (lighter in dark mode via CSS vars)
- Border radius: `rounded-2xl`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100`
- NO multiple shadows (cleaner appearance)
- Checkbox border: `border-Stroke-Highlight/50` (вместо Stroke-Stroke2)

**Content Changes:**
- URL строка заменяется на action buttons
- Action buttons: Edit, Delete, Schedule (или другие actions)
- Buttons располагаются в том же месте где URL
- Same layout для category, price, date

**Action Buttons:**
- Padding: `pl-1 pr-1.5 py-1`
- Border radius: `rounded-md`
- Gap: `gap-2` between buttons
- Icon: `w-4 h-4` with `w-3 h-3` shape inside
- Text: `text-sm font-semibold opacity-80 text-Text-Secondary`
- Default state: no outline
- Hover state: with `outline-Stroke-Stroke2`

##### Row with Border Separator

**Light Mode:**
- Border bottom: `border-b-[1.50px] border-Stroke-Subtle/10`
- Используется между строками в списке

**Dark Mode:**
- Border bottom: `border-b-[1.50px] border-Stroke-Subtle`
- More visible border для contrast

##### Skeleton/Loading Row State

**Purpose:**
- Показывает загрузку новых данных
- Placeholder во время fetch операций
- Создает smooth transition при добавлении новых строк

**Light Mode Skeleton:**
- Checkbox: `w-6 h-6 opacity-80 bg-shade09-100 rounded-md`
- Image: `w-16 h-16 bg-shade09-100 rounded-xl`
- Text lines: `h-2 bg-shade09-100 rounded`
- Title line: `w-24 h-2`
- URL line: `w-40 h-2` (self-stretch)
- Price line: `w-16 h-2`
- Date line: `w-40 h-2`

**Dark Mode Skeleton:**
- Checkbox: `w-6 h-6 opacity-80 bg-shade04-100 rounded-md`
- Image: `w-16 h-16 bg-shade04-100 rounded-xl`
- Text lines: `h-2 bg-shade04-100 rounded`
- Same dimensions as light mode
- Lighter shade для dark backgrounds

**Layout:**
- Same padding and structure as regular row (`p-4`)
- Border top: `border-t border-Stroke-Subtle/10` (light) или `border-Stroke-Subtle` (dark)
- Gap between elements maintained
- Text containers positioned with relative positioning

**Animation (optional):**
- Pulse animation можно добавить для loading effect
- Shimmer effect для более динамичного вида
- Maintains consistent height с regular rows

**Usage:**
- Display skeleton rows внизу списка при infinite scroll
- Replace skeleton с real data when loaded
- Show 1-3 skeleton rows в зависимости от loading state
- Используется в таблицах, lists, feeds

#### Price Badge Variants

**Active/Paid Price (Green):**
- Background: `bg-green-600/5` (5% opacity green)
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20`
- Text color: `text-Primary-primary02` (green)
- Border radius: `rounded-lg`
- Padding: `px-3 py-1.5`
- Width: `w-12`
- Example: "$98", "$49", "$299"

**Free/Zero Price (Gray):**
- Background: `bg-Backgrounds-surface1`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2`
- Text color: `text-Text-Primary`
- Border radius: `rounded-lg`
- Padding: `px-3 py-1.5`
- Width: `w-12`
- Example: "$0.0", "Free"

**Free/Zero Price (Red) - Alternative:**
- Background: `bg-red-600/5` (5% opacity red)
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-red-600/20`
- Text color: `text-Primary-primary03` (red)
- Border radius: `rounded-lg`
- Padding: `px-2 py-1.5`
- Width: `w-16`
- Data attribute: `data-property-1="False"`
- Example: "$0.00"

**Usage:**
- Green badge: для платных продуктов, привлекает внимание к цене
- Gray badge: для бесплатных продуктов, нейтральный appearance
- Red badge: для бесплатных продуктов с предупреждением или выделением
- Consistent width для alignment в таблице

#### Responsive Behavior

- Fixed width: `w-[1148px]` для desktop layouts
- Overflow handling: `overflow-hidden`
- Mobile: требует адаптации (stack vertical или scroll horizontal)

#### Пример использования / Usage Example

```jsx
// Simplified Product Row
<div className="w-[1148px] p-4 inline-flex justify-start items-start gap-6 overflow-hidden">
  {/* Left Section: Checkbox + Image + Info */}
  <div className="w-96 h-16 flex justify-start items-center gap-5">
    {/* Checkbox */}
    <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
    </div>

    {/* Product Image */}
    <img
      className="w-16 h-16 relative rounded-xl"
      src="https://placehold.co/64x64"
    />

    {/* Product Info */}
    <div className="flex-1 self-stretch inline-flex flex-col justify-center items-start">
      <div className="self-stretch justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
        Bento Matte 3D Illustration
      </div>
      <div className="self-stretch opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
        ui8.net/product/product-link
      </div>
    </div>
  </div>

  {/* Right Section: Category + Price + Date */}
  <div className="flex-1 py-2 flex justify-start items-center gap-12">
    {/* Category with Icon */}
    <div className="flex justify-start items-center gap-2">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-4 h-4 left-[3.75px] top-[3.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      </div>
      <div className="w-32 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
        UI Design Kit
      </div>
    </div>

    {/* Price Badge */}
    <div className="w-28 h-7 relative">
      <div
        data-property-1="Default"
        className="w-12 px-3 py-1.5 left-0 top-0 absolute bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 inline-flex justify-center items-center gap-1"
      >
        <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
          $98
        </div>
      </div>
    </div>

    {/* Date and Time */}
    <div className="w-40 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
      Apr 9, 2044 at 3:55 PM
    </div>
  </div>
</div>

// Highlighted/Active Row - Light Mode
<div className="w-[1148px] p-4 bg-Backgrounds-highlight rounded-2xl shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)] shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)] shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)] outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100 inline-flex justify-start items-start gap-6 overflow-hidden">
  {/* Left Section */}
  <div className="w-96 h-16 flex justify-start items-center gap-5">
    <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
    </div>

    <img
      className="w-16 h-16 relative rounded-xl"
      src="https://placehold.co/64x64"
    />

    <div className="flex-1 self-stretch inline-flex flex-col justify-center items-start">
      <div className="self-stretch justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
        Bento Matte 3D Illustration
      </div>

      {/* Action Buttons instead of URL */}
      <div className="inline-flex justify-start items-start gap-2">
        {/* Edit Button */}
        <div
          data-property-1="default"
          className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1"
        >
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Edit
          </div>
        </div>

        {/* Delete Button */}
        <div
          data-property-1="default"
          className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1"
        >
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[1.83px] top-[1.83px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Delete
          </div>
        </div>

        {/* Schedule Button */}
        <div
          data-property-1="default"
          className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1"
        >
          <div className="w-4 h-4 relative">
            <div className="w-3 h-3 left-[2px] top-[2px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Schedule
          </div>
        </div>
      </div>
    </div>
  </div>

  {/* Right Section */}
  <div className="flex-1 py-2 flex justify-start items-center gap-12">
    <div className="flex justify-start items-center gap-2">
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-4 h-4 left-[3.75px] top-[3.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      </div>
      <div className="w-32 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
        UI Design Kit
      </div>
    </div>

    <div className="w-28 h-7 relative">
      <div className="w-12 px-3 py-1.5 left-0 top-0 absolute bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 inline-flex justify-center items-center gap-1">
        <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
          $98
        </div>
      </div>
    </div>

    <div className="w-40 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
      Apr 9, 2044 at 3:55 PM
    </div>
  </div>
</div>

// Highlighted/Active Row - Dark Mode
<div className="w-[1148px] p-4 bg-Backgrounds-highlight rounded-2xl outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100 inline-flex justify-start items-start gap-6 overflow-hidden">
  <div className="w-96 h-16 flex justify-start items-center gap-5">
    {/* Checkbox with different border in dark mode */}
    <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Highlight/50" />
    </div>
    {/* Rest of content same as light mode */}
  </div>
</div>

// Row with Border Separator - Light Mode
<div className="w-[1148px] p-4 border-b-[1.50px] border-Stroke-Subtle/10 inline-flex justify-start items-start gap-6 overflow-hidden">
  {/* Standard row content */}
</div>

// Row with Border Separator - Dark Mode
<div className="w-[1148px] p-4 border-b-[1.50px] border-Stroke-Subtle inline-flex justify-start items-start gap-6 overflow-hidden">
  {/* Standard row content */}
</div>

// Price Badge Variants
<>
  {/* Green Badge - Paid Price */}
  <div className="w-12 px-3 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 inline-flex justify-center items-center gap-1">
    <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
      $98
    </div>
  </div>

  {/* Gray Badge - Free Price */}
  <div className="w-12 px-3 py-1.5 bg-Backgrounds-surface1 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-center items-center gap-1">
    <div className="justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
      $0.0
    </div>
  </div>

  {/* Red Badge - Free Price Alternative */}
  <div
    data-property-1="False"
    className="w-16 px-2 py-1.5 bg-red-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-red-600/20 inline-flex justify-center items-center gap-2 overflow-hidden"
  >
    <div className="justify-start text-Primary-primary03 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
      $0.00
    </div>
  </div>
</>

// Skeleton/Loading Row - Light Mode
<div className="self-stretch p-4 border-t border-Stroke-Subtle/10 inline-flex justify-start items-start gap-6 overflow-hidden">
  <div className="w-[480px] h-16 flex justify-start items-center gap-5">
    {/* Skeleton Checkbox */}
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute opacity-80 bg-shade09-100 rounded-md" />
    </div>

    {/* Skeleton Image */}
    <div className="w-16 h-16 relative bg-shade09-100 rounded-xl" />

    {/* Skeleton Text Lines */}
    <div className="flex-1 self-stretch inline-flex flex-col justify-center items-start">
      <div className="w-80 h-12 relative">
        <div className="w-40 left-0 top-[12px] absolute inline-flex flex-col justify-start items-start gap-2">
          <div className="w-24 h-2 bg-shade09-100 rounded" />
          <div className="self-stretch h-2 bg-shade09-100 rounded" />
        </div>
      </div>
    </div>
  </div>

  {/* Skeleton Price and Date */}
  <div className="flex-1 py-2 flex justify-between items-center">
    <div className="w-36 h-7 relative">
      <div className="w-16 h-2 left-0 top-[10px] absolute bg-shade09-100 rounded" />
    </div>
    <div className="w-96 h-6 relative">
      <div className="w-40 h-2 left-0 top-[8px] absolute bg-shade09-100 rounded" />
    </div>
  </div>
</div>

// Skeleton/Loading Row - Dark Mode
<div className="self-stretch p-4 border-t border-Stroke-Subtle inline-flex justify-start items-start gap-6 overflow-hidden">
  <div className="w-[480px] h-16 flex justify-start items-center gap-5">
    {/* Skeleton Checkbox */}
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-6 h-6 left-0 top-0 absolute opacity-80 bg-shade04-100 rounded-md" />
    </div>

    {/* Skeleton Image */}
    <div className="w-16 h-16 relative bg-shade04-100 rounded-xl" />

    {/* Skeleton Text Lines */}
    <div className="flex-1 self-stretch inline-flex flex-col justify-center items-start">
      <div className="w-80 h-12 relative">
        <div className="w-40 left-0 top-[12px] absolute inline-flex flex-col justify-start items-start gap-2">
          <div className="w-24 h-2 bg-shade04-100 rounded" />
          <div className="self-stretch h-2 bg-shade04-100 rounded" />
        </div>
      </div>
    </div>
  </div>

  {/* Skeleton Price and Date */}
  <div className="flex-1 py-2 flex justify-between items-center">
    <div className="w-36 h-7 relative">
      <div className="w-16 h-2 left-0 top-[10px] absolute bg-shade04-100 rounded" />
    </div>
    <div className="w-96 h-6 relative">
      <div className="w-40 h-2 left-0 top-[8px] absolute bg-shade04-100 rounded" />
    </div>
  </div>
</div>
```

#### Usage Notes

- Используется для компактных списков продуктов без подробной статистики
- Checkbox позволяет множественный выбор строк
- Price badge с зеленым цветом подчеркивает ценность
- Category icon помогает быстро идентифицировать тип продукта
- Date/Time формат: "MMM D, YYYY at H:MM AM/PM"
- Можно комбинировать с полными строками (section 33) в одной таблице
- Подходит для Product Lists, Order History, Purchase Records

**Highlighted/Active Row State:**
- Используйте для активной строки при editing, drag-and-drop, или focused item
- Light mode: multiple shadow layers создают elevation и depth
- Dark mode: cleaner appearance без теней, только outline
- Action buttons заменяют URL в highlighted state
- Inset shadow в light mode создает white border effect
- Border radius `rounded-2xl` выделяет строку из списка

**Border Separators:**
- Light mode: `border-Stroke-Subtle/10` для subtle разделения
- Dark mode: `border-Stroke-Subtle` для better visibility
- Используйте между строками в длинных списках
- Можно комбинировать с highlighted rows

**Price Badge Variants:**
- Green badge: для платных продуктов ($98, $49, $299, etc.)
- Gray badge: для бесплатных продуктов ($0.0, Free) - neutral appearance
- Red badge: для бесплатных продуктов с warning или alert ($0.00) - draws attention
- Green привлекает внимание к paid products
- Gray нейтральный для free products
- Red используется когда нужно выделить free product (например, expired trial, downgraded plan)
- Используйте conditional rendering based on price value и business logic

**Action Buttons:**
- Появляются в highlighted row вместо URL
- Common actions: Edit, Delete, Schedule, Publish, Archive
- Default state: no outline, secondary text color
- Hover state: with outline для emphasis
- Compact size (`pl-1 pr-1.5 py-1`) для inline placement
- Icons + text labels для clarity

**Skeleton/Loading State:**
- Display во время загрузки новых данных
- Light mode: `bg-shade09-100` для placeholders
- Dark mode: `bg-shade04-100` для placeholders
- Maintains same height и structure как regular rows
- Text lines: `h-2 rounded` для smooth edges
- Usually displayed at bottom of list при infinite scroll
- Можно добавить pulse/shimmer animation для better UX
- Replace skeleton с real data when loaded
- 1-3 skeleton rows в зависимости от loading context

---

## 35. Comments / Products Toolbar

### Описание / Description

Универсальная панель инструментов для списков комментариев или продуктов. Имеет два состояния: по умолчанию (с поиском и сортировкой) и режим выбора (с bulk actions).

Universal toolbar for comments or products lists. Has two states: default (with search and sorting) and selection mode (with bulk actions).

### Спецификация / Specification

#### Базовая структура / Base Structure

```
Container (w-[1180px] p-3)
├── Default State
│   ├── Left Section
│   │   ├── Counter (e.g., "8 new comments")
│   │   └── Search Input
│   └── Right Section
│       └── Sort Dropdown
└── Selection State
    ├── Left Section
    │   ├── Selection Counter (e.g., "3 comments selected")
    │   └── Deselect Button
    └── Right Section
        ├── Delete Button
        └── Primary Action Button
```

#### Dimensions

- Container width: `w-[1180px]`
- Container padding: `p-3` (12px all sides)
- Height: `h-12` (48px) для кнопок и inputs
- Search input: `w-72` (288px)
- Sort dropdown: `w-44` (176px)
- Icon size: `w-6 h-6` (24x24px)
- Gap between sections: `gap-6` (24px)
- Gap between buttons: `gap-2` (8px)

#### Typography

**Counter / Title:**
- Font: `font-['Inter_Display']`
- Size: `text-xl` (20px)
- Weight: `font-semibold` (600)
- Line height: `leading-7` (28px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Primary`

**Search Placeholder:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Color: `text-Text-Secondary`

**Dropdown Text:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Color: `text-Text-Secondary`

**Button Text:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Letter spacing: `tracking-tight`

#### Colors

**Default State - Search Input (Light Mode):**
- Background: `bg-Backgrounds-surface1`
- Border radius: `rounded-[90px]`
- Padding: `pl-3 pr-5 py-3`
- Icon: `outline-Text-Secondary`
- Data attribute: `data-light-mode="True"`

**Default State - Search Input (Dark Mode):**
- Background: `bg-Backgrounds-surface1`
- Border radius: `rounded-[90px]`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Subtle`
- Padding: `pl-3 pr-5 py-3`
- Icon: `outline-Text-Secondary`
- Data attribute: `data-light-mode="False"`
- Adds subtle outline для better visibility на dark backgrounds

**Default State - Sort Dropdown:**
- Background: `bg-Backgrounds-surface2`
- Border radius: `rounded-[90px]`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2`
- Padding: `pl-5 pr-3 py-3`

**Selection State - Secondary Buttons:**
- Background: transparent
- Border radius: `rounded-[32px]`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2`
- Padding: `px-7 py-3.5`
- Text color: `text-Text-Secondary`

**Selection State - Primary Button (Light Mode):**
- Background: `bg-gradient-to-b from-zinc-800 to-zinc-800`
- Border radius: `rounded-[32px]`
- Shadow: `shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)]`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-white/40`
- Padding: `px-7 py-4`
- Text color: `text-Text-Light`

#### States

##### Default State (No Selection)

**Layout:**
- Display: `inline-flex justify-between items-center`
- Left section: counter + search input (`gap-6`)
- Right section: sort dropdown

**Components:**
- Counter showing number of items ("8 new comments")
- Search input с иконкой поиска
- Sort dropdown с chevron down icon ("Newest first", "Oldest first", etc.)

**Search Input:**
- Icon: search icon (круг с handle)
- Placeholder: "Search comments" или "Search products"
- Background: surface1
- Rounded: pill shape (`rounded-[90px]`)

**Sort Dropdown:**
- Icon: chevron down
- Text: sorting option
- Background: surface2 с outline
- Rounded: pill shape

##### Selection State (Items Selected)

**Layout:**
- Display: `inline-flex justify-between items-center`
- Left section: selection counter + deselect button (`gap-6`)
- Right section: delete + primary action (`gap-2`)

**Components:**
- Selection counter ("3 comments selected")
- "Deselect" button (secondary)
- "Delete" button (secondary)
- Primary action button ("Mark as read", "Archive", etc.)

**Selection Counter:**
- Same styling as default counter
- Dynamic number based on selection

**Deselect Button:**
- Outline style
- Secondary appearance
- Text: "Deselect"

**Delete Button:**
- Outline style
- Secondary appearance
- Text: "Delete"

**Primary Action Button:**
- Gradient background (dark in light mode, light in dark mode)
- Inset shadow for depth
- Prominent appearance
- Text varies: "Mark as read", "Archive", "Approve", etc.

#### Icon Specifications

**Search Icon:**
- Circle: `w-3 h-3` (12x12px)
- Handle: `w-1 h-1` (4x4px)
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Color: `outline-Text-Secondary`
- Position: круг centered, handle positioned down-left

**Chevron Down Icon:**
- Size: `w-2 h-[3.38px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Color: `outline-Text-Secondary`
- Position: centered в icon container

#### Responsive Behavior

- Fixed width: `w-[1180px]` для desktop
- Mobile: stack vertically или adjust widths
- Search input может сокращаться first
- Buttons сохраняют padding но могут уменьшить text

#### Пример использования / Usage Example

```jsx
// Default State (No Selection)
<div className="w-[1180px] p-3 inline-flex justify-between items-center">
  {/* Left Section: Counter + Search */}
  <div className="h-12 pl-5 flex justify-center items-center gap-6">
    {/* Counter */}
    <div className="justify-start text-Text-Primary text-xl font-semibold font-['Inter_Display'] leading-7 tracking-tight">
      8 new comments
    </div>

    {/* Search Input */}
    <div
      data-light-mode="True"
      data-state="default"
      className="w-72 pl-3 pr-5 py-3 bg-Backgrounds-surface1 rounded-[90px] flex justify-start items-center gap-2 overflow-hidden"
    >
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      </div>
      <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
        Search comments
      </div>
    </div>
  </div>

  {/* Right Section: Sort Dropdown */}
  <div
    data-light-mode="True"
    data-state="default"
    className="w-44 h-12 pl-5 pr-3 py-3 bg-Backgrounds-surface2 rounded-[90px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-between items-center overflow-hidden"
  >
    <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
      Newest first
    </div>
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-2 h-[3.38px] left-[8px] top-[10px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
    </div>
  </div>
</div>

// Default State - Dark Mode Search Input (with outline)
<div className="w-[1180px] p-3 inline-flex justify-between items-center">
  <div className="h-12 pl-5 flex justify-center items-center gap-6">
    <div className="justify-start text-Text-Primary text-xl font-semibold font-['Inter_Display'] leading-7 tracking-tight">
      5 scheduled products
    </div>

    {/* Search Input - Dark Mode with Outline */}
    <div
      data-light-mode="False"
      data-state="default"
      className="w-72 pl-3 pr-5 py-3 bg-Backgrounds-surface1 rounded-[90px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Subtle flex justify-start items-center gap-2 overflow-hidden"
    >
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
      </div>
      <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
        Search products
      </div>
    </div>
  </div>

  {/* Sort Dropdown (same as light mode) */}
  <div
    data-light-mode="True"
    data-state="default"
    className="w-44 h-12 pl-5 pr-3 py-3 bg-Backgrounds-surface2 rounded-[90px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-between items-center overflow-hidden"
  >
    <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
      Newest first
    </div>
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-2 h-[3.38px] left-[8px] top-[10px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
    </div>
  </div>
</div>

// Selection State (Items Selected)
<div className="w-[1180px] p-3 inline-flex justify-between items-center">
  {/* Left Section: Selection Counter + Deselect */}
  <div className="h-12 pl-5 flex justify-center items-center gap-6">
    {/* Selection Counter */}
    <div className="justify-start text-Text-Primary text-xl font-semibold font-['Inter_Display'] leading-7 tracking-tight">
      3 comments selected
    </div>

    {/* Deselect Button */}
    <div className="self-stretch px-7 py-3.5 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-center items-center gap-2 overflow-hidden">
      <div className="text-center justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
        Deselect
      </div>
    </div>
  </div>

  {/* Right Section: Delete + Primary Action */}
  <div className="flex justify-start items-start gap-2">
    {/* Delete Button */}
    <div className="h-12 px-7 py-3.5 rounded-[32px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-center items-center gap-2 overflow-hidden">
      <div className="text-center justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
        Delete
      </div>
    </div>

    {/* Primary Action Button */}
    <div
      data-light-mode="True"
      data-state="Default"
      data-style="Button"
      className="px-7 py-4 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/40 flex justify-center items-center gap-2.5 overflow-hidden"
    >
      <div className="justify-start text-Text-Light text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
        Mark as read
      </div>
    </div>
  </div>
</div>

// For Products Toolbar - just change text content
<div className="w-[1180px] p-3 inline-flex justify-between items-center">
  <div className="h-12 pl-5 flex justify-center items-center gap-6">
    <div className="justify-start text-Text-Primary text-xl font-semibold font-['Inter_Display'] leading-7 tracking-tight">
      245 products
    </div>
    {/* Search with placeholder "Search products" */}
  </div>
  {/* Sort dropdown with options like "Best selling", "Price: Low to High", etc. */}
</div>
```

#### Usage Notes

- Toolbar переключается между Default и Selection states
- Counter динамически обновляется (количество items или selected items)
- Search input может быть активным или placeholder
- **Search Input Variants:**
  - Light mode: no outline, clean appearance
  - Dark mode: with `outline-Stroke-Subtle` для better visibility на dark backgrounds
  - Use `data-light-mode="True"` или `"False"` для switching
- Sort dropdown может показывать разные опции:
  - Comments: "Newest first", "Oldest first", "Most likes"
  - Products: "Best selling", "Price: Low to High", "Rating"
- Primary action button text зависит от контекста:
  - Comments: "Mark as read", "Approve", "Archive"
  - Products: "Add to collection", "Export", "Publish"
- Delete button всегда destructive action
- Deselect button снимает выбор со всех items
- В mobile версии возможно collapse в menu или vertical stack

---

## 36. Table Container / Product Table

### Описание / Description

Полноценный контейнер таблицы с заголовком, строками, поиском и пагинацией. Комбинирует toolbar (section 35) и table rows (sections 33-34) в единый компонент. Поддерживает light/dark режимы.

Complete table container with header, rows, search, and pagination. Combines toolbar (section 35) and table rows (sections 33-34) into unified component. Supports light/dark modes.

### Спецификация / Specification

#### Базовая структура / Base Structure

```
Container (w-[1180px] bg-Backgrounds-surface2)
├── Header Section
│   ├── Title + Search + View Toggle
│   └── Controls (Grid/List buttons)
├── Table Header Row
│   ├── Checkbox (select all)
│   └── Column Headers (Product, Status, Price, Sales, Ratings, Views)
├── Table Body
│   ├── Table Row 1 (section 33 or 34 pattern)
│   ├── Table Row 2
│   └── ... (multiple rows)
└── Footer Section
    └── "Show more" Button
```

#### Dimensions

- Container width: `w-[1180px]`
- Border radius: `rounded-[32px]`
- Total structure creates cohesive table component
- Header padding: `p-3` (12px)
- Table rows: varies by type (sections 33/34)
- Footer button: full width centered

#### Typography

**Section Title (Header):**
- Font: `font-['Inter_Display']`
- Size: `text-xl` (20px)
- Weight: `font-semibold` (600)
- Line height: `leading-7` (28px)
- Color: `text-Text-Primary`

**Column Headers:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-medium` (500)
- Color: `text-Text-Secondary`
- Uppercase: optional

**"Show more" Button:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Color: light mode = `text-Text-Light`, dark mode = `text-Text-Primary`

#### Colors and Theming

**Container (Light Mode):**
- Background: `bg-Backgrounds-surface2`
- Border radius: `rounded-[32px]`
- Shadow: `shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)]`
- Outline: `outline-offset-[-1.50px]` (subtle border effect)
- Border: `border-Stroke-Subtle/10`

**Container (Dark Mode):**
- Background: `bg-Backgrounds-surface2` (darker in dark mode via CSS vars)
- Shadow: `shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.50)]` (stronger shadow)
- Outline: `outline-white`
- Border: `border-Stroke-Subtle` (more visible in dark)

**"Show more" Button (Light Mode):**
- Background: `bg-gradient-to-b from-zinc-800 to-zinc-800`
- Shadow: `shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)]`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-white/40`
- Text: `text-Text-Light` (white)
- Border radius: `rounded-[32px]`
- Padding: `px-7 py-4`

**"Show more" Button (Dark Mode):**
- Background: `bg-gradient-to-b from-white to-neutral-200`
- Shadow: similar structure but adjusted for light background
- Outline: adjusted for light button
- Text: `text-Text-Primary` (dark)
- Same border radius and padding

#### Layout Structure

**Header Section:**
- Contains toolbar from section 35
- Includes title, search input, sort dropdown, view toggles
- Padding: `p-3`
- Background: same as container

**Table Header Row:**
- Column headers: Product, Status, Price, Sales, Ratings, Views
- Select all checkbox on left
- Sticky header: optional `sticky top-0`
- Background: `bg-Backgrounds-surface2`
- Border bottom: subtle separator

**Table Body:**
- Multiple table rows (sections 33 or 34)
- Each row: full width
- Dividers: subtle borders between rows
- Scrollable: if content exceeds max height

**Footer Section:**
- "Show more" button centered
- Padding: `p-4` или `p-6`
- Background: same as container
- Button: full width or centered with max-width

#### States

##### Empty State
- Показывает placeholder: "No products yet" или "No comments"
- Icon: empty state illustration
- CTA button: "Add product" или создать первый item

##### Loading State
- Skeleton loaders для rows
- Shimmer effect
- Preserves layout structure

##### Loaded State
- Displays all table rows
- Toolbar active
- "Show more" button если есть pagination

##### Filtered/Searched State
- Rows фильтруются по search query
- Counter обновляется: "8 results" вместо "245 products"
- Возможно "No results found" state

##### Selection State
- Toolbar переключается на selection mode (section 35)
- Selected rows highlighted
- Bulk actions доступны

#### Shadow Stacking (Depth)

**Light Mode:**
- Container shadow: `0px 5px 1.5px -4px rgba(8,8,8,0.09)`
- Button inset shadow: `inset 2px 0px 8px 2px rgba(248,248,248,0.20)`
- Creates subtle depth and layering

**Dark Mode:**
- Container shadow: `0px 5px 1.5px -4px rgba(8,8,8,0.50)` (stronger)
- Button shadow adjusted for light button on dark surface
- More pronounced contrast

#### Responsive Behavior

- Desktop: full `w-[1180px]` width
- Tablet: может использовать `max-w-full` с horizontal scroll
- Mobile: возможно vertical card layout вместо table
- "Show more" button: всегда visible и centered
- Columns могут скрываться на меньших экранах (priority: Product > Price > Status > others)

#### Пример использования / Usage Example

```jsx
// Complete Table Container (Light Mode)
<div className="w-[1180px] bg-Backgrounds-surface2 rounded-[32px] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] outline outline-offset-[-1.50px] border border-Stroke-Subtle/10">

  {/* Header / Toolbar Section */}
  <div className="w-full p-3 inline-flex justify-between items-center">
    <div className="h-12 pl-5 flex justify-center items-center gap-6">
      <div className="justify-start text-Text-Primary text-xl font-semibold font-['Inter_Display'] leading-7 tracking-tight">
        245 products
      </div>

      {/* Search Input */}
      <div className="w-72 pl-3 pr-5 py-3 bg-Backgrounds-surface1 rounded-[90px] flex justify-start items-center gap-2">
        <div className="w-6 h-6 relative overflow-hidden">
          <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        </div>
        <div className="text-Text-Secondary text-sm font-normal font-['Inter_Display']">
          Search products
        </div>
      </div>
    </div>

    {/* View Toggle / Sort */}
    <div className="flex items-center gap-2">
      {/* Grid/List toggle buttons could go here */}
      <div className="w-44 h-12 pl-5 pr-3 py-3 bg-Backgrounds-surface2 rounded-[90px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-between items-center">
        <div className="text-Text-Secondary text-sm font-normal font-['Inter_Display']">
          Best selling
        </div>
        <div className="w-6 h-6 relative overflow-hidden">
          <div className="w-2 h-[3.38px] left-[8px] top-[10px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        </div>
      </div>
    </div>
  </div>

  {/* Table Header Row */}
  <div className="w-full px-4 py-2 flex items-center border-b border-Stroke-Subtle/10">
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-6 h-6 rounded-md border-2 border-Stroke-Stroke2" />
    </div>
    <div className="flex-1 flex items-center gap-6 pl-6">
      <div className="w-96 text-Text-Secondary text-sm font-medium font-['Inter_Display']">Product</div>
      <div className="w-32 text-Text-Secondary text-sm font-medium font-['Inter_Display']">Status</div>
      <div className="w-28 text-Text-Secondary text-sm font-medium font-['Inter_Display']">Price</div>
      <div className="w-24 text-Text-Secondary text-sm font-medium font-['Inter_Display']">Sales</div>
      <div className="w-28 text-Text-Secondary text-sm font-medium font-['Inter_Display']">Ratings</div>
      <div className="w-20 text-Text-Secondary text-sm font-medium font-['Inter_Display']">Views</div>
    </div>
  </div>

  {/* Table Body - Multiple Rows */}
  <div className="w-full">
    {/* Row 1 - use section 33 pattern (full metrics) */}
    <div className="w-full p-4 border-b border-Stroke-Subtle/10">
      {/* Full table row from section 33 */}
    </div>

    {/* Row 2 - use section 34 pattern (simplified) */}
    <div className="w-full p-4 border-b border-Stroke-Subtle/10">
      {/* Simplified row from section 34 */}
    </div>

    {/* More rows... */}
  </div>

  {/* Footer - Show More Button */}
  <div className="w-full p-6 flex justify-center items-center">
    <div
      data-light-mode="True"
      className="px-7 py-4 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/40 flex justify-center items-center cursor-pointer"
    >
      <div className="text-Text-Light text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
        Show more
      </div>
    </div>
  </div>

</div>

// Dark Mode Variant - adjust these properties:
<div className="w-[1180px] bg-Backgrounds-surface2 rounded-[32px] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.50)] outline outline-white border border-Stroke-Subtle">
  {/* Same structure but with dark mode styling */}

  {/* Footer button in dark mode */}
  <div className="w-full p-6 flex justify-center items-center">
    <div className="px-7 py-4 bg-gradient-to-b from-white to-neutral-200 rounded-[32px] flex justify-center items-center cursor-pointer">
      <div className="text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
        Show more
      </div>
    </div>
  </div>
</div>
```

#### Column Structure

**Product Column (w-96):**
- Checkbox + Image + Title + URL
- Самая широкая колонка
- Contains main product info

**Status Column (w-32):**
- Badge component (Active, Draft, Archived)
- Uses badge from earlier sections
- Color coded

**Price Column (w-28):**
- Price в формате $XX или $XXX
- Green badge background
- Semibold font

**Sales Column (w-24):**
- Number или "N/A"
- Right-aligned: optional
- Secondary text color

**Ratings Column (w-28):**
- Stars + count (e.g., "4.8 (234)")
- Star icons + numeric rating
- Compact display

**Views Column (w-20):**
- View count (e.g., "1.2k", "45.3k")
- Secondary text
- Abbreviated numbers

#### Usage Notes

- Комбинирует все предыдущие table components
- Используйте section 35 toolbar для header
- Используйте section 33 для full metric rows
- Используйте section 34 для simplified rows
- Можно миксовать row types в одной таблице
- Light/dark mode переключается через data-attributes и CSS variables
- "Show more" button загружает следующую страницу (pagination)
- Sticky header: добавьте `sticky top-0 z-10` к table header row
- Empty state: показывайте когда нет данных
- Loading state: используйте skeleton loaders
- Selection state: интегрируйте с toolbar selection mode
- Responsive: на mobile переключайтесь на card layout
- Shadow stacking создает глубину: container shadow + button inset shadow

---

## 37. Product Grid View / Products Gallery

### Описание / Description

Полноценный компонент галереи продуктов с grid layout, переключением view modes (grid/list), поиском и hover состояниями с быстрыми действиями. Карточки продуктов показывают изображение, название, цену и рейтинг.

Complete product gallery component with grid layout, view mode switching (grid/list), search, and hover states with quick actions. Product cards display image, title, price, and rating.

### Спецификация / Specification

#### Базовая структура / Base Structure

```
Container (w-[1180px] bg-Backgrounds-surface2)
├── Header Section
│   ├── Left: Title + Search Input
│   └── Right: View Toggle (Grid/List buttons)
└── Product Grid
    ├── Product Card 1 (default state)
    ├── Product Card 2 (hover state)
    └── ... (multiple cards, flex-wrap)

Product Card Structure:
├── Image Container (h-56)
│   ├── Product Image
│   ├── Hover Overlay (opacity-30)
│   └── Checkbox (hover only)
├── Card Content
│   ├── Title + Price Badge
│   └── Rating (star + count)
└── Hover Actions (positioned absolute)
    ├── Edit button
    ├── Delete button
    ├── Unpublish button
    └── Drag handle icon
```

#### Dimensions

**Container:**
- Width: `w-[1180px]`
- Border radius: `rounded-[32px]`
- Padding: varies by section

**Header Section:**
- Padding: `p-3` (12px all sides)
- Height: `h-12` (48px) для элементов
- Search input: `w-72` (288px)
- View toggle buttons: `w-6 h-6` (24x24px icon area)
- Button padding: `p-3` (12px)
- Button border radius: `rounded-[48px]`

**Product Grid:**
- Padding: `px-8 pt-5 pb-8` (32px horizontal, 20px top, 32px bottom)
- Gap between cards: `gap-6` (24px)
- Layout: flex-wrap

**Product Card:**
- Min width: `min-w-72` (288px)
- Flex: `flex-1` (равномерное распределение)
- Gap between elements: `gap-3` (12px)

**Image Container:**
- Height: `h-56` (224px)
- Width: `w-96` (384px) или self-stretch
- Border radius: `rounded-3xl`

**Card Content:**
- Gap between rows: `gap-1` (4px)
- Title/Price row: space-between
- Rating row: gap-2.5 (10px)

#### Typography

**Page Title ("Products"):**
- Font: `font-['Inter_Display']`
- Size: `text-2xl` (24px)
- Weight: `font-medium` (500)
- Line height: `leading-9` (36px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Primary`

**Search Placeholder:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Color: `text-Text-Secondary`

**Product Title:**
- Font: `font-['Inter_Display']`
- Size: `text-base` (16px)
- Weight: `font-semibold` (600)
- Line height: `leading-6` (24px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Primary`
- Truncation: `line-clamp-1`

**Price:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Color: `text-Primary-primary02` (green)

**Rating Number:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Color: `text-Text-Primary`

**Rating Count:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Color: `text-Text-Secondary`

**Action Button Labels:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Color: varies by state
- Opacity: `opacity-80`

#### Colors and Theming

**Container (Light Mode):**
- Background: `bg-Backgrounds-surface2`
- Border radius: `rounded-[32px]`
- Shadow layer 1: `shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)]`
- Shadow layer 2: `shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)]`
- Outline: `outline-[1.50px] outline-offset-[-1.50px]`
- Border: subtle (without explicit border class in light mode)

**Container (Dark Mode):**
- Background: `bg-Backgrounds-surface2` (darker via CSS vars)
- Shadow layer 1: `shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)]` (same)
- Shadow layer 2: `shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.50)]` (stronger)
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-white`

**Search Input (Light Mode):**
- Background: `bg-Backgrounds-surface1`
- Border radius: `rounded-[90px]`
- Padding: `pl-3 pr-5 py-3`
- No explicit outline

**Search Input (Dark Mode):**
- Background: `bg-Backgrounds-surface1`
- Border radius: `rounded-[90px]`
- Padding: `pl-3 pr-5 py-3`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Subtle`

**View Toggle - Grid Button (Active):**
- Background: transparent
- Border radius: `rounded-[48px]`
- Padding: `p-3`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2`
- Icon color: `outline-Text-Primary`

**View Toggle - List Button (Default):**
- Background: transparent
- Border radius: `rounded-[48px]`
- Padding: `p-3`
- No outline
- Icon color: `outline-Text-Secondary`

**Product Image:**
- Background: `bg-gray-200` (placeholder)
- Border radius: `rounded-3xl`

**Hover Overlay:**
- Background: `bg-Backgrounds-dark1`
- Opacity: `opacity-30`
- Покрывает всю image area

**Checkbox (Hover State):**
- Background: `bg-Backgrounds-surface2`
- Border: `border-2 border-Stroke-Stroke2`
- Border radius: `rounded-md`
- Position: left-[16px] top-[16px]
- Size: `w-6 h-6`

**Price Badge:**
- Background: `bg-green-600/5` (5% opacity green)
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20`
- Border radius: `rounded-lg`
- Padding: `px-3 py-1.5`
- Width: `w-12`

**Action Buttons:**

*Default state (Edit, Unpublish):*
- Background: transparent
- Border radius: `rounded-md`
- Padding: `pl-1 pr-1.5 py-1`
- Icon: `outline-Text-Secondary`
- Text: `text-Text-Secondary opacity-80`

*Hover state (Delete shown as example):*
- Background: transparent
- Border radius: `rounded-md`
- Padding: `pl-1 pr-1.5 py-1`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2`
- Icon: `outline-Text-Primary`
- Text: `text-Text-Primary opacity-80`

**Rating Star Icon:**
- Background: `bg-Text-Secondary`
- Size: `w-4 h-4` (positioned within `w-5 h-5` container)

#### Layout Structure

**Header Section:**
- Display: `inline-flex justify-between items-center`
- Full width: `self-stretch`
- Padding: `p-3`
- Left section: `h-12 pl-5 flex justify-center items-center gap-6`
  - Contains: title + search input
- Right section: `flex justify-start items-center gap-2`
  - Contains: grid button + list button

**Product Grid:**
- Display: `inline-flex justify-start items-center gap-6 flex-wrap content-center`
- Width: `w-[1180px]`
- Padding: `px-8 pt-5 pb-8`
- Cards automatically wrap to new rows

**Product Card:**
- Display: `inline-flex flex-col justify-start items-start`
- Flex: `flex-1 min-w-72`
- Gap: `gap-3` (between image and content)
- Responsive: grows/shrinks with container

**Card Content Section:**
- Display: `flex flex-col justify-center items-start`
- Gap: `gap-1` (4px between rows)
- Full width: `self-stretch`

**Title + Price Row:**
- Display: `inline-flex justify-between items-center`
- Full width: `self-stretch`

**Rating Row:**
- Display: `inline-flex justify-start items-start`
- Gap: `gap-2.5` (10px)
- Width: `w-20` (80px) minimum

#### States

##### Default State (No Hover)

**Card appearance:**
- Image: full visibility, no overlay
- Checkbox: hidden
- Action buttons: hidden
- Drag handle: hidden
- Content: always visible (title, price, rating)

**Components visible:**
- Product image
- Product title (truncated to 1 line)
- Price badge (green)
- Rating: star icon + number + count

##### Hover State

**Card appearance:**
- Image: `opacity-30 bg-Backgrounds-dark1` overlay applied
- Checkbox: appears in top-left (16px, 16px)
- Action buttons: appear below content (Edit, Delete, Unpublish)
- Drag handle: appears (positioned absolute)
- Content: remains visible

**Hover overlay:**
- Full image coverage: `w-96 h-56`
- Position: `left-0 top-0 absolute`
- Background: `bg-Backgrounds-dark1`
- Opacity: `opacity-30`

**Checkbox appearance:**
- Position: `left-[16px] top-[16px] absolute`
- Size: `w-6 h-6`
- Background: `bg-Backgrounds-surface2`
- Border: `border-2 border-Stroke-Stroke2`
- Border radius: `rounded-md`
- Status: `data-status="placeholder"`

**Action Buttons Row:**
- Position: `left-[-4px] top-0 absolute` (relative to card content)
- Display: `inline-flex justify-start items-start gap-2`
- Contains: Edit, Delete, Unpublish buttons
- Width: `w-56 h-6`

**Action Button States:**
- Edit: default appearance (no outline)
- Delete: hover appearance (with outline) - shown as example
- Unpublish: default appearance (no outline)

**Drag Handle:**
- Position: `left-[90px] top-[35px] absolute`
- Size: `w-8 h-8`
- Complex SVG path structure
- Colors: bg-white + outline-black
- Used for reordering cards

##### Grid View Active

**Header:**
- Grid button: `data-property-2="active"` with outline
- List button: `data-property-2="default"` no outline

**Grid layout:**
- Cards displayed in grid with flex-wrap
- Multiple cards per row (typically 3 cards)
- Equal width distribution via `flex-1 min-w-72`

##### List View Active (not shown but implied)

**Header:**
- Grid button: no outline
- List button: with outline

**List layout:**
- Cards displayed vertically (one per row)
- Full width for each card
- Similar to table rows from section 33/34

#### Icon Specifications

**Search Icon:**
- Circle: `w-3 h-3` at position `left-[6.75px] top-[4.48px]`
- Handle: `w-1 h-1` at position `left-[4.87px] top-[15.60px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Color: `outline-Text-Secondary`

**Grid Icon (View Toggle):**
- Size: `w-4 h-4` at position `left-[3.75px] top-[3.75px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Color: active = `outline-Text-Primary`, default = `outline-Text-Secondary`
- Shape: grid squares

**List Icon (View Toggle):**
- Size: `w-4 h-3.5` at position `left-[3.75px] top-[5.25px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Color: active = `outline-Text-Primary`, default = `outline-Text-Secondary`
- Shape: horizontal lines

**Rating Star Icon:**
- Size: `w-4 h-4` at position `left-[1.25px] top-[0.83px]`
- Background: `bg-Text-Secondary` (filled)
- Container: `w-5 h-5`

**Action Button Icons:**

*Edit icon:*
- Size: `w-3 h-3` at position `left-[2.50px] top-[2.05px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Shape: pencil/edit

*Delete icon:*
- Size: `w-3 h-3` at position `left-[1.83px] top-[1.83px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Shape: trash/delete

*Unpublish icon:*
- Size: `w-3 h-3` at position `left-[2px] top-[2px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Shape: unpublish/hide

**Drag Handle:**
- Complex multi-part SVG
- Size: `w-8 h-8`
- Main shape: `w-3.5 h-4` at `left-[10.47px] top-[10.17px]`
- Multiple small elements for grip dots
- Colors: bg-white with outline-black

#### Responsive Behavior

**Desktop (>1180px):**
- Full `w-[1180px]` width
- 3 cards per row (flex-1 min-w-72)
- All elements visible

**Tablet (768px - 1180px):**
- Container adapts to available width
- 2 cards per row
- Search input может сокращаться
- Grid/list toggle остается

**Mobile (<768px):**
- Single column layout
- 1 card per row
- Search может перемещаться на новую строку
- View toggle может скрываться (force grid view)
- Hover actions могут быть always visible или accessible via tap

**Card Flexibility:**
- `flex-1`: cards grow to fill available space
- `min-w-72`: minimum width 288px before wrapping
- `flex-wrap`: cards wrap to new row when needed
- `content-center`: centers wrapped content

#### Shadow Stacking (Depth)

**Light Mode Shadows:**
- Layer 1: `0px 6px 4px -4px rgba(8,8,8,0.05)` - soft outer shadow
- Layer 2: `0px 5px 1.5px -4px rgba(8,8,8,0.09)` - subtle definition
- Combined effect: soft floating appearance

**Dark Mode Shadows:**
- Layer 1: `0px 6px 4px -4px rgba(8,8,8,0.05)` - same soft shadow
- Layer 2: `0px 5px 1.5px -4px rgba(8,8,8,0.50)` - much stronger
- Combined effect: more pronounced depth

**Purpose:**
- Creates elevation for entire gallery container
- Separates gallery from page background
- More subtle in light mode, more dramatic in dark mode

#### Пример использования / Usage Example

```jsx
// Product Grid View - Light Mode
<div className="w-[1180px] bg-Backgrounds-surface2 rounded-[32px] shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.09)] outline outline-[1.50px] outline-offset-[-1.50px] inline-flex flex-col justify-start items-center gap-3 overflow-hidden">

  {/* Header Section */}
  <div data-state="Grid" className="self-stretch p-3 inline-flex justify-between items-center">
    {/* Left: Title + Search */}
    <div className="h-12 pl-5 flex justify-center items-center gap-6">
      <div className="justify-start text-Text-Primary text-2xl font-medium font-['Inter_Display'] leading-9 tracking-tight">
        Products
      </div>

      {/* Search Input */}
      <div
        data-light-mode="True"
        data-state="default"
        className="w-72 pl-3 pr-5 py-3 bg-Backgrounds-surface1 rounded-[90px] flex justify-start items-center gap-2 overflow-hidden"
      >
        <div className="w-6 h-6 relative overflow-hidden">
          <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        </div>
        <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
          Search products
        </div>
      </div>
    </div>

    {/* Right: View Toggle */}
    <div className="flex justify-start items-center gap-2">
      {/* Grid Button - Active */}
      <div
        data-property-1="grid"
        data-property-2="active"
        className="p-3 rounded-[48px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex flex-col justify-center items-center gap-2.5 overflow-hidden"
      >
        <div className="w-6 h-6 relative overflow-hidden">
          <div className="w-4 h-4 left-[3.75px] top-[3.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
        </div>
      </div>

      {/* List Button - Default */}
      <div
        data-property-1="list"
        data-property-2="default"
        className="p-3 rounded-[48px] inline-flex flex-col justify-center items-center gap-2.5 overflow-hidden"
      >
        <div className="w-6 h-6 relative overflow-hidden">
          <div className="w-4 h-3.5 left-[3.75px] top-[5.25px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        </div>
      </div>
    </div>
  </div>

  {/* Product Grid */}
  <div className="w-[1180px] px-8 pt-5 pb-8 inline-flex justify-start items-center gap-6 flex-wrap content-center">

    {/* Product Card - Default State */}
    <div
      data-property-1="Default"
      className="flex-1 min-w-72 inline-flex flex-col justify-start items-start gap-3"
    >
      {/* Image Container */}
      <div className="self-stretch h-56 relative bg-gray-200 rounded-3xl overflow-hidden">
        <img
          className="w-96 h-56 left-0 top-0 absolute"
          src="https://placehold.co/356x230"
        />
      </div>

      {/* Card Content */}
      <div className="self-stretch flex flex-col justify-center items-start gap-1">
        {/* Title + Price */}
        <div className="self-stretch inline-flex justify-between items-center">
          <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
            Bento Design System
          </div>
          <div
            data-property-1="Default"
            className="w-12 px-3 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 flex justify-center items-center gap-1"
          >
            <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
              $98
            </div>
          </div>
        </div>

        {/* Rating */}
        <div className="w-20 inline-flex justify-start items-start gap-2.5">
          <div className="flex justify-start items-center gap-2">
            <div className="w-5 h-5 relative overflow-hidden">
              <div className="w-4 h-4 left-[1.25px] top-[0.83px] absolute bg-Text-Secondary" />
            </div>
            <div className="flex justify-start items-center gap-1">
              <div className="justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
                4.8
              </div>
              <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
                (88)
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    {/* Product Card - Hover State */}
    <div
      data-property-1="hover"
      className="flex-1 min-w-72 inline-flex flex-col justify-start items-start gap-3"
    >
      {/* Image Container with Overlay */}
      <div className="self-stretch h-56 relative bg-gray-200 rounded-3xl overflow-hidden">
        <img
          className="w-96 h-56 left-0 top-0 absolute"
          src="https://placehold.co/356x230"
        />

        {/* Hover Overlay */}
        <div className="w-96 h-56 left-0 top-0 absolute opacity-30 bg-Backgrounds-dark1" />

        {/* Checkbox (appears on hover) */}
        <div
          data-status="placeholder"
          className="w-6 h-6 left-[16px] top-[16px] absolute overflow-hidden"
        >
          <div className="w-6 h-6 left-0 top-0 absolute bg-Backgrounds-surface2 rounded-md border-2 border-Stroke-Stroke2" />
        </div>
      </div>

      {/* Card Content with Hover Actions */}
      <div className="self-stretch relative flex flex-col justify-center items-start gap-1">
        {/* Title + Price */}
        <div className="self-stretch inline-flex justify-between items-center">
          <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
            Bento Design System
          </div>
          <div
            data-property-1="Default"
            className="w-12 px-3 py-1.5 bg-green-600/5 rounded-lg outline outline-[1.50px] outline-offset-[-1.50px] outline-green-600/20 flex justify-center items-center gap-1"
          >
            <div className="justify-start text-Primary-primary02 text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
              $98
            </div>
          </div>
        </div>

        {/* Action Buttons Row (appears on hover) */}
        <div className="w-56 h-6 relative">
          <div className="left-[-4px] top-0 absolute inline-flex justify-start items-start gap-2">
            {/* Edit Button - Default */}
            <div
              data-property-1="default"
              className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1"
            >
              <div className="w-4 h-4 relative overflow-hidden">
                <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
              </div>
              <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
                Edit
              </div>
            </div>

            {/* Delete Button - Hover */}
            <div
              data-property-1="hover"
              className="pl-1 pr-1.5 py-1 rounded-md outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-start items-center gap-1"
            >
              <div className="w-4 h-4 relative overflow-hidden">
                <div className="w-3 h-3 left-[1.83px] top-[1.83px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
              </div>
              <div className="opacity-80 justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
                Delete
              </div>
            </div>

            {/* Unpublish Button - Default */}
            <div
              data-property-1="default"
              className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1"
            >
              <div className="w-4 h-4 relative">
                <div className="w-3 h-3 left-[2px] top-[2px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
              </div>
              <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
                Unpublish
              </div>
            </div>
          </div>
        </div>

        {/* Drag Handle (positioned absolute) */}
        <div className="w-8 h-8 left-[90px] top-[35px] absolute">
          <div className="w-3.5 h-4 left-[10.47px] top-[10.17px] absolute bg-white" />
          <div className="w-3.5 h-4 left-[10.47px] top-[10.17px] absolute outline outline-[0.75px] outline-offset-[-0.38px] outline-black" />
          <div className="w-0 h-1 left-[20.68px] top-[18.33px] absolute outline outline-[0.75px] outline-offset-[-0.38px] outline-black" />
          <div className="w-[0.01px] h-1 left-[18.53px] top-[18.33px] absolute outline outline-[0.75px] outline-offset-[-0.38px] outline-black" />
          <div className="w-[0.02px] h-1 left-[16.42px] top-[18.36px] absolute outline outline-[0.75px] outline-offset-[-0.38px] outline-black" />
        </div>
      </div>
    </div>

    {/* Additional cards... (repeat pattern) */}
  </div>
</div>

// Dark Mode Variant
<div className="w-[1180px] bg-Backgrounds-surface2 rounded-[32px] shadow-[0px_6px_4px_-4px_rgba(8,8,8,0.05)] shadow-[0px_5px_1.5px_-4px_rgba(8,8,8,0.50)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white inline-flex flex-col justify-start items-center gap-3 overflow-hidden">

  {/* Header Section */}
  <div data-state="Grid" className="self-stretch p-3 inline-flex justify-between items-center">
    <div className="h-12 pl-5 flex justify-center items-center gap-6">
      <div className="justify-start text-Text-Primary text-2xl font-medium font-['Inter_Display'] leading-9 tracking-tight">
        Products
      </div>

      {/* Search Input - Dark Mode with outline */}
      <div
        data-light-mode="False"
        data-state="default"
        className="w-72 pl-3 pr-5 py-3 bg-Backgrounds-surface1 rounded-[90px] outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Subtle flex justify-start items-center gap-2 overflow-hidden"
      >
        <div className="w-6 h-6 relative overflow-hidden">
          <div className="w-3 h-3 left-[6.75px] top-[4.48px] absolute rounded-full outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          <div className="w-1 h-1 left-[4.87px] top-[15.60px] absolute rounded-sm outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
        </div>
        <div className="justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
          Search products
        </div>
      </div>
    </div>

    {/* View Toggle - same as light mode */}
    <div className="flex justify-start items-center gap-2">
      {/* Grid and List buttons... */}
    </div>
  </div>

  {/* Product Grid - same structure as light mode */}
  <div className="w-[1180px] px-8 pt-5 pb-8 inline-flex justify-start items-center gap-6 flex-wrap content-center">
    {/* Product cards... */}
  </div>
</div>
```

#### Usage Notes

- Компонент объединяет header с view toggles и grid layout продуктов
- Grid/List toggle переключает между grid и list views (list view использует table layout из sections 33-34)
- Hover состояние показывает overlay, checkbox и quick actions
- Action buttons: Edit, Delete, Unpublish с разными состояниями
- Drag handle позволяет перетаскивать карточки для изменения порядка
- Checkbox в hover state позволяет множественный выбор для bulk actions
- Price badge использует green color scheme для привлечения внимания
- Rating показывает star icon + numeric rating + count отзывов
- Responsive: карточки автоматически wrappятся на новые строки
- Light/dark mode различаются:
  - Shadow strength (layer 2: 0.09 vs 0.50)
  - Container outline (subtle vs white)
  - Search input outline (none vs Stroke-Subtle)
- Multiple shadow layers создают depth и elevation
- Image overlay на hover: opacity-30 темного фона
- Cards используют `flex-1 min-w-72` для responsive grid
- Title truncation: `line-clamp-1` предотвращает overflow
- Action buttons могут быть в default или hover состоянии
- Drag handle имеет сложную SVG структуру для grip визуала
- Можно комбинировать с pagination или "Load more" button
- Search интегрируется с filtering логикой
- View state сохраняется через `data-state` attribute

---

## 38. Comment Row / Comment Thread Item

### Описание / Description

Компонент строки комментария для систем обсуждений, отзывов и коммуникации. Поддерживает множественные состояния: default, highlighted, with inline reply, nested threads, unread indicator. Включает user avatar, comment text, product context, action buttons.

Comment row component for discussion systems, reviews, and communication. Supports multiple states: default, highlighted, with inline reply, nested threads, unread indicator. Includes user avatar, comment text, product context, action buttons.

### Спецификация / Specification

#### Базовая структура / Base Structure

```
Container (w-[1180px] p-4)
├── Left Section (w-[720px])
│   ├── Checkbox (w-6 h-6)
│   ├── User Avatar (w-12 h-12 rounded-[80px])
│   └── Comment Content
│       ├── User Info Row
│       │   ├── Name (text-base font-semibold)
│       │   ├── @username (text-sm opacity-80)
│       │   ├── Dot separator
│       │   └── Time (text-sm)
│       ├── Comment Text (text-sm line-clamp-1 or 3)
│       ├── Reply Input (optional, highlighted state)
│       └── Nested Reply (optional, thread state)
├── Right Section (flex-1)
│   ├── Product Image (w-16 h-16)
│   └── Product Info
│       ├── Title (text-base font-semibold)
│       └── Category (text-sm)
├── Action Buttons (w-96, absolute positioned in highlighted)
│   ├── Reply button
│   ├── Like button
│   └── Remove button
└── Unread Indicator (w-2 h-2, absolute positioned)
```

#### Dimensions

**Container:**
- Width: `w-[1180px]`
- Padding: `p-4` (16px all sides)
- Height: varies (`h-24` minimum для standard row)
- Border radius: `rounded-2xl` (в highlighted state)

**Left Section:**
- Width: `w-[720px]` (fixed)
- Gap: `gap-5` (20px) между элементами

**User Avatar:**
- Size: `w-12 h-12` (48x48px) для main comment
- Size: `w-8 h-8` (32x32px) для nested reply
- Border radius: `rounded-[80px]` (полный круг)

**Checkbox:**
- Size: `w-6 h-6` (24x24px)
- Border: `border-2 border-Stroke-Stroke2` или `border-Stroke-Highlight/50`

**Product Section:**
- Image: `w-16 h-16` (64x64px)
- Border radius: `rounded-xl`
- Gap: `gap-5` (20px)

**Comment Content:**
- Width: `w-[608px]` (varies based on layout)
- Flex: `flex-1` для adaptive width

**Dot Separator:**
- Size: `w-3 h-3` container
- Dot: `w-0.5 h-0.5` (2x2px)
- Position: centered в container
- Opacity: `opacity-50`
- Color: `bg-Text-Tertiary`

**Unread Indicator:**
- Size: `w-2 h-2` (8x8px)
- Position: `left-[1124px] top-[16px] absolute`
- Shape: `rounded-full`
- Color: `bg-Primary-primary02` (green)

**Action Buttons Container:**
- Width: `w-96` или `w-56`
- Position: `left-0 top-[20px] absolute` relative to parent
- Left offset: `left-[-4px]` для alignment

**Nested Reply Connection:**
- Width: `w-8 h-9` (32x36px)
- Position: `left-[24px] top-[48px] absolute`
- Border radius: `rounded-[10px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px] outline-Stroke-Stroke2`
- Creates visual connection line

**Reply Input Field:**
- Background: `bg-Backgrounds-surface2` (light) или `bg-shade05-20/20` (dark)
- Border radius: `rounded-[80px]` (pill shape)
- Padding: `p-1`
- Outline: `outline-1 outline-offset-[-1px] outline-Stroke-Stroke2`
- Contains: @mention tag + cursor + Send button

**Reply Avatar Icon:**
- Container: `w-11 h-11` (44x44px)
- Border radius: `rounded-[90px]`
- Icon inside: `w-6 h-6` with `w-5 h-5` shape

**Send Button:**
- Height: `h-11` (44px)
- Padding: `px-7 py-4`
- Border radius: `rounded-[32px]`
- Light mode: `bg-gradient-to-b from-zinc-800 to-zinc-800`
- Dark mode: `bg-gradient-to-b from-white to-neutral-200`
- Shadow: `shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)]` (light)
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-white/40`

#### Typography

**User Name:**
- Font: `font-['Inter_Display']`
- Size: `text-base` (16px)
- Weight: `font-semibold` (600)
- Line height: `leading-6` (24px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Primary`
- Truncation: `line-clamp-1`

**@Username:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Secondary`
- Opacity: `opacity-80`
- Truncation: `line-clamp-1`

**Time Stamp:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Color: `text-Text-Secondary`
- Opacity: `opacity-80`
- Examples: "19h", "2m", "1s"

**Comment Text:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Primary`
- Opacity: `opacity-80`
- Truncation: `line-clamp-1` или `line-clamp-3`

**Reply Text (with @mention):**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-medium` (500)
- Line height: `leading-5` (20px)
- Color: `text-Text-Primary`
- Opacity: `opacity-80`
- @mention: `underline` decoration
- Line clamp: `line-clamp-3`

**Product Title:**
- Font: `font-['Inter_Display']`
- Size: `text-base` (16px)
- Weight: `font-semibold` (600)
- Line height: `leading-6` (24px)
- Color: `text-Text-Primary`
- Truncation: `line-clamp-1`

**Product Category:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Color: `text-Text-Secondary`
- Opacity: `opacity-80`

**Action Button Labels:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Secondary` (default) или `text-Text-Primary` (hover)
- Opacity: `opacity-80`

**Reply Input @mention:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-normal` (400)
- Line height: `leading-5` (20px)
- Color: `text-Text-Primary`
- Truncation: `line-clamp-3`

**Send Button Text:**
- Font: `font-['Inter_Display']`
- Size: `text-sm` (14px)
- Weight: `font-semibold` (600)
- Line height: `leading-4` (16px)
- Letter spacing: `tracking-tight`
- Color: `text-Text-Light`

#### Colors and Theming

**Default Row:**
- Background: transparent
- No border radius
- No shadows
- No outline

**Row with Border Separator (Light Mode):**
- Border bottom: `border-b-[1.50px] border-Stroke-Subtle/10`
- Subtle разделитель между комментариями

**Row with Border Separator (Dark Mode):**
- Border bottom: `border-b-[1.50px] border-Stroke-Subtle`
- More visible для contrast

**Highlighted Row (Light Mode):**
- Background: `bg-Backgrounds-highlight`
- Border radius: `rounded-2xl`
- Multiple shadow layers:
  - Layer 1: `shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)]`
  - Layer 2: `shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)]`
  - Layer 3: `shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)]` - white inset border
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100`

**Highlighted Row (Dark Mode):**
- Background: `bg-Backgrounds-highlight`
- Border radius: `rounded-2xl`
- NO multiple shadows (cleaner)
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100`
- Checkbox border: `border-Stroke-Highlight/50`

**Unread Indicator:**
- Color: `bg-Primary-primary02` (green - matches primary color)
- Size: `w-2 h-2` dot
- Position: absolute top-right corner
- Indicates new/unread comment

**Action Buttons:**

*Default State:*
- Background: transparent
- No outline
- Icon color: `outline-Text-Secondary`
- Text color: `text-Text-Secondary opacity-80`
- Padding: `pl-1 pr-1.5 py-1`
- Border radius: `rounded-md`

*Hover State:*
- Background: transparent
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2`
- Icon color: `outline-Text-Primary`
- Text color: `text-Text-Primary opacity-80`

*Like Button - Liked State:*
- Icon: filled heart `bg-Primary-primary03` (no outline)
- Text color: `text-Text-Primary opacity-80`
- No outline in default state

**Reply Input Field (Light Mode):**
- Background: `bg-Backgrounds-surface2`
- Outline: `outline-1 outline-offset-[-1px] outline-Stroke-Stroke2`
- Border radius: `rounded-[80px]`

**Reply Input Field (Dark Mode):**
- Background: `bg-shade05-20/20`
- Outline: `outline-1 outline-offset-[-1px] outline-Stroke-Stroke2`
- Border radius: `rounded-[80px]`

**@Mention Tag:**
- Text: `text-Text-Primary`
- Font weight: `font-normal`
- No background (inline text)

**Cursor Indicator:**
- Width: `w-0.5`
- Height: `h-4`
- Color: `bg-Text-Blue`
- Border radius: `rounded-sm`
- Blinks/animates

**Nested Reply:**
- Smaller avatar: `w-8 h-8`
- Indented from main comment
- Connection line visual
- Same text styling but slightly smaller hierarchy

#### States

##### Default State

**Layout:**
- Standard height: `h-24` (96px)
- Padding: `p-4`
- No background color
- No border radius
- Display: `inline-flex justify-start items-center`

**Components visible:**
- Checkbox (unchecked)
- User avatar (circular)
- User name + @username + time
- Comment text (truncated to 1 line)
- Product image + info
- Optional: unread indicator dot

**Action buttons:**
- NOT visible by default (или always visible в некоторых вариантах)

**Position:**
- Left section: `w-[720px]`
- Right section: `flex-1`
- Gap: `gap-6` (24px)

##### Row with Border Separator

**Purpose:**
- Разделяет комментарии в списке
- Light mode: subtle `border-Stroke-Subtle/10`
- Dark mode: more visible `border-Stroke-Subtle`

**Border:**
- Position: `border-b-[1.50px]`
- Applies to entire row width

##### Highlighted State (Active Comment)

**Purpose:**
- Indicates focused/active comment
- Shows action buttons
- Elevated appearance

**Visual Changes:**
- Background: `bg-Backgrounds-highlight`
- Border radius: `rounded-2xl`
- Multiple shadows (light mode only)
- Outline: `outline-zinc-100`

**Layout Changes:**
- Comment content width: `w-[608px]` (slightly narrower)
- Action buttons container: `w-96 h-16` positioned relative
- May show fewer lines of product info

**Action Buttons:**
- Positioned: `w-96 h-16 relative` container
- Buttons at: `left-[-4px] top-0 absolute`
- Gap: `gap-5` (20px) between buttons
- Shows: Reply (hover state), Like, Remove

##### State with Reply Input

**Purpose:**
- User is composing a reply
- Shows inline reply field below comment

**Additional Component:**
- Reply input field container
- Background: `bg-Backgrounds-surface2` (light) or `bg-shade05-20/20` (dark)
- Pill shape: `rounded-[80px]`
- Contains: avatar icon + @mention + cursor + Send button

**Reply Field Layout:**
- Full width: `self-stretch`
- Padding: `p-1`
- Display: `inline-flex justify-between items-center`
- Left: avatar icon + @mention text + cursor
- Right: Send button

**@Mention Tag:**
- Shows: `@samstoo` (username being replied to)
- Color: `text-Text-Primary`
- Cursor: animated blue line `bg-Text-Blue`

**Send Button:**
- Height: `h-11`
- Gradient background (dark in light mode, light in dark mode)
- Inset shadow для depth
- Text: "Send"

##### State with Nested Reply (Thread)

**Purpose:**
- Shows reply to the comment
- Creates conversation thread
- Visual connection between parent and child

**Layout:**
- Parent comment: standard layout
- Gap: `gap-4` (16px) before nested reply
- Nested reply container: `inline-flex justify-start items-start gap-4`

**Nested Reply Components:**
- Smaller avatar: `w-8 h-8` (vs `w-12 h-12`)
- Same text structure but nested
- Connection line: `w-8 h-9` rounded rectangle outline
- Position: `left-[24px] top-[48px] absolute`

**Connection Line:**
- Visual connector from parent to child
- Border radius: `rounded-[10px]`
- Outline: `outline-[1.50px] outline-Stroke-Stroke2`
- Creates tree-like visual hierarchy

**Nested Reply Content:**
- Width: `flex-1`
- Same user info structure: name + @username + time
- Reply text with @mention support
- Action buttons: Reply, Like, Remove

##### State with Unread Indicator

**Purpose:**
- Shows new/unread comments
- Indicates user attention needed

**Indicator:**
- Green dot: `w-2 h-2 bg-Primary-primary02`
- Position: `left-[1124px] top-[16px] absolute` (top-right)
- Shape: `rounded-full`
- Always visible until marked as read

**Placement:**
- Positioned absolute relative to row container
- Top-right corner near product section
- Does not affect layout of other elements

##### Like Button States

**Default (Not Liked):**
- Icon: outline heart
- Outline: `outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary`
- Text: `text-Text-Secondary opacity-80`

**Liked State:**
- Icon: filled heart `bg-Primary-primary03` (solid blue)
- Size: `w-3.5 h-3` positioned at `left-[1.33px] top-[2px]`
- Text: `text-Text-Primary opacity-80` (darker)
- No outline (filled background)

##### Action Button Interaction States

**Reply Button:**
- Default: outline icon, secondary text
- Hover: with outline border, primary text
- Purpose: открывает reply input field

**Like Button:**
- Default: outline icon
- Hover: with outline border (if not liked)
- Liked: filled icon, no outline border
- Purpose: toggles like state

**Remove Button:**
- Default: outline icon, secondary text
- Hover: with outline border, primary text
- Purpose: удаляет комментарий (requires confirmation)

#### Responsive Behavior

**Desktop (>1180px):**
- Full `w-[1180px]` width
- Two-column layout: comment + product info
- All elements visible

**Tablet (768px - 1180px):**
- Width adapts to container
- Product section может сократиться
- Comment text может wrap to 2-3 lines

**Mobile (<768px):**
- Stack vertically: comment above, product below
- Full width avatar and text
- Action buttons може быть always visible
- Nested replies может иметь less indentation

#### Icon Specifications

**Reply Icon:**
- Size: `w-3 h-3` at `left-[2.50px] top-[2.05px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Color: `outline-Text-Secondary` (default) or `outline-Text-Primary` (hover)
- Shape: reply/comment arrow

**Like/Heart Icon (Outline):**
- Size: `w-3 h-3` at `left-[1.83px] top-[2.50px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Color: `outline-Text-Secondary`
- Shape: heart outline

**Like/Heart Icon (Filled):**
- Size: `w-3.5 h-3` at `left-[1.33px] top-[2px]`
- Background: `bg-Primary-primary03` (blue filled)
- No outline
- Shape: solid heart

**Remove/Delete Icon:**
- Size: `w-3 h-3` at `left-[1.83px] top-[1.83px]`
- Outline: `outline-[1.50px] outline-offset-[-0.75px]`
- Color: `outline-Text-Secondary`
- Shape: trash/delete

**Reply Input Avatar Icon:**
- Container: `w-6 h-6` at `left-[10px] top-[10px]`
- Icon: `w-5 h-5` at `left-[2px] top-[2px]`
- Background: `bg-Text-Secondary`
- Represents reply action

#### Пример использования / Usage Example

```jsx
// Default Comment Row with Unread Indicator
<div className="self-stretch h-24 p-4 relative inline-flex justify-start items-center gap-6 overflow-hidden">
  {/* Left Section: Checkbox + Avatar + Comment */}
  <div className="w-[720px] flex justify-start items-start gap-5">
    <div className="h-12 flex justify-start items-center gap-2">
      <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
        <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
      </div>
    </div>

    <div className="flex-1 flex justify-start items-start gap-5">
      {/* User Avatar */}
      <img className="w-12 h-12 relative rounded-[80px]" src="https://placehold.co/48x48" />

      {/* Comment Content */}
      <div className="flex-1 inline-flex flex-col justify-center items-start">
        {/* User Info Row */}
        <div className="inline-flex justify-start items-center gap-3">
          <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
            Sam Stoof
          </div>

          <div className="flex justify-start items-center gap-2">
            <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
              @samstoo
            </div>

            {/* Dot Separator */}
            <div className="w-3 h-3 relative overflow-hidden">
              <div className="w-0.5 h-0.5 left-[5px] top-[5px] absolute opacity-50 bg-Text-Tertiary rounded-full" />
            </div>

            <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
              19h
            </div>
          </div>
        </div>

        {/* Comment Text */}
        <div className="self-stretch inline-flex justify-center items-center gap-2">
          <div className="flex-1 opacity-80 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
            Can you make a version for automated penetration testing and cybersecurity?
          </div>
        </div>
      </div>
    </div>
  </div>

  {/* Right Section: Product Info */}
  <div className="flex-1 flex justify-start items-center gap-5">
    <img className="w-16 h-16 relative rounded-xl" src="https://placehold.co/64x64" />
    <div className="flex-1 self-stretch inline-flex flex-col justify-center items-start">
      <div className="self-stretch justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
        Bento Pro v.2
      </div>
      <div className="self-stretch opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight">
        UI Design Kit
      </div>
    </div>
  </div>

  {/* Unread Indicator */}
  <div className="w-2 h-2 left-[1124px] top-[16px] absolute bg-Primary-primary02 rounded-full" />
</div>

// Comment Row with Border Separator - Light Mode
<div className="self-stretch h-24 p-4 relative border-b-[1.50px] border-Stroke-Subtle/10 inline-flex justify-start items-center gap-6 overflow-hidden">
  {/* Same structure as default */}
</div>

// Comment Row with Border Separator - Dark Mode
<div className="self-stretch h-24 p-4 relative border-b-[1.50px] border-Stroke-Subtle inline-flex justify-start items-center gap-6 overflow-hidden">
  {/* Same structure as default */}
</div>

// Highlighted Comment Row with Action Buttons - Light Mode
<div className="self-stretch h-24 p-4 bg-Backgrounds-highlight rounded-2xl shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)] shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)] shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)] outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100 inline-flex justify-start items-center gap-6 overflow-hidden">
  <div className="w-[720px] flex justify-start items-start gap-5">
    <div className="h-12 flex justify-start items-center gap-2">
      <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
        <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
      </div>
    </div>

    <div className="flex-1 flex justify-start items-start gap-5">
      <img className="w-12 h-12 relative rounded-[80px]" src="https://placehold.co/48x48" />

      <div className="w-[608px] inline-flex flex-col justify-center items-start">
        {/* User Info and Comment Text */}
        <div className="inline-flex justify-start items-center gap-3">
          <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
            Sam Stoof
          </div>
          <div className="flex justify-start items-center gap-2">
            <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
              @samstoo
            </div>
            <div className="w-3 h-3 relative overflow-hidden">
              <div className="w-0.5 h-0.5 left-[5px] top-[5px] absolute opacity-50 bg-Text-Tertiary rounded-full" />
            </div>
            <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
              19h
            </div>
          </div>
        </div>
        <div className="self-stretch inline-flex justify-center items-center gap-2">
          <div className="flex-1 opacity-80 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
            Can you make a version for automated penetration testing and cybersecurity?
          </div>
        </div>
      </div>
    </div>
  </div>

  {/* Action Buttons - Right Side */}
  <div className="w-96 h-16 relative">
    <div className="w-56 h-6 left-0 top-[20px] absolute">
      <div className="left-[-4px] top-0 absolute inline-flex justify-start items-start gap-5">
        {/* Reply Button - Hover State */}
        <div
          data-property-1="hover"
          className="pl-1 pr-1.5 py-1 rounded-md outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 flex justify-start items-center gap-1"
        >
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Primary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Reply
          </div>
        </div>

        {/* Like Button - Default */}
        <div
          data-property-1="default"
          className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1"
        >
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[1.83px] top-[2.50px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Like
          </div>
        </div>

        {/* Remove Button */}
        <div
          data-property-1="default"
          className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1"
        >
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[1.83px] top-[1.83px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Remove
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

// Highlighted Comment with Like Button - Liked State
<div className="self-stretch h-24 p-4 bg-Backgrounds-highlight rounded-2xl outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100 inline-flex justify-start items-center gap-6 overflow-hidden">
  {/* ...comment content... */}

  {/* Action Buttons with Liked State */}
  <div className="w-96 h-16 relative">
    <div className="w-56 h-6 left-0 top-[20px] absolute">
      <div className="left-[-4px] top-0 absolute inline-flex justify-start items-start gap-5">
        <div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Reply
          </div>
        </div>

        {/* Like Button - Liked/Filled State */}
        <div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3.5 h-3 left-[1.33px] top-[2px] absolute bg-Primary-primary03" />
          </div>
          <div className="opacity-80 justify-start text-Text-Primary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Like
          </div>
        </div>

        <div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
          <div className="w-4 h-4 relative overflow-hidden">
            <div className="w-3 h-3 left-[1.83px] top-[1.83px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
          </div>
          <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
            Remove
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

// Comment with Reply Input Field - Light Mode
<div className="self-stretch p-4 bg-Backgrounds-highlight rounded-2xl shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)] shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)] shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)] outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100 inline-flex justify-start items-center gap-6 overflow-hidden">
  <div className="w-[720px] flex justify-start items-start gap-5">
    <div className="h-12 flex justify-start items-center gap-2">
      <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
        <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
      </div>
    </div>

    <div className="flex-1 flex justify-start items-start gap-5">
      <img className="w-12 h-12 relative rounded-[80px]" src="https://placehold.co/48x48" />

      <div className="w-[608px] inline-flex flex-col justify-start items-start gap-4">
        {/* Comment Content */}
        <div className="self-stretch flex flex-col justify-center items-start">
          <div className="inline-flex justify-start items-center gap-3">
            <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
              Sam Stoof
            </div>
            <div className="flex justify-start items-center gap-2">
              <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
                @samstoo
              </div>
              <div className="w-3 h-3 relative overflow-hidden">
                <div className="w-0.5 h-0.5 left-[5px] top-[5px] absolute opacity-50 bg-Text-Tertiary rounded-full" />
              </div>
              <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
                2m
              </div>
            </div>
          </div>
          <div className="self-stretch inline-flex justify-center items-center gap-2">
            <div className="flex-1 opacity-80 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
              Can you make a version for automated penetration testing and cybersecurity?
            </div>
          </div>
        </div>

        {/* Reply Input Field */}
        <div className="self-stretch p-1 bg-Backgrounds-surface2 rounded-[80px] outline outline-1 outline-offset-[-1px] outline-Stroke-Stroke2 inline-flex justify-between items-center overflow-hidden">
          <div className="flex justify-start items-center">
            {/* Reply Icon */}
            <div data-light-mode="True" className="w-11 h-11 relative rounded-[90px] overflow-hidden">
              <div className="w-6 h-6 left-[10px] top-[10px] absolute overflow-hidden">
                <div className="w-5 h-5 left-[2px] top-[2px] absolute bg-Text-Secondary" />
              </div>
            </div>

            {/* @Mention + Cursor */}
            <div className="flex justify-start items-center">
              <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-3">
                @samstoo
              </div>
              <div className="w-0.5 h-4 bg-Text-Blue rounded-sm" />
            </div>
          </div>

          {/* Send Button */}
          <div
            data-light-mode="True"
            data-state="Default"
            data-style="Button"
            className="h-11 px-7 py-4 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/40 flex justify-center items-center gap-2.5 overflow-hidden"
          >
            <div className="justify-start text-Text-Light text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
              Send
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  {/* Action Buttons */}
  <div className="w-96 h-16 relative">
    {/* ...action buttons... */}
  </div>
</div>

// Comment with Reply Input Field - Dark Mode
<div className="self-stretch p-4 bg-Backgrounds-highlight rounded-2xl outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100 inline-flex justify-start items-center gap-6 overflow-hidden">
  {/* ...same structure... */}

  {/* Reply Input Field - Dark Mode */}
  <div className="self-stretch p-1 bg-shade05-20/20 rounded-[80px] outline outline-1 outline-offset-[-1px] outline-Stroke-Stroke2 inline-flex justify-between items-center overflow-hidden">
    <div className="flex justify-start items-center">
      <div data-light-mode="False" className="w-11 h-11 relative rounded-[90px] overflow-hidden">
        <div className="w-6 h-6 left-[10px] top-[10px] absolute overflow-hidden">
          <div className="w-5 h-5 left-[2px] top-[2px] absolute bg-Text-Secondary" />
        </div>
      </div>
      <div className="flex justify-start items-center">
        <div className="justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-3">
          @samstoo
        </div>
        <div className="w-0.5 h-4 bg-Text-Blue rounded-sm" />
      </div>
    </div>

    {/* Send Button - Dark Mode */}
    <div
      data-light-mode="False"
      className="h-11 px-7 py-4 bg-gradient-to-b from-white to-neutral-200 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(24,24,24,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/60 flex justify-center items-center gap-2.5 overflow-hidden"
    >
      <div className="justify-start text-Text-Light text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
        Send
      </div>
    </div>
  </div>
</div>

// Comment with Nested Reply (Thread) - Light Mode
<div className="self-stretch p-4 bg-Backgrounds-highlight rounded-2xl shadow-[0px_1px_4px_0px_rgba(0,0,0,0.05)] shadow-[0px_8px_8px_-2px_rgba(0,0,0,0.08)] shadow-[inset_0px_0px_0px_3px_rgba(255,255,255,1.00)] outline outline-[1.50px] outline-offset-[-1.50px] outline-zinc-100 inline-flex justify-start items-center gap-6 overflow-hidden">
  <div className="w-[720px] flex justify-start items-start gap-5">
    <div className="h-12 flex justify-start items-center gap-2">
      <div data-status="placeholder" className="w-6 h-6 relative overflow-hidden">
        <div className="w-6 h-6 left-0 top-0 absolute rounded-md border-2 border-Stroke-Stroke2" />
      </div>
    </div>

    <div className="flex-1 relative flex justify-start items-start gap-5">
      <img className="w-12 h-12 relative rounded-[80px]" src="https://placehold.co/48x48" />

      <div className="w-[608px] inline-flex flex-col justify-start items-start gap-4">
        {/* Parent Comment */}
        <div className="self-stretch flex flex-col justify-center items-start">
          <div className="inline-flex justify-start items-center gap-3">
            <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
              Sam Stoof
            </div>
            <div className="flex justify-start items-center gap-2">
              <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
                @samstoo
              </div>
              <div className="w-3 h-3 relative overflow-hidden">
                <div className="w-0.5 h-0.5 left-[5px] top-[5px] absolute opacity-50 bg-Text-Tertiary rounded-full" />
              </div>
              <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
                2m
              </div>
            </div>
          </div>
          <div className="self-stretch inline-flex justify-center items-center gap-2">
            <div className="flex-1 opacity-80 justify-start text-Text-Primary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
              Can you make a version for automated penetration testing and cybersecurity?
            </div>
          </div>
        </div>

        {/* Nested Reply */}
        <div className="self-stretch inline-flex justify-start items-start gap-4">
          <img className="w-8 h-8 relative rounded-[80px]" src="https://placehold.co/32x32" />

          <div className="flex-1 inline-flex flex-col justify-start items-start gap-2">
            <div className="self-stretch flex flex-col justify-center items-start">
              <div className="inline-flex justify-start items-center gap-3">
                <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight line-clamp-1">
                  Dash
                </div>
                <div className="flex justify-start items-center gap-2">
                  <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
                    @dash
                  </div>
                  <div className="w-3 h-3 relative overflow-hidden">
                    <div className="w-0.5 h-0.5 left-[5px] top-[5px] absolute opacity-50 bg-Text-Tertiary rounded-full" />
                  </div>
                  <div className="opacity-80 justify-start text-Text-Secondary text-sm font-normal font-['Inter_Display'] leading-5 tracking-tight line-clamp-1">
                    1s
                  </div>
                </div>
              </div>

              {/* Reply Text with @mention */}
              <div className="self-stretch opacity-80 justify-start">
                <span className="text-Text-Primary text-sm font-medium font-['Inter_Display'] leading-5 tracking-tight line-clamp-3">
                  Hey{" "}
                </span>
                <span className="text-Text-Primary text-sm font-medium font-['Inter_Display'] underline leading-5 tracking-tight line-clamp-3">
                  @samstoo
                </span>
                <span className="text-Text-Primary text-sm font-medium font-['Inter_Display'] leading-5 tracking-tight line-clamp-3">
                  ! 😊 We're working on cool stuff in the cybersecurity space. Stay tuned, and thanks for the awesome idea! 🔍✨
                </span>
              </div>
            </div>

            {/* Action Buttons for Nested Reply */}
            <div className="w-56 h-6 relative">
              <div className="left-[-4px] top-0 absolute inline-flex justify-start items-start gap-5">
                <div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
                  <div className="w-4 h-4 relative overflow-hidden">
                    <div className="w-3 h-3 left-[2.50px] top-[2.05px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
                  </div>
                  <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
                    Reply
                  </div>
                </div>
                <div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
                  <div className="w-4 h-4 relative overflow-hidden">
                    <div className="w-3 h-3 left-[1.83px] top-[2.50px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
                  </div>
                  <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
                    Like
                  </div>
                </div>
                <div className="pl-1 pr-1.5 py-1 rounded-md flex justify-start items-center gap-1">
                  <div className="w-4 h-4 relative overflow-hidden">
                    <div className="w-3 h-3 left-[1.83px] top-[1.83px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Secondary" />
                  </div>
                  <div className="opacity-80 justify-start text-Text-Secondary text-sm font-semibold font-['Inter_Display'] leading-4 tracking-tight">
                    Remove
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      {/* Connection Line */}
      <div className="w-8 h-9 left-[24px] top-[48px] absolute rounded-[10px] outline outline-[1.50px] outline-offset-[-0.75px] outline-Stroke-Stroke2" />
    </div>
  </div>

  {/* Parent Action Buttons */}
  <div className="w-96 h-16 relative">
    {/* ...action buttons... */}
  </div>
</div>
```

#### Usage Notes

**Comment Row Component:**
- Используйте для систем комментариев, отзывов, discussions
- Поддерживает checkbox для bulk operations
- Avatar круглый (border-radius: 80px)
- Product context показывает связь комментария с товаром/темой

**States Overview:**
- **Default**: simple row без выделения
- **Border Separator**: разделяет комментарии в списке (light/dark variants)
- **Highlighted**: активный комментарий с elevated appearance и action buttons
- **With Reply Input**: показывает inline reply field
- **With Nested Reply**: creates conversation thread с connection line
- **Unread Indicator**: green dot для new comments

**Highlighted State:**
- Light mode: 3 shadow layers для depth (soft + depth + white inset)
- Dark mode: cleaner без теней, только outline
- Action buttons появляются справа
- Border radius `rounded-2xl` выделяет из списка
- Width slightly narrower (`w-[608px]`) для action buttons space

**Reply Input Field:**
- Pill shape (`rounded-[80px]`)
- Light mode: `bg-Backgrounds-surface2`
- Dark mode: `bg-shade05-20/20` (semi-transparent)
- Contains: reply icon + @mention + cursor + Send button
- @mention underlined в reply text
- Cursor indicator: blue vertical line (`bg-Text-Blue`)

**Nested Replies:**
- Smaller avatar: `w-8 h-8` (vs parent `w-12 h-12`)
- Connection line: rounded rectangle outline
- Positioned: `left-[24px] top-[48px] absolute`
- Indented from parent comment
- Full action buttons: Reply, Like, Remove
- Supports @mentions с underline

**Unread Indicator:**
- Green dot: `bg-Primary-primary02`
- Position: top-right corner (`left-[1124px] top-[16px]`)
- Always visible until marked as read
- Draws attention to new comments

**Action Buttons:**
- **Reply**: opens inline reply field
- **Like**: toggles liked state (outline → filled heart)
- **Remove**: deletes comment (requires confirmation)
- Default: no outline, secondary colors
- Hover: with outline border, primary colors
- Compact: `pl-1 pr-1.5 py-1`

**Like Button States:**
- Not Liked: outline heart icon (`outline-Text-Secondary`)
- Liked: filled heart (`bg-Primary-primary03` blue)
- Icon size changes: `w-3 h-3` → `w-3.5 h-3` when filled
- Text color: secondary → primary when liked

**Send Button:**
- Light mode: dark gradient (`from-zinc-800`)
- Dark mode: light gradient (`from-white to-neutral-200`)
- Inset shadow для depth effect
- Height: `h-11` (matches input field)
- Prominent appearance для primary action

**Dot Separator:**
- Tiny dot (`w-0.5 h-0.5`) between user info elements
- Opacity: 50%
- Color: `bg-Text-Tertiary`
- Creates subtle visual separation

**Time Stamps:**
- Relative format: "19h", "2m", "1s"
- Opacity: 80%
- Secondary text color
- Updates in real-time

**Product Context:**
- Shows which product/topic comment belongs to
- Image: `w-16 h-16 rounded-xl`
- Title + category below
- Right side of row
- Helps users identify context quickly

**@Mentions:**
- Underlined в reply text
- Links to user profile
- Auto-complete при typing
- Blue cursor indicator shows typing position

**Threading:**
- Connection line creates visual hierarchy
- Supports nested discussions
- Smaller avatars для replies
- Same action buttons at all levels
- Can nest multiple levels deep

**Responsive Behavior:**
- Desktop: two-column layout (comment + product)
- Tablet: may wrap text, shrink product section
- Mobile: stack vertically, full width elements
- Action buttons may be always visible on touch devices

**Border Separators:**
- Light mode: `border-Stroke-Subtle/10` (very subtle)
- Dark mode: `border-Stroke-Subtle` (more visible)
- Only between rows, not on first/last
- Creates visual rhythm in long lists

**Accessibility:**
- Checkbox для keyboard navigation
- Action buttons keyboard accessible
- Clear focus states
- Screen reader friendly structure
- Relative time stamps update

---

### 39. File Download Card / File Attachment Card

**Описание (Russian):**
Карточка файла для скачивания с информацией о размере, иконкой типа файла и кнопкой загрузки. Используется для отображения прикрепленных файлов, загружаемых ресурсов или архивов. Компактный дизайн с четкой визуальной иерархией и понятными action points.

**Description (English):**
File download card displaying file information, size, file type icon, and download button. Used for showing attached files, downloadable resources, or archives. Compact design with clear visual hierarchy and obvious action points.

**Specification:**

**Container:**
- Width: `w-[664px]`
- Padding: `p-6`
- Border radius: `rounded-3xl`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2`
- Layout: `inline-flex justify-between items-center`
- Overflow: `overflow-hidden`

**File Information Section (Left):**
- Layout: `inline-flex flex-col gap-2`
- Contains: file name + (icon + size)

**File Name:**
- Text color: `text-Text-Primary`
- Font size: `text-base` (16px)
- Font weight: `font-semibold`
- Font family: `font-['Inter_Display']`
- Line height: `leading-6`
- Letter spacing: `tracking-tight`
- Content: Full file name with extension

**File Info Row:**
- Layout: `inline-flex items-center gap-2`
- Contains: file type icon + size text

**File Type Icon:**
- Size: `w-6 h-6`
- Color: `bg-Primary-primary02`
- Type: Archive/ZIP icon (multiple rectangles)
- Icon composition:
  - Top bar: `w-4 h-2.5` at `left-[3px] top-[1px]`
  - Left bar: `w-1.5 h-2` at `left-[3px] top-[14px]`
  - Center divider: `w-0.5 h-2` at `left-[11px] top-[14px]`
  - Right bar: `w-1.5 h-2` at `left-[15px] top-[14px]`

**File Size:**
- Text color: `text-Text-Secondary`
- Font size: `text-base` (16px)
- Font weight: `font-normal`
- Font family: `font-['Inter_Display']`
- Line height: `leading-6`
- Letter spacing: `tracking-tight`
- Format: Number + "MB" or "GB"

**Download Button (Right):**
- Size: `w-12 h-12`
- Padding: `p-3.5`
- Background: `bg-gradient-to-b from-zinc-800 to-zinc-800` (dark gradient)
- Border radius: `rounded-[32px]`
- Shadow: `shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)]`
- Outline: `outline-[1.50px] outline-offset-[-1.50px] outline-white/40`
- Layout: `flex justify-center items-center`
- Data attributes: `data-light-mode="True" data-state="Default" data-style="Icon"`

**Download Icon:**
- Size: `w-6 h-6`
- Color: `outline-Text-Light`
- Icon: Download arrow (circle with arrow pointing down)
- Stroke: `outline-[1.50px] outline-offset-[-0.75px]`

**Colors & Theming:**

**Light Mode:**
- Container outline: `outline-Stroke-Stroke2`
- File name: `text-Text-Primary`
- File size: `text-Text-Secondary`
- File icon: `bg-Primary-primary02` (green)
- Button background: Dark gradient (`from-zinc-800 to-zinc-800`)
- Button outline: `outline-white/40`
- Button shadow: Inset white glow
- Download icon: `outline-Text-Light` (white)

**Dark Mode:**
- Container outline: `outline-Stroke-Stroke2` (lighter in dark mode)
- File name: `text-Text-Primary` (white)
- File size: `text-Text-Secondary` (gray)
- File icon: `bg-Primary-primary02` (green, same)
- Button: Light gradient for dark mode
- Button outline: Darker outline
- Download icon: Adapts to theme

**States:**
- Default: As described above
- Hover (button): Slightly lighter background
- Active (button): Pressed state with different shadow
- Disabled: Reduced opacity, no interaction

**Icons:**
1. **File Type Icon (Archive/ZIP):**
   - Multiple rectangles forming archive symbol
   - Primary green color
   - 24x24px container

2. **Download Icon:**
   - Circle with down arrow
   - White/light color
   - 24x24px size
   - Clear action indicator

**Example JSX:**

```jsx
// File Download Card - Default State
<div className="w-[664px] p-6 rounded-3xl outline outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Stroke2 inline-flex justify-between items-center overflow-hidden">
  {/* Left: File Information */}
  <div className="inline-flex flex-col justify-start items-start gap-2">
    {/* File Name */}
    <div className="justify-start text-Text-Primary text-base font-semibold font-['Inter_Display'] leading-6 tracking-tight">
      Bento Pro v 2.0 – Illustration Kit.zip
    </div>

    {/* File Icon + Size */}
    <div className="inline-flex justify-start items-center gap-2">
      {/* Archive/ZIP Icon */}
      <div className="w-6 h-6 relative overflow-hidden">
        <div className="w-0.5 h-2 left-[11px] top-[14px] absolute bg-Primary-primary02" />
        <div className="w-1.5 h-2 left-[15px] top-[14px] absolute bg-Primary-primary02" />
        <div className="w-1.5 h-2 left-[3px] top-[14px] absolute bg-Primary-primary02" />
        <div className="w-4 h-2.5 left-[3px] top-[1px] absolute bg-Primary-primary02" />
      </div>

      {/* File Size */}
      <div className="justify-start text-Text-Secondary text-base font-normal font-['Inter_Display'] leading-6 tracking-tight">
        128 MB
      </div>
    </div>
  </div>

  {/* Right: Download Button */}
  <div
    data-light-mode="True"
    data-state="Default"
    data-style="Icon"
    className="w-12 h-12 p-3.5 bg-gradient-to-b from-zinc-800 to-zinc-800 rounded-[32px] shadow-[inset_2px_0px_8px_2px_rgba(248,248,248,0.20)] outline outline-[1.50px] outline-offset-[-1.50px] outline-white/40 flex justify-center items-center gap-2.5 overflow-hidden"
  >
    {/* Download Icon */}
    <div className="w-6 h-6 relative overflow-hidden">
      <div className="w-5 h-5 left-[2.75px] top-[2.75px] absolute outline outline-[1.50px] outline-offset-[-0.75px] outline-Text-Light" />
    </div>
  </div>
</div>
```

**Usage Notes:**

**When to Use:**
- Displaying downloadable files in product listings
- Showing attached resources in comments or messages
- File management interfaces
- Download centers or resource libraries
- Email attachments preview
- Product deliverables (like design kits, templates)

**File Type Icons:**
- Archive/ZIP: Multiple rectangles (as shown)
- PDF: Document symbol
- Image: Picture frame icon
- Video: Play button icon
- Audio: Waveform icon
- Create consistent icon set для all file types

**File Size Display:**
- Show в appropriate units (KB, MB, GB)
- Round to reasonable precision (128 MB, не 128.47 MB)
- Use consistent formatting across interface
- Gray color indicates secondary information

**Download Button:**
- Always visible and accessible
- Dark button works on light backgrounds
- Icon-only design keeps card compact
- Clear affordance for download action
- Consider adding tooltip on hover

**Responsive Behavior:**
- Desktop: Full width (664px)
- Tablet: May reduce width, maintain proportions
- Mobile: Full width, possibly stack elements vertically
- Button always remains accessible

**Variations:**
- With progress bar (during download)
- With "Downloaded" checkmark state
- With file preview thumbnail
- With additional metadata (date, uploader)
- Multiple files in list/grid
- With delete/remove button

**Accessibility:**
- Download button keyboard accessible
- File name readable by screen readers
- Clear focus states on button
- File size announced
- ARIA labels for icon-only button

**Design Principles:**
- Clean, minimal design
- File information clearly visible
- Download action obvious
- Compact footprint
- Works in lists or individually
- Consistent с other cards в system

---

## Как использовать эту дизайн-систему

### Для дизайнеров

1. Используйте переменные CSS из секций выше для всех дизайнов
2. Соблюдайте spacing scale при создании макетов
3. Применяйте consistent border radius для схожих компонентов
4. Проверяйте контрастность текста (используйте Text-Primary, Secondary, Tertiary)
5. Используйте defined shadows для создания глубины
6. Создавайте компоненты для светлой и темной тем

### Для разработчиков

1. Используйте CSS переменные из дизайн-системы
2. Применяйте Tailwind классы согласно спецификациям
3. Структура компонентов:
   - Используйте semantic HTML
   - Применяйте data-атрибуты для состояний (data-state, data-light-mode)
   - Следуйте accessibility guidelines
4. Именование классов:
   - Используйте переменные вида `var(--Text-Primary)`
   - Применяйте Tailwind utilities где возможно
   - Создавайте custom CSS только для уникальных случаев

### Для продуктовой команды

1. Все компоненты должны соответствовать спецификациям дизайн-системы
2. Новые компоненты должны быть задокументированы и добавлены в систему
3. Изменения в дизайн-системе требуют review и approval
4. Используйте дизайн-систему как single source of truth для UI решений


---
