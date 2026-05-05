---
version: alpha
name: Telezhky Industrial
description: Dark industrial theme for warehouse cart manufacturer. Steel greys, functional orange accent, geometric typography.
colors:
  primary: "#0a0e14"
  secondary: "#131820"
  border: "#2a3040"
  text: "#e6edf3"
  text-dim: "#9ba3af"
  accent: "#f0883e"
  accent-hover: "#e8831a"
  green: "#25d366"
  blue: "#58a6ff"
typography:
  h1:
    fontFamily: Unbounded
    fontSize: 2.8rem
    fontWeight: 800
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  h2:
    fontFamily: Unbounded
    fontSize: 2rem
    fontWeight: 700
    lineHeight: 1.3
    letterSpacing: "-0.02em"
  body-lg:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, sans-serif"
    fontSize: 1.2rem
    lineHeight: 1.7
  body-md:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, sans-serif"
    fontSize: 1rem
    lineHeight: 1.7
rounded:
  sm: 4px
  md: 8px
  lg: 12px
spacing:
  sm: 0.75rem
  md: 1.5rem
  lg: 2rem
  xl: 4rem
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
    rounded: "{rounded.md}"
    padding: 12px 32px
  button-primary-hover:
    backgroundColor: "{colors.accent-hover}"
    textColor: "#ffffff"
  button-green:
    backgroundColor: "{colors.green}"
    textColor: "#ffffff"
    rounded: "{rounded.md}"
    padding: 12px 32px
  button-outline:
    backgroundColor: transparent
    textColor: "{colors.accent}"
    rounded: "{rounded.md}"
    padding: 12px 32px
  card:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.text}"
    rounded: "{rounded.lg}"
    padding: "{spacing.md}"
  card-hover:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.text}"
  tag:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
    rounded: "{rounded.sm}"
    padding: 2px 8px
---

## Overview

Telezhky.kz — производитель складских тележек в Казахстане. Индустриальный
тёмный стиль. Никаких градиентов, никаких украшений. Сталь, бетон, функция.

Главный приём: **один акцентный цвет (orange `#f0883e`) на всём сайте**.
Больше никакой цветовой информации. Карточки, кнопки, hover — всё через
этот единственный accent.

## Colors

- **Primary (`#0a0e14`):** Глубокий graphite — фон страницы. Почти чёрный,
  но с лёгким синим отливом чтобы не выглядеть как `#000`.
- **Secondary (`#131820`):** Карточки и приподнятые поверхности.
- **Border (`#2a3040`):** Разделители. На 2px светлее secondary, не более.
- **Text (`#e6edf3`):** Основной текст. Достаточно яркий на `#0a0e14` —
  контраст 14.5:1 (AAA).
- **Text-dim (`#9ba3af`):** Второстепенный текст. Контраст 6.3:1 (AA).
- **Accent (`#f0883e`):** ЕДИНСТВЕННЫЙ цвет для взаимодействия. Кнопки,
  hover-бордеры, теги. Никакой другой цвет не должен использоваться для
  UI-акцентов.
- **Green (`#25d366`):** Только для WhatsApp-кнопок. Не использовать в
  основном UI.
- **Blue (`#58a6ff`):** Только для email-кнопок. Не использовать в основном UI.

## Typography

**Unbounded** — геометричный гротеск с поддержкой кириллицы. Используется
только для заголовков (h1, h2, h3). Жирные начертания (700, 800) —
индустриальный характер без засечек.

Для body — системный sans-serif стек. Никаких дополнительных веб-шрифтов.
Быстро, читаемо, не тратит bandwidth.

Никаких засечек. Это не журнал и не лендинг премиум-класса. Это спецификация
на железо.

## Layout & Spacing

Одна колонка, максимальная ширина 1100px. Отступы по 1.5rem с краёв на
мобильных. Вертикальный ритм — секции по 4rem (`--xl`), gap между карточками
1.5rem (`--md`).

Grid: `repeat(auto-fit, minmax(300px, 1fr))` — карточки сами перестраиваются
под ширину экрана без media queries.

## Components

- **button-primary:** Единственная высокоприоритетная кнопка. Orange фон,
  белый текст. Hover темнеет до `#e8831a`.
- **button-green:** WhatsApp CTA. Только в блоке контактов.
- **button-outline:** Прозрачная с orange обводкой. Для вторичных действий.
- **card:** Приподнятый контейнер. При hover border становится accent-оранжевым
  и карточка поднимается на 2px. Единственная анимация на сайте.
- **tag:** Маленький оранжевый лейбл — «В наличии» / «Под заказ».

## Do's and Don'ts

- ✅ Один accent на весь сайт. Другие цвета — только по функциональной необходимости (WhatsApp зелёный, email синий).
- ✅ Unbounded только для h1/h2/h3. Не использовать в body и кнопках.
- ✅ Никаких градиентов.
- ❌ Не выдумывать новые цвета. Все цвета — из этого файла.
- ❌ Не добавлять иконки-эмодзи в карточки (кроме секции features).
- ❌ Не делать больше одной анимации на странице. Только card hover.
