# Battlemap FX Editor

A browser-based WebGL battlemap editor for tabletop RPGs. It supports separate Master and Player views, dynamic effects, lighting, fog-of-war, drawing tools, sound effects, and timed scenarios.

## Planned features!

 - More effects
 - Camera effects (shaking, eg)
 - Water

   
For feature requests be free to write me on email!
garikmkrtchyan277353@gmail.com
Also, you can use telegram for feedback and feature requests!
My tg: @V1king_W

## Running the program

For best results, run the HTML file through a local web server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/battlemap_webgl_editor_v7_scenarios.html
```

Use **Open Player Window** to create the separate Player display.

## Basic controls

- Mouse wheel — zoom
- Right mouse / Middle mouse drag — pan
- Space + drag — pan
- `0` — Pan
- `1` — Select
- `2` — Wall
- `3` — Smoke
- `4` — Light
- `5` — Reveal fog
- `6` — Hide fog
- `7` — Fire
- `8` — Explosion
- `9` — Magic Burst

Effects can be configured in the **Inspector** before or after placement.

Objects can be selected and moved directly on the map. Walls, light radius, smoke/fire spread and drawing geometry can also be resized using their handles.

## Map

Use **Map / Grid** to:

- load a battlemap image
- set world size
- enable/disable the grid
- configure grid size and opacity
- fit the map to the screen

Master and Player have independent pan and zoom cameras.

## Effects

Available effects include:

- Smoke
- Fire
- Lights
- Wind
- Top-down rain
- Explosion
- Magic Burst

Walls can block both light and smoke.

Explosion and Magic Burst are temporary effects and automatically disappear.

## Fog of War

Use **Reveal Fog** and **Hide Fog** to paint visibility.

The circular cursor shows the current brush size.

Use:

- **Reset Fog** — cover the map again
- **Clear / Reveal All** — remove all fog

Fog visibility can be controlled independently for Master and Player.

## Layers

All placed objects appear under **Active Layers**.

Each layer can be:

- selected
- configured
- deleted
- shown/hidden on the Master screen
- shown/hidden on the Player screen

`M` controls Master visibility and `P` controls Player visibility.

## Drawing Tools

The editor supports:

- Text
- Lines
- Rectangles
- Circles
- Polygons

Drawing properties include:

- line width
- solid or dashed lines
- line color
- fill color
- transparency

For polygons, click to place vertices and press **Enter** or right-click to finish.

## Sound

The **Program Audio** section supports:

- Explosion
- Fire
- Rain
- Magic Burst
- Ambient sound

Sounds can be loaded from a URL or local audio file.

Volume and mute can be configured independently.

## Scenario Editor

Press **Scenario Editor** to open the timeline at the bottom of the Master window.

A scenario can schedule effects to appear and disappear over time.

You can:

- add Smoke, Light, Fire, Rain, Explosion and Magic clips
- capture an existing configured map layer
- drag clips along the timeline
- resize clips to change their duration
- configure exact start time and duration
- edit an effect using the normal Inspector
- set separate Master / Player visibility
- choose an effect position directly on the map
- duplicate or delete clips
- Play, Pause and Stop
- loop a scenario
- scrub through the timeline

Scenarios are saved separately from the map as:

```text
My_Scenario.scenario.json
```

Battlemap scenes and scenario files are independent, allowing multiple scenarios to be used with the same map.

## Saving

Use **Save JSON** to save the battlemap scene.

Use **Save Scenario JSON** inside the Scenario Editor to save a timeline separately.
