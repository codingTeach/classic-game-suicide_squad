# Game System

Capa de UI y pantallas. Contiene el bootstrap de la partida.

## Archivos clave
- `app.js` arranque principal del juego.
- `screens/` HTML de pantallas (index, create, game, worlds, diary, config).
- `ui/` HUD, router y componentes.
- `styles/` estilos globales y por pantalla.

## Router
`ui/router.js` maneja los botones con `data-route` y el back con `Esc`.

## HUD
`ui/hud/` monta y actualiza el HUD desde `app.js`.

## Flujo de pantallas
- `screens/index.html` -> menu principal.
- `screens/create.html` -> nueva expedicion.
- `screens/worlds.html` -> load/rename/borrar.
- `screens/game.html` -> escena A-Frame.
