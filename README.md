# China Business & Pleasure Trips

Landing page estática para expediciones ejecutivas B2B entre México y China.

## Publicar en GitHub Pages

En el repositorio, abre **Settings → Pages** y selecciona **Deploy from a branch**, la rama `main` y la carpeta `/(root)`. GitHub Pages publicará `index.html`.

## Formulario de contacto

El formulario envía solicitudes mediante EmailJS. Los IDs del servicio, la plantilla y la clave pública ya están configurados en `assets/email-config.js`. La clave pública está diseñada para uso en el navegador; nunca agregues la clave privada.

En EmailJS, confirma que la plantilla `Contact Us` tenga como destinatario (`To Email`) `ventas@chinabusinesssolutions.com`, `{{email}}` como Reply-To y `{{title}}` como asunto. La plantilla usa `{{name}}`, `{{empresa}}`, `{{email}}`, `{{telefono}}`, `{{expedicion}}`, `{{message}}` y `{{time}}` en el contenido. El formulario envía los nombres que la plantilla espera, junto con alias equivalentes en inglés. En la configuración de seguridad, limita los orígenes permitidos a `https://rubenstein0146.github.io`.

El envío se realiza desde el navegador mediante la API de EmailJS. El formulario muestra confirmación solo si la API acepta la solicitud; un error de EmailJS se muestra como fallo y conserva los datos para poder reintentar.
