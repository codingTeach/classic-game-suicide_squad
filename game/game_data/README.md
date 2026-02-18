# Game Data

Datos y assets del juego. Todo es consumido via `fetch` desde el navegador.

## Carpetas
- `assets/` modelos GLB, audio, texturas.
- `items/` items versionados y `latest.json`.
- `entities/` jugadores, enemigos, bots.
- `modes/` reglas de modos de juego.
- `difficults/` escalado de dificultad.
- `worlds/` mundos predefinidos.
- `config/` parametros de gameplay.
- `schemas/` schemas JSON basicos.
- `profiles/` datos de perfiles y logros.

## Convenciones
- Cada item/enemigo debe tener `asset` valido.
- Los IDs se usan como clave estable.
- Los mundos guardan `width`, `height`, `wallHeight`.
