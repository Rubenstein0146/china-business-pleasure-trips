# China Business & Pleasure Trips

Landing page estática para expediciones ejecutivas B2B entre México y China.

## Publicar en GitHub Pages

En el repositorio, abre **Settings → Pages** y selecciona **Deploy from a branch**, la rama `main` y la carpeta `/(root)`. GitHub Pages publicará `index.html`.

## Formulario de contacto

El formulario envía las solicitudes mediante EmailJS. Antes de que pueda enviar correos:

1. Crea una cuenta en EmailJS y conecta el servicio de correo que recibirá las solicitudes.
2. Crea una plantilla cuyo destinatario (`To Email`) sea `ventas@chinabusinesssolutions.com`, cuyo campo `Reply-To` sea `{{reply_to}}` y cuyo asunto sea `{{subject}}`.
3. En el cuerpo de la plantilla, usa `{{name}}`, `{{company}}`, `{{phone}}`, `{{email}}`, `{{industry}}` y `{{needs}}`.
4. Copia el Service ID, Template ID y Public Key de EmailJS en `assets/email-config.js`, reemplazando los valores `YOUR_EMAILJS_...`.
5. En la configuración de seguridad de EmailJS, limita los orígenes permitidos a `https://rubenstein0146.github.io`.
6. Sube el archivo de configuración actualizado al repositorio y prueba el formulario.

El envío se realiza desde el navegador con la API pública de EmailJS; no pongas una clave privada en el sitio. Mientras los identificadores sigan siendo marcadores de posición, el formulario no intentará enviar la solicitud y mostrará que falta configurar el correo.
