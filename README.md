# Laboratorio 2 — Material interactivo

Sitio web con material **interactivo** para acompañar las clases virtuales de
**Laboratorio 2**, el curso para jóvenes que participan en olimpiadas de matemática
(OMAPA · Jóvenes Talentos).

La idea es explicar conceptos de forma más dinámica que en una clase virtual común:
juegos, exploradores y comparativos con los que el estudiante puede "jugar" para entender.

## El curso

Dos módulos a lo largo del año:

1. **Teoría de Números**
2. **Geometría**

La página de inicio enlaza a los tópicos disponibles de cada módulo.

## ¿Cómo veo el sitio?

No hace falta instalar nada. Abrí el archivo **`index.html`** con doble clic y se abre
en el navegador. Desde ahí se navega a cada tópico, y cada tópico tiene un enlace
"← Volver al inicio".

## Organización de los archivos

Cada módulo tiene su carpeta; `index.html` queda en la raíz:

```
index.html                 ← página de inicio
teoria-numeros/            ← Teoría de Números
  vasos.html
  congruencias_vs_igualdades.html
  juego_143.html
geometria/                 ← Geometría
  circunferencia.html
```

Cada página es **un solo archivo** HTML autocontenido (incluye su propio diseño y la parte
interactiva adentro).

## ¿Querés sumar un tópico nuevo?

1. **Copiá** una página que ya exista del mismo módulo (por ejemplo
   `teoria-numeros/congruencias_vs_igualdades.html`) y guardá la copia con un nombre claro
   dentro de la carpeta del módulo (ej. `geometria/triangulos.html`).
2. **Reemplazá el contenido** por el de tu tópico. Conservá el enlace "← Volver al inicio"
   de arriba (apunta a `../index.html`).
3. **Enlazala desde el inicio**: en `index.html`, dentro del módulo que corresponda, copiá
   una de las tarjetas `<a class="topic"> … </a>` existentes y cambiá el enlace (con la
   carpeta, ej. `geometria/triangulos.html`), el título y la descripción.

Si trabajás con un asistente de IA (Claude Code), el archivo `CLAUDE.md` tiene el contexto
del proyecto para que te ayude a mantener el estilo.

## Pautas para mantener todo coherente

- **Sin instalaciones ni frameworks.** Solo HTML, CSS y JavaScript dentro de cada archivo.
  La única dependencia externa son las tipografías de Google Fonts.
- **Diseño por módulo.** Teoría de Números usa un tema claro (fondo crema, violeta de
  acento); Geometría usa un tema de "pizarrón" oscuro (fondo azul, dorado). Al crear una
  página nueva, seguí el estilo del resto de su módulo (está definido en el bloque `:root`
  arriba de cada archivo).
- **Idioma y tono.** Todo en español, con voseo ("tenés", "podés", "mirá"), cercano y
  didáctico, pensado para estudiantes adolescentes. Las explicaciones matemáticas tienen
  que ser correctas y rigurosas.

## Dudas o aportes

Si sos profe y querés colaborar, escribile a la responsable del curso para coordinar.
Toda mejora al material es bienvenida. 🙂
