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
--color-info: #60a5fa; /* blue-400 */
--color-info-bg: rgba(96, 165, 250, 0.05); /* blue-400/5 */
--color-info-border: rgba(96, 165, 250, 0.20); /* blue-400/20 */
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
--color-chart-1: #8b5cf6; /* violet-500 - primary chart color */
--color-chart-2: #06b6d4; /* cyan-500 */
--color-chart-3: #10b981; /* emerald-500 */
--color-chart-4: #f59e0b; /* amber-500 */
--color-chart-5: #ec4899; /* pink-500 */
--color-chart-6: #6366f1; /* indigo-500 */
--color-chart-7: #14b8a6; /* teal-500 */
--color-chart-8: #f97316; /* orange-500 */
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
--color-brand-facebook: #1877f2;
--color-brand-twitter: #1da1f2;
--color-brand-instagram: #e4405f;
--color-brand-linkedin: #0a66c2;
--color-brand-youtube: #ff0000;
--color-brand-github: #181717;
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
--font-size-xs: 0.75rem;    /* 12px - labels, captions */
--font-size-sm: 0.875rem;   /* 14px - body, buttons */
--font-size-base: 1rem;     /* 16px - base text */
--font-size-md: 1.125rem;   /* 18px */
--font-size-lg: 1.25rem;    /* 20px */
--font-size-xl: 1.5rem;     /* 24px */
--font-size-2xl: 1.875rem;  /* 30px */
--font-size-3xl: 2rem;      /* 32px - headings */
--font-size-4xl: 2.5rem;    /* 40px */
--font-size-5xl: 3rem;      /* 48px */
```

### Font Weights

```css
--font-weight-thin: 100;
--font-weight-light: 300;
--font-weight-normal: 400;   /* Основной текст */
--font-weight-medium: 500;   /* Password input text */
--font-weight-semibold: 600; /* Buttons, headings */
--font-weight-bold: 700;
--font-weight-extrabold: 800;
--font-weight-black: 900;
```

### Line Heights

```css
--line-height-tight: 1rem;      /* 16px - leading-4 for buttons */
--line-height-snug: 1.25rem;    /* 20px - leading-5 for text */
--line-height-normal: 1.5rem;   /* 24px */
--line-height-relaxed: 2.5rem;  /* 40px - leading-10 for headings */
--line-height-loose: 3rem;      /* 48px */
```

### Text Styles

#### Headings

- **H1**: font-size: 3xl (32px), font-weight: semibold (600), line-height: 40px, tracking: tight
- **H2**: font-size: 2xl (30px), font-weight: semibold (600), line-height: 36px
- **H3**: font-size: xl (24px), font-weight: semibold (600)
- **H4**: font-size: lg (20px), font-weight: semibold (600)
- **H5**: font-size: base (16px), font-weight: semibold (600)
- **H6**: font-size: sm (14px), font-weight: semibold (600)

#### Body Text

- **Body Large**: font-size: base (16px), font-weight: normal (400), line-height: 24px
- **Body**: font-size: sm (14px), font-weight: normal (400), line-height: 20px
- **Body Small**: font-size: xs (12px), font-weight: normal (400), line-height: 16px
- **Caption**: font-size: xs (12px), font-weight: normal (400), line-height: 20px, tracking: tight

#### Tracking (Letter Spacing)

```css
--letter-spacing-tight: -0.01em;  /* tracking-tight - используется повсеместно */
--letter-spacing-normal: 0;
--letter-spacing-wide: 0.025em;
--letter-spacing-wider: 0.05em;
```

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
--shadow-xs: 0px 1px 2px 0px rgba(0, 0, 0, 0.05);
--shadow-sm: 0px 1px 3px 0px rgba(0, 0, 0, 0.1), 0px 1px 2px -1px rgba(0, 0, 0, 0.1);
--shadow-base: 0px 4px 6px -1px rgba(0, 0, 0, 0.1), 0px 2px 4px -2px rgba(0, 0, 0, 0.1);
--shadow-md: 0px 10px 15px -3px rgba(0, 0, 0, 0.1), 0px 4px 6px -4px rgba(0, 0, 0, 0.1);
--shadow-lg: 0px 20px 25px -5px rgba(0, 0, 0, 0.1), 0px 8px 10px -6px rgba(0, 0, 0, 0.1);
--shadow-xl: 0px 25px 50px -12px rgba(0, 0, 0, 0.25);

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
--shadow-button-hover: 0px 4px 12px 0px rgba(0, 0, 0, 0.15), inset 2px 0px 8px 2px rgba(24, 24, 24, 0.25);
--shadow-button-active: inset 2px 2px 8px 2px rgba(0, 0, 0, 0.25), 0px 1px 2px 0px rgba(0, 0, 0, 0.1);
```

