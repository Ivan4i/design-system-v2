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
--color-success: ;
--color-success-bg: ;
--color-success-border: ;

/* Error / Trend Down */
--color-error: ;
--color-error-bg: ;
--color-error-border: ;

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

#### Badge

- **Padding**:
- **Radius**:
- **Font Size**:
- **Variants**:
  - Success:
  - Error:
  - Warning:
  - Info:
  - Neutral:

#### Tag

- **Padding**:
- **Radius**:
- **Font Size**:
- **Close Button**:

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
  - Compact:
  - Default:
  - Comfortable:
- **Cell Padding**:
- **Header**:
  - Background:
  - Font Weight:
  - Border Bottom:
- **Row Borders**:
- **Hover State**:
- **Striped Rows**:

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
- **XL**: 56x56px
- **2XL**: 64x64px

#### Styles

- **Border Radius**: rounded-full (полностью круглый)
- **Border**:
  - Default: outline-[1.50px] outline-Stroke-Subtle/10 (светлый режим)
  - Active: outline-[1.50px] outline-Stroke-Subtle (темный режим)
- **Container**: px-4 py-3.5, bg-Backgrounds-surface2, rounded-[90px]
- **Placeholder**: img placeholder (placehold.co)
- **Status Indicator**: (to be defined)

---

### 10. List Items

#### List Item

- **Height**:
- **Padding**:
- **Border Bottom**:
- **States**:
  - Hover:
  - Active:
  - Selected:

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

#### Side Panel

- **Width**:
- **Background**:
- **Shadow**:
- **Padding**:
- **Header**:
  - Padding Bottom:
  - Border Bottom:

#### Modal

- **Max Width**:
- **Background**:
- **Border Radius**:
- **Shadow**:
- **Overlay**:
- **Padding**:

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
