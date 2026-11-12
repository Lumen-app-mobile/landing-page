# Lumen · Landing page

Web de presentación del proyecto **Lumen**, una app móvil que registra tus tickets de compra y, con OCR + IA, te ayuda a controlar en qué gastas. Desde la landing se explica la app y se ofrecen los enlaces de descarga.

## Stack

- [Astro 6](https://astro.build)
- [Tailwind CSS 4](https://tailwindcss.com)

## Estructura

```
landing-page/
└── landing/
    ├── src/
    │   ├── pages/index.astro       # Página principal
    │   ├── layouts/BaseLayout.astro
    │   ├── components/
    │   │   ├── landing/            # Secciones (Navbar…)
    │   │   └── ui/                 # Button, MaterialIcon
    │   ├── styles/                 # global.css y design tokens
    │   └── assets/
    ├── docs/                       # Sistema de diseño y tokens de color
    ├── astro.config.mjs
    └── package.json
```

## Desarrollo

```bash
cd landing
npm install
npm run dev       # http://localhost:4321
npm run build     # genera la web estática en dist/
npm run preview   # sirve el build en local
```

## Despliegue

El build genera una web estática en `landing/dist/`, que se puede publicar en cualquier hosting estático (GitHub Pages, Vercel, Netlify…).

> El archivo `.gitlab-ci.yml` es el pipeline que se usaba para publicar en GitLab Pages cuando el proyecto estaba alojado en GitLab. En GitHub no se ejecuta.

## Proyecto Lumen

| Repo | Descripción |
|---|---|
| [api-main](https://github.com/Lumen-app-mobile/api-main) | API principal (Go) |
| [ocr-processor](https://github.com/Lumen-app-mobile/ocr-processor) | Extracción de datos de tickets con OCR + LLM |
| [mobile-app](https://github.com/Lumen-app-mobile/mobile-app) | App móvil (Expo / React Native) |
| **landing-page** | Web del proyecto (este repo) |
| [docs](https://github.com/Lumen-app-mobile/docs) | Memoria y documentación |
