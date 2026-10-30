<!-- l10n-sync: source-file="03-agent-mode.md" -->
# Parte 3: Construcción del juego con flujos de trabajo agénticos

---

En esta parte, Copilot pasa de planificar a implementar. En lugar de escribir código línea por línea, describes lo que quieres y Copilot realiza el trabajo en los archivos que debe cambiar.

## Tarea 1: Conecta la Batalla

<!-- track:vscode:start -->
1. Cambia al modo **Agent** en Copilot Chat.
2. Ingresa este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Devuelve Copilot CLI al flujo de programación estándar (o mantén el modo autopilot si quieres que siga trabajando hasta que lo detengas).
2. Si te sirve, menciona el archivo de la página para dar más contexto: `@src/pages/index.astro`.
3. Ingresa este prompt:
<!-- track:cli:end -->

   > Añade JavaScript en el cliente a la página de batalla para que:
   > 1. Al hacer clic en el botón Battle, obtenga los nombres de usuario de ambos campos
   > 2. Compruebe que ambos estén completos y muestre un error si no lo están
   > 3. Obtenga en paralelo de nuestra API los datos de contribuciones de ambos usuarios
   > 4. Muestre los gráficos de contribuciones como cuadrículas de colores: cada día debe ser un cuadrado de color de la paleta de GitHub
   > 5. Muestre una insignia VS entre ambos usuarios
   > 6. Muestre el nombre de usuario, el total de contribuciones y el intervalo de fechas de cada usuario
   > 7. Gestione los estados de carga y los errores
   > 8. También se active al pulsar Enter en los campos de entrada
   > 9. Por ahora, usa la interfaz sencilla que ya está creada.
   >
   > Usa interfaces de TypeScript para la estructura de datos de contribuciones.

<!-- track:vscode:start -->
3. Deja que Agent Mode implemente los cambios en `index.astro`.
4. Revisa las modificaciones propuestas en la vista de diferencias antes de aceptarlas.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deja que Copilot CLI trabaje en `src/pages/index.astro`.
5. Inspecciona los cambios generados con `/diff` y apruébalos.
<!-- track:cli:end -->

## Tarea 2: Prueba la Batalla

1. Ingresa `octocat` y `torvalds` como los dos nombres de usuario, luego haz clic en **Battle**.
2. Deberías ver ambos gráficos de contribuciones renderizados lado a lado con cuadrículas de colores.
3. Prueba los casos de error:
   - Deja uno o ambos campos vacíos y haz clic en Battle — deberías ver un error de validación.
   - Ingresa un nombre de usuario inválido — la app debería mostrar un error de la API.
4. Prueba presionar **Enter** en cualquier campo de entrada — debería activar la batalla igual que al hacer clic en el botón.

## Tarea 3: Itera con Copilot

Si algo no está del todo bien, dale instrucciones de seguimiento a Copilot. Por ejemplo:

- *"Los cuadrados de contribuciones son demasiado grandes; hazlos de 12x12 px"*
- *"Añade una ayuda emergente al pasar el cursor que muestre la fecha y el número de contribuciones"*
- *"El estado de carga necesita una animación de pulsación"*

<!-- track:vscode:start -->
Agent Mode gestiona de forma natural los cambios en varios archivos y las iteraciones. Cada indicación de seguimiento aprovecha el contexto de la conversación para que puedas mejorar la implementación sin empezar de cero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Las sesiones de Copilot CLI conservan el historial, así que cada indicación de seguimiento parte de la anterior. Usa `/session` o `/context` para inspeccionar el contexto y ejecuta `/review` después de una iteración importante para buscar errores o mejoras.
<!-- track:cli:end -->

## Consejos para Agent Mode

- **Sé específico sobre lo que quieres** — requisitos claros producen mejores resultados.
- **Divide tareas grandes en prompts más pequeños** si Agent se desvía.
- **Revisa los cambios antes de aceptar** — usa la vista de diferencias para entender qué se modificó.
- **Si los resultados no son perfectos, da retroalimentación e itera** — Agent aprende de tus correcciones dentro de la conversación.

## ✅ Parte 3 Completa

Has aprendido a:

- Usar **Agent Mode** para implementaciones complejas en múltiples archivos
- **Iterar sobre los resultados** con retroalimentación dirigida
- Manejar el **ciclo de vida completo de una funcionalidad** — desde la implementación hasta las pruebas y el refinamiento — en una sola conversación
