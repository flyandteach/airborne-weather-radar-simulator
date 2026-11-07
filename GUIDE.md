# The Storm Your Radar Isn't Showing You

*Adapted from the LinkedIn article of the same name. A guide to the free
Airborne Weather Radar Simulator — what it teaches, how to use it, and the
tips that transfer to the airplane.*

**Try it:** https://flyandteach.github.io/airborne-weather-radar-simulator/
**Source:** https://github.com/flyandteach/airborne-weather-radar-simulator

---

Every pilot has heard the statistic in some form: weather is unforgiving of poor judgment, and the accidents rarely happen to pilots who saw the storm clearly and early. Yet the tool we rely on most to see weather — the airborne radar — is one of the least intuitively understood instruments in the cockpit. It does not show you "the weather." It shows you a thin, tilted slice of the sky, painted according to physics that can hide a mature thunderstorm completely if your tilt is a few degrees off.

I know, because the first scenario in the simulator I built does exactly that. You start at FL350, tilt +2°, looking at an empty scope — while a 37,000 ft cumulonimbus sits 55 NM ahead, tall enough to top your altitude by 2,000 ft. The beam is passing clean over it. Nothing is wrong with the airplane. Nothing is wrong with the radar. The picture is a lie told by geometry.

That is why I built this tool, and why I'm making it freely available.

## What it is

The Airborne Weather Radar Simulator runs in any browser, no install, no account. It models a generic airborne weather radar honestly: a 3.5° beam with 4/3-earth curvature, tilt from −15° to +15°, gain from −10 to +10 dB with a calibrated detent, per-radial attenuation with true radar shadowing (a strong cell blacks out everything behind it, weather and ground alike), PAC alerting, turbulence detection limited to 40 NM as on real sets, predictive and reactive windshear, lightning activity, and a ground-mapping mode.

You get three views — the classic top-down navigation display, a side vertical profile, and a split view — plus an external "Aircraft & Weather" learning view that shows your airplane, the actual storms, and the live radar beam in 3D, so you can *see* which slice of the sky your radar is painting. An instructor panel scores your technique and includes a Beam Painting section that shows, at your current settings, exactly which altitudes your beam covers at 5, 10, 20, 40, 80, and 160 NM.

There are nine scenarios: an isolated thunderstorm, a squall line with a tempting gap, a supercell, thunderstorms embedded in stratiform rain, a microburst on approach (wet and dry), tropical rainbands, a frontal system, winter weather, and a storm that builds from 26,000 ft to 43,000 ft in front of you. Each has a briefing, a deliberate trap, and a challenge to pass.

## Basic instructions

1. Open the simulator and leave everything at its defaults. You are in the Isolated Thunderstorm scenario, in split view.
2. Look at the SIDE view first. It shows the truth: your beam as a wedge, the storm in profile, and whether the two intersect. This is your teacher.
3. Now fix the TOP view using tilt alone. Lower the tilt until the storm paints — then keep going a little and watch the ground start to paint as the beam's lower edge reaches the earth. Find the tilt where the storm is fully painted and the ground isn't.
4. Change one control at a time. Gain up: weak returns fatten and can look threatening. Gain down: embedded cores hidden in stratiform rain separate out. Range out: watch attenuation carve the far side of a strong cell into a lens shape and erase what's behind it.
5. Use the flight controls to deviate around weather, change altitude, and try the approach scenario at 1,500 ft. Mind the G meter — fly into a severe core and the simulator will show you, bluntly, what structural limits mean. Restart begins paused at 1× speed so you can think before it happens again.
6. Read the debrief after every run. It tells you whether you were painting the storm's core, its top, or mostly sky — and the tilt that would have centered the beam.

## Five tips that transfer to the airplane

- **Do the beam math in your head.** Beam center height ≈ your altitude + 100 × range in NM × tilt in degrees. At 40 NM, each degree of tilt moves the beam center about 4,000 ft. The beam is roughly 350 ft thick per NM of range — at 80 NM it's painting a slab nearly 28,000 ft deep. "Where is my beam?" should be a continuous question.
- **An empty scope is information about your tilt, not about the sky.** Overshooting at altitude and undershooting on approach are the two classic errors. When in doubt, sweep the tilt slowly and watch what appears — then ask why it wasn't there before.
- **Black behind red is a warning, not an absence.** If a strong cell shows a clean black wedge behind it, that's attenuation shadow: the radar is blind there, not clear. Deviate around the shadow, not through it.
- **Gain is a scalpel, not a volume knob.** Calibrated gain is home. Reduce gain to find the hardest core inside a blob; increase it briefly to check for weak building cells — then return to CAL before you judge distances.
- **Respect what turbulence mode can't see.** Turbulence detection only works where there's precipitation to measure, and only out to about 40 NM. A dry microburst can show as a weak green smudge — the windshear scenario's dry toggle demonstrates why the shear alert, not the paint, is what saves you.

## An honest limitation

This is a generic training approximation. Beam width is a property of the specific radar and antenna installed in an aircraft — it varies by device, commonly from about 3° on large flat-plate antennas to 10° or more on smaller ones — and it matters: beam width sets how thick the sampled slice of sky is at any range, how sharply cells are defined, and how much of what you see is weather versus beam-filling smear. This simulator uses a fixed, representative 3.5° beam; your aircraft's radar will differ, and with it the exact tilt technique and the numbers in the beam math above. The same applies to its windshear thresholds and its turbulence and structural values — representative training numbers, not the specifications of any particular radar or airframe. Use the simulator to build the mental model and the habits; use your aircraft's radar manual for the values. It is a training aid, not a substitute for that manual, your operator's procedures, or formal instruction.

It has also been tested the way I'd want any training tool tested: two full independent review passes, every control exercised, the math checked by hand, and the failure modes forced rather than assumed. The source is open on GitHub — read it, fork it, improve it.

## Try it

Simulator: https://flyandteach.github.io/airborne-weather-radar-simulator/
Source code: https://github.com/flyandteach/airborne-weather-radar-simulator

Start with Scenario 1. When the scope is empty and the side view is showing you a storm your radar insists isn't there, you'll understand the entire point.
