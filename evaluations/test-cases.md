# Evaluation test cases — 12 Principles

A set of reproducible tests to validate an animation against the 12
principles. Run these before a release or milestone.

## Before you start
- Record a screen capture for every test.
- Play on the target device and in the target environment.
- Use the rubric in `evaluation-criteria.md`.

## Test cases

| # | Test | Steps | Pass criteria | Fail indicator |
|---|---|---|---|---|
| T1 | Squash and Stretch | Press a button; watch its scale | Button compresses on press and springs on release, with constant volume | Rigid press, no squash/stretch, or volume changes |
| T2 | Anticipation | Hover a button | There is a preparatory movement before the main click | No wind-up; button jumps straight to the clicked state |
| T3 | Staging | Open a page; note first focus | The eye lands on the primary action first | Two competing focal points |
| T4 | Straight Ahead / Pose to Pose | Play a subtle page transition | Motion is smooth, no frame-jumping, no proportion drift | Jittery, proportion jump, or odd looping |
| T5 | Follow Through and Overlapping | Scroll and release | Elements settle, do not float; text/picture lag | Elements continue racing or don't settle |
| T6 | Slow In and Slow Out | Play enter & exit | Entrance is ease-out, exit is ease-in; no linear | Linear or "staccato" timing |
| T7 | Arcs | Trace any curved UI motion | Motion follows a logical arc | Straight-line or erratic curves |
| T8 | Secondary Action | Open a card | Secondary motion supports the main action | Secondary motion dominates or contradicts |
| T9 | Timing | Measure durations | Durations match intent; 60 fps; no dropped frames | <60 fps, or durations randomly too short/long |
| T10 | Exaggeration | Inspect a hero animation | Presentation is clear, not confusing | Cluttered or over-exaggerated |
| T11 | Solid Drawing | Silhouette test (remove colors) | Core shape is legible | Silhouette unrecognizable |
| T12 | Appeal | Ask a user | Interface feels pleasant, intuitive, clear | Frustrating, unclear, or robotic |

## Pass/fail scoring
- Each test is Pass / Fail / Borderline.
- **12/12** = Production-ready.
- **10–11** = Shipped.
- **7–9** = Work in progress.
- **<7** = Hold.

## Running the suite
1. Review `evaluation-criteria.md` for the rubric.
2. Pick the tests relevant to your build.
3. Record and score each test.
4. Re-run until the target score is reached.
