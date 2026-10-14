---
title: "Título de la entrada"
date: {{ .Date }}
draft: true # cámbialo a false cuando quieras publicarla
slug: "{{ replaceRE `^\d{4}-\d{2}-` "" .File.ContentBaseName }}"
description: "Resumen de una o dos líneas. Aparece en la lista de artículos y en Google."
# Una o dos categorías de esta lista:
# Hung Gar · Tai Chi · Qigong · Kung Fu y Shaolin · Medicina tradicional
# Salud y ciencia · Filosofía taoísta · Noticias de la escuela · Varios
categories: ["Qigong"]
tags: []
# Imagen opcional para la lista de artículos. Guárdala en static/img/blog/
# y escribe la ruta sin "static/", por ejemplo: "img/blog/postura-del-jinete.webp"
thumbnail: ""
---

Escribe aquí el contenido en Markdown.

## Un subtítulo

Texto normal, **negritas**, *cursivas* y [un enlace](https://ejemplo.com).

![Descripción de la imagen](/img/blog/nombre-de-la-imagen.webp)