#### Hover Shadows

```css
--shadow-hover-sm: 0px 2px 8px 0px rgba(0, 0, 0, 0.08), 0px 1px 4px 0px rgba(0, 0, 0, 0.05);
--shadow-hover-md: 0px 4px 12px 0px rgba(0, 0, 0, 0.1), 0px 2px 6px 0px rgba(0, 0, 0, 0.08);
--shadow-hover-lg: 0px 8px 24px 0px rgba(0, 0, 0, 0.12), 0px 4px 12px 0px rgba(0, 0, 0, 0.1);

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

- **Padding**: p-6 (24px all sides)
- **Border Radius**: rounded-[5px] (5px для основных карточек)
- **Background**: var(--Backgrounds-surface2)
- **Shadow**: var(--shadow-sm)
- **Border**: outline-[1.50px] outline-offset-[-1.50px] outline-Stroke-Subtle/10

**Варианты:**
- **Compact Card**: p-4 (16px padding), для меньших элементов
- **Dashboard Card**: p-6, gap-4 для внутреннего содержимого
- **Highlighted Card**: hover:shadow-md, transition-shadow duration-200

#### Пример использования

```css
.card {
  padding: 1.5rem; /* p-6 */
  border-radius: 5px; /* rounded-[5px] */
  background: var(--Backgrounds-surface2);
  box-shadow: var(--shadow-sm);
  outline: 1.5px solid rgba(var(--Stroke-Subtle), 0.1);
  outline-offset: -1.5px;
}

.card:hover {
  box-shadow: var(--shadow-md);
}
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
  - Hover: scale-102, shadow-button-hover, transition-all duration-150
  - Active: scale-98, shadow-button-active
  - Disabled: opacity-50, cursor-not-allowed, pointer-events-none

#### Icon Button (Round)

- **Size**: w-12 h-12 (48x48px)
- **Radius**: 90px (rounded-[90px]) - pill shape
- **Background**:
  - Light mode: Backgrounds-surface2
  - Dark mode: gradient from-zinc-800 to-neutral-800
- **Icon Size**: 24x24px (w-6 h-6)
- **States**:
  - Default: (описано выше)
  - Hover: scale-105, bg-Backgrounds-highlight, transition-all duration-150
  - Active: scale-95, bg-Backgrounds-surface1

#### Segment Control Button (Tabs)

- **Size**: px-6 py-3 (24px horizontal, 12px vertical), height: 48px
- **Radius**: 48px (rounded-[48px])
- **Font**: font-semibold, text-sm (14px), leading-4, tracking-tight
- **States**:
  - Default: transparent, text-Text-Secondary
  - Active: outline-[1.50px] Stroke-Stroke2, text-Text-Primary
  - Hover: bg-Backgrounds-surface2/50, text-Text-Primary, transition-colors duration-150

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
  - Disabled: opacity-50, cursor-not-allowed, bg-Backgrounds-surface1
- **Icons**:
  - Eye icon (show/hide): w-6 h-6, right-[12px], top-[12px]

#### Search Input

- **Size**: w-80 p-3 (320px width, 12px padding)
- **Radius**: 90px (rounded-[90px])
- **Background**:
  - Light mode: Backgrounds-surface2
  - Dark mode: Stroke-Subtle, outline-[1.50px] white
- **Icon**: Search icon 24x24px (w-6 h-6), left aligned, gap-2
- **Placeholder**: "Search anything...", text-sm, text-Text-Secondary
- **Font**: font-normal, text-sm, leading-5, tracking-tight

#### Select / Dropdown

- **Size**: max-w-44 pl-5 pr-3 py-3, height: 48px
- **Radius**: 90px (rounded-[90px])
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Text**: text-sm, text-Text-Secondary, leading-5, tracking-tight
- **Icon**: Chevron down, w-6 h-6, right aligned
- **Example**: "Last 7 days"

