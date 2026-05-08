# Darkflowii ✦

**Campo de partículas ASCII reactivo al cursor · Con palabras secretas · Standalone · Sin dependencias**

---

Darkflowii nació del mismo origen que Flowii — un recurso visual dentro de un proyecto personal. Esta variante va un paso más allá: además del campo de partículas ASCII reactivo al cursor, integra un sistema de **palabras y frases secretas** que emergen del ruido de forma autónoma, con su propio color, cadencia y tiempo de vida. Todo configurable desde el editor, sin tocar una sola línea de código.

---

## ¿Qué es?

Un **campo de partículas ASCII reactivo al cursor con palabras secretas emergentes**, renderizado sobre canvas 2D. Cada celda de la cuadrícula tiene estado propio — intensidad, morph, desplazamiento, tono de color — y reacciona en tiempo real a la posición del ratón. Las palabras configuradas aparecen periódicamente en posiciones aleatorias, con color propio y duración ajustable. Sin WebGL. Sin librerías. Un único archivo HTML.

```
archivo único · ~1500 líneas · vanilla JS · 0 dependencias
```

---

## ✦ Características

**Tipografía**
- 🔤 Charset activo con 7 presets — ASCII, numérico, Katakana, Braille, Griego, bloques, matemáticas
- ✏️ Charset y carácter de reposo completamente editables
- 👁️ Toggle para mostrar u ocultar el carácter de reposo
- 📐 Tamaño de fuente ajustable (recalcula la cuadrícula al vuelo)

**Palabras Secretas**
- 💬 Lista de palabras o frases configurable, una por línea
- 🎨 Color propio para las palabras, independiente del campo ASCII
- 🎛️ Paleta de colores predefinida para las palabras
- ⏱️ Intervalo entre apariciones, duración de visibilidad y probabilidad ajustables
- 🔧 Morph inicial, opacidad máxima y umbral de morph propios

**Color**
- 🖍️ Color picker para el campo — modo fijo o rotación HSL automática
- 🎛️ Paleta de colores predefinida para el campo
- 🌈 Control de saturación, luminosidad y velocidad de rotación de hue
- 🔆 Umbral de visibilidad y opacidad máxima del campo

**Física**
- 🧲 Radio de influencia del cursor (hasta 1500px)
- 🔷 Forma del radio configurable — rombo, círculo, cuadrado y todo lo intermedio (métrica Minkowski)
- 💨 Fuerza de repulsión y suavizado de movimiento
- ⏱️ Tiempo de inactividad, persistencia (cola), ganancia de intensidad
- 📈 Perfil de influencia configurable (lineal → borde duro)

**Morph**
- 🔀 Velocidad, umbral y decaimiento del morph entre caracteres
- 🎲 Probabilidad de cambio de carácter objetivo por frame

**Ruido & Oscilación**
- 〰️ Amplitud X/Y y frecuencia de la oscilación base

**Renderizado**
- 🎞️ Estela (trail) — longitud del rastro visual
- 🖌️ Color de fondo con color picker (activo solo con fondo sólido)
- 👁️ Toggle fondo sólido / transparente

**Exportación**
- 📦 Descarga HTML standalone con todos los parámetros horneados
- 📄 Descarga JS y CSS por separado
- 🎲 Botón Random — varía charset, forma de radio, física, palabras, colores y más
- ↺ Reset a valores originales

---

## 🚀 Uso

Abre `darkflowii.html` en el navegador. No hay servidor, no hay instalación.

Mueve el cursor sobre el canvas y ajusta los parámetros desde el panel lateral. Las palabras secretas aparecen de forma autónoma — edítalas en la sección **Palabras Secretas** del panel. Cuando estés satisfecho con el resultado, pulsa **Descargar HTML** y tendrás un archivo listo para incrustar en cualquier proyecto.

---

## 📁 Estructura

```
darkflowii.html   ← todo en un único archivo
```

---

## 🔧 Incrustar en tu proyecto

El iframe funciona, pero tiene una limitación: los eventos de ratón del iframe son independientes del documento padre, por lo que el efecto no reacciona al cursor cuando está sobre contenido externo al iframe.

**La forma correcta** es incrustar el JS directamente en tu página:

```html
<!-- Añade el canvas donde quieras — normalmente como fondo fijo -->
<canvas id="darkflowii-canvas" style="position:fixed;inset:0;width:100%;height:100%;z-index:0;pointer-events:none;"></canvas>

<!-- Incluye el JS exportado -->
<script src="darkflowii.js"></script>
```

