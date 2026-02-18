# Game (MVP A-Frame)

`game/` es la fuente de verdad del proyecto. Todo lo jugable y mantenible vive aqui.

## Objetivo
- MVP 3D en navegador con A-Frame.
- Datos versionados en JSON dentro de `game_data/`.
- Motor y UI desacoplados, sin bundler.

## Estructura
- `game_data/` datos, assets, modos, dificultades y mundos.
- `game_engine/` motor (core, generacion, sistemas, render, mundo).
- `game_system/` pantallas, UI, router y `app.js`.
- `tools/` utilidades (server local, validacion assets).
- `docs/` documentacion del proyecto.

## Inicio rapido
1. Levanta el server local.
2. Abre el menu principal.
3. Inicia una partida nueva o carga la ultima.

```powershell
node game/tools/dev_server.js
```

```text
http://127.0.0.1:5501/game/game_system/screens/index.html
```

## Controles (MVP)
- `WASD` mover.
- Mouse: mirar.
- Click izquierdo: disparar.
- Click derecho: dash/teleport corto.
- `Shift` sprint.
- `E` recoger item cercano.
- Rueda del mouse: cambiar slot del inventario.
- `1-9` seleccionar slots.
- `Esc` pausar / volver.

## Guardado
- Autosave y guardado manual en `localStorage`.
- Se persiste: mapa, altura, items, enemigos, vida, intentos, puntaje.

## Notas
- A-Frame se carga por CDN (sin bundler).
- `engine_basics/` solo referencia historica.
