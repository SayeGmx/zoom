# ZOOM!~ v0.2 — Overlay + Control Panel

## Arranque

```powershell
npm.cmd install
npm.cmd run dev
```

## URLs

- Control Panel: `http://localhost:5173/control`
- Overlay para OBS: `http://localhost:5173/overlay`

OBS debe usar solamente `/overlay`.

## Arquitectura

El proyecto separa el HUD de la aplicación de control. Ambos comparten estado y configuración mediante `localStorage` + eventos de sincronización; el Overlay escucha el WebSocket local de TikFinity en `ws://127.0.0.1:21213/`.

El parser reconoce `arriba`, `ariba`, `ariva`, `arriva`, `up`, `↑`, `⬆️` y `abajo`, `abaho`, `down`, `↓`, `⬇️`.

La zona segura viene pensada para el formato vertical de TikTok y se puede ajustar desde el panel.

## Próxima iteración

1. Ajustar el parser al payload real de tu TikFinity.
2. Sustituir el placeholder de movimiento por tu vampirito/asset transparente.
3. Añadir sonidos, combos y cierre automático de ronda.
4. Añadir presets y hotkeys.