El atributo `pointer-events:none` hace que el canvas sea puramente decorativo y los clics atraviesen hacia el contenido. Quítalo si quieres que el efecto sea interactivo en primer plano.

> El CSS exportado solo contiene estilos de `body` y `canvas`. Si tu proyecto ya los define, no hace falta incluirlo.

---
---

# Darkflowii ✦

**Cursor-reactive ASCII particle field · With secret words · Standalone · Zero dependencies**

---

Darkflowii was born from the same origin as Flowii — a visual resource inside a personal project. This variant goes one step further: on top of the cursor-reactive ASCII particle field, it integrates a system of **secret words and phrases** that emerge from the noise autonomously, with their own color, cadence, and lifetime. Everything configurable from the editor, without touching a single line of code.

---

## What is it?

A **cursor-reactive ASCII particle field with emerging secret words**, rendered on a 2D canvas. Each cell in the grid has its own state — intensity, morph, displacement, color hue — and reacts in real time to the mouse position. Configured words appear periodically at random positions, with their own color and adjustable duration. No WebGL. No libraries. A single HTML file.

```
single file · ~1500 lines · vanilla JS · 0 dependencies
```

---

## ✦ Features

**Typography**
- 🔤 Active charset with 7 presets — ASCII, numeric, Katakana, Braille, Greek, block, math
- ✏️ Fully editable active and rest characters
- 👁️ Toggle to show or hide the rest character
- 📐 Adjustable font size (recalculates the grid on the fly)

**Secret Words**
- 💬 Configurable word/phrase list, one per line
- 🎨 Independent color for words, separate from the ASCII field
- 🎛️ Preset color palette for words
- ⏱️ Appearance interval, visibility duration, and probability controls
- 🔧 Initial morph, max opacity, and morph threshold for words

**Color**
- 🖍️ Field color picker — fixed mode or automatic HSL rotation
- 🎛️ Preset color palette for the field
- 🌈 Saturation, lightness, and hue rotation speed controls
- 🔆 Visibility threshold and max field opacity

**Physics**
- 🧲 Cursor influence radius (up to 1500px)
- 🔷 Configurable radius shape — diamond, circle, square and everything in between (Minkowski metric)
- 💨 Repulsion strength and movement smoothing
- ⏱️ Idle time, persistence (trail decay), intensity gain
- 📈 Configurable influence profile (linear → hard edge)

**Morph**
- 🔀 Morph speed, threshold, and decay between characters
- 🎲 Per-frame probability of target character change

**Noise & Oscillation**
- 〰️ X/Y amplitude and frequency of the base oscillation

**Rendering**
- 🎞️ Trail — visual trace length
- 🖌️ Background color picker (active only with solid background)
- 👁️ Solid / transparent background toggle

**Export**
- 📦 Download standalone HTML with all parameters baked in
- 📄 Download JS and CSS separately
- 🎲 Random button — varies charset, radius shape, physics, words, colors and more
- ↺ Reset to original values

---

## 🚀 Usage

Open `darkflowii.html` in a browser. No server, no install.

Move the cursor over the canvas and adjust parameters from the side panel. Secret words appear autonomously — edit them in the **Secret Words** section of the panel. When you're happy with the result, hit **Download HTML** and you'll have a file ready to embed in any project.

---

## 📁 Structure

```
darkflowii.html   ← everything in a single file
```

---

## 🔧 Embed in your project

Using an iframe works but has a key limitation: mouse events inside the iframe are isolated from the parent document, so the effect won't react to the cursor when it hovers over content outside the iframe.

**The correct approach** is to embed the JS directly in your page:

```html
<!-- Add the canvas wherever you need it — typically as a fixed background -->
<canvas id="darkflowii-canvas" style="position:fixed;inset:0;width:100%;height:100%;z-index:0;pointer-events:none;"></canvas>

<!-- Include the exported JS -->
<script src="darkflowii.js"></script>
```

The `pointer-events:none` attribute makes the canvas purely decorative so clicks pass through to the content below. Remove it if you want the effect to be interactive in the foreground.

> The exported CSS only contains `body` and `canvas` styles. If your project already defines those, you don't need to include it.

---

*Made with cursor, monospace font, and hidden words.*
