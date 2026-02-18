# Game Engine

Modulo de motor para el MVP. Todo es ES Modules.

## Carpetas
- `core/` loop de tiempo, bus de eventos, config, logger.
- `data/` rutas, loader JSON, validacion ligera.
- `generation/` generacion de mapas y spawns.
- `render/` adaptadores A-Frame, cache de assets, culling.
- `world/` estado del mundo, loader, saver, sistemas.
- `behaviors/` comportamientos y helpers AI.
- `network/` reservado para multi-player y sync.

## Flujo general
1. `game_system/app.js` carga datos y crea `worldState`.
2. Se crea escena A-Frame con `render/aframe_adapter.js`.
3. Se inicializan sistemas: movimiento, colisiones, AI, items, spawn.
4. `core/time.js` ejecuta el tick principal.

## Sistemas importantes
- `world/systems/movement_system.js`
- `world/systems/collision_system.js`
- `world/systems/ai_system.js`
- `world/systems/item_system.js`
- `world/systems/spawn_system.js`

## Agregar un sistema
1. Crea el archivo en `world/systems/`.
2. Exporta una funcion `createXSystem`.
3. Inicializalo en `game_system/app.js`.
4. Llamalo en el loop si requiere `update`.

## Datos
El motor consume JSON desde `game_data/`. Ver `docs/data_formats.md`.
