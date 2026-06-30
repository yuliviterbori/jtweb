# Laboratorio 2 — Material interactivo

Sitio web con material **interactivo** para acompañar las clases virtuales de
**Laboratorio 2**, el curso para jóvenes que participan en olimpiadas de matemática
(OMAPA · Jóvenes Talentos).

La idea es explicar conceptos de forma más dinámica que en una clase virtual común:
juegos, exploradores y comparativos con los que el estudiante puede "jugar" para entender.

## El curso

Tres módulos a lo largo del año:

1. **Álgebra**
2. **Teoría de Números**
3. **Geometría**

La página de inicio muestra cada módulo con su estado y enlaza a los tópicos disponibles.

## ¿Cómo veo el sitio?

No hace falta instalar nada. Abrí el archivo **`index.html`** con doble clic y se abre
en el navegador. Desde ahí se navega a cada tópico, y cada tópico tiene un enlace
"← Volver al inicio".

## ¿Querés sumar un tópico nuevo?

Cada página es **un solo archivo** HTML autocontenido (incluye su propio diseño y la parte
interactiva adentro). Para agregar un tópico:

1. **Copiá** una página que ya exista (por ejemplo `congruencias_vs_igualdades.html`) y
   renombrá la copia con un nombre claro (ej. `triangulos.html`).
2. **Reemplazá el contenido** por el de tu tópico. Conservá el enlace
   "← Volver al inicio" que está arriba de todo.
3. **Enlazala desde el inicio**: en `index.html`, dentro del módulo que corresponda,
   copiá una de las tarjetas `<a class="topic"> … </a>` existentes y cambiá el enlace,
   el título y la descripción.

Si trabajás con un asistente de IA (Claude Code), el archivo `CLAUDE.md` tiene el contexto
del proyecto para que te ayude a mantener el estilo.

## Pautas para mantener todo coherente

- **Sin instalaciones ni frameworks.** Solo HTML, CSS y JavaScript dentro de cada archivo.
  La única dependencia externa son las tipografías de Google Fonts.
- **Diseño compartido.** Todas las páginas usan la misma paleta y tipografías (definidas
  arriba de cada archivo, en el bloque `:root`): fondo crema, violeta de acento, y verde /
  rojo / ámbar para marcar correcto / error / advertencia. Reutilizá ese estilo.
- **Idioma y tono.** Todo en español, con voseo ("tenés", "podés", "mirá"), cercano y
  didáctico, pensado para estudiantes adolescentes. Las explicaciones matemáticas tienen
  que ser correctas y rigurosas.

## Dudas o aportes

Si sos profe y querés colaborar, escribile a la responsable del curso para coordinar.
Toda mejora al material es bienvenida. 🙂
