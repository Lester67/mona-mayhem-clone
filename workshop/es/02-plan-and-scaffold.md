<!-- l10n-sync: source-file="workshop/02-plan-and-scaffold.md" -->
# Parte 2: Plan y base

---

Antes de escribir ningún código, usemos los flujos de planificación de Copilot para pensar en la arquitectura. Planificar primero te ayuda a diseñar mejores sistemas y da a Copilot el contexto que necesita para generar código de mayor calidad.

## Tarea 1: Planifica la arquitectura de la API

<!-- track:vscode:start -->
1. Cambia al modo **Plan** en Copilot Chat (haz clic en el selector de modo en la parte inferior del panel de chat)
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Entra en **plan mode** en Copilot CLI pulsando **Shift+Tab** hasta que cambie el modo, o usando `/plan`.
<!-- track:cli:end -->

2. Introduce este prompt:

   ```
   Necesito crear un proxy de API del lado del servidor que obtenga datos de
   contribución de GitHub para cualquier usuario. El endpoint es
   https://github.com/{username}.contribs y devuelve JSON. Tenemos que sortear
   las restricciones CORS. Planifica la implementación incluyendo la estructura
   de rutas, el manejo de errores y la estrategia de caché.
   ```

3. **Revisa el plan**: aquí es donde brilla la planificación. No aceptes la primera respuesta sin más:
   - Pide aclaraciones sobre cualquier cosa que no esté clara
   - Sugiere cambios si algo no te convence
   - Itera hasta que estés satisfecho con el enfoque

<!-- track:vscode:start -->
4. Cuando estés conforme con el plan, pide a Copilot que lo implemente: cambia al modo **Agent** y dile que continúe.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Cuando estés satisfecho con el plan, dile a Copilot CLI que continúe con la implementación.
5. Revisa los cambios del archivo con `/diff` antes de aprobarlos.
<!-- track:cli:end -->

6. **Resultado:** ahora deberías tener una ruta de API creada en:

   ```
   src/pages/api/contributions/[username].ts
   ```

## Tarea 2: Prueba la API

> **⚠️ ¿No ves cambios?** Si el servidor de desarrollo no detecta la nueva ruta, deténlo (`Ctrl+C`) y reinícialo con `npm run dev`.

1. Asegúrate de que tu servidor de desarrollo esté ejecutándose y luego prueba el endpoint:

   ```bash
   curl http://localhost:4321/api/contributions/octocat
   ```

2. Deberías ver JSON con datos de contribución devueltos.
3. Prueba también el caso de error: intenta un usuario no válido y confirma que devuelve una respuesta de error apropiada.

## Tarea 3: Planifica la página de batalla

<!-- track:vscode:start -->
1. Sigue en modo **Plan** e introduce este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Sigue en plan mode (o ejecuta `/plan`) e introduce este prompt:
<!-- track:cli:end -->

   ```
   Ahora necesito la página principal. Planifica una página de batalla para
   "Mona Mayhem - GitHub Contribution Battle Arena" con: dos entradas de nombre
   de usuario (Jugador 1 y Jugador 2), un botón de batalla y un área de resultados.
   Mantén la UI simple: no sobreingenierices el diseño ni el estilo en esta fase.
   Planea la estructura HTML, el estilo básico y cómo funcionará la interacción de la batalla.
   ```

2. **Revisa e itera** sobre el plan: haz preguntas, sugiere cambios y refina el enfoque.

<!-- track:vscode:start -->
3. Cuando estés satisfecho, cambia a **Agent** mode y deja que Copilot construya la página.
<!-- track:vscode:end -->

<!-- track:cli:start -->
3. Cuando estés satisfecho, pide a Copilot CLI que implemente el plan aprobado.
4. Usa `/diff` otra vez para inspeccionar el andamiaje HTML y CSS antes de aprobarlo.
<!-- track:cli:end -->

## Tarea 4: Verifica la base

> **⚠️ ¿No ves cambios?** Si la página no se ve bien o no se ha actualizado, detén el servidor de desarrollo (`Ctrl+C`) y reinícialo con `npm run dev`, luego refresca el navegador.

1. Abre http://localhost:4321 en tu navegador.
2. Deberías ver:
   - El título del juego
   - Dos campos de entrada para nombres de usuario (Jugador 1 y Jugador 2)
   - Un botón de batalla
3. El botón aún no funcionará: ¡es lo esperado! Aún no hemos conectado la lógica de interacción. Eso llega después.

---

## ✅ ¡Parte 2 completada!

Has aprendido a:

- **Planificar antes de codificar** en lugar de saltar directamente a la implementación
- **Iterar sobre los planes** hasta que la arquitectura se sienta bien
- **Pasar del plan a la implementación** con un flujo más claro y seguro
