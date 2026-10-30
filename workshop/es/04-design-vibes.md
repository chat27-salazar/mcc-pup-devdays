<!-- l10n-sync: source-file="04-design-vibes.md" -->
# Parte 4: Tematización Orientada al Diseño

---

En esta parte, usarás **Plan Mode** para diseñar una transformación de tema completa, y luego **Agent Mode** para implementarla. Esto es desarrollo orientado al diseño — comienza con la visión, itera sobre los elementos visuales y deja que Copilot se encargue del trabajo pesado de CSS.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia al modo **Plan** de GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo plan.
<!-- track:cli:end -->

Ingresa este prompt:

> Quiero transformar esta página en una experiencia completa de arcade retro. Planifica una renovación visual integral que incluya: efectos de líneas de barrido CRT en el fondo, un brillo de neón en el título que pulse como un letrero, una insignia VS animada con cambios de color en el degradado, una superposición brillante e iridiscente en las tarjetas de resultados, animaciones de entrada flotante para los campos de texto, texto de carga que cambie entre verde y morado, y efectos de brillo al pasar el cursor sobre los cuadrados de contribuciones. Mantén el fondo oscuro (#0a0a1a) con acentos verdes (#5fed83) y morados (#8a2be2). Usa un tema oscuro con la fuente retro Press Start 2P de Google Fonts.

Copilot generará un plan detallado de implementación cubriendo todos los efectos visuales. **No lo aceptes de inmediato** — revisa el plan e itera:

- Sugiere ajustes en la velocidad de las animaciones (por ejemplo, "Haz que el pulso del neón sea más lento, de unos 3 segundos").
- Pregunta por efectos concretos (por ejemplo, "¿Cómo funcionará la superposición iridiscente en las tarjetas?").
- Solicita cambios en el enfoque si algo no te convence

<!-- track:vscode:start -->
Cuando estés satisfecho con el plan, cambia al modo **Agent** y pide a Copilot que lo implemente.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Cuando estés satisfecho con el plan, pide a Copilot CLI que lo implemente.
<!-- track:cli:end -->

## Tarea 2: Implementa el Tema

> Implementa el plan del tema de arcade retro que acabamos de diseñar.

Copilot agregará múltiples animaciones CSS, pseudo-elementos y transiciones en tu hoja de estilos. Esto puede incluir:

- `@keyframes` para scanlines, pulso neón, shimmer y efectos de aparición flotante
- Pseudo-elementos (`::before`, `::after`) para efectos de superposición
- CSS custom properties para los colores del tema
- Transiciones y estados hover para elementos interactivos

<!-- track:cli:start -->
Cuando terminen los cambios, usa `/diff` para revisar los estilos antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Afina el estilo visual

> **⚠️ ¿No ves los cambios?** Si el nuevo tema o las animaciones no aparecen, detén el servidor (`Ctrl+C`), reinícialo con `npm run dev` y actualiza el navegador con una recarga forzada (`Ctrl+Shift+R`).

Mantén la vista previa del navegador abierta e itera sobre el diseño. Prueba indicaciones como:

> El efecto de líneas de barrido es demasiado intenso; reduce la opacidad a 0.03.

> Añade un sutil parpadeo eléctrico al texto del título.

> La insignia VS debería pulsar con más intensidad.

Esto es **desarrollo orientado al diseño**: iteras sobre el resultado visual en tiempo real. Cada indicación afina la experiencia hasta que tenga el aspecto que buscas. No te conformes con algo "suficientemente bueno": ajusta el estilo hasta que la página parezca sacada de una máquina recreativa.

## Tarea 4: Actualiza las Instrucciones

Tus instrucciones deben reflejar las decisiones de diseño importantes. Pídele a Copilot:

<!-- track:vscode:start -->
> Añade una sección de guía de diseño a copilot-instructions.md que describa nuestro tema de arcade retro: colores, fuentes y estilo de animación.
<!-- track:vscode:end -->

<!-- track:cli:start -->
> Actualiza las instrucciones del repositorio con una breve guía de diseño para el tema de arcade retro: colores, fuentes, estilo de animación y la regla de que la nueva interfaz debe mantener la estética de neón.
<!-- track:cli:end -->

Esto mantiene las interacciones futuras de Copilot consistentes con la identidad visual que has establecido. Cualquier nueva funcionalidad o componente seguirá automáticamente la estética retro arcade.

Confirma los cambios en las instrucciones y el diseño cuando la página tenga el aspecto que buscas.

## ✅ Parte 4 Completa

**Lo que aprendiste:**

- **Plan Mode para sistemas de diseño** — esbozar una renovación visual completa antes de escribir código
- **Iterar sobre la salida visual** — usar prompts rápidos de seguimiento para ajustar animaciones, colores y efectos
- **Mantener las instrucciones actualizadas con decisiones de diseño** — documentar tu tema para que Copilot se mantenga consistente
- **Flujo de trabajo de desarrollo orientado al diseño** — comenzar con la visión, implementar con IA, refinar hasta que se sienta correcto
