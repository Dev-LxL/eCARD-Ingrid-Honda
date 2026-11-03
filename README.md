# Ingrid Honda eCARD — Adaptación a estructura LXL v1.2

**Estado:** previsualización de personalización, sin publicación ni cambios en repositorios.

## Origen y criterio
- Base estructural: `Propuesta LXL Tarjeta de presentación.zip` (presentación vertical centrada, identidad, accesos circulares, banner, bloques de información, ubicación y tarjeta para guardar contacto).
- Contenido comercial, marca, enlaces, imágenes y carrusel: `Propuesta HONDA Ingrid.zip` (v1.1).
- La estructura se reinterpretó para Honda sin introducir datos de contacto o marca LXL en la interfaz visible.

## Abrir
Descomprimir y abrir `index.html` en Chrome o Edge. Para pruebas de enlaces, mapa y portapapeles, es preferible usar un servidor local (por ejemplo VS Code Live Server).

## Funciones
- Contacto directo, correo, WhatsApp con mensajes específicos, catálogo y vCard.
- Carrusel con avance automático, flechas, pausa, navegación táctil y detención por preferencia de movimiento reducido.
- Fichas resumidas en diálogo y botón de consulta.
- Google Maps y acceso externo a PayZen; no es una plataforma de cobro.
- Compartir URL sólo si la tarjeta ya tiene una dirección pública.

## Validaciones y límites
- Precios provienen de Ingrid y se muestran como valores informados **sin papeles**. No son una cotización final ni disponibilidad garantizada.
- Algunas fotos están identificadas como referenciales: cotejar variante/color exactos antes de publicación.
- Los rótulos 2027 se basan en información comercial aportada; no se certifica cada unidad.
- La estructura visual y los scripts se inspeccionaron; pruebas de dispositivos físicos y aprobación visual de v1.2 pendientes.
- No genera QR final, pagos, registros ni transmisión de formularios.

## Archivos
`index.html`, `css/style.css`, `js/app.js`, `js/products.js`, `img/`, `QA.md`, `README.md`.


## v1.3 — Correcciones solicitadas
- QR local `img/qr-whatsapp-ingrid.png` escaneable, abre directamente el WhatsApp laboral autorizado (+57 310 474 1193) con un mensaje prellenado. Este QR NO apunta a la URL pública de la eCARD.
- Sustituido el aviso de QR pendiente por imagen, explicación y botón activo.
- Eliminado el ancho máximo global de 1000px del contenedor principal: el sitio aprovecha la anchura disponible. Se conservan límites de longitud de lectura para determinados textos y el tratamiento mobile-first.
- Se preservan diseño Honda/GSM, enlaces, productos, carrusel y recursos originales.
- No hubo publicación, push ni cambios productivos.


## Actualización v1.4 — UX responsive
- Navegación inferior real en teléfonos y tabletas pequeñas (<=767 px).
- Carrusel sin scroll visible, con una tarjeta completa en móviles <=540 px.
- Layouts de 1/2 columnas según ancho; controles táctiles >=44 px.
- Protecciones contra desbordamiento; QR y mapa fluidos.
- Vista horizontal compacta y safe area de móvil.
- La capa responsive se agrega al final de CSS para evitar alteraciones de lógica comercial o contenidos.
- Pendiente aprobación visual antes de cualquier despliegue o push.
