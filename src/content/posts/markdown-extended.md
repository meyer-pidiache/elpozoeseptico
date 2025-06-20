---
title: Funcionalidades Extendidas de Markdown
published: 2024-05-01
updated: 2024-11-29
description: 'Lea más sobre las funcionalidades de Markdown en Fuwari'
image: ''
tags: [Demo, Example, Markdown, Fuwari]
category: 'Ejemplos'
draft: false 
---

## Tarjetas de Repositorio de GitHub
Puede agregar tarjetas dinámicas que enlazan a repositorios de GitHub. Al cargar la página, la información del repositorio se obtiene de la API de GitHub. 

::github{repo="Fabrizz/MMM-OnSpotify"}

Cree una tarjeta de repositorio de GitHub con el código `::github{repo="<propietario>/<repositorio>"}`.

```markdown
::github{repo="saicaca/fuwari"}
```

## Advertencias (Admonitions)

Se admiten los siguientes tipos de advertencias: `note` `tip` `important` `warning` `caution`

:::note
Resalta información que los usuarios deben tener en cuenta, incluso al leer rápidamente.
:::

:::tip
Información opcional para ayudar a un usuario a tener más éxito.
:::

:::important
Información crucial necesaria para que los usuarios tengan éxito.
:::

:::warning
Contenido crítico que exige la atención inmediata del usuario debido a posibles riesgos.
:::

:::caution
Posibles consecuencias negativas de una acción.
:::

### Sintaxis Básica

```markdown
:::note
Resalta información que los usuarios deben tener en cuenta, incluso al leer rápidamente.
:::

:::tip
Información opcional para ayudar a un usuario a tener más éxito.
:::
```

### Títulos Personalizados

El título de la advertencia se puede personalizar.

:::note[MI TÍTULO PERSONALIZADO]
Esta es una nota con un título personalizado.
:::

```markdown
:::note[MI TÍTULO PERSONALIZADO]
Esta es una nota con un título personalizado.
:::
```

### Sintaxis de GitHub

> [!TIP]
> [La sintaxis de GitHub](https://github.com/orgs/community/discussions/16925) también es compatible.

```
> [!NOTE]
> La sintaxis de GitHub también es compatible.

> [!TIP]
> La sintaxis de GitHub también es compatible.
```