---
name: 12-principles-of-animation
description: >
  Execution skill for animation agents. Identifies the task type, selects
  the relevant principles of animation, applies them to the context, generates
  a solution, and self-evaluates against defined criteria. Includes the full
  12 Principles of Animation reference and an evaluation rubric.
category: creative
tags: [animation, principles, disney, agent-framework, execution, motion, evaluation]
version: 2.0.0
author: CaioBLima
homepage: https://pt.wikipedia.org/wiki/12_princ%C3%ADpios_b%C3%A1sicos_de_anima%C3%A7%C3%A3o
---

# 12 Principles of Animation — Agent Execution Skill

## What this skill does

This skill turns the **12 Basic Principles of Animation** into a repeatable
workflow for an AI animation agent. Every time the agent receives an
animation request, it follows a **5-step loop**:

1. Identify the type of task
2. Select the relevant principles
3. Apply them to the context
4. Generate a solution
5. Evaluate the result using defined criteria

The agent then keeps its own results against a self-assessment checklist.

---

## The 5-Step Workflow

### Step 1 — Identify the type of task

Classify the request into one or more task types:

| Task type | Examples | Primary mediums |
|---|---|---|
| **UI / web animation** | Components, transitions, micro-interactions | Web, CSS, GSAP |
| **Character animation** | Poses, walk cycles, expressions | 2D, 3D, Blender, Spine |
| **Motion graphics / brand** | Logo reveal, kinetic typography | After Effects, GSAP, HTML/CSS |
| **Video / film** | Short film, product video, explainer | Motion design, video generation |
| **Game animation** | Character, gameplay, UI, mechanics | Unity, Godot, Unreal |

For the chosen type, the agent notes:
- **Medium** — web, video, 2D, 3D, game, etc.
- **Tool / path** — CSS, GSAP, Blender, After Effects, video-generation
  prompt, etc.
- **Constraints** — duration, resolution, framerate, file size, performance.

### Step 2 — Select the relevant principles

From the 12 principles, select the ones that matter for this task type.
Use the table below as a guide, then refine with reasons.

| Task type | Principles to prioritise |
|---|---|
| UI / web | Staging, Timing, Arcs, Slow In & Slow Out, Appeal |
| Character | Anticipation, Arcs, Solid Drawing, Appeal, Timing |
| Motion graphics | Timing, Arcs, Appeal, Staging, Exaggeration |
| Video / film | Staging, Anticipation, Timing, Arcs, Appeal |
| Game | Timing, Anticipation, Follow Through, Solid Drawing, Appeal |

The agent must output **which** principles it selected and **why**.

### Step 3 — Apply them to the context

For each selected principle, the agent defines the concrete parameters:

- **What** is affected in this task?
- **How** is it applied? (e.g. easing curve, duration, scale factor, arc
  degrees)
- **What is the expected effect?**

Example (UI button press):

| Principle | Application |
|---|---|
| Squash and Stretch | button scale 0.92–0.98 on press, transform-origin centre |
| Anticipation | 100ms hover lift before the click |
| Timing | press 200ms, spring return |

### Step 4 — Generate a solution

Produce the concrete artifact. Depending on the task type:

- **Code:** HTML/CSS/JS, GSAP, Blender script, After Effects script, etc.
- **Prompt:** a video/film generation prompt, script, storyboard, or shot
  list.
- **Plan:** a prototype, asset list, or shot plan when no code exists yet.

The solution must be **complete and directly usable** (not a sketch).

### Step 5 — Evaluate the result

The agent self-assesses the generated solution using the rubric below:

| Score | Meaning |
|---|---|
| 1 | Missing or actively harmful |
| 2 | Clearly failing |
| 3 | Inconsistent / borderline |
| 4 | Generally present, minor issues |
| 5 | Present, applied deliberately and well |

Then:
1. Score each selected principle.
2. Sum the scores (max 60).
3. Map to a global label:
   - 48–60: Production-ready
   - 36–47: Polished
   - 24–35: Work in progress
   - 12–23: Hold
   - 0–11: Critical
4. List the failing items and how they will be remediated.

---

## The 12 Principles of Animation (reference)

### 1. Squash and Stretch
- **Definition:** Drawing objects to give weight and flexibility.
- **Purpose:** convey weight, elasticity, and volume.
- **Example:** a bouncing ball squashes on impact and stretches during the
  fall; volume stays constant.

### 2. Anticipation
- **Definition:** A preparatory movement that makes the following action
  look real.
- **Purpose:** lead the eye and make the action feel intentional.
- **Example:** a dancer bending knees before a jump; a golfer winding up.

### 3. Staging
- **Definition:** Presenting an idea so that it is complete and clear.
- **Purpose:** direct attention and hide detail that does not support the
  story.
- **Example:** the hero action is the first thing to animate; other elements
  stay quiet.

