# Laboratorio 2 — Material interactivo

Sitio web educativo para apoyar las clases **virtuales** de "Laboratorio 2", un curso
para jóvenes que participan en olimpiadas de matemática (OMAPA · Jóvenes Talentos).
La autora es la profesora del curso. La idea es explicar conceptos de forma más
**dinámica e interactiva** que en una clase virtual común.

## El curso

Recorre dos módulos a lo largo del año:

1. **Teoría de Números**
2. **Geometría**

(El módulo de Álgebra se descartó: finalmente no se dicta.)

## Estructura del sitio

Los archivos están organizados en carpetas por módulo. `index.html` queda en la raíz.

- `index.html` — Página de inicio / portal. Lista los módulos y, dentro de cada uno,
  tarjetas que enlazan a cada tópico. Es el punto de entrada.

**`teoria-numeros/`**
- `vasos.html` — "El problema de los vasos": juego interactivo (vasos de 99 ml y 105 ml)
  que lleva al **Teorema de Bézout** y al mcd.
- `congruencias_vs_igualdades.html` — Comparativo entre igualdades y congruencias, con un
  explorador interactivo (la "trampa" de la división y el rol de mcd(c, m) = 1).
- `juego_143.html` — "El juego del múltiplo de 143": problema de estrategia (Andrés vs.
  Blas). Cada jugador elige libremente en qué casilla vacía juega. Usa que 1000 ≡ −1
  (mód 143): las casillas se emparejan (1ª↔4ª, 2ª↔5ª, 3ª↔6ª) con pesos opuestos. Respuesta:
  **gana Blas** con estrategia de espejo (copia el dígito de Andrés en la casilla pareja →
  el número queda ABCABC = ABC·1001, múltiplo de 143). Incluye explorador de restos y
  juego interactivo con IA óptima (minimax sobre máscara+resto).

**`geometria/`**
- `circunferencia.html` — **Capítulo 1.** "Explorador de la circunferencia": lugar
  geométrico, elementos (cuerda, diámetro, secante, tangente, sagita), ángulos central/
  inscrito/ex-inscrito/interior/exterior, arco capaz y un reto rápido. Diagramas SVG con
  puntos arrastrables (mouse y táctil). **Usa su propio tema visual de "pizarrón"** (fondo
  azul oscuro `--ink`, dorado `--brass`, tipografía Space Grotesk), distinto del resto del
  sitio.
- `cuadrilateros_ciclicos.html` — **Capítulo 2.** "Cuadriláteros cíclicos": definición,
  las tres propiedades (ángulos opuestos suplementarios, diagonales/ángulos inscritos,
  ángulo exterior = interior opuesto), el **Teorema de Ptolomeo** con verificación numérica
  en vivo, los 10 problemas propuestos y un reto rápido. Mismo tema de pizarrón que el Cap. 1.
- `potencia_de_un_punto.html` — **Capítulo 3.** "Potencia de un punto": potencia interna
  (AP·BP = CP·DP) y externa (PA·PB = PC·PD), secante y tangente (PM² = PA·PB), la fórmula
  R² − PO², y el **eje radical** de dos circunferencias (recta ⊥ a la línea de centros,
  igual potencia respecto a ambas), todo con verificación en vivo; más propiedades, casos y
  6 problemas relacionados. Mismo tema de pizarrón.
- `trigonometria.html` — **Capítulo 4.** "Introducción a la trigonometría": círculo unitario
  y los tres sistemas de medida (sexagesimal/centesimal/circular), fórmulas fundamentales,
  de la suma, de arco doble y mitad, y los teoremas del seno y del coseno (triángulo
  arrastrable con circunradio), todo con verificación numérica en vivo; más la tabla de
  ángulos notables, aplicaciones y 8 problemas. Mismo tema de pizarrón.

En Geometría se hace **un archivo por capítulo** del material del curso.

Cada página de tópico tiene un enlace "← Volver al inicio" hacia `../index.html`.

## Cómo agregar un tópico nuevo

1. Crear el archivo HTML dentro de la carpeta del módulo (`teoria-numeros/` o `geometria/`),
   copiando el estilo de una página existente del mismo módulo.
2. Incluir el enlace "← Volver al inicio" apuntando a `../index.html`.
3. Agregar una tarjeta `<a class="topic">` dentro del módulo correspondiente en `index.html`
   (con el href relativo a la subcarpeta, p. ej. `geometria/mi-clase.html`).

**No numerar el material como "Clase 1", "Clase 2", etc.** El material es reutilizable y,
según el tiempo disponible, un mismo tópico puede ocupar una o más clases. Usar títulos
descriptivos del contenido (p. ej. "Teorema de Bézout", "Elementos y ángulos").

## Convenciones de diseño

Sitio estático: solo HTML + CSS + JavaScript embebidos en cada archivo. Sin frameworks,
sin build, sin dependencias (salvo las tipografías de Google Fonts). Cada página es
autocontenida.

Hay **dos lenguajes visuales** según el módulo:

- **Teoría de Números** (e `index.html`): fondo crema `--bg: #F7F6F2`, violeta de acento
  `--purple: #534AB7`, verde/rojo/ámbar para correcto/error/advertencia. Tipografías
  **Inter** (texto) y **JetBrains Mono** (fórmulas y números). Componentes: tarjetas con
  `--radius: 10px`, "eyebrow" en mayúsculas, pie "Laboratorio 2 · Jóvenes Talentos · OMAPA".
- **Geometría**: tema de "pizarrón" oscuro establecido en `circunferencia.html` (fondo azul
  `--ink`, dorado `--brass`, óxido/verde de acento, tipografía **Space Grotesk** + Inter +
  JetBrains Mono). Las próximas clases de geometría deberían seguir ESTE tema para ser
  coherentes dentro del módulo.

Al crear una página nueva, mantené el lenguaje visual de su módulo.

## Idioma y tono

Todo en **español**, con voseo (forma "vos": "tenés", "podés", "mirá"), que es el registro
que usa la profesora con sus estudiantes. Tono cercano y didáctico, dirigido a estudiantes
adolescentes. Las explicaciones matemáticas deben ser correctas y rigurosas.
