# Tai Chi Kung Fu México

Renovación de [taichikungfumexico.blogspot.com](https://taichikungfumexico.blogspot.com/): sitio en [Hugo](https://gohugo.io/) con el tema [hugo-dpsg](https://github.com/pfadfinder-konstanz/hugo-dpsg) (copiado en `themes/hugo-dpsg`, licencia GPL-2.0), publicado en Vercel al hacer push a `main`.

- `content/blog/` — los posts del blog original (2008–2023), importados con su HTML. Cada uno conserva un alias a su URL de Blogger.
- `data/clases.yaml` — grupos, horarios y cuotas (`confirmado: false` muestra un aviso en la página de clases).
- `layouts/` — ajustes sobre el tema: logo tipo banner, widget de clases, resúmenes en texto plano.
- `static/css/custom.css` — estilos propios.

Desarrollo local:

```bash
hugo server
```