### 4. Straight Ahead Action and Pose to Pose
- **Definition:** Two animation approaches — frame-by-frame from the start
  (straight ahead) or from key poses with in-betweens (pose to pose).
- **Purpose:** straight ahead suits fluid, organic action; pose to pose
  suits composed, emotional, and controlled scenes.
- **Example:** CSS `@keyframes` are pose to pose; GSAP timeline sequences
  are often straight ahead.

### 5. Follow Through and Overlapping Action
- **Definition:** Parts of a body or object keep moving after the main body
  stops (follow through) and parts move at different speeds
  (overlapping).
- **Purpose:** realism, inertia, and weight.
- **Example:** hair and capes lag behind a stopping character; arms move at
  a different rate from the head.

### 6. Slow In and Slow Out
- **Definition:** Acceleration and deceleration — more frames at the start
  and end of an action, fewer in the middle.
- **Purpose:** give motion weight and natural physics.
- **Example:** a ball rolls slowly up and down a curve, faster in the
  middle.

### 7. Arcs
- **Definition:** Natural motion follows an arc, not a straight line.
- **Purpose:** smoothness and organic movement.
- **Example:** an arm swings on an arc around the shoulder; a thrown ball
  follows a parabolic path.

### 8. Secondary Action
- **Definition:** A supporting action that reinforces the main action.
- **Purpose:** adds life and context, without stealing focus.
- **Example:** a character walking while swinging their arms; a hand on
  hip while speaking.

### 9. Timing
- **Definition:** The number of frames per action, which sets speed,
  weight, mood, and character.
- **Purpose:** the primary tool for enforcing physics and emotion.
- **Example:** a light object reacts fast to a push; a heavy one reacts
  slowly. A long pause says more than a line of dialogue.

### 10. Exaggeration
- **Definition:** Presenting reality in a more evident or extreme way.
- **Purpose:** avoid stiffness; create style and clarity.
- **Example:** a dramatic punch with a bigger wind-up; a caricatured face
  that still reads as the same character.

### 11. Solid Drawing
- **Definition:** Taking into account 3D forms, volume, weight, balance,
  light, and shadow.
- **Purpose:** give the image weight and credibility.
- **Example:** avoiding "twins" — mirrored left/right sides that look
  lifeless. In 3D, keeping camera, light, and silhouette consistent.

### 12. Appeal
- **Definition:** The charisma of a character, or the quality that makes it
  engaging.
- **Purpose:** make the character real, interesting, and memorable.
- **Example:** friendly characters use symmetrical, "baby-like" features;
  villains can have appeal too.

---

## Evaluation Criteria

Use this rubric when evaluating a generated solution (see Step 5).

### Per-principle rubric

| Score | Meaning |
|---|---|
| 1 | Missing or actively harmful |
| 2 | Clearly failing |
| 3 | Inconsistent / borderline |
| 4 | Generally present, minor issues |
| 5 | Present, applied deliberately and well |

### Global scores

| Total (out of 60) | Label | Action |
|---|---|---|
| 48–60 | Production-ready | Ship |
| 36–47 | Polished | Fix marked items, then ship |
| 24–35 | Work in progress | Fix before shipping |
| 12–23 | Hold | Pull, remediate, re-test |
| 0–11 | Critical | Immediate review required |

### Quick checklist

- [ ] **Staging:** one focal point per screen/sequence
- [ ] **Anticipation:** preparatory movement present
- [ ] **Timing:** durations match intent; 60 fps
- [ ] **Arcs:** natural paths, no linear or erratic motion
- [ ] **Follow-through:** elements settle after the action
- [ ] **Secondary:** supports, does not contradict
- [ ] **Appeal:** pleasant, clear, engaging
- [ ] **Squash & Stretch:** volume constant, weight readable
- [ ] **Solid Drawing:** silhouette legible at distance

---

## Self-Assessment Checklist (for the agent)

Before delivering a result, the agent must confirm:

- [ ] I identified the task type (UI / Character / Motion graphics / Video
  / Game).
- [ ] I selected the relevant principles and gave reasons for each.
- [ ] I applied each selected principle with concrete parameters (values,
  durations, easing, etc.).
- [ ] I generated a complete, usable solution (code, prompt, or plan).
- [ ] I evaluated the result with the rubric and recorded the score and the
  failing items.

---

## References

1. Johnston, Ollie; Thomas, Frank. *The Illusion of Life: Disney Animation*
   (1981).
2. Wikipedia —
   [12 basic principles of animation](https://pt.wikipedia.org/wiki/12_princ%C3%ADpios_b%C3%A1sicos_de_anima%C3%A7%C3%A3o).
3. Lasseter, John. "Principles of traditional animation applied to 3D
   computer animation" (SIGGRAPH, 1987).
