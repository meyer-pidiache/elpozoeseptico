---
title: Ejemplo de Código Expresivo
published: 2024-04-10
description: Cómo se ven los bloques de código en Markdown usando Expressive Code.
tags: [Markdown, Blogging, Demo]
category: Ejemplos
draft: false
---

Aquí, exploraremos cómo se ven los bloques de código usando [Expressive Code](https://expressive-code.com/). Los ejemplos proporcionados se basan en la documentación oficial, que puede consultar para más detalles.

## Código Expresivo

### Resaltado de Sintaxis

[Resaltado de Sintaxis](https://expressive-code.com/key-features/syntax-highlighting/)

#### Resaltado de sintaxis regular

```js
console.log('¡Este código tiene resaltado de sintaxis!')
```

#### Renderizado de secuencias de escape ANSI

```ansi
Colores ANSI:
- Regular:  [31mRojo [0m  [32mVerde [0m  [33mAmarillo [0m  [34mAzul [0m  [35mMagneta [0m  [36mCian [0m
- Negrita:     [1;31mRojo [0m  [1;32mVerde [0m  [1;33mAmarillo [0m  [1;34mAzul [0m  [1;35mMagneta [0m  [1;36mCian [0m
- Atenuado:   [2;31mRojo [0m  [2;32mVerde [0m  [2;33mAmarillo [0m  [2;34mAzul [0m  [2;35mMagneta [0m  [2;36mCian [0m

256 colores (mostrando colores 160-177):
 [38;5;160m160  [38;5;161m161  [38;5;162m162  [38;5;163m163  [38;5;164m164  [38;5;165m165 [0m
 [38;5;166m166  [38;5;167m167  [38;5;168m168  [38;5;169m169  [38;5;170m170  [38;5;171m171 [0m
 [38;5;172m172  [38;5;173m173  [38;5;174m174  [38;5;175m175  [38;5;176m176  [38;5;177m177 [0m

Colores RGB completos:
 [38;2;34;139;34mVerdeBosque - RGB(34, 139, 34) [0m

Formato de texto:  [1mNegrita [0m  [2mAtenuado [0m  [3mCursiva [0m  [4mSubrayado [0m
```

### Marcos de Editor y Terminal

[Marcos de Editor y Terminal](https://expressive-code.com/key-features/frames/)

#### Marcos de editor de código

```js title="mi-archivo-de-prueba.js"
console.log('Ejemplo de atributo de título')
```

---

```html
<!-- src/content/index.html -->
<div>Ejemplo de comentario con nombre de archivo</div>
```

#### Marcos de terminal

```bash
echo "Este marco de terminal no tiene título"
```

---

```powershell title="Ejemplo de terminal PowerShell"
Write-Output "¡Este sí tiene título!"
```

#### Anulación de tipos de marco

```sh frame="none"
echo "¡Mira mamá, sin marco!"
```

---

```ps frame="code" title="PerfilDePowerShell.ps1"
# Sin anular, esto sería un marco de terminal
function Watch-Tail { Get-Content -Tail 20 -Wait $args }
New-Alias tail Watch-Tail
```

### Marcadores de Texto y Línea

[Marcadores de Texto y Línea](https://expressive-code.com/key-features/text-markers/)

#### Marcado de líneas completas y rangos de líneas

```js {1, 4, 7-8}
// Línea 1 - seleccionada por número de línea
// Línea 2
// Línea 3
// Línea 4 - seleccionada por número de línea
// Línea 5
// Línea 6
// Línea 7 - seleccionada por rango "7-8"
// Línea 8 - seleccionada por rango "7-8"
```

#### Selección de tipos de marcador de línea (mark, ins, del)

```js title="marcadores-de-linea.js" del={2} ins={3-4} {6}
function demo() {
  console.log('esta línea está marcada como eliminada')
  // Esta línea y la siguiente están marcadas como insertadas
  console.log('esta es la segunda línea insertada')

  return 'esta línea utiliza el tipo de marcador neutro por defecto'
}
```

#### Adición de etiquetas a los marcadores de línea

```jsx {"1":5} del={"2":7-8} ins={"3":10-12}
// marcadores-de-linea-etiquetados.jsx
<button
  role="button"
  {...props}
  value={value}
  className={buttonClassName}
  disabled={disabled}
  active={active}
>
  {children &&
    !active &&
    (typeof children === 'string' ? <span>{children}</span> : children)}
</button>
```

#### Adición de etiquetas largas en sus propias líneas

```jsx {"1. Proporcione la prop value aquí:":5-6} del={"2. Elimine los estados disabled y active:":8-10} ins={"3. Agregue esto para renderizar los hijos dentro del botón:":12-15}
// marcadores-de-linea-etiquetados.jsx
<button
  role="button"
  {...props}

  value={value}
  className={buttonClassName}

  disabled={disabled}
  active={active}
>

  {children &&
    !active &&
    (typeof children === 'string' ? <span>{children}</span> : children)}
</button>
```

#### Uso de sintaxis similar a diff

```diff
+esta línea se marcará como insertada
-esta línea se marcará como eliminada
esta es una línea regular
```

---

```diff
--- a/README.md
+++ b/README.md
@@ -1,3 +1,4 @@
+este es un archivo diff real
-todo el contenido permanecerá sin modificar
 no se eliminará ningún espacio en blanco tampoco
```

#### Combinación de resaltado de sintaxis con sintaxis similar a diff

```diff lang="js"
  function estoEsJavaScript() {
    // ¡Todo este bloque se resalta como JavaScript,
    // y aún podemos agregarle marcadores diff!
-   console.log('Código antiguo para ser eliminado')
+   console.log('¡Código nuevo y reluciente!')
  }
```

#### Marcado de texto individual dentro de las líneas

```js "texto dado"
function demo() {
  // Marcar cualquier texto dado dentro de las líneas
  return 'Se admiten múltiples coincidencias del texto dado';
}
```

#### Expresiones regulares

```ts /ye[sp]/
console.log('Las palabras yes y yep serán marcadas.')
```

#### Escapando barras diagonales

```sh /\/ho.*\//
echo "Prueba" > /home/test.txt
```

#### Selección de tipos de marcador en línea (mark, ins, del)

```js "return true;" ins="insertado" del="eliminado"
function demo() {
  console.log('Estos son tipos de marcadores insertados y eliminados');
  // La declaración de retorno utiliza el tipo de marcador predeterminado
  return true;
}
```

### Ajuste de Línea

[Ajuste de Línea](https://expressive-code.com/key-features/word-wrap/)

#### Configuración del ajuste de línea por bloque

```js wrap
// Ejemplo con ajuste de línea
function getLongString() {
  return 'Esta es una cadena de texto muy larga que muy probablemente no quepa en el espacio disponible a menos que el contenedor sea extremadamente ancho'
}
```

---

```js wrap=false
// Ejemplo con wrap=false
function getLongString() {
  return 'Esta es una cadena de texto muy larga que muy probablemente no quepa en el espacio disponible a menos que el contenedor sea extremadamente ancho'
}
```

#### Configuración de la sangría de las líneas ajustadas

```js wrap preserveIndent
// Ejemplo con preserveIndent (habilitado por defecto)
function getLongString() {
  return 'Esta es una cadena de texto muy larga que muy probablemente no quepa en el espacio disponible a menos que el contenedor sea extremadamente ancho'
}
```

---

```js wrap preserveIndent=false
// Ejemplo con preserveIndent=false
function getLongString() {
  return 'Esta es una cadena de texto muy larga que muy probablemente no quepa en el espacio disponible a menos que el contenedor sea extremadamente ancho'
}
```

## Secciones Plegables

[Secciones Plegables](https://expressive-code.com/plugins/collapsible-sections/)

```js collapse={1-5, 12-14, 21-24}
// Todo este código de configuración repetitivo se colapsará
import { someBoilerplateEngine } from '@example/some-boilerplate'
import { evenMoreBoilerplate } from '@example/even-more-boilerplate'

const engine = someBoilerplateEngine(evenMoreBoilerplate())

// Esta parte del código será visible por defecto
engine.doSomething(1, 2, 3, calcFn)

function calcFn() {
  // Puedes tener múltiples secciones colapsadas
  const a = 1
  const b = 2
  const c = a + b

  // Esto permanecerá visible
  console.log(`Resultado del cálculo: ${a} + ${b} = ${c}`)
  return c
}

// Todo este código hasta el final del bloque se colapsará de nuevo
engine.closeConnection()
engine.freeMemory()
engine.shutdown({ reason: 'Fin del código de ejemplo repetitivo' })
```

## Números de Línea

[Números de Línea](https://expressive-code.com/plugins/line-numbers/)

### Mostrando números de línea por bloque

```js showLineNumbers
// Este bloque de código mostrará números de línea
console.log('¡Saludos desde la línea 2!')
console.log('Estoy en la línea 3')
```

---

```js showLineNumbers=false
// Los números de línea están deshabilitados para este bloque
console.log('¿Hola?')
console.log('Disculpa, ¿sabes en qué línea estoy?')
```

### Cambiando el número de línea inicial

```js showLineNumbers startLineNumber=5
console.log('¡Saludos desde la línea 5!')
console.log('Estoy en la línea 6')
```