---

### 4. Badges & Tags

#### Status Badge (Small)

- **Padding**: px-2 py-0.5 (8px horizontal, 2px vertical)
- **Height**: h-6 (24px)
- **Radius**: rounded-lg (12px)
- **Border**: outline-[1.50px] outline-offset-[-1.50px]
- **Font**: text-xs, font-normal, leading-5, tracking-tight
- **Variants**:
  - **Success/Active**: bg-green-600/5, outline-green-600/20, text-Primary-primary02
  - **Error/Offline**: bg-red-400/5, outline-red-400/20, text-red-400
  - **Warning**: bg-warning-bg, outline-warning-border, text-warning
  - **Info**: bg-info-bg, outline-info-border, text-info
  - **Neutral**: bg-Backgrounds-surface2, outline-Stroke-Subtle/20, text-Text-Secondary

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

#### Tag

- **Padding**: px-2.5 py-1 (10px horizontal, 4px vertical)
- **Radius**: rounded-md (8px)
- **Font Size**: text-xs (12px), font-medium
- **Background**: var(--Backgrounds-surface2)
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Layout**: inline-flex items-center gap-1.5
- **Close Button**:
  - Size: w-3 h-3 (12px)
  - Icon: X icon
  - Padding: p-0.5
  - Hover: text-Text-Primary, transition-colors duration-150
  - Position: relative, ml-1

---

### 5. Forms

#### Form Layout

- **Label**:
  - Margin Bottom: mb-2 (8px)
  - Font Weight: font-semibold (600)
  - Font Size: text-sm (14px)
  - Color: var(--Text-Primary)
- **Field Group**:
  - Margin Bottom: mb-6 (24px) между полями
  - Gap: gap-2 (8px) внутри группы
- **Helper Text**:
  - Margin Top: mt-1.5 (6px)
  - Font Size: text-xs (12px)
  - Color: var(--Text-Secondary)
  - Line Height: leading-5 (20px)
- **Error Message**:
  - Color: var(--color-error)
  - Font Size: text-xs (12px)
  - Margin Top: mt-1.5 (6px)

---

### 6. Tables

#### Table Structure

- **Row Height**:
  - Compact: h-10 (40px)
  - Default: h-12 (48px)
  - Comfortable: h-16 (64px)
- **Cell Padding**: px-4 py-3 (16px horizontal, 12px vertical)
- **Header**:
  - Background: var(--Backgrounds-surface1)
  - Font Weight: font-semibold (600)
  - Font Size: text-sm (14px)
  - Border Bottom: border-b-[1.5px] border-Stroke-Stroke2
  - Color: var(--Text-Secondary)
- **Row Borders**: border-b border-Stroke-Subtle/10
- **Hover State**: bg-Backgrounds-surface2, transition-colors duration-150
- **Striped Rows**: nth-child(even) bg-Backgrounds-surface2/50
- **Selected Row**: bg-Primary-primary03/5, outline-[1.50px] outline-Primary-primary03/20

---

### 7. Navigation

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
  - Disabled: opacity-40, cursor-not-allowed, pointer-events-none
  - Hover (non-disabled): bg-Backgrounds-highlight, transition-colors duration-150
- **Icons**: Arrow left/right icons

#### Sidebar Navigation

- **Width**: w-64 (256px) expanded, w-20 (80px) collapsed
- **Background**: var(--Backgrounds-surface2)
- **Border**: border-r border-Stroke-Subtle/10
- **Item Height**: h-12 (48px)
- **Item Padding**: px-4 py-3 (16px horizontal, 12px vertical)
- **Item Layout**: flex items-center gap-3
- **Icon**: w-5 h-5 (20px)
- **Text**: text-sm font-medium, hidden когда collapsed
- **States**:
  - Default: transparent, text-Text-Secondary
  - Hover: bg-Backgrounds-highlight, text-Text-Primary, transition-colors duration-150
  - Active: bg-Primary-primary03/10, text-Primary-primary03, border-l-2 border-Primary-primary03
  - Disabled: opacity-50, cursor-not-allowed

---

### 8. Charts

#### Line Chart

- **Line Width**: 2px (default), 3px (highlighted)
- **Point Radius**: 4px (default), 6px (hover/active)
- **Grid Lines**:
  - Color: var(--Stroke-Subtle)/10
  - Width: 0.5px
  - Dash: [4, 4] для пунктирных линий
