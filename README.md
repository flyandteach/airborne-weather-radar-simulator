# Airborne Weather Radar Simulator

A browser-based airborne weather radar simulator for pilot training. Open it
directly in any modern browser — no build step, no server, no dependencies
beyond an optional web font (it falls back to system fonts offline).

**Live page:** https://flyandteach.github.io/airborne-weather-radar-simulator/

## What it simulates

- TOP (plan), SIDE (vertical profile) and SPLIT radar views with animated sweep
- Working gain (−10…+10 dB and CAL), tilt (−15…+15°), 3.5° beam with 4/3-earth
  curvature, per-radial attenuation and radar shadowing, PAC alert
- WX / WX+T (turbulence to 40 NM) / MAP (ground-mapping) / STBY / OFF modes
- Predictive and reactive windshear, lightning, ground clutter and shadowing
- Nine training scenarios with deliberate tilt/gain traps, an instructor /
  debrief panel (including a Beam Painting & Formulas section), a G meter with
  structural-overload consequences, and an external "Aircraft & Weather"
  learning view showing true weather and the live radar beam

## Important

This is a **generic training approximation**. Beam width varies by radar and
antenna — commonly about 3° on large flat-plate antennas to 10° or more on
smaller ones; this simulator uses a fixed, representative 3.5° beam, so learn
the technique here and take the exact numbers from your own radar's manual.
Predictive-windshear ranges and thresholds, turbulence and structural values
are representative training values — they are **not** the specifications of the
RDR-4000 or any specific radar, and not a structural model of any specific
aircraft.

**Training aid only — not for navigation or operational use.**
