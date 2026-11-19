# Web de Pleximar

Una página (`index.html`) más la carpeta `fotos/`. Sin servidor, sin cookies y sin peticiones a otras webs. Se abre con doble clic. Dominio: `https://pleximar.com/`.

## Qué hay
- `index.html`: la web (portada, qué hay dentro, dónde y cuándo con el «cartel» del horario, y aviso legal al pie).
- `fotos/`: la foto de la tienda en varios tamaños y recortes (`tienda`, `tienda-480`, `lamparas`, `flores`; cada una en `.webp` y `.jpg`). **Esta carpeta hay que subirla junto a `index.html`.** Pesan unos 145 KB en total en el móvil.
- `capturas/`: cómo se ve a 360 px, 768 px y 1280 px.
- `referencia/`: el logotipo y la foto original que pasaste. No se publican ni se usan en la página.

Los datos (nombre, dirección, teléfono, horario) son los de la ficha de Google y están escritos igual en el texto visible y en los datos estructurados para Google (bloque `application/ld+json` del `<head>`). Si cambia algo de la ficha, cámbialo en los dos sitios.

El indicador «Abierto ahora / Cerrado ahora» usa un script pequeño con la hora de Madrid. No tiene en cuenta festivos. Si el navegador no ejecuta scripts, no aparece.

## Qué conviene hacer
1. **Logotipo:** la marca de arriba es un dibujo propio en SVG inspirado en el rótulo. Busca en `index.html` el comentario `LOGO:` y sustituye ese bloque por el archivo oficial cuando lo tengas (mejor SVG o PNG grande).
2. **Más fotos:** la foto de la tienda es pequeña (765 px de ancho), así que no se amplía más de lo que da. Con una foto mejor, sustituye los archivos de `fotos/` (mismos nombres) y ajusta `width` y `height` en el HTML. Hay dos huecos preparados, `FOTO FUTURA 1` y `FOTO FUTURA 2`: quita los símbolos `<!--` y `-->` que rodean la línea `<img ...>` y pon el archivo en `fotos/`. Mientras estén comentados no se pintan.
3. **Aviso legal:** hay un comentario `REVISAR con un abogado antes de publicar` justo antes del apartado «Aviso legal» (al final de la página).
4. **Facebook:** solo consta Facebook. No se han puesto Instagram ni WhatsApp.

## Cómo publicarla (gratis, tú decides)
Cuando tengas acceso al dominio `pleximar.com`:
- **Cloudflare Pages:** sube la carpeta (arrastrar y soltar), añade el dominio en el panel y sigue sus pasos.
- **Netlify Drop** (`app.netlify.com/drop`): arrastras la carpeta, te da una dirección y luego añades el dominio propio.
- **GitHub Pages:** crea un repositorio, sube `index.html` y `fotos/`, activa Pages en Ajustes y pon el dominio.
No hace falta subir `referencia/` ni `capturas/`.

Después, pon `https://pleximar.com/` como «Sitio web» en la ficha de Google.
