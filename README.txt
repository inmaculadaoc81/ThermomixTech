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
