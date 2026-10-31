<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Construir el juego con flujos agentic

---

Esta parte es donde Copilot pasa de planificador a implementador. En lugar de escribir código línea por línea, describes lo que quieres y dejas que Copilot lleve a cabo el trabajo a través de los archivos que necesite cambiar.

## Tarea 1: Conecta la batalla

<!-- track:vscode:start -->
1. Cambia al modo **Agent** en Copilot Chat.
2. Introduce este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Devuelve Copilot CLI a su flujo habitual de codificación (o sigue en autopilot si quieres que Copilot siga avanzando hasta que lo detengas).
2. Menciona el archivo de la página si te resulta útil: `@src/pages/index.astro`
3. Introduce este prompt:
<!-- track:cli:end -->

   > Añade JavaScript del lado del cliente a la página de batalla que:
   > 1. Cuando se hace clic en el botón Battle, obtenga ambos nombres de usuario de los inputs.
   > 2. Valide que ambos estén rellenos (muestra un error si no lo están).
   > 3. Obtenga los datos de contribución de ambos usuarios en paralelo desde nuestra API.
   > 4. Renderice los gráficos de contribución como cuadrículas coloreadas: cada día es un cuadrado con el color de la paleta de GitHub.
   > 5. Muestre una insignia VS entre los dos usuarios.
   > 6. Muestra el nombre de usuario, el total de contribuciones y el rango de fechas para cada usuario.
   > 7. Maneje estados de carga y errores.
   > 8. También se active con la tecla Enter en los campos de entrada.
   > 9. La UI es simple por ahora y ya está esbozada.
   >
   > Usa interfaces TypeScript para la estructura de datos de contribución.

<!-- track:vscode:start -->
3. Deja que Agent Mode trabaje en la implementación a través de `index.astro`.
4. Revisa los cambios propuestos en la vista de diff antes de aceptarlos.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deja que Copilot CLI trabaje en la implementación a través de `src/pages/index.astro`.
5. Usa `/diff` para inspeccionar los cambios generados y luego aprobalos.
<!-- track:cli:end -->

## Tarea 2: Prueba la batalla

> **⚠️ ¿No ves cambios?** Si la página de batalla no se ha actualizado, detén el servidor de desarrollo (`Ctrl+C`) y reinícialo con `npm run dev`, luego refresca el navegador.

1. Introduce `octocat` y `torvalds` como los dos nombres de usuario y luego haz clic en **Battle**.
2. Deberías ver ambos gráficos de contribución renderizados uno al lado del otro con cuadrículas de colores.
3. Prueba los casos de error:
   - Deja uno o ambos campos vacíos y haz clic en Battle: deberías ver un error de validación.
   - Introduce un nombre de usuario no válido: la app debería mostrar un error de la API.
4. Prueba a pulsar **Enter** en cualquiera de los campos: debería desencadenar la batalla igual que el botón.

## Tarea 3: Itera con Copilot

Si algo no está del todo bien, da a Copilot comentarios de seguimiento directamente. Por ejemplo:

- *"Las casillas de contribución son demasiado grandes, hazlas de 12x12px"*
- *"Añade un tooltip al pasar el ratón con la fecha y el número de contribuciones"*
- *"El estado de carga necesita una animación de pulso"*

<!-- track:vscode:start -->
Agent Mode maneja cambios y iteraciones en varios archivos de forma natural. Cada prompt de seguimiento se basa en la conversación anterior, así que puedes refinar la implementación de forma incremental sin empezar de cero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Las sesiones de Copilot CLI mantienen el historial, así que cada prompt de seguimiento se basa en el anterior. Usa `/session` o `/context` si quieres inspeccionar lo que Copilot está llevando adelante, y `/review` tras una iteración más grande si quieres una pasada extra para bugs o pulido.
<!-- track:cli:end -->

## Consejos para esta parte

- **Sé específico sobre lo que quieres**: unos requisitos claros generan mejores resultados.
- **Divide tareas grandes en prompts más pequeños** si Copilot se desvía del rumbo.
- **Revisa los cambios antes de aceptarlos**: es más rápido inspeccionar el código generado que reescribirlo después.
- **Prueba la app inmediatamente después de cada pasada de implementación** para mantener los problemas acotados.

## ✅ Parte 3 completada

Has aprendido a:

- Usar Copilot para **trabajos de implementación multiarchivo**
- **Iterar sobre los resultados** con prompts de seguimiento enfocados
- Manejar el **bucle completo de una funcionalidad**: implementación, revisión, pruebas y refinamiento
