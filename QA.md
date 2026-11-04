# QA · Ingrid eCARD v1.5.1 (3 noviembre 2026)

## Comprobación documental
- 10 modelos en `js/products.js`; fuentes técnicas oficiales enlazadas en fichas.
- PDF catálogo original integrado en docs y dos páginas disponibles.
- Certificado bancario completo excluido. Datos públicos de cuenta limitados a titular y número por petición del cliente.
- QR original de pago integrado; no se ha validado escaneo físico, beneficiario, ni límite operativo de 3 millones.
- Banner CB125 Hornet con imagen externa indicada y respaldo local del catálogo.
- Enlaces PayZen y WhatsApp no realizan cobros en el propio sitio.

## Diferencias y verificaciones
- CB190R 2.0: Ingrid 12.590.000; Honda Colombia 12.790.000.
- CB125 Hornet: Ingrid/Grupo Supermotos 8.290.000; Honda Colombia 8.690.000.
- PCX 160, DIO DLX, XR150L, CB125F y CB100 coinciden en precio anunciado por Honda consultado.
- BIZ 110: Honda confirma 109,1 cc / 8,23 HP / 8,59 Nm (no extrapolar ficha de versiones previas).
- XR190L: Honda informa 184 cc en resumen / 184,43 cc en descripción; usar 184 cc como dato editorial y conservar advertencia.
- CB190R: prevalece ficha Honda Colombia sobre ficha mexicana para el mercado colombiano.
- X-Blade 13,7 HP comunicado por Ingrid; si no aparece en fuente oficial citada, no presentarlo como verificado.

## Pendientes visuales/funcionales
- Ejecutar Chromium responsive: 320, 390, 430, 768, 1024, 1280, 1920, y landscape; prueba de teclado y sin JS errors.
- Escaneo físico QR Bancolombia; confirmar beneficiario y autorización de límite de pago.
- Abrir y descargar PDF catálogo en móvil real.
- Verificar que recursos remotos permitan acceso estable y uso autorizado.

## Ejecución Chromium en este entorno
- Se intentó Chromium headless en 390 px, pero terminó con un error fatal del subsistema GPU antes de generar captura. No se declara PASS visual.
- Pruebas estáticas de rutas internas y sintaxis JS correctas; pendientes las pruebas de navegador reales.

## Control de precios v1.5.1
- PASS estático: 10/10 nombres y valores de `js/products.js` coinciden con lo autorizado por Ingrid.
- Las divergencias frente a terceros permanecen documentadas aquí únicamente para trazabilidad; no alteran la tarjeta pública.
- Aclaración comercial visible actualizada en `index.html`.
- Sigue pendiente prueba en navegador/dispositivo físico, igual que v1.5.

## v1.6 — checklist de pagos
- PASS estático: 3 tarjetas y botones con SVG.
- PASS estático: certificado PDF copiado a `docs/`, archivo QR conservado y enlace PayZen preservado.
- PASS estático: scripts y rutas locales verificables; pendiente ejecución del navegador, lectores de pantalla y escaneo QR real.
- Riesgo operativo: el certificado bancario será accesible públicamente una vez publicado el sitio; la autorización comercial fue comunicada por la usuaria.
- Chromium: prueba automatizada intentada para 320/390/768/1024/1280 px, bloqueada por `net::ERR_BLOCKED_BY_ADMINISTRATOR` al abrir `file://`. No se afirma PASS visual ni de interacción de los modales.

## v1.7 — controles
- PASS estático: texto comercial exacto reemplazado.
- PASS estático: visor accesible único; botones de ampliar en cada producto; conserva fallback de fotografía.
- Prueba visual y táctil real por dispositivo pendiente.

## v1.8 — Alcance QA
- Ajustes CSS por tipo de modal (bank, qr, pse) y selección JS verificados estáticamente.
- La barra interna del visor PDF puede permanecer por ser funcional al documento.
- El desbordamiento del modal en pantallas de altura muy reducida permite scroll como alternativa de accesibilidad.
- Pendiente prueba en móviles físicos y navegadores alternativos.

## v1.9 — QA estático
- PASS: retirado bloque `contact-links` del cierre rojo.
- PASS: enlaces `tel:` y `mailto:` permanecen en accesos rápidos.
- PASS: WhatsApp, vCard y QR permanecen sin modificaciones.
- Pendiente: inspección visual en navegador y dispositivos.

## v1.12 — Pie de página
- PASS estático: crédito profesional presente una vez y texto anterior retirado.
- PASS estático: reglas CSS de ajuste en móvil presentes.
- Pendiente: comprobación visual en navegador y móvil físico.

## Ajuste v1.12
- PASS estático: orden del contenido invertido en la sección de introducción comercial.
- Sin cambios funcionales en carrusel, pagos, catálogo o contacto.

