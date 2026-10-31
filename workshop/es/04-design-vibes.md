<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematización centrada en el diseño

---

En esta parte usarás Copilot's planning and implementation loops to design a comprehensive theme transformation. This is design-first development — start with the vision, iterate on the visuals, and let Copilot handle the CSS heavy lifting.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia al modo **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI, o pulsa **Shift+Tab** hasta que el modo plan esté activo.
<!-- track:cli:end -->

Introduce este prompt:

> Quiero transformar esta página en una experiencia retro arcade completa. Haz un rediseño visual completo que incluya: efectos de líneas CRT en el fondo, brillo neón en el título que palpite como un letrero de neón, insignia VS animada con cambios de gradiente, superposición de brillo/en brillante en las tarjetas de resultados, animaciones de entrada para los campos, texto de carga con cambio de color entre verde y morado, y efectos de brillo al pasar el cursor sobre los cuadrados de contribución. Mantén el fondo oscuro (`#0a0a1a`) con acentos verdes (`#5fed83`) y morados (`#8a2be2`). Usa un tema oscuro con la fuente retro de arcade Press Start 2P de Google Fonts.

Copilot generará un plan detallado de implementación que cubra todos los efectos visuales. **No lo aceptes de inmediato**: revisa el plan e itera:

- Sugiere ajustes en la velocidad de las animaciones (por ejemplo, *"Haz que el pulso neón sea más lento, alrededor de 3 segundos"*)
- Pregunta por efectos concretos (por ejemplo, *"¿Cómo funcionará la superposición de brillo en las tarjetas?"*)
- Solicita cambios en el enfoque si algo no te convence

## Tarea 2: Implementa el tema

Cuando estés satisfecho con el plan, dile a Copilot que lo implemente.

> Implementa el plan del tema retro arcade que acabamos de diseñar.

Copilot añadirá varias animaciones CSS, pseudo-elementos y transiciones a tu hoja de estilos. Esto puede incluir:

- `@keyframes` para líneas CRT, pulso neón, brillo y efectos de entrada flotante
- Pseudo-elementos (`::before`, `::after`) para efectos de superposición
- Propiedades CSS personalizadas para los colores del tema
- Transiciones y estados hover para elementos interactivos

<!-- track:cli:start -->
Después de que los cambios entren, usa `/diff` para revisar los cambios de estilo antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Ajusta las vibas

> **⚠️ ¿No ves cambios?** Si el nuevo tema o las animaciones no se muestran, detén el servidor de desarrollo (`Ctrl+C`) y reinícialo con `npm run dev`, luego haz una recarga forzada (`Ctrl+Shift+R`) en tu navegador.

Mantén la vista previa del navegador abierta e itera sobre el diseño. Prueba prompts como:

> El efecto de líneas CRT es demasiado fuerte, reduce la opacidad a 0.03

> Añade un ligero parpadeo eléctrico al texto del título

> La insignia VS debe pulsar de forma más dramática

Esto es **desarrollo centrado en el diseño**: estás iterando sobre la salida visual en tiempo real. Cada prompt refina la experiencia hasta que parece bien. No te conformes con “bastante bien”: empuja las vibras hasta que la página parezca salida de un gabinete arcade.

## Tarea 4: Actualiza las instrucciones

Tus instrucciones deben reflejar los cambios de diseño más importantes para que los siguientes prompts sigan alineados.

<!-- track:vscode:start -->
Pregunta a Copilot Chat:

> Añade una sección de guía de diseño a copilot-instructions.md describiendo nuestro tema retro arcade: colores, fuentes y estilo de animación
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pregunta a Copilot CLI:

> Actualiza nuestras instrucciones del repositorio con una breve guía de diseño para el tema retro arcade: colores, fuentes, estilo de animación y la regla de que la nueva UI debe mantener la estética neón.
<!-- track:cli:end -->

Haz commit de tus instrucciones actualizadas y de los cambios de diseño cuando la página tenga el aspecto correcto.

## ✅ Parte 4 completada

**Lo que aprendiste:**

- Usa los flujos de planificación para esbozar un **sistema de diseño antes de la implementación**
- **Itera sobre el resultado visual** con prompts cortos de seguimiento
- **Actualiza las instrucciones tras decisiones importantes** para que Copilot mantenga la identidad visual de forma consistente
