THERMOMIXTECH ONE PAGE

Dominio:
https://reparacionderobotcocina.com.es/
(este es el repositorio original de Madrid, del que partió una copia
para crear ThermomixRepair Valladolid, repo ThermomixValladolid. Ese
repo usaba este mismo dominio por error; el cliente confirmó que su
dominio real es reparacionrobotcocina.es, distinto a este. El dominio
de este repo -Madrid- es correcto y no se ha tocado. Sin colisión con
ningún otro dominio revisado en esta sesión.)

Teléfono caja y botones:
+34 910 05 24 89

Diagnóstico:
GRATUITO

Mensaje de rapidez:
Podemos reparar tu Thermomix en 2 h, según la avería.

Modelos:
- TM21
- TM31
- TM5
- TM6
- TM7: SOLO cambio de cuchilla

Incluye:
- Logo suministrado
- Favicon/isotipo adaptado
- WhatsApp 24/365
- Recogida
- Atención telefónica
- Google Business
- YouTube
- Cal.com
- Formulario SMTP
- Chatbot n8n con posiciones y z-index consolidados
- Mapa
- SEO One Page

Variables SMTP compartidas en Vercel:
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada únicamente en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo no aparece visible en la web; solo se utiliza en /api/contacto.

Google Analytics:
G-K4XP2RLCZN

HISTORIAL: el repositorio era multipágina (5 páginas /modelos/ de
TM21/TM31/TM5/TM6/TM7 y varias páginas /servicios/) y se convirtió a
one-page; esas páginas fueron eliminadas en commits anteriores. Como
ya no existen en el sitemap actual, se ha añadido middleware.mjs para
redirigir (301) cualquier URL antigua a la home, evitando 404 en
enlaces indexados o backlinks antiguos. Excluye /api/* y cualquier
ruta con extensión de archivo. Se añadió "@vercel/functions": "^2.0.3"
a package.json como dependencia de esta función.

REVISIÓN (fixes aplicados en esta pasada):
- Ya estaba bien: banner de cookies (ya corregido en un commit
  anterior), schema.org LocalBusiness completo (con areaServed y
  sameAs), sección SEO, menú móvil, borde blanco del chat,
  api/contacto.js con SMTP + nodemailer, dominio ya en https. No se ha
  modificado ninguno de estos.
- Google Analytics: no existía. Añadido G-K4XP2RLCZN.
- .navcall: el texto largo ("Atención Telefónica 24 horas 365 días")
  deformaba la píldora del menú. Acortado a solo el número (mismo
  número, +34 910 05 24 89) y añadido white-space:nowrap como
  salvaguarda.
- H1 de portada reescrito, corto, directo y totalmente afirmativo
  (sin interrogación ni condicionales), incluye la marca: "Tu
  Thermomix no funciona. Aquí la dejamos como nueva." Tamaño del H1
  aumentado: clamp(38-56px) → clamp(46-74px) en escritorio, 40px →
  48px en móvil.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- H1 repetía la plantilla "no funciona. Aquí la dejamos como nueva."
  Reescrito con síntoma específico: "Tu Thermomix no calienta o no
  gira. La reparamos." (9 palabras).
- BUG REAL — dos textos decorativos sin reducción de tamaño en móvil
  (mismo patrón que MedionTech/AsusTech/BoschTech): ".models::after"
  ("THERMOMIX", 165px) y ".fast-art::before" ("2 h", 160px), que en
  pantallas pequeñas se verían enormes/cortados. Añadida reducción en
  tablet (100px) y móvil (64px) para ambos.
- El aviso de servicio independiente solo estaba en letra pequeña del
  footer. Añadida la franja destacada bajo el menú, igual que en el
  resto de la familia.
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- Enlace de política de privacidad: la casilla existía pero sin
  enlace. Añadido a https://kelatos.com/privacy-policy/, en azul y
  subrayado.
- Botón "Atención Telefónica..." sin icono, a diferencia del de
  WhatsApp. Añadido.
- Formulario verificado: fetch a /api/contacto coincide con
  api/contacto.js; conexión correcta.

REVISIÓN ADICIONAL (a petición del cliente):
- Quitadas de la caja de información las filas "Servicio" y
  "Diagnóstico" (ambas redundantes con lo ya mostrado en el hero, la
  insignia "✓ Diagnóstico gratuito" y otras secciones de la página).
- Quitada la etiqueta "TM21 · TM31 · TM5 · TM6 · TM7" (.hero-note)
  del hero.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente — repo 21/48):
- BUG REAL — enlace de Cal.com desactualizado. Actualizado a
  https://cal.com/kelatos/30min?embed=true&theme=light&attendeePhoneNumber=%2B34&overlayCalendar=true.
- Verificado: el correo soporte@kelatos.com no aparece visible.
- BUG REAL — el mensaje prellenado de WhatsApp decía "¡Hola Kelatos!".
  Corregido a "¡Hola ThermomixTech!".
- Verificado: el menú móvil ya se cerraba correctamente al pulsar un
  enlace.
- Verificado: sin iconos ni imágenes con proporciones fijas
  incorrectas.
- Verificado: el H1 en móvil ya está en 48px.
- BUG REAL — botones del hero (.cta) con border-radius de 16px y sin
  estado hover. Aumentado a border-radius:999px; añadido
  filter:brightness(.88) en wa/pickup (colores sólidos) y relleno
  sólido con var(--deep) + texto blanco en el botón de teléfono
  (estilo contorno) al pasar el ratón.
- Verificado: la franja de insignias (.badges-strip) ya estaba
  correctamente ubicada fuera del hero, debajo de él. Cambiado su
  layout de flex-wrap a grid de 4 columnas en escritorio y 2 en móvil
  (mismo patrón aplicado en DyFix/DysonValladolid), en vez de dejar
  las píldoras envolver libremente.

REVISIÓN ADICIONAL (nueva regla de menú móvil, a petición del cliente):
- BUG REAL — la franja de aviso de independencia estaba dentro de
  <header>. Movida fuera de <header>, como hermana justo después de
  él y antes del hero: sigue siendo la misma franja amarilla de ancho
  completo.
- Verificado: el header (.header{position:sticky;top:0}) ya se
  mantenía fijo/pegado arriba al hacer scroll; no requería cambios.
- Verificado de nuevo: el checklist de 7 puntos y la franja de
  insignias reubicada ya estaban aplicados de pasadas anteriores; no
  requerían cambios.