- **Colors**: используйте переменные --color-chart-1 through --color-chart-8
- **Area Fill**: gradient с opacity от 0.2 до 0 (top to bottom)

#### Bar Chart

- **Bar Spacing**: gap-2 (8px) между группами, gap-1 (4px) внутри группы
- **Border Radius**: rounded-t-sm (2px) для верха столбцов
- **Min Bar Width**: 8px
- **Max Bar Width**: 48px
- **Colors**: используйте переменные --color-chart-*
- **Hover**: opacity-80, transition-opacity duration-150

#### Pie/Donut Chart

- **Border Width**: 0 (без обводки по умолчанию), 2px для hover
- **Donut Hole**: 60% от радиуса (для donut charts)
- **Spacing**: 2px gap между сегментами (для разделенных диаграмм)
- **Colors**: используйте переменные --color-chart-1 through --color-chart-8
- **Hover**: scale-105, transition-transform duration-200
- **Legend**: gap-3, text-sm, items с gap-2

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
- **Status Indicator**:
  - Size: w-3 h-3 (12px), w-2.5 h-2.5 (10px) для маленьких аватаров
  - Position: absolute, bottom-0, right-0
  - Border: border-2 border-Backgrounds-surface2 (чтобы отделить от фона)
  - Border Radius: rounded-full
  - Colors:
    - Online: bg-success (зеленый)
    - Busy: bg-error (красный)
    - Away: bg-warning (оранжевый)
    - Offline: bg-gray-400 (серый)

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

- **Width**: min-w-80 max-w-96 (320px-384px)
- **Padding**: p-4 (16px all sides), gap-3 между icon и content
- **Radius**: rounded-lg (12px)
- **Shadow**: var(--shadow-lg)
- **Position**: fixed, top-4 right-4 (или bottom-4 для нижних уведомлений)
- **Border**: outline-[1.50px] outline-offset-[-1.50px]
- **Variants**:
  - Success: bg-success-bg, outline-success-border, text-Primary-primary02
  - Error: bg-error-bg, outline-error-border, text-red-400
  - Warning: bg-warning-bg, outline-warning-border, text-warning
  - Info: bg-info-bg, outline-info-border, text-info
- **Auto-dismiss**: 5000ms (5 seconds) по умолчанию
- **Icon**: w-5 h-5 (20px) слева
- **Close Button**: w-5 h-5, absolute top-3 right-3
- **Animation**: slide-in-right, fade-in duration-300

#### Alert Banner

- **Padding**: px-4 py-3 (16px horizontal, 12px vertical)
- **Border Left**: border-l-4 для акцента типа уведомления
- **Border Radius**: rounded-md (8px)
- **Background**: зависит от варианта (см. ниже)
- **Layout**: flex items-start gap-3
- **Variants**:
  - Success: bg-success-bg, border-l-success
  - Error: bg-error-bg, border-l-error
  - Warning: bg-warning-bg, border-l-warning
  - Info: bg-info-bg, border-l-info
- **Icon**: w-5 h-5 (20px) слева, соответствует варианту
- **Title**: text-sm font-semibold, mb-1
- **Description**: text-sm text-Text-Secondary
- **Close Button**: w-5 h-5, ml-auto, text-Text-Tertiary hover:text-Text-Primary

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

- **Width**: w-96 (384px) по умолчанию, max-w-md для адаптивности
- **Background**: var(--Backgrounds-surface2)
- **Shadow**: var(--shadow-xl), shadow-[-10px_0_25px_-5px_rgba(0,0,0,0.1)] для левой панели
- **Padding**: p-6 (24px)
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Position**: fixed, top-0, right-0 (или left-0), h-full
- **Header**:
  - Padding Bottom: pb-4 (16px)
  - Border Bottom: border-b border-Stroke-Subtle/10
  - Title: text-xl font-semibold
  - Close Button: absolute top-6 right-6, w-6 h-6
- **Content**: flex-1 overflow-y-auto, py-4
- **Footer**: pt-4, border-t border-Stroke-Subtle/10
- **Overlay**: fixed inset-0, bg-black/40, backdrop-blur-sm
- **Animation**: slide-in-right (или slide-in-left), duration-300

