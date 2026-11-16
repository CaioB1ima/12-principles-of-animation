# Character Animation — cycle breakdown

Practical notes for the walk cycle and jump in this folder.

## 1. Walk cycle (12 frames)

- **Anticipation:** frame 1 holds, then the body leans. Use a "counter"
  pose before the step.
- **Arcs:** the leg swings on an arc around the hip; the arm swings the
  opposite arc to counterbalance.
- **Follow-through:** the hair and coat continue to swing after the body
  stops.
- **Squash & Stretch:** body compresses slightly on the load phase, and
  elongates on the recovery.

## 2. Jump (8–12 frames, light)

- **Anticipation:** a slight crouch before takeoff.
- **Timing:** faster frames for the ascent, slower on the peak, faster
  descent, and a squash on landing.
- **Arcs:** the trajectory follows an arc.
- **Squash & Stretch:** body elongates on the ascent; squash on landing.

## 3. Blocking notes

1. Block the extreme poses (start, peak, landing).
2. Add the intermediate poses and the timing.
3. Refine the stretch and squash.
4. Add secondary action (hair, coat, breath).

## Files

- `README.md` — this file
- `cycle.md` — detailed cycle breakdown
