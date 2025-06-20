---
title: Ejemplo de Markdown
published: 2023-10-01
description: Un ejemplo simple de una publicación de blog en Markdown.
tags: [Markdown, Blogging, Demo]
category: Ejemplos
draft: false
---

# Un encabezado h1

Los párrafos se separan por una línea en blanco.

Segundo párrafo. _Cursiva_, **negrita** y `monoespaciado`. Las listas de elementos se ven así:

- este
- aquel
- el otro

Nótese que --- sin considerar el asterisco --- el contenido de texto real comienza con una sangría de 4 columnas.

> Las citas en bloque se
> escriben así.
>
> Pueden abarcar múltiples párrafos,
> si lo desea.

Use 3 guiones para un guion largo (em-dash). Use 2 guiones para rangos (ej., "está todo en los capítulos 12--14"). Tres puntos ... se convertirán en puntos suspensivos. Se admite Unicode. ☺

## Un encabezado h2

Aquí hay una lista numerada:

1. primer elemento
2. segundo elemento
3. tercer elemento

Nótese de nuevo cómo el texto real comienza con una sangría de 4 columnas (4 caracteres desde el lado izquierdo). Aquí hay un ejemplo de código:

    # Déjame reiterar ...
    for i in 1 .. 10 { do-something(i) }

Como probablemente adivinó, con una sangría de 4 espacios. Por cierto, en lugar de indentar el bloque, puede usar bloques delimitados, si lo prefiere:

```
define foobar() {
    print "¡Bienvenido al país del sabor!";
}
```

(lo que facilita copiar y pegar). Opcionalmente, puede marcar el bloque delimitado para que Pandoc lo resalte sintácticamente:

```python
import time
# ¡Rápido, cuenta hasta diez!
for i in range(10):
    # (pero no *demasiado* rápido)
    time.sleep(0.5)
    print i
```

### Un encabezado h3

Ahora una lista anidada:

1. Primero, consiga estos ingredientes:

    - zanahorias
    - apio
    - lentejas

2. Hierva un poco de agua.

3. Vierta todo en la olla y siga este algoritmo:

        encontrar cuchara de madera
        destapar la olla
        remover
        tapar la olla
        equilibrar precariamente la cuchara de madera en el mango de la olla
        esperar 10 minutos
        ir al primer paso (o apagar el fuego cuando termine)

    No golpee la cuchara de madera o se caerá.

Nótese de nuevo cómo el texto siempre se alinea con sangrías de 4 espacios (incluida esa última línea que continúa el punto 3 anterior).

Aquí hay un enlace a [un sitio web](http://foo.bar), a un [documento local](local-doc.html) y a un [encabezado de sección en el documento actual](#un-encabezado-h2). Aquí hay una nota al pie [^1].

[^1]: El texto de la nota al pie va aquí.

Las tablas pueden verse así:

tamaño material color

---

9 cuero marrón
10 cáñamo lona natural
11 vidrio transparente

Tabla: Zapatos, sus tamaños y de qué están hechos

(Lo anterior es el pie de foto de la tabla). Pandoc también admite tablas de varias líneas:

---

palabra clave texto

---

rojo Atardeceres, manzanas y
otras cosas rojas o rojizas.

verde Hojas, hierba, ranas
y otras cosas con las que
no es fácil ser.

---

A continuación, una regla horizontal.

---

Aquí hay una lista de definiciones:

manzanas
: Buenas para hacer puré de manzana.
naranjas
: ¡Cítricos!
tomates
: No hay "e" en "tomatoe".

De nuevo, el texto tiene una sangría de 4 spaces. (Ponga una línea en blanco entre cada par término/definición para espaciar más las cosas).

Aquí hay un "bloque de líneas":

| Línea uno
| Línea dos
| Línea tres

y las imágenes se pueden especificar así:

[//]: # (![imagen de ejemplo]&#40;./demo-banner.png "Una imagen ejemplar"&#41;)


Las ecuaciones matemáticas en línea van así: $\omega = d\phi / dt$. Las matemáticas de visualización deben tener su propia línea y ponerse entre signos de dólar dobles:

$$I = \int \rho R^{2} dV$$

$$
\begin{equation*}
\pi
=3.1415926535
 \;8979323846\;2643383279\;5028841971\;6939937510\;5820974944
 \;5923078164\;0628620899\;8628034825\;3421170679\;\ldots
\end{equation*}
$$

Y nótese que puede escapar con una barra invertida cualquier carácter de puntuación que desee que se muestre literalmente, ej.: \`foo\`, \*bar\*, etc.
