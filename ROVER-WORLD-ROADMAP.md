# Rover World: staged interaction roadmap

This roadmap grows the existing drivable rover world in small, reversible increments. The guiding principle is to make every new object useful as orientation, story, portfolio discovery, or playful feedback before adding more simulation complexity.

## Design principles

- Keep the portfolio content discoverable without requiring visitors to play. Every important project, skill, and contact path should remain available through readable panels and ordinary page navigation.
- Prefer one interaction system at a time. Each stage should ship with a reset/respawn path, a clear visual affordance, keyboard support where practical, and a lightweight fallback for reduced-motion or low-power devices.
- Use physical placement as wayfinding: paths guide movement, boundaries frame zones, and panels provide concise explanations. Do not hide essential information behind collision puzzles.
- Start with simple collision primitives and mostly static objects. Add heavier physics only after the interaction has proved useful; keep inactive objects asleep and load detailed assets by proximity.

## Stage 0 — establish the world contract

**Goal:** make the current rover world dependable before adding content.

1. Define named zones for the existing base, checkpoint route, project area, and map/telemetry area.
2. Standardize object metadata: `id`, `zone`, `label`, `interaction`, `asset`, `collision`, and `reducedMotionFallback`.
3. Add a consistent interaction prompt, respawn/reset action, and a small help panel listing drive, brake, boost, map, interact, and respawn controls.
4. Add a debug-only object bounds mode so placement and collision errors can be corrected without changing the visitor experience.

**Exit check:** a visitor can always understand where they are, what can be interacted with, and how to recover from a stuck rover.

## Stage 1 — readable landmarks and project kiosks

**Goal:** turn the existing world into a navigable portfolio index.

- Add three to five large, low-poly landmarks: a base mast, a project archive sign, a skills beacon, and a contact/links station.
- Give each landmark a high-contrast sign visible from the approach direction. Entering a small trigger zone opens a concise HTML project panel with a close button and ordinary links.
- Add a compass or minimap marker for each zone, but keep the landmark itself as the primary cue.
- Use camera easing/zoom only while opening a panel; never take control away without an obvious escape key or close control.

**Exit check:** the rover can reach a project from the map and from physical signage, and the same project remains accessible in the non-3D page.

## Stage 2 — bumpable playground objects

**Goal:** add Bruno-Simon-style physicality without turning the portfolio into a physics demo.

- Introduce a small set of colorful crates, cones, balls, or rover-safe barrels near a dedicated playground zone.
- Use simple boxes/spheres for collision and sleeping bodies for objects that are not moving. Cap velocities and add a reset when an object leaves the playable bounds.
- Give objects subtle audio/visual feedback only after user interaction; respect reduced-motion and muted-autoplay constraints.
- Add a “playground” achievement for discovering the zone, not for requiring a difficult maneuver.

**Exit check:** objects feel responsive, remain performant on mid-range hardware, and cannot block access to portfolio content.

## Stage 3 — collectibles, achievements, and route feedback

**Goal:** reward exploration while keeping it optional.

- Place a small number of clearly signposted tokens representing portfolio themes: build, learn, compete, and share.
- Store progress locally and expose a visible achievements panel with a reset-progress action.
- Add checkpoint beacons that record the last safe location. Make checkpoint completion readable on the map and in the regular page UI.
- Use short feedback animations and text rather than constant particles or heavy effects.

**Exit check:** exploration has a satisfying loop, but no important information is permanently missable.

## Stage 4 — gates, circuits, and time trials

**Goal:** create a compact optional challenge inspired by Bruno Simon’s circuit/time-trial structure.

- Add one short loop with a start gate, three to five checkpoints, and a finish board.
- Show the current time, best local time, and a calm reset/respawn option. Never make the timer run while the visitor is reading a project panel.
- Keep the route physically obvious with paint, arrows, flags, or light poles; avoid invisible walls.
- Load the circuit props only when the rover enters the zone and unload or sleep them after leaving.

**Exit check:** the time trial is replayable, understandable in under a minute, and does not interfere with ordinary browsing.

## Stage 5 — richer project spaces and camera transitions

**Goal:** make selected projects feel like places without building a separate game.

- Give two or three flagship projects a small “room” or outdoor vignette: a workbench, a rover test pad, or a document wall.
- Use a controlled camera transition to frame the project artifact, then return the camera to the rover with an explicit close action.
- Combine physical props with concise text panels, image/video thumbnails, and links to the existing project log.
- Gate high-detail models, videos, and audio by proximity and provide a lightweight placeholder while they load.

**Exit check:** the 3D scene adds context and delight while the page remains fast, accessible, and easy to scan.

## Stage 6 — polish, accessibility, and measurement

**Goal:** turn the growing world into a maintainable feature rather than an expanding one-off demo.

- Add keyboard/controller mappings, focus management for every HTML panel, screen-reader labels for map and interaction controls, and a reduced-motion mode.
- Measure load cost, frame rate, memory, input errors, and interaction completion. Test with the rover disabled, on touch devices, and on low-power hardware.
- Keep a small object budget per zone and document asset dimensions, collision complexity, and fallback behavior.
- Add a content-authoring checklist so new objects can be added from data rather than bespoke renderer code.

**Definition of done:** every object has a purpose, a readable label, a safe collision model, a fallback, and a way to reset or leave it.

## Suggested implementation order

1. Zone/object data contract and reliable reset behavior.
2. Project kiosks and landmark signage.
3. Small playground with bumpable props.
4. Collectibles and achievements.
5. One optional circuit/time trial.
6. Flagship project vignettes and camera framing.
7. Performance, accessibility, and authoring polish after each stage—not only at the end.

This sequencing follows Bruno Simon’s useful pattern of a readable world with paths, boundaries, panels, interactive zones, achievements, circuits, and camera transitions, while keeping the existing portfolio’s ordinary navigation and content as the dependable primary experience.
