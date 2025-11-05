# DESIGN: Reaction Tapper

## Visión
Juego móvil de reacción para sesiones cortas (30–60s). Mecánica simple: toca el objetivo que aparece; cuanto más rápido, más puntos; la frecuencia aumenta para hacer el juego adictivo.

## Mecánica principal (MVP)
- Escena principal:
  - Objetivo aparece en posiciones aleatorias.
  - Jugador toca el objetivo => +1 punto, efecto visual/sonoro, objetivo respawnea.
  - Temporizador de la partida (TimeLeft) de 30s por defecto.
  - SpawnInterval disminuye ligeramente con cada acierto (dificultad escala).
- Game over: mostrar puntuación, botón de reiniciar y opción de compartir.

## Variables principales
- Score (entero)
- TimeLeft (entero, segundos)
- SpawnInterval (float, segundos; p. ej. inicial 1.0s)
- HitCount (entero, opcional)
- BestScore (guardado local)

## UI
- Pantalla de inicio: título, botón Start, best score visible
- In-game: timer grande, score, pausa
- Game Over: score final, best score, share, restart

## Dificultad y balance
- SpawnInterval inicial = 1.0s
- Al acertar: SpawnInterval = max(0.35, SpawnInterval - 0.03)
- Opcional: combos que dan puntos extra si aciertas consecutivamente rápido

## Sonido y feedback
- Sonido pop al tocar objetivo
- FX corto al fallar (si detectas un toque fuera)
- Animación de escala + brillo del objetivo al tocar

## Guardado y analítica
- Guardar BestScore en almacenamiento local (LocalStorage / device storage)
- Analytics opcional: Firebase Analytics para eventos (game_start, game_over, score)

## Monetización (opcional posterior a MVP)
- Ads (intersticials entre partidas)
- Comprar remover anuncios (IAP)
- Tabla de clasificación con Game Center (recomendado para iOS)

## Roadmap MVP (7 días)
Día 1: Crear repo, README, DESIGN.md, assets placeholders, configurar GDevelop  
Día 2: Prototipo core (spawn, touch, score, timer)  
Día 3: Ajuste de dificultad, feedback visual y sonidos  
Día 4: UI (pantalla inicio, pause, game over)  
Día 5: Testing en dispositivo y bugfixes  
Día 6: Añadir best score guardado local y share button  
Día 7: Preparar export, documentación y testflight notes

## Backlog (post-MVP)
- Integrar Game Center leaderboards
- Analytics avanzadas y A/B test de colores/dificultad
- Mejorar arte y añadir más modos (endless, timed)
