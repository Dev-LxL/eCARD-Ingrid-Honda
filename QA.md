# QA — Ingrid Honda eCARD LXL v1.4

## Correcciones aplicadas
- Navegación inferior visible y funcional mediante CSS en <=767 px (antes permanecía oculta por `display:none`).
- Carrusel con ancho de tarjeta completo en móviles <=540 px; se conserva JS de avance automático, control de pausa y gestos.
- Contenido, imágenes, QR, mapa, encabezados y botones con anchos fluidos y protección frente a desbordamientos.
- Ajustes de tabletas 768–1024 px y vista horizontal compacta.
- Acciones comerciales, precios y fuentes de imágenes sin cambios.

## Prueba de motor Chromium (3 de noviembre de 2026)
Se ejecutó el DOM real del HTML con CSS inline y JavaScript local insertado mediante Playwright `set_content`, porque el entorno bloqueó la navegación directa a archivos. En esta modalidad se sustituyó el mapa externo por `about:blank` y no se pudieron comprobar como imágenes originales las fotos generadas dinámicamente ni el QR.

| Viewport | Ancho documento / viewport | Navegación inferior | JS exceptions |
|---|---|---|---|
| 320x740 | 320/320 | visible | 0 |
| 390x844 | 390/390 | visible | 0 |
| 768x1024 | 768/768 | oculta, header presente | 0 |
| 1024x768 | 1024/1024 | oculta, header presente | 0 |

En el primer intento apareció un desbordamiento horizontal de 12 px a 320 px causado por un encabezado; se corrigió con partición responsiva y se repitió la prueba, resultado PASS. Anteriormente se midieron también 360, 430, 540, 820, 1280, 1920 y orientación horizontal sin desbordamiento, pero fue antes de la última corrección y requiere regresión final.

## Pendientes que NO se declaran PASS
- Comprobación manual en Android/iOS, Safari y tabletas reales.
- Validación visual y carga de imágenes con Live Server, QR escaneado con cámara y Google Maps conectado.
- Pruebas funcionales reales de WhatsApp, descarga vCard, diálogo de fichas, navegación táctil y bucle automático tras varios ciclos.
- Zoom 200%/400%, lectores de pantalla y auditoría WCAG completa.
- Aprobación visual del cliente y publicación.

No se realizaron operaciones en GitHub, Pages o servicios externos.