#### Modal

- **Max Width**:
  - Small: max-w-md (448px)
  - Medium: max-w-lg (512px)
  - Large: max-w-2xl (672px)
  - Full: max-w-4xl (896px)
- **Background**: var(--Backgrounds-surface2)
- **Border Radius**: rounded-[32px]
- **Shadow**: var(--shadow-xl)
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Position**: fixed, top-1/2, left-1/2, transform -translate-x-1/2 -translate-y-1/2
- **Padding**: p-6 (24px), для больших модалов p-8 (32px)
- **Header**:
  - Padding Bottom: pb-4
  - Border Bottom: border-b border-Stroke-Subtle/10
  - Title: text-2xl font-semibold
  - Close Button: absolute top-6 right-6, w-6 h-6
- **Content**: py-4, max-h-[60vh] overflow-y-auto
- **Footer**:
  - Padding Top: pt-4
  - Border Top: border-t border-Stroke-Subtle/10
  - Buttons: flex justify-end gap-3
- **Overlay**: fixed inset-0, bg-black/60, backdrop-blur-sm
- **Animation**: fade-in, scale-in duration-200

---

### 13. Accordion / FAQ

#### Accordion Item

- **Padding**: p-4 (16px) для header, p-4 для content
- **Border**: outline-[1.50px] outline-Stroke-Stroke2
- **Border Radius**: rounded-lg (12px)
- **Margin Bottom**: mb-2 (8px) между items
- **Background**: var(--Backgrounds-surface2)
- **Header**:
  - Layout: flex justify-between items-center
  - Title: text-base font-semibold
  - Icon: w-5 h-5 chevron, rotate-180 когда expanded
  - Cursor: pointer
- **Content**:
  - Padding Top: pt-2 (когда expanded)
  - Max Height: 0 (collapsed), auto (expanded)
  - Overflow: hidden
  - Text: text-sm text-Text-Secondary
- **States**:
  - Collapsed: max-h-0, chevron rotate-0
  - Expanded: max-h-auto, chevron rotate-180, border-Primary-primary03/20
  - Hover: bg-Backgrounds-highlight, transition-colors duration-150
- **Animation**: transition-all duration-300 ease-in-out

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

- **Sizes**:
  - Small: w-4 h-4 (16px)
  - Medium: w-6 h-6 (24px)
  - Large: w-8 h-8 (32px)
  - XL: w-12 h-12 (48px)
- **Color**:
  - Primary: border-Primary-primary03
  - Secondary: border-Text-Secondary
  - Light: border-white (для темных фонов)
- **Style**: border-2, border-t-transparent, rounded-full
- **Animation**: animate-spin, duration-700 linear infinite

---

### 15. Empty States

#### Empty State Layout

- **Container**:
  - Layout: flex flex-col items-center justify-center
  - Padding: py-16 px-8 (64px vertical, 32px horizontal)
  - Text Align: center
  - Min Height: min-h-96 (384px)
- **Icon**:
  - Size: w-16 h-16 (64px) или w-20 h-20 (80px)
  - Color: var(--Text-Tertiary)
  - Style: outline style, stroke-width 1.5px
- **Heading**:
  - Font Size: text-xl (20px)
  - Font Weight: font-semibold (600)
  - Color: var(--Text-Primary)
  - Line Height: leading-7
- **Description**:
  - Font Size: text-sm (14px)
  - Color: var(--Text-Secondary)
  - Max Width: max-w-md (448px)
  - Line Height: leading-6
- **Action Button**:
  - Variant: Primary button
  - Size: Medium или Large
- **Spacing**:
  - Icon → Heading: mt-6 (24px)
  - Heading → Description: mt-2 (8px)
  - Description → Button: mt-6 (24px)

---

### 16. Special Effects

#### Focus Ring

```css
--focus-ring: 0 0 0 3px rgba(var(--Primary-primary03), 0.2); /* Focus ring для accessibility */
--focus-ring-offset: 2px; /* Отступ для focus ring */
--focus-ring-color: var(--Primary-primary03); /* Цвет focus ring */
--focus-ring-width: 2px; /* Толщина focus ring */
```

**Использование:**
- Применяется на интерактивные элементы при :focus-visible
- outline: var(--focus-ring-width) solid var(--focus-ring-color)
- outline-offset: var(--focus-ring-offset)
- border-radius: inherit (наследуется от элемента)

