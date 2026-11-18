# FLEXO Plate travel

A one-file simulator of how far the end of a flexo print repeat moves when the plate cylinder, its temperature, the plate or the mounting tape is off the standard.

- **Simulator:** [FLEXO_PLATE_DRIFT.html](https://magicphase.github.io/Flexo_Drift_Sim/FLEXO_PLATE_DRIFT.html)
- **Demo walkthrough:** [FLEXO_PLATE_DRIFT_DEMO.html](https://magicphase.github.io/Flexo_Drift_Sim/FLEXO_PLATE_DRIFT_DEMO.html)

![The four sliders, explained](FLEXO_PLATE_DRIFT_DEMO_files/slide-2.png)

## The simulator

Type a tooth count, pick steel or aluminium, and move four sliders:

| Slider | What it is |
| --- | --- |
| Cylinder BCD | The bare cylinder diameter as measured, against the standard BCD |
| Cylinder temperature | How much warmer or colder the cylinder runs than when it was measured |
| Plate thickness | The plate on the cylinder |
| Mounting tape | The tape under the plate |

Each row shows the change, a bar on one shared short / long scale, and the travel at the end of the repeat in inches and thousandths (or millimetres and micrometres). Each slider has its own reset button. Below the rows:

- **At the end of the repeat:** a magnified view with the standard in grey and the four changes together in black, in six test patterns. On the two rosettes the view splits: standard on the left, as set on the right.
- **The stack:** the standard build-up beside the one as set, drawn to scale, with the four changes together as one figure.

It is a single HTML file with nothing to install. It loads nothing and saves nothing. Add `#example` to the address to open it with a small example set, or `#light` for the light theme.

## The demo

Six stops over a light screenshot of the simulator: the page dims, one part stays lit, and a few bubbles explain it. Move with the ← → keys, the Back and Next buttons, or the numbered dots. The same six stops are in `FLEXO_PLATE_DRIFT_DEMO_files/` as images, `slide-0.png` to `slide-5.png`.

The demo is a picture of the simulator, not the simulator: its sliders do not move.

## What the figures assume

- **A fixed gear.** The repeat is the tooth count times the circular pitch (0.125"). The gear sets how fast the cylinder turns, and the art keeps its length at the plate's backing. Anything that lifts the backing further from the centre prints short; anything that lowers it prints long.
- **The standard stack** is a 0.067" plate with a 0.005" backing on 0.015" tape. The standard BCD is the cylinder diameter that puts that plate's face on the gear's pitch line.
- **Art made for the plate in use.** A thicker plate carries shorter art, so on a cylinder cut for the standard plate it prints short.
- **Only the cylinder grows with heat:** 6.5 × 10⁻⁶ per °F for steel and 13.1 × 10⁻⁶ per °F for aluminium.

These are a model for showing which factor matters most, not a measurement of any press.
