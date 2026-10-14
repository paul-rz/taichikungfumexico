# Tai Chi Kung Fu México

Renovación de [taichikungfumexico.blogspot.com](https://taichikungfumexico.blogspot.com/): sitio en [Hugo](https://gohugo.io/) con el tema [hugo-dpsg](https://github.com/pfadfinder-konstanz/hugo-dpsg). Vercel lo publica en https://taichikungfumexico.vercel.app cada vez que se hace push a `main`.

## Carpetas

| Carpeta / archivo | Qué contiene | ¿Se edita a mano? |
|---|---|---|
| `content/blog/` | Las entradas del blog. Las importadas de Blogger son `.html`; las nuevas, `.md`. | **Sí**: aquí van las entradas nuevas |
| `content/*.md` | Páginas fijas: `_index.md` (inicio), `sifu-efren.md`, `fundamentos.md`, `clases.md`, `contacto.md` | Sí |
| `data/clases.yaml` | Grupos, horarios, cuotas y teléfono. Con `confirmado: false` la página de clases muestra un aviso. | Sí |
| `static/img/` | Imágenes del sitio (logo, emblema, foto del Sifu) | Sí, para agregar imágenes |
| `static/img/blog/` | Imágenes de las entradas nuevas | Sí |
| `static/css/custom.css` | Estilos propios del sitio | Solo para cambiar el diseño |
| `archetypes/blog.md` | Plantilla que se copia al crear una entrada nueva | Rara vez |
| `layouts/` | Ajustes a las plantillas del tema (logo, widget de clases, resúmenes) | No |
| `themes/hugo-dpsg/` | El tema, copiado tal cual (licencia GPL-2.0) | No |
| `hugo.toml` | Configuración: título, menú, colores, barra lateral | Rara vez |
| `vercel.json` | Cómo Vercel construye el sitio (versión de Hugo) | No |

`public/`, `resources/` y `.vercel/` los generan Hugo y Vercel; están en `.gitignore`.

## Agregar una entrada al blog

1. Desde esta carpeta, crea la entrada (el nombre empieza con año y mes; lo que sigue será la URL):

   ```bash
   hugo new content blog/2026-10-postura-del-jinete.md
   ```

   Se crea `content/blog/2026-10-postura-del-jinete.md` con todos los campos listos. También puedes copiar ese archivo a mano en Obsidian.

2. Llena el encabezado (entre las líneas `---`):
   - `title`: el título.
   - `description`: una o dos líneas de resumen.
   - `categories`: una o dos de la lista que viene en la plantilla.
   - `tags`: opcional, por ejemplo `["postura", "básicos"]`.
   - `thumbnail`: opcional, imagen para la lista de artículos.
   - `draft: false` cuando quieras publicarla (con `true` no aparece en el sitio).

3. Escribe el contenido en Markdown debajo del encabezado.
   - **Imágenes:** guárdalas en `static/img/blog/` (de preferencia `.webp` o `.jpg`, máximo ~1600 px de ancho) y enlázalas así: `![Descripción](/img/blog/nombre.webp)`
   - **Videos de YouTube:** escribe el shortcode `youtube` entre `{{<` y `>}}` con el ID del video (lo que va después de `v=` en la URL), por ejemplo: `{{< youtube mFDoaoCxwME >}}`

4. Revisa cómo se ve (el `-D` muestra también los borradores):

   ```bash
   hugo server -D
   ```

   y abre http://localhost:1313

5. Publica:

   ```bash
   git add -A
   git commit -m "Nueva entrada: Postura del jinete"
   git push
   ```

   Vercel la publica en uno o dos minutos en `https://taichikungfumexico.vercel.app/blog/2026/10/postura-del-jinete/`.

## Desarrollo local

```bash
hugo server
```
