# Ingrid Lizeth Guerrero — Honda × Grupo Supermotos | eCARD DEMO v1.0

**Estado:** Demostración local. Sin publicación ni backend. Desarrollo independiente inspirado en los patrones de eCARD LXL v3.19; no es una copia literal de la interfaz de LXL.

## Uso
Abrir `index.html` desde una carpeta descomprimida. Para pruebas de URL, mapa y Web Share, ejecutar un servidor local (por ejemplo `python -m http.server 8000`). La tarjeta contiene HTML, CSS y JS independientes y fotos WebP locales. La tipografía Google Fonts y el mapa requieren internet; hay fuentes de reserva.

## Contenido y origen
Nombre, cargo, número +57 310 474 1193, correo ilguerrero@gruposupermotos.com, ubicación y horarios: proporcionados/autorizados por la usuaria. Catálogo: https://wa.me/c/30885294419994. Teléfono laboral para CTAs: +57 310 474 1193; verificar operacionalmente que WhatsApp acepta mensajes en ese número antes de publicar (se indicó autorizado, no se probó envío).

Precios informados por Ingrid al 03/11/2026: X-Blade 160 $10.290.000, CB 125 Hornet $8.290.000, CB 125F DLX $7.100.000, CB 125F STD $6.890.000, CB 100 $5.500.000, sin papeles. Se omitió la denominación CB 125F MAX a $7.030.000 porque no se logró verificar como versión distinta.

Diferencias con Honda: Hornet Honda publica $8.690.000 (diferente de Ingrid); DLX Honda publica $7.050.000 (diferente de Ingrid). Debe aclararse vigencia y condiciones antes de publicación. X-Blade, CB125F STD y CB100 figuran con valores equivalentes a los proporcionados en la web Honda consultada; las fichas CB100 se conservan como información facilitada mientras se verifica la ficha oficial completa. Las imágenes de usuario no están certificadas individualmente como foto de la versión exacta; se etiquetan referenciales.

Fuentes oficiales al 03/11/2026:
- https://motos.honda.com.co/motos-honda/motos-sport/XBLADE-160
- https://motos.honda.com.co/CB-125-Hornet
- https://motos.honda.com.co/CB-125F-DLX-20
- https://motos.honda.com.co/CB-125F-STD-20
- https://motos.honda.com.co/

## Límites
El archivo no crea una URL pública ni un QR. El botón Compartir solo funciona con una URL HTTP/HTTPS. El mapa es una búsqueda de dirección; verificar PIN real antes de publicar. PayZen enlaza a dominio externo facilitado/autorizado, no integra cobros; verificar destinatario de cada pago. No se publica QR de pagos ni certificado bancario. No se afirman promociones, aprobaciones de crédito o existencias.

## QA pendiente
La inspección HTML/CSS/JS y revisión de enlaces en fuente no sustituyen QA real en Chromium. Probar 320/390/430/768/1024/1280/1920 px y landscape, navegación por teclado, imágenes, mapa, carrusel, .vcf, teléfono, WhatsApp, correo, ausencia de errores y desbordamiento. Probar en Android/iPhone antes del cierre. No modificar fuentes ni precios sin conservar referencia de cambio.


## v1.1 — refinamiento de UI y móvil (2026-11-03)
- Copia independiente de la demo v1.0, sin despliegue ni cambios de repositorio.
- Iconografía SVG local y reutilizable para contactos, navegación, fichas, acciones y controles. Ningún emoji/Unicode usado como icono de interfaz. Identidad Honda/GSM original conservada.
- Carrusel automático cada 4,2 segundos, sin barra de scroll visible; bucle entre tarjetas, flechas, deslizamiento táctil y botón Pausar/Reanudar. Pausa durante foco, hover, ventana oculta, diálogo abierto y fuera de pantalla. Con `prefers-reduced-motion: reduce` no comienza reproducción automática.
- Mejoras prioritarias para 320-480 px: tarjetas ancho móvil, botones táctiles, cabecera compacta, navegación inferior con iconos, mapa y diálogo adaptados.
- Sin cambios en modelos, precios, enlaces de contacto, destino WhatsApp ni sección de pagos.
- Nota: enlace de compartir local se desactiva en localhost/127.0.0.1, porque no representa una URL pública compartible.
- Estado: demo para nueva revisión visual. No equivale a aprobación final ni publicación.