#### Backdrop Blur

```css
--backdrop-blur-none: 0;
--backdrop-blur-sm: blur(4px); /* Легкое размытие для subtle overlays */
--backdrop-blur-base: blur(8px); /* Стандартное размытие для modals */
--backdrop-blur-md: blur(12px); /* Среднее размытие */
--backdrop-blur-lg: blur(16px); /* Сильное размытие для side panels */
--backdrop-blur-xl: blur(24px); /* Очень сильное размытие */
```

**Использование:**
- Overlay для модалов: backdrop-blur-base
- Sidebar overlay: backdrop-blur-lg
- Glass morphism эффект: backdrop-blur-md с bg-opacity

---

### 17. Toggle Switch

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

---

### 18. Page Headers

#### Section Header with Dropdown

- **Container**: inline-flex justify-between items-center
- **Title**:
  - Padding: px-5 (h-12 container с p-3 gap-2)
  - Font: text-xl, font-semibold, leading-7, tracking-tight
  - Color: text-Text-Primary
- **Dropdown**: w-40 max-w-44, positioned на правой стороне
- **Layout**: flex между title и dropdown
- **Example**: "Overview" + "Last 7 days" dropdown

---

## Паттерны

### Dashboard Layouts

#### Grid Dashboard

- **Grid**:
  - Desktop: grid-cols-4 (4 колонки для metrics), grid-cols-2 (для больших карточек)
  - Tablet: grid-cols-2
  - Mobile: grid-cols-1
- **Card Spacing**: gap-6 (24px) между карточками
- **Container Padding**: px-16 py-8 (64px horizontal, 32px vertical)
- **Card Layout**:
  - Metric Cards: 1 column width, min-h-32 (128px)
  - Chart Cards: 2-4 columns width, min-h-96 (384px)
  - Table Cards: full width (col-span-4), min-h-64 (256px)
- **Responsive**:
  - xl (1280px+): grid-cols-4, full dashboard
  - lg (1024px+): grid-cols-3
  - md (768px+): grid-cols-2
  - sm (640px): grid-cols-1

#### Sidebar + Content

- **Sidebar Width**:
  - Expanded: w-64 (256px)
  - Collapsed: w-20 (80px)
  - Mobile: fixed overlay, w-64
- **Content Area**:
  - Margin Left: ml-64 (когда sidebar expanded), ml-20 (collapsed)
  - Padding: p-8 (32px)
  - Min Height: min-h-screen
  - Background: var(--Backgrounds-surface1)
- **Gap**: нет gap, sidebar fixed, content с margin
- **Sidebar Style**:
  - Background: var(--Backgrounds-surface2)
  - Border Right: border-r border-Stroke-Subtle/10
  - Position: fixed, left-0, top-0, h-full
  - Z-index: z-40
- **Responsive**:
  - Desktop: sidebar visible, content с margin
  - Tablet/Mobile: sidebar overlay, content full width
  - Toggle: hamburger menu для mobile

---

### Form Patterns

#### Single Column Form

- **Max Width**: max-w-md (448px) по центру
- **Field Spacing**: space-y-6 (24px между полями)
- **Container Padding**: p-6 или p-8 (24px или 32px)
- **Button Group**:
  - Layout: flex gap-3 justify-end
  - Margin Top: mt-8 (32px от последнего поля)
  - Primary + Secondary buttons
- **Layout**:
  - Container: flex flex-col
  - Card wrapper: с border и shadow
  - Form: w-full

#### Multi Column Form

- **Grid**:
  - Desktop: grid-cols-2 gap-6
  - Mobile: grid-cols-1
- **Container**: max-w-4xl (896px)
- **Full Width Fields**:
  - Text areas: col-span-2
  - Rich text editors: col-span-2
  - File uploads: col-span-2
  - Submit buttons: col-span-2
- **Section Headers**: col-span-2, text-lg font-semibold, mb-4, mt-6
- **Responsive**:
  - lg (1024px+): grid-cols-2
  - md и меньше: grid-cols-1

#### Wizard / Stepper Form

