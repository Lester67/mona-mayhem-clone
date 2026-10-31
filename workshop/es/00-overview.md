# 🎮 Mona Mayhem — Taller de GitHub Copilot

---

> **Duración:** ~1 hora  
> **Nivel:** Intermedio  
> **Stack:** Astro / Node.js / TypeScript

Construye una aplicación de comparación de contribuciones de GitHub con estilo retro arcade — **Mona Mayhem** — mientras aprendes todo el espectro de flujos de trabajo de GitHub Copilot. El taller admite **dos rutas**: una experiencia en VS Code y otra en GitHub Copilot CLI.

---

## 🎯 Elige tu ruta

- **Ruta de VS Code** — mantente dentro del editor y practica Chat, Plan Mode, Agent Mode, background agents y el ciclo de revisión integrado.
- **Ruta de CLI** — mantente en la terminal y practica `copilot`, contexto con `@file`, `/plan`, ediciones autónomas, `/fleet`, `/delegate` y `/review`.

Sigue la ruta que mejor se adapte a tu flujo de trabajo.

---

## 📋 Lista rápida

Antes de empezar, verifica:

- [ ] GitHub Copilot está habilitado para tu cuenta
- [ ] Node.js instalado
- [ ] Git instalado y configurado
- [ ] Tu navegador y terminal están listos

<!-- track:vscode:start -->
- [ ] VS Code **v1.107+** (sin actualizaciones pendientes)
- [ ] Iniciado sesión en la extensión **GitHub Copilot**
- [ ] Panel de Chat abierto y Agent listo
<!-- track:vscode:end -->

<!-- track:cli:start -->
- [ ] GitHub Copilot CLI instalado y disponible como `copilot`
- [ ] Autenticado en la CLI con `/login`
- [ ] Cómodo usando comandos con barra como `/help`, `/plan` y `/review`
<!-- track:cli:end -->

> 💡 **Consejo:** Usa el DevContainer para un entorno preconfigurado si quieres arrancar rápido en VS Code.

---

## 🧠 Qué aprenderás

| # | Habilidad | Descripción |
|---|-----------|-------------|
| 1 | **Ingeniería de contexto** | Enseña a Copilot sobre tu código con instrucciones, referencias y restricciones claras |
| 2 | **Planificación primero** | Diseña la arquitectura antes de implementar |
| 3 | **Implementación agéntica** | Deja que Copilot realice tareas de codificación de varios pasos bajo tu supervisión |
| 4 | **Diseño iterativo** | Usa Copilot para transformar visuales y refinar detalles de interacción |
| 5 | **Flujos paralelos** | Divide el trabajo entre agentes, sesiones o tareas delegadas |

<!-- track:vscode:start -->
### Enfoque de funciones en VS Code

- **Chat + Ask mode** para exploración
- **Plan Mode** para arquitectura y prompts de diseño
- **Agent Mode** para implementación multiarchivo
- **Agentes en segundo plano y en la nube** para pulido paralelo
<!-- track:vscode:end -->

<!-- track:cli:start -->
### Enfoque de funciones en Copilot CLI

- **Sesiones interactivas del CLI** con `copilot`
- **`/plan` y Shift+Tab** para planificación estructurada
- **Ediciones autónomas** con aprobaciones inline y `/diff`
- **`/fleet`, `/delegate` y `/review`** para paralelismo y control de calidad
<!-- track:cli:end -->

---

## 📚 Partes del laboratorio

| Parte | Título | Descripción |
|-------|--------|-------------|
| [**01**](01-setup.md) | Configuración e ingeniería de contexto | Crea tu repositorio, prepara tu entorno y da a Copilot el contexto adecuado |
| [**02**](02-plan-and-scaffold.md) | Plan y base | Diseña la arquitectura de la API y la página antes de implementar |
| [**03**](03-agent-mode.md) | Construir el juego | Conecta la página de batalla y los gráficos de contribución con ayuda agéntica |
| [**04**](04-design-vibes.md) | Tematización centrada en el diseño | Convierte la base en una experiencia retro arcade |
| [**05**](05-polish.md) | Pulido y trabajo paralelo | Usa flujos multiagente para mejorar UX, robustez y calidad |
| [**06**](06-bonus.md) | Bonus y extensiones | Explora funciones abiertas, flujos de compartición y experimentos extra |

---

## 💡 Consejos útiles

1. **Mantén el navegador abierto** — observa las actualizaciones en vivo mientras codificas.
2. **Haz commits con frecuencia** — guarda puntos de control limpios mientras iteras.
3. **Refina el plan antes de implementar** — mejores planes producen mejores resultados.
4. **Revisa los cambios de Copilot** — usa la vista de diff o las herramientas de revisión de la CLI en lugar de aceptar ciegamente.

<!-- track:vscode:start -->
5. **Usa checkpoints y Deshacer** en el chat si una iteración se desvía del rumbo.
<!-- track:vscode:end -->

<!-- track:cli:start -->
5. **Usa `/session`, `/context` y `/share file`** cuando quieras inspeccionar o preservar tu trabajo.
<!-- track:cli:end -->
