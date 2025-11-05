# Reaction Tapper

Reaction Tapper es un juego rápido y adictivo para iOS que pone a prueba la velocidad de reacción del jugador. El MVP es una pantalla única: aparece un objetivo aleatorio, el jugador toca lo más rápido posible, la frecuencia aumenta y la partida dura 30–60s.

## Contenido del repositorio
- README.md (este archivo)
- DESIGN.md (diseño del juego y backlog)
- GDevelop-Instructions.md (guía paso a paso para implementar el prototipo en GDevelop)
- .gitignore
- LICENSE (MIT)
- /assets (placeholders y nombres sugeridos)
- ISSUES.md (lista de issues sugeridos para crear en GitHub)

## Requisitos mínimos para el desarrollo
- Para el prototipo: GDevelop (gratuito, multiplataforma) o cualquier editor de juegos 2D.
- Para exportar a iOS: Mac con Xcode y cuenta Apple Developer (99 USD/año) para TestFlight/App Store (ver sección Exportar a iOS).

## Cómo usar este repo
1. Crea el repositorio en GitHub (nombre recomendado: `reaction-tapper`) y añade estos archivos.
2. Abre GDevelop y sigue GDevelop-Instructions.md para construir el prototipo.
3. Testea en móvil (previsualización de GDevelop) y ajusta parámetros en DESIGN.md.
4. Para exportar a iOS, genera el build desde GDevelop/Cordova y abre el proyecto en Xcode para firmar/subir a App Store Connect.

## Exportar a iOS / TestFlight (resumen)
1. Necesitas Mac + Xcode + Apple Developer account.
2. Exporta desde GDevelop a formato compatible (Cordova / Xcode) o usa el servicio de exportación de GDevelop.
3. Abre el proyecto en Xcode, ajusta signing (tu Team), incrementa versión/build.
4. Archive y sube a App Store Connect → TestFlight → invitar testers.

## Contribuciones
- Fork y PR bienvenidos.
- Revisa ISSUES.md para tareas sugeridas.
- Usa el milestone "MVP" para PRs relacionados con el MVP.
