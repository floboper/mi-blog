## Contexto rápido

Este repositorio es un blog estático muy simple. Archivos clave en la raíz:

- `index.html.txt` — página principal (en el repo tiene sufijo `.txt`).
- `style.css.txt` — estilos globales.
- `script.js.txt` — JavaScript mínimo.
- `README.md` — descripción mínima del proyecto.

Nota: los archivos están guardados con sufijo `.txt` en este workspace; al desplegar/usar, los nombres esperados son `index.html`, `style.css` y `script.js`.

## Arquitectura y flujo de datos

- Proyecto sin backend: HTML estático, CSS y JavaScript de cliente.
- Estructura del DOM relevante: `main > article` para entradas del blog; `header` y `footer` están en la raíz del `body`.
- Flujo simple: `index.html` carga `style.css` en el `head` y `script.js` al final del `body`. El JS usa `DOMContentLoaded` para inicialización (ver `script.js.txt`).

## Convenciones y prácticas observables

- Idioma: HTML usa `lang="es"` — mantener textos y meta cuando añadas contenido.
- Meta y accesibilidad: el `head` incluye `meta charset="UTF-8"` y `meta viewport` — conserva estas etiquetas al editar.
- Nombres y rutas: los recursos son relativos y residen en la raíz. No hay bundler ni subcarpetas por defecto.
- Estilos globales: `style.css` contiene estilos para `body`, `header`, `footer`, `main` — prefiera reglas globales simples antes que CSS complejo.

## Ejemplos concretos (copiar/usar)

- Inicializar JS: en `script.js.txt` se usa:

  - `document.addEventListener("DOMContentLoaded", () => { /* init */ });`

- Estructura HTML de un post (en `index.html.txt`):

  - `<main><article><h2>...</h2><p>...</p></article></main>`

- Enlaces a recursos:

  - `<link rel="stylesheet" href="style.css">`
  - `<script src="script.js"></script>`

## Flujo de desarrollo / debug

- No hay paso de build: para probar localmente abre `index.html` en un navegador.
- Recomendación práctica: usa la extensión Live Server (VS Code) o arrastra `index.html` al navegador para ver cambios en vivo.
- Depuración: usar las DevTools del navegador; la inicialización usa `DOMContentLoaded` y suele registrar `console.log("Blog cargado correctamente.")`.

## PR / cambios rápidos — checklist mínimo

1. Mantener `meta charset` y `viewport` en `head`.
2. Verificar que `lang="es"` sigue presente si se editan textos.
3. Actualizar el pie de página si cambias el año/autor en `index.html.txt` (hay `© 2025 Fernando`).
4. Mantener rutas relativas a `style.css` y `script.js` o documentar si las mueves.
5. Probar en navegador y verificar consola por errores JS.

## Integraciones y dependencias

- Actualmente no hay dependencias externas ni servicios (no hay package.json, build tools ni APIs externas). Cualquier integración nueva debe documentarse en `README.md` y reflejarse en estas instrucciones.

## Dónde mirar para entender cambios futuros

- Contenido principal: `index.html.txt`, `script.js.txt`, `style.css.txt`.
- Documentación del repo: `README.md` (muy breve — actualizar si se añaden pasos de build/despliegue).

## Qué espero del agente

- Hacer cambios que respeten la sencillez del proyecto (sin añadir herramientas sin necesidad).
- Usar las rutas relativas y las convenciones de archivos actuales.
- Si propones añadir CI, build, o frameworks, describe el cambio en un issue y propón una migración paso a paso.

Si quieres, ajusto el archivo (por ejemplo añadir pasos de despliegue a GitHub Pages, o un pequeño `package.json` para añadir herramientas) — dime qué prefieres y lo adapto.
