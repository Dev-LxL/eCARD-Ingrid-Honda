# QA técnico — Ingrid Honda eCARD v1.1
Fecha: 2026-11-03

## Comprobado
- JavaScript: `node --check js/app.js` — PASS.
- Archivos locales y referencias de imágenes y scripts: verificados estáticamente.
- SVG: símbolos y referencias locales cruzados.
- Control de carrusel automático, pausa, flechas, visibilidad, interacción y movimiento reducido: implementado, sin ejecución de navegador acreditada.

## No comprobado / bloqueado
- Chromium bloqueó `file://` con `ERR_BLOCKED_BY_ADMINISTRATOR` durante el intento de ejecución.
- No se acredita QA visual/funcional en 320, 360, 390, 430, 768, 820, 1024, 1280, 1920 px.
- Pendiente comprobar navegación táctil en teléfono físico, foco/modal, `prefers-reduced-motion`, scroll horizontal, uso real de vCard y enlaces externos.

## Estado
Propuesta local de revisión, sin publicación, sin activaciones ni modificaciones de v1.0.
