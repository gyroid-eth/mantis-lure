# Mantis Lure

[日本語](README.md) / **English**

A single-file, browser-based **lure for a live praying mantis**. Lay a tablet flat, drive the on-screen
prey with the thumbstick and the A/B/C/D buttons, and let the mantis hunt it through the glass. Prey
size, speed, colour and contrast are parametric; every strike can be logged and exported as CSV.
No build step, no dependencies — just open `index.html`.

**▶ Live demo: https://gyroid-eth.github.io/mantis-lure/**

![The app in use — a housefly on a plain bright field](screenshots/hero.png)

## The design problem

One screen, two audiences with completely different visual systems.

A mantis responds to a **small dark shape moving on a plain bright field**. Decoration is noise to it.
Its keeper is the opposite: without decoration there is nothing to look at. Mixing the two muddies both.

So the two are kept physically apart. Inside the field there is nothing but the background and the prey.
Every instrument, button and number lives outside it, in the metal frame — and the console sits along the
**top edge**, so your hand never crosses the stimulus while you play.

![The console](screenshots/console.png)

## Prey

![The four prey](screenshots/prey.png)

| Species | How it moves |
|---|---|
| Housefly (イエバエ) | Never quite still. Wings beat even while it hovers |
| Grasshopper (ショウリョウバッタ) | Big hops, long waits |
| Cricket (エンマコオロギ) | Short quick hops, straight on to the next |
| Jumping spider (ハエトリグモ) | Scuttles, then freezes dead still |

The artwork is SVG with **one path per body part** — abdomen, wings, legs, antennae — each with its own
pivot. Parts are rotated at runtime, so the wingbeat and the leg cadence follow the speed. Movement, not
shape, is what releases a strike, so the prey is never a rigid stamp.

## Controls

| Control | What it does |
|---|---|
| Thumbstick | Moves the prey. How far you push is how fast it goes |
| Drag on the field | Pulls the prey to your finger |
| **A** | Buzz — shudder in place |
| **B** | Flee — bolt away |
| **C** | Hold — freeze |
| **D** | Loom — swell towards the viewer |
| 手動 / 徘徊 / らせん | Who decides where it travels: you, the prey, or a fixed spiral |
| 襲った | Log a strike under the current conditions |

The keyboard works too (arrows, space/A, B, C, D). Speed is shown as a meter rather than a number; the
green band marks where the reported values cluster (45–120 °/s, converted at a 10 cm viewing distance).

**手動 / 徘徊 / らせん** only chooses who steers. Each species' own motion — the fly's tremor, the
grasshopper's hop, the spider's freeze — runs in every mode. In 手動 the prey keeps an anchor that only
you move, so it stays where you put it and misbehaves on the spot.

## On a phone

A narrow screen cannot hold the console along the top, but the rule that a hand must never cross the
stimulus still stands. So the **stick and the A/B/C/D buttons pin themselves to the bottom edge** — out of
the field, and where your thumbs already are — while the top strip keeps only the selectors and the
instruments. The language switch sits at the top right (**EN / 日本語**) and is remembered on the device.

<img src="screenshots/phone.png" width="380" alt="The narrow-screen layout">

## Calibration, and why there is no viewing-distance setting

![Calibration with the on-screen ruler](screenshots/calibration.png)

An early version had a *viewing distance* slider. It was a lie: where the mantis sits is not something
the software decides, and it changes as the animal walks. So this app only controls what it can actually
put on the glass — **a length in millimetres and a speed in millimetres per second**. Angles are reported
as conditional references at a stated distance, and the settings panel carries a conversion table
(5 cm → 29°, 10 cm → 15°, …). When you can measure the distance at which a strike happened, read that row.

**Millimetres are only millimetres once calibrated**, because on-screen length depends on the device's
pixel density. Open the settings and a **ruler appears along the bottom of the field**: lay a real ruler
against it and move the slider until the graduations line up. Picking your device from the preset list is
usually good enough. The value is stored on the device.

## Where the defaults come from

| Setting | Default | Basis |
|---|---|---|
| Size | 26 mm (≈15° at 10 cm) | Strongly species-dependent. *Sphodromantis lineola* strikes most at 10–20° (an inverted U); *Parasphendale affinis* peaks at a 9° disc with a 6.9° threshold; *Popa spurca* keeps increasing up to 44°. [Prete et al. 2013](https://doi.org/10.1242/jeb.089474) |
| Speed | 140 mm/s (≈80 °/s at 10 cm) | Reported figures are experimental *conditions*, not measured optima: 74–180 °/s in [Prete et al. 2013](https://doi.org/10.1242/jeb.089474), 82 °/s as the model input in [O'Keeffe et al. 2022](https://doi.org/10.1371/journal.pcbi.1009666) |
| Contrast | Dark prey on a bright field | All three species struck more at a dark target on white than at the reverse. [Prete et al. 2013](https://doi.org/10.1242/jeb.089474) |
| Colour | Presentation only | No behavioural evidence was found that wavelength matters independently of luminance. Receptor spectral sensitivities are known ([Zhu et al. 2025](https://doi.org/10.1007/s00359-025-01776-z)), which is a different claim |
| **D** (loom) | Smooth expansion | An expanding luminance edge drew ~60% strikes; holding size constant and moving only disparity dropped it to 15–35%. [Nityananda et al. 2019](https://doi.org/10.1242/jeb.198614) |

A stepped loom (0.85 s per step) is offered as an alternative, because the "at least 0.8 s per step"
result could not be traced to a readable primary source. Which one works is something you can test on
your own animal.

The full survey, including what could **not** be verified, is in [`docs/RESEARCH.md`](docs/RESEARCH.md).

## Recording

**襲った** logs one row with everything that was set at that moment: species, size in mm, the 10 cm
reference angle, commanded and observed speed, target and background colour, Michelson contrast, motion
mode, loom style, and whether the screen was calibrated. Settings → RECORD → CSV を書き出す exports them.

To start the count again, press the strike counter twice — the first press only arms it, and it disarms
after four seconds. **Export before you clear.**

## Caveats

- **The mantis will lunge at the screen.** Use a protective glass and set the tablet down so it cannot fall.
- An LCD is built for human trichromatic vision. It has no UV, and whether its refresh rate reads as
  flicker to a mantis is unresolved — critical flicker fusion in related species straddles 60 Hz. If your
  animal ignores a stimulus that should work, the display itself is a suspect.
- **This is not food.** It is a toy and an observation instrument; nothing here feeds the animal.

## Development

Everything is in `index.html` — markup, styles, logic, and the prey artwork as path data. Open it, or
serve the directory (`python3 -m http.server`) and point a tablet at it over the LAN.

## License

MIT
