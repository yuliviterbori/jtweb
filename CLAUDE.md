# Laboratorio 2 — Material interactivo

Sitio web educativo para apoyar las clases **virtuales** de "Laboratorio 2", un curso
para jóvenes que participan en olimpiadas de matemática (OMAPA · Jóvenes Talentos).
La autora es la profesora del curso. La idea es explicar conceptos de forma más
**dinámica e interactiva** que en una clase virtual común.

## El curso

Recorre tres módulos a lo largo del año:

1. **Álgebra**
2. **Teoría de Números**
3. **Geometría**

La página de inicio refleja el estado de cada módulo (completado / en curso / próximo),
que se va actualizando con el avance del curso.

## Estructura del sitio

- `index.html` — Página de inicio / portal. Lista los tres módulos con su estado y,
  dentro de cada uno, tarjetas que enlazan a cada tópico. Es el punto de entrada.
- `vasos.html` — **Teoría de Números, Clase 1.** "El problema de los vasos": juego
  interactivo (vasos de 99 ml y 105 ml) que lleva al **Teorema de Bézout** y al mcd.
- `congruencias_vs_igualdades.html` — **Teoría de Números, Clase 2.** Comparativo entre
  igualdades y congruencias, con un explorador interactivo (la "trampa" de la división
  y el rol de mcd(c, m) = 1).

Cada página de tópico tiene un enlace "← Volver al inicio" hacia `index.html`.

## Cómo agregar un tópico nuevo

1. Crear un archivo HTML nuevo para el tópico (copiar el estilo de una página existente).
2. Incluir el enlace "← Volver al inicio" (`<a href="index.html" class="back-link">`).
3. Agregar una tarjeta `<a class="topic">` dentro del módulo correspondiente en `index.html`.

## Convenciones de diseño

Sitio estático: solo HTML + CSS + JavaScript embebidos en cada archivo. Sin frameworks,
sin build, sin dependencias (salvo las tipografías de Google Fonts). Cada página es
autocontenida.

Sistema de diseño compartido (mismas variables CSS `:root` en todos los archivos):
- Tipografías: **Inter** (texto) y **JetBrains Mono** (fórmulas, números, código).
- Paleta: fondo crema `--bg: #F7F6F2`, violeta de acento `--purple: #534AB7`,
  verde `--teal` (correcto/válido), rojo `--red` (error), ámbar `--amber` (advertencia).
- Componentes recurrentes: tarjetas con `--radius: 10px` y borde `--border`, "eyebrow"
  (etiqueta superior en mayúsculas), pies de página con la línea
  "Laboratorio 2 · Jóvenes Talentos · OMAPA".

Mantener este lenguaje visual al crear páginas nuevas para que todo se vea coherente.

## Idioma y tono

Todo en **español**, con voseo (forma "vos": "tenés", "podés", "mirá"), que es el registro
que usa la profesora con sus estudiantes. Tono cercano y didáctico, dirigido a estudiantes
adolescentes. Las explicaciones matemáticas deben ser correctas y rigurosas.