- **Steps Indicator**:
  - Layout: flex justify-between items-center, mb-8
  - Step Item: flex items-center gap-2
  - Step Number: w-8 h-8, rounded-full, flex items-center justify-center
  - Step Line: flex-1, h-0.5, bg-Stroke-Subtle
  - Active Step: bg-Primary-primary03, text-white
  - Completed Step: bg-success, text-white, с checkmark
  - Pending Step: bg-Backgrounds-surface2, text-Text-Secondary
- **Content Area**:
  - Min Height: min-h-96 (384px)
  - Padding: p-6
  - Background: var(--Backgrounds-surface2)
  - Border Radius: rounded-lg
- **Navigation**:
  - Layout: flex justify-between mt-8
  - Back Button: Secondary button
  - Next/Submit Button: Primary button
  - Skip Button (optional): Ghost button
- **Progress**:
  - Progress Bar: h-1, rounded-full, bg-Stroke-Subtle
  - Progress Fill: bg-Primary-primary03, transition-width
  - Position: top of form, mb-6

---

### Data Visualization

#### Dashboard Card with Chart

- **Card Container**:
  - Padding: p-6 (24px)
  - Background: var(--Backgrounds-surface2)
  - Border Radius: rounded-[5px]
  - Shadow: var(--shadow-sm)
  - Border: outline-[1.50px] outline-Stroke-Subtle/10
- **Header**:
  - Layout: flex justify-between items-start, mb-6
  - Title: text-xl font-semibold text-Text-Primary
  - Subtitle: text-sm text-Text-Secondary, mt-1
  - Actions: dropdown или button group на правой стороне
  - Time Range Selector: Select component (Last 7 days, Last 30 days, etc.)
- **Chart Area**:
  - Min Height: min-h-80 (320px)
  - Padding: py-4
  - Aspect Ratio: aspect-video для responsive charts
  - Legend: positioned внизу или справа, gap-3, text-sm
- **Footer**:
  - Layout: flex justify-between items-center, mt-4
  - Border Top: border-t border-Stroke-Subtle/10, pt-4
  - Summary Stats: flex gap-6
  - Stat Item: flex flex-col, gap-1
  - Stat Label: text-xs text-Text-Secondary
  - Stat Value: text-base font-semibold
  - View Details Link: text-sm text-Primary-primary03, hover:underline

#### Table with Filters

- **Filter Bar**:
  - Height: h-16 (64px)
  - Background: var(--Backgrounds-surface2)
  - Padding: px-6 py-3
  - Border Bottom: border-b border-Stroke-Subtle/10
  - Layout: flex items-center gap-4
  - Search Input: flex-1, max-w-md
  - Filter Buttons: flex gap-2
  - Action Buttons: ml-auto
- **Table**:
  - Background: var(--Backgrounds-surface2)
  - Border: outline-[1.50px] outline-Stroke-Subtle/10
  - Border Radius: rounded-[5px]
  - Max Height: max-h-screen-minus-header, overflow-y-auto
- **Pagination**:
  - Layout: flex justify-between items-center
  - Padding: px-6 py-4
  - Border Top: border-t border-Stroke-Subtle/10
  - Page Info: text-sm text-Text-Secondary (Showing 1-10 of 100)
  - Navigation: flex gap-1, pagination component
  - Items Per Page: Select component, w-20

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
- Border: outline-[1.50px] outline-success (зеленая обводка)
- Background: bg-success-bg (легкий зеленый фон)
- Text: text-success
- Icon: checkmark icon, w-5 h-5, text-success
- Message: text-sm text-success, mt-1.5, отображается под полем

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
| Arrow Right | Navigation, pagination | 24x24px (w-6 h-6) |
| Arrow Left | Navigation, pagination | 24x24px (w-6 h-6) |
| Eye / Eye Off | Password visibility toggle | 16x16px (w-4 h-4) |
| Bell | Notifications | 24x24px (w-6 h-6) |
| Mail | Messages | 24x24px (w-6 h-6) |
| User | Profile, avatar placeholder | 24x24px (w-6 h-6) |
| Settings | Settings button | 16x16px (w-4 h-4) |

**Иконки в компонентах:**
- Icons имеют вложенную структуру: контейнер (w-6 h-6) → overflow-hidden → внутренний icon (w-4 h-4 или w-3.5)
- Offset позиционирование: left-[4px] top-[4px] внутри контейнера
- Для иконок используется outline style с offset для создания эффекта обводки

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
