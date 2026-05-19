---
name: Lumen
source_of_truth: ./Mode_1_updated_colors.tokens.json
framework: Astro
styles: Tailwind CSS v4 + CSS Custom Properties
---

# Lumen Design System

Lumen usa los tokens de Figma exportados en `Mode_1_updated_colors.tokens.json` como unica fuente de verdad visual. La landing debe consumir esos tokens desde `src/styles/tokens.css` y evitar valores hardcodeados fuera de ese archivo y del SVG del logo.

## Brand

- Producto: app movil de finanzas personales.
- Tono: claro, directo, practico y orientado a decisiones de ahorro.
- Estetica: luminosa, precisa y ligeramente tecnica, con bordes rectos, tipografia mono para identidad y superficies suaves para lectura.
- Logo: `src/assets/logo.svg`.

## Colors

- Primary: `--color-primary-v1` a `--color-primary-v4`, teal principal para marca, CTAs y fondos suaves.
- Secondary: `--color-secondary-v1` a `--color-secondary-v4`, coral para acentos de conversion y contraste calido.
- Accent 1: `--color-accent1-v1` a `--color-accent1-v4`, amarillo para highlights, rating y ahorro visible.
- Accent 2: `--color-accent2-v1` a `--color-accent2-v4`, rojo suave para alertas no destructivas o enfasis puntual.
- Accent 3: `--color-accent3-v1` a `--color-accent3-v4`, base clara para fondos y superficies.
- Feedback: success, danger, warning e info con cuatro intensidades cada uno.
- Categories: `category_obligacion`, `category_ahorro` y `category_ocio` para comunicar tipos de gasto.
- Base: `--color-base-white` y `--color-base-black`.

## Typography

- Primary font: Red Hat Mono, para logo textual, headlines, labels, numeros y CTAs.
- Secondary font: Inter, para cuerpo, parrafos largos y testimonios.
- Mobile display: `--font-size-mobile-h1-display` y `--font-size-mobile-h2-display`.
- Body: `--font-size-mobile-body-standard`.
- Labels: `--font-size-mobile-label-tech-bold`, uppercase cuando actuan como kicker.
- Line-height: usar aliases `--line-height-tight`, `--line-height-heading`, `--line-height-body` y `--line-height-label`.

## Spacing And Shadow

- Spacing: escala `--spacing-*`, desde `--spacing-px` hasta `--spacing-s32`.
- Container: `--spacing-container`, derivado de `movil.padding_container`.
- Radius: la landing no utiliza `border-radius`; las superficies, botones, cards y placeholders mantienen esquinas rectas.
- Shadow: el JSON no define sombras explicitas; la landing crea aliases `--shadow-sm`, `--shadow-md` y `--shadow-lg` derivados de color tokens con `color-mix`.

## Components

- Buttons: borde visible, esquinas rectas, tipografia mono, minimo tactil de 44px y sombra `4px 4px 1px`.
- Secondary buttons: estilo Figma `218:1900`; fondo `--color-secondary-v1`, borde negro `3px`, sombra `4px 4px 0`, texto blanco mono medium de `12px`, padding `19px 11px` y gap `8px`. El componente permite contenido con icono o solo texto.
- Inputs: borde visible, esquinas rectas, fondo de superficie y la misma sombra `4px 4px 1px` que los botones.
- Cards: estilo Figma `36:554`; fondo blanco, borde negro de `3px`, sombra `4px 4px 0`, padding `30px` horizontal y `17px` vertical, gap `16px`. Las feature cards incluyen banda superior de color con icono Material dentro de una caja blanca con borde negro.
- Badges/labels: mono, uppercase, color secondary.
- Icons: usar Material Design Icons como SVG inline mediante el componente `MaterialIcon`.
- Placeholders de imagen: `div.img-placeholder` con `data-placeholder`, `aspect-ratio`, fondo tokenizado y texto descriptivo.
- Navbar: sticky con backdrop blur, logo SVG y CTA principal.

## Rules

- No usar librerias UI externas.
- No usar React islands salvo interactividad real.
- No usar imagenes de producto inexistentes; representar mockups con placeholders.
- Mantener copywriting orientado a beneficios y sin jerga tecnica.
- Respetar `prefers-reduced-motion` para animaciones.
