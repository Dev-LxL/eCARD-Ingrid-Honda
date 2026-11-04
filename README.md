# eCARD Ingrid Honda · LXL v1.5.1 — DEMOSTRACIÓN

Base: v1.4 responsive. Mantiene los componentes aprobados y actualiza diez motocicletas, imagen de CB 125 Hornet en hero, catálogo PDF local y tres medios de pago. No se publica ni modifica GitHub.

## Abrir
Abrir `index.html` o usar Live Server. El catálogo `docs/catalogo-honda-ingrid.pdf` abre en una pestaña nueva. Las imágenes principales apuntan a las URLs aportadas; si alguna falla, se muestra un respaldo local extraído del catálogo suministrado. La foto externa puede diferir del color del respaldo local.

## Pagos
Cuenta corriente Bancolombia de Grupo Supermotos SAS, dato reproducido del certificado recibido. El certificado bancario completo se mantiene fuera del ZIP para minimizar exposición de información documental. Foto de QR Bancolombia/Redeban aportada, sin modificación; escaneo real y tope anunciado de $3.000.000 COP pendientes de comprobación operativa. Enlace PayZen externo. No hay procesamiento local ni comprobación de pagos.

## Criterio de fichas
Cilindraje, potencia, torque y frenos comparados con las fichas oficiales donde existen. Los diez precios visibles en el carrusel y sus fichas son exclusivamente los valores comerciales autorizados por Ingrid Lizeth Guerrero. Nunca se sustituyen automáticamente por cifras de Honda Colombia ni de distribuidores. Las eventuales diferencias con precios externos se registran solo en QA documental, no se incorporan como precios alternativos en la tarjeta. Los valores se expresan en COP y excluyen matrícula y gastos de papeles; no se declara inventario disponible ni precio final.

## Siguientes decisiones
Aprobación visual y pruebas físicas de QR de pago, catálogo, galería e interacciones. Validar permisos de redistribución de imágenes externas y confirmar correspondencia exacta de color/modelo. No habilitar despliegue sin nueva autorización.

## Ajuste v1.5.1
Se conservaron los diez precios de Ingrid sin cambios numéricos y se unificó la aclaración comercial de cara al comprador. Sin cambios en los PDFs, QR, imágenes, pagos o destino de enlaces.

## v1.6 — tarjetas y modales de pago
- Las tres opciones de pago se presentan en tarjetas compactas con iconografía SVG.
- Cuenta Bancolombia: PDF autorizado disponible en `docs/certificacion-bancolombia-grupo-supermotos.pdf`, con vista integrada y enlaces para abrir/descargar. **Este PDF será públicamente descargable si se publica el sitio**.
- QR Bancolombia/Redeban: original sin alterar en vista ampliada; escaneo real pendiente.
- PayZen: explicación y enlace externo, sin procesamiento local.
- Modales con cierre por Escape, botón y clic en fondo, y recuperación de foco.
- No se ha publicado en GitHub.

## v1.7 — imágenes ampliables y texto comercial
- Sustituido el aviso de precios por la redacción exacta aprobada.
- Las diez fotografías del carrusel se amplían al seleccionar la imagen o el icono de lupa.
- El visor usa la imagen cargada realmente (remota o respaldo local), permite cerrar con X, Escape o el fondo, recupera el foco y pausa el carrusel.
- No se alteraron precios, enlaces de contacto, fichas ni medios de pago.

## v1.8 — Modales de pago compactos
- Se elimina el scroll del contenedor externo de los tres modales en pantallas de altura normal. El PDF mantiene desplazamiento propio necesario para leer el documento.
- PayZen adapta anchura y altura al contenido, sin relleno vertical.
- QR ajusta su tamaño a la altura del dispositivo.
- En alturas muy bajas se permite desplazamiento accesible para no ocultar acciones.
- Sin cambios en motos, precios, enlaces, PDFs, QR y la restante UI.

## v1.9 — Cierre sin datos duplicados
- Retirados teléfono y correo visibles únicamente del bloque rojo de contacto final.
- Conservados enlaces del encabezado/accesos rápidos, WhatsApp, vCard y QR.
- No se ha publicado en GitHub.

