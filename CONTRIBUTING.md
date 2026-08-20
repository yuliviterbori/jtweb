# Cómo colaborar

¡Gracias por sumar material a **Laboratorio 2**! Para mantener el sitio ordenado y que
nada se rompa, todos los cambios entran por **Pull Request (PR)** y los revisa y aprueba
la responsable del curso antes de mezclarse a `main`. **Nadie mergea directo a `main`.**

## El flujo, paso a paso

1. **Actualizá tu copia de `main`.**
   ```bash
   git checkout main
   git pull
   ```
2. **Creá una rama** desde `main`, con un nombre descriptivo (no trabajes sobre `main`):
   ```bash
   git checkout -b geometria/nuevo-capitulo
   ```
   Convención sugerida: `modulo/tema` o `fix/que-arreglas`.
   Ejemplos: `teoria-numeros/divisibilidad`, `geometria/semejanza`, `fix/typo-vasos`.
3. **Hacé tus cambios.** Regla general: **un tópico/capítulo por rama**, cada página en
   un solo archivo HTML autocontenido dentro de la carpeta de su módulo
   (`teoria-numeros/` o `geometria/`). Ver la guía de estilo abajo.
4. **Probalo de verdad**: abrí el/los HTML en el navegador (doble clic) y revisá que
   funcione, que se vean bien los acentos y que los enlaces anden.
5. **Commiteá** con un mensaje claro de qué hiciste:
   ```bash
   git add .
   git commit -m "Geometría: agrega capítulo de semejanza"
   ```
6. **Subí la rama:**
   ```bash
   git push -u origin geometria/nuevo-capitulo
   ```
7. **Abrí el PR** hacia `main` en GitHub. Completá la descripción (qué cambia y por qué)
   y, si es un cambio visual, adjuntá una **captura de pantalla**.
8. **Esperá la revisión.** Si te piden ajustes, seguís commiteando en la **misma rama** y
   el PR se actualiza solo. Cuando esté aprobado, **la responsable hace el merge**.
9. Después del merge podés borrar la rama.

> Consejo: mantené los PR **chicos y enfocados** (un tema por PR). Es más fácil de revisar
> y de aprobar.

## Checklist antes de abrir el PR

- [ ] La página abre bien en el navegador y la parte interactiva funciona.
- [ ] Si es un tópico nuevo: agregaste su **tarjeta** en `index.html` con el enlace a la
      subcarpeta (p. ej. `geometria/mi-clase.html`).
- [ ] La página tiene el enlace **"← Volver al inicio"** apuntando a `../index.html`.
- [ ] Respeta el **estilo del módulo** (ver abajo).
- [ ] Todo en **español con voseo**; la matemática es correcta y rigurosa.
- [ ] **Sin dependencias externas** nuevas (salvo las tipografías de Google Fonts).
- [ ] Sin numerar el material como "Clase 1/2": usá títulos descriptivos del contenido.

## Guía de estilo (resumen)

Sitio estático: solo HTML + CSS + JavaScript embebidos en cada archivo. Sin frameworks,
sin build. Hay **dos lenguajes visuales** según el módulo:

- **Teoría de Números** (e `index.html`): tema claro, fondo crema, violeta de acento,
  tipografías Inter + JetBrains Mono.
- **Geometría**: tema de "pizarrón" oscuro (fondo azul, dorado), tipografía Space Grotesk.
  Copiá una página existente del módulo para arrancar.

Más detalles en el `README.md`. Si usás un asistente de IA (Claude Code), el archivo
`CLAUDE.md` tiene el contexto del proyecto.
