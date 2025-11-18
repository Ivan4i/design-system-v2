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

- **Консистентность**:
- **Читаемость**:
- **Эффективность**:
- **Адаптивность**:

### Философия

>

---

## Цветовая палитра

### Primary Colors

```css
/* Основной цвет бренда */
--color-primary: ;
--color-primary-hover: ;
--color-primary-active: ;
--color-primary-light: ;
--color-primary-dark: ;

/* Вторичный цвет */
--color-secondary: ;
--color-secondary-hover: ;
--color-secondary-active: ;
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
--color-text-primary: ;
--color-text-secondary: ;
--color-text-tertiary: ;
--color-text-disabled: ;
--color-text-inverse: ;

/* Backgrounds */
--color-bg-primary: ;
--color-bg-secondary: ;
--color-bg-tertiary: ;
--color-bg-elevated: ;
--color-bg-overlay: ;

/* Stroke / Borders */
--color-border-primary: ;
--color-border-secondary: ;
--color-border-focus: ;
--color-border-disabled: ;

/* Shades */
--color-gray-50: ;
--color-gray-100: ;
--color-gray-200: ;
--color-gray-300: ;
--color-gray-400: ;
--color-gray-500: ;
--color-gray-600: ;
--color-gray-700: ;
--color-gray-800: ;
--color-gray-900: ;
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
--gradient-primary: ;
--gradient-secondary: ;
--gradient-accent: ;
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
--font-primary: ;
--font-secondary: ;
--font-mono: ;
```

### Font Sizes

```css
--font-size-xs: ;
--font-size-sm: ;
--font-size-base: ;
--font-size-md: ;
--font-size-lg: ;
--font-size-xl: ;
--font-size-2xl: ;
--font-size-3xl: ;
--font-size-4xl: ;
--font-size-5xl: ;
```

### Font Weights

```css
--font-weight-thin: ;
--font-weight-light: ;
--font-weight-normal: ;
--font-weight-medium: ;
--font-weight-semibold: ;
--font-weight-bold: ;
--font-weight-extrabold: ;
--font-weight-black: ;
```

### Line Heights

```css
--line-height-tight: ;
--line-height-snug: ;
--line-height-normal: ;
--line-height-relaxed: ;
--line-height-loose: ;
```

### Text Styles

#### Headings

- **H1**:
- **H2**:
- **H3**:
- **H4**:
- **H5**:
- **H6**:

#### Body Text

- **Body Large**:
- **Body**:
- **Body Small**:
- **Caption**:

#### Tracking (Letter Spacing)

```css
--letter-spacing-tight: ;
--letter-spacing-normal: ;
--letter-spacing-wide: ;
--letter-spacing-wider: ;
```

---

## Spacing & Layout

### Spacing Scale

```css
--space-0: ;
--space-1: ;
--space-2: ;
--space-3: ;
--space-4: ;
--space-5: ;
--space-6: ;
--space-8: ;
--space-10: ;
--space-12: ;
--space-16: ;
--space-20: ;
--space-24: ;
```

### Border Radius

```css
--radius-none: ;
--radius-sm: ;
--radius-base: ;
--radius-md: ;
--radius-lg: ;
--radius-xl: ;
--radius-2xl: ;
--radius-full: ;
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
--shadow-button: ;
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
--border-width-0: ;
--border-width-1: ;
--border-width-2: ;
--border-width-4: ;
```

#### Border Offset

```css
--border-offset-0: ;
--border-offset-1: ;
--border-offset-2: ;
```

### Opacity Scale

```css
--opacity-0: ;
--opacity-10: ;
--opacity-20: ;
--opacity-30: ;
--opacity-40: ;
--opacity-50: ;
--opacity-60: ;
--opacity-70: ;
--opacity-80: ;
--opacity-90: ;
--opacity-100: ;
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

#### Primary Button

- **Size**:
  - Small:
  - Medium:
  - Large:
- **Radius**:
- **States**:
  - Default:
  - Hover:
  - Active:
  - Disabled:

#### Secondary Button

- **Size**:
- **Radius**:
- **States**:
  - Default:
  - Hover:

#### Outline Button

- **Border**:
- **Background**:
- **States**:
  - Hover:

#### Ghost Button

- **Background**:
- **States**:
  - Hover:

---

### 3. Inputs

#### Text Input

- **Height**:
  - Small:
  - Medium:
  - Large:
- **Padding**:
- **Radius**:
- **Border**:
- **States**:
  - Focus:
  - Error:
  - Disabled:

#### Textarea

- **Min Height**:
- **Padding**:
- **Radius**:
- **Resize**:

#### Select

- **Height**:
- **Padding**:
- **Icon**:

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

#### Main Navigation

- **Height**:
- **Background**:
- **Shadow**:
- **Item Padding**:
- **States**:
  - Default:
  - Hover:
  - Active:

#### Sidebar Navigation

- **Width**:
- **Item Height**:
- **Item Padding**:
- **States**:

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

- **XS**:
- **Small**:
- **Medium**:
- **Large**:
- **XL**:
- **2XL**:

#### Styles

- **Border Radius**:
- **Border**:
- **Placeholder**:
- **Status Indicator**:

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

#### Toast Notification

- **Width**:
- **Padding**:
- **Radius**:
- **Shadow**:
- **Position**:
- **Variants**:
- **Auto-dismiss**:

#### Alert Banner

- **Padding**:
- **Border Left**:
- **Background**:
- **Close Button**:

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

#### Skeleton Loader

- **Background**:
- **Animation**:
- **Border Radius**:
- **Sizes**:

#### Spinner

- **Size**:
- **Color**:
- **Animation**:

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
-

#### Hover
-

#### Active/Focus
-

#### Disabled
-

#### Loading
-

#### Error
-

#### Success
-

---

## Иконки

### Icon System

- **Library**:
- **Sizes**:
  - XS:
  - SM:
  - Base:
  - MD:
  - LG:
  - XL:
- **Stroke Width**:
- **Style**:
- **Color**:

### Common Icons

| Название | Использование | Размер по умолчанию |
|----------|---------------|---------------------|
| Search | | |
| Close / X | | |
| Chevron Down | | |
| Arrow Right | | |
| Check | | |
| Alert Circle | | |
| X Circle | | |
| Menu / Hamburger | | |
| User | | |
| Settings | | |
| Plus | | |
| Trash | | |
| Edit / Pencil | | |

---

## Как использовать эту дизайн-систему

### Для дизайнеров


### Для разработчиков


### Для продуктовой команды


---