## Ajuste v1.12 — Crédito profesional
Se reemplazó exclusivamente la etiqueta de previsualización del footer por el crédito © 2026 de Lina Lizeth Londoño Marín. No se modificaron contactos, enlaces, pagos ni catálogo. Pendiente aprobación visual en móvil.

## Ajuste v1.12
- Se invirtió la composición de la sección “Asesoría que te acompaña”: el texto descriptivo queda a la izquierda y el titular principal a la derecha.

## v1.12 — Asesoría + video
La sección de asesoría conserva íntegros el encabezado y la descripción, agrega CTA WhatsApp e iframe de YouTube (modo de privacidad mejorada) 16:9, con enlace alternativo. Requiere conexión y permiso de inserción del autor; no se garantiza reproducción si YouTube la bloquea. Diseño 55/45 desktop y apilado en móvil.


## v1.16 — Revisión responsive y galería
- Fotografías locales de los diez modelos como fuente inicial, para evitar depender de imágenes externas al presentar las tarjetas.
- Retiradas de la vista pública las notas técnicas sobre origen y respaldo de fotos. Se conserva “Fotografías de referencia” en el aviso general.
- Visor de imágenes ampliadas y carrusel automático con controles existentes, manteniendo precios y fichas.
- Revisión de móvil/tableta/PC documentada en QA.md.
- Sin publicación automática ni modificación del repositorio.


## Corrección v1.16
Se corrigió el orden DOM: el diálogo de fotografías se declara antes de `js/app.js`. El error anterior interrumpía la inicialización de los botones del carrusel, el visor y las fichas.

## v1.16 — Galería de mejor resolución
- Las 10 fotografías del carrusel cargan primero los enlaces originales facilitados por Ingrid (Honda Colombia, Grupo Supermotos, Honda México o los sitios de referencia indicados).
- Si falla una imagen externa, se muestra la fotografía local existente de esa moto, sin presentar una imagen ajena.
- El zoom amplía la imagen que se haya cargado. No interpola artificialmente los archivos pequeños.
- **Dependencia:** para calidad alta sin conexión, es necesario disponer de archivos originales de mayor resolución en `img/`. Los recursos de las webs externas pueden cambiar o bloquear solicitudes.
- Los precios, fichas, orden de modelos, pagos, PDF y botones no se alteraron.


## Ajustes v1.16
- Se retiró de la interfaz de fichas técnicas cualquier enlace visible a Honda; la conversión queda dirigida a Ingrid.
- XR 150L 2.0 y XR 190L 2.0 ahora usan recursos locales separados para tarjeta y ampliación (`-card` y `-zoom`).
- El modal de ampliación prioriza la imagen local de zoom cuando existe.

## v1.17 — selección fotográfica XR
- XR 190L 2.0 y XR 150L 2.0: se priorizan las URL de miniaturas de Google suministradas por el cliente, tanto en tarjeta como zoom.
- Si falla el recurso de Google, se usa el archivo local anterior. Los archivos locales de zoom fueron ampliados digitalmente a partir de miniaturas; no son originales HD.
- No se pudieron descargar ni inspeccionar las dos nuevas imágenes en este entorno. La resolución y fidelidad de estas referencias quedan **pendientes de validación**.
- Los precios, fichas y CTA a Ingrid no se modificaron.


## Actualización v1.18 — XR seleccionadas por Ingrid
- XR 150L 2.0: fotografía lateral roja Mundo Honda Costa Rica (URL de 1400 px) en tarjeta y zoom.
- XR 190L 2.0: fotografía lateral roja Mundo Honda Costa Rica (URL de 1400 px) en tarjeta y zoom.
- No se descargaron las imágenes de Mundo Honda; son recursos externos y necesitan red. Las imágenes locales anteriores se conservan únicamente como respaldo.
- Las imágenes de Costa Rica son referencias visuales aportadas por la clienta; debe cotejarse la versión de venta colombiana antes de afirmar equivalencia exacta.
- Sin cambios en precios, cotización, fichas, botones, catálogo o pagos.