## v1.12 — video asesoría
- PASS estático: conservación del texto, enlace WhatsApp y video embebido identificado wDXr_xRylkU.
- Prueba externa real de reproducción: pendiente; sujeta a YouTube y conexión del visitante.
- Se conserva el enlace alternativo «Ver en YouTube».


## QA adicional — v1.16 (2026-11-03)
**Entorno:** Chromium headless con HTML, CSS, JS y fotos locales incorporados en una copia de prueba autocontenida. El servidor local HTTP fue bloqueado por el entorno y se sustituyó solo para esta prueba; la entrega mantiene archivos independientes.

- **PASS**: 10 modelos y 10 fotografías locales en el carrusel. Las 10 imágenes cargaron con `loading=eager` durante la comprobación; en producción mantienen carga diferida.
- **PASS**: zoom de fotografía abre `dialog`, muestra fotografía real cargada y se cierra; se observó apertura a 320, 390, 768, 1024 y 1920 px.
- **PASS**: avance automático a 390 px, `scrollLeft` 0 → 370 después de 5,1 s, siguiente manual 370 → 740. El carrusel se pausa al enfocar/interactuar o abrir un modal, por diseño.
- **PASS**: sin desbordamiento horizontal (`documentElement.scrollWidth == innerWidth`) ni errores JS a 320, 390, 768, 1024, 1920 px.
- **PASS estático**: los 10 precios suministrados por Ingrid, destinos internos existentes, JS válido, documentos PDF presentes y ausencia de notas técnicas visibles de fotografías en tarjetas.
- **No verificado**: funcionamiento del embed de YouTube, QR bancario con app real, pagos externos, enlaces en equipos de usuario, Safari/iOS, lectores de pantalla y todas las interacciones de modales de pago desde un sitio publicado.
- **Pendiente antes de publicación**: revisión visual humana en teléfono y tablet físicos y comprobación comercial de contenido, imagen por modelo y destino real del QR.


## Corrección v1.16
Se corrigió el orden DOM: el diálogo de fotografías se declara antes de `js/app.js`. El error anterior interrumpía la inicialización de los botones del carrusel, el visor y las fichas.

## Prueba funcional corregida — 2026-11-03
- Causa raíz: `#photo-viewer` estaba definido después de `js/app.js`; la suscripción a `#photo-viewer-close` lanzaba una excepción al iniciar, interrumpiendo el resto de listeners.
- Chromium autocontenido a 320 px: diez tarjetas cargadas, sin desbordamiento horizontal, cero errores JS, pausa activa, Siguiente 0→308 px, Anterior 308→0 px, zoom abre/cierra y ficha abre/cierra. PASS.
- Chromium autocontenido en escritorio (prueba puntual anterior): Siguiente, Anterior, zoom y ficha responden. PASS funcional parcial.
- La corrida de todos los anchos se interrumpió por tiempo límite; no declararlos PASS en este parche. Pendiente QA Live Server, otros anchos y dispositivos reales.
- El paquete no ha sido desplegado ni subido a GitHub.

## v1.16 — Control de imágenes
- PASS estático: diez URLs remotas presentes y fallback local para diez modelos.
- PASS estático: scripts incluyen manejo de errores para miniaturas y visor.
- PASS estático: precios de Ingrid no modificados y diez modelos conservados.
- PENDIENTE: comprobar descarga efectiva y resolución natural de las 10 imágenes externas en el navegador conectado a Internet.
- PENDIENTE: validar zoom y fallback en móvil real; recurso de Honda Colombia puede responder diferente según navegador/red.
- No se certifican 10 imágenes en calidad alta offline; los originales adjuntos son en varios casos miniaturas de baja resolución.


## QA adicional v1.16
- Verificado: las fichas de producto ya no muestran botón ni enlace visible a Honda.
- Verificado: XR 150L 2.0 y XR 190L 2.0 abren ampliación desde archivo local dedicado de mayor tamaño.

## QA v1.17
- PASS estático: ambas URL aportadas están asociadas al modelo correcto en `products.js`.
- PASS estático: el visor acepta URL HTTPS o ruta local y conserva fallback local.
- PENDIENTE: verificar carga HTTP, resolución real, nitidez y versión exacta de ambas fotos. Las URL `encrypted-tbn0.gstatic.com` pueden ser miniaturas de baja resolución.
- PENDIENTE: interacción en navegador con recursos externos. No se declara calidad HD.


## QA v1.18 — cambio de imágenes XR
- PASS estático: ambas motos apuntan a sus nuevas URL de Mundo Honda para tarjeta y zoom, con correspondencia de modelo según los nombres aportados.
- PASS estático: archivos locales de respaldo disponibles.
- PASS estático: diez precios y textos de contacto conservados.
- PENDIENTE: descarga efectiva, dimensiones/resolución real, respuesta HTTP y permisos de carga desde navegador. El entorno no pudo resolver el dominio de origen.
- PENDIENTE: verificación visual y de zoom en Live Server con conexión a Internet, y correspondencia exacta de variante Colombia.
