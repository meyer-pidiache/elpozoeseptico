---
title: Guías Simples para Fuwari
published: 2024-04-01
description: "Cómo usar esta plantilla de blog."
image: "./cover.jpeg"
tags: ["Fuwari", "Blogging", "Personalización"]
category: Guías
draft: false
---

> Fuente de la imagen de portada: [Fuente](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/208fc754-890d-4adb-9753-2c963332675d/width=2048/01651-1456859105-(colour_1.5),girl,_Blue,yellow,green,cyan,purple,red,pink,_best,8k,UHD,masterpiece,male%20focus,%201boy,gloves,%20ponytail,%20long%20hair,.jpeg)

Esta plantilla de blog está construida con [Astro](https://astro.build/). Para las cosas que no se mencionan en esta guía, puede encontrar las respuestas en la [documentación de Astro](https://docs.astro.build/).

## Front-matter de las Publicaciones

```yaml
---
title: Mi Primera Publicación de Blog
published: 2023-09-09
description: Esta es la primera publicación de mi nuevo blog de Astro.
image: ./cover.jpg
tags: [Foo, Bar]
category: Front-end
draft: false
---
```

| Atributo      | Descripción                                                                                                                                                                                                |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `title`       | El título de la publicación.                                                                                                                                                                               |
| `published`   | La fecha de publicación de la entrada.                                                                                                                                                                     |
| `description` | Una breve descripción de la publicación. Se muestra en la página de índice.                                                                                                                                |
| `image`       | La ruta de la imagen de portada de la publicación.<br/>1. Comienza con `http://` o `https://`: Usa una imagen web<br/>2. Comienza con `/`: Para una imagen en el directorio `public`<br/>3. Sin ninguno de los prefijos: Relativo al archivo markdown |
| `tags`        | Las etiquetas de la publicación.                                                                                                                                                                            |
| `category`    | La categoría de la publicación.                                                                                                                                                                            |
| `draft`       | Si esta publicación todavía es un borrador, no se mostrará.                                                                                                                                                |

## Dónde Colocar los Archivos de las Publicaciones

Los archivos de sus publicaciones deben colocarse en el directorio `src/content/posts/`. También puede crear subdirectorios para organizar mejor sus publicaciones y activos.

```
src/content/posts/
├── publicacion-1.md
└── publicacion-2/
    ├── portada.png
    └── index.md
```
