# Feature name
Cosmic Toaster

## Feature description
The Cosmic Toaster is a kitchen device that launches bread into “interstellar crisp mode,” producing toast that allegedly tastes like starlight. The user inserts bread, presses the Warp Toast button, and the toaster performs a sequence of theatrical sci‑fi operations before ejecting the toast with a dramatic “whoosh.”

## Steps (funny, auditable, and intentionally odd)
User inserts bread into the Quantum Slot.

Device scans the bread for “cosmic potential.”

If cosmic potential is low, the toaster plays motivational audio to encourage the bread.

The Warp Toast button is pressed.

The toaster begins micro‑warp oscillation, shaking slightly and glowing purple.

A tiny hologram of a star appears above the toaster and narrates the toasting process.

Toast is launched upward with a gentle “photon‑powered pop.”

Device logs the toasting result into warp-toast-log.txt.

## Bugs present
Bug 1: Toast occasionally launches too high, hitting the underside of kitchen cabinets.

Bug 2: Motivational audio sometimes plays after the toast is already finished, confusing users.

Bug 3: The hologram star occasionally mispronounces “photon,” saying “potato” instead.

Bug 4: The purple glow sometimes persists for several minutes after toasting, alarming pets.

## Current testing status
Only end‑to‑end testing exists.
There is no unit testing for individual components (e.g., cosmic potential scanner, hologram star narrator).
There is no integration testing for multi‑component interactions (e.g., warp oscillation + hologram narration).
E2E tests simply run the full toasting cycle and confirm toast appears.

## Notes for future agents
E2E tests do not detect the mispronunciation bug.

No logs exist for motivational audio timing.

The launch‑height bug is only detected when cabinets are present, making tests inconsistent across environments.