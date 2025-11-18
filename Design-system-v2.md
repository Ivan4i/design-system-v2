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
--color-warning: ;
--color-warning-bg: ;
--color-warning-border: ;

/* Info */
--color-info: ;
--color-info-bg: ;
--color-info-border: ;
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
--color-chart-1: ;
--color-chart-2: ;
--color-chart-3: ;
--color-chart-4: ;
--color-chart-5: ;
--color-chart-6: ;
--color-chart-7: ;
--color-chart-8: ;
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
--color-brand-facebook: ;
--color-brand-twitter: ;
--color-brand-instagram: ;
--color-brand-linkedin: ;
--color-brand-youtube: ;
--color-brand-github: ;
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
--shadow-xs: ;
--shadow-sm: ;
--shadow-base: ;
--shadow-md: ;
--shadow-lg: ;
--shadow-xl: ;

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
--shadow-button-hover: ;
--shadow-button-active: ;
```

#### Hover Shadows

```css
--shadow-hover-sm: ;
--shadow-hover-md: ;
--shadow-hover-lg: ;

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

#### Segment Control Button (Tabs)

- **Size**: px-6 py-3 (24px horizontal, 12px vertical), height: 48px
- **Radius**: 48px (rounded-[48px])
- **Font**: font-semibold, text-sm (14px), leading-4, tracking-tight
- **States**:
  - Default: transparent, text-Text-Secondary
  - Active: outline-[1.50px] Stroke-Stroke2, text-Text-Primary
  - Hover: (to be defined)

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

#### Tag

- **Padding**: (to be defined)
- **Radius**: (to be defined)
- **Font Size**: (to be defined)
- **Close Button**: (to be defined)

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

- **Width**: (to be defined)
- **Item Height**: (to be defined)
- **Item Padding**: (to be defined)
- **States**: (to be defined)

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
--focus-ring: ;
```

#### Backdrop Blur

```css
--backdrop-blur-sm: ;
--backdrop-blur-base: ;
--backdrop-blur-md: ;
--backdrop-blur-lg: ;
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
