# 12 Principles of Animation — Web Development

The 12 principles also govern how motion behaves in the browser. This guide
maps each principle to frontend animation and motion design for web
products.

## 1. Squash and Stretch
- Buttons depress when clicked; cards lift with a subtle scale of the
  contact surface.
- Use `transform: scale()` with the correct `transform-origin`.
- Preserve volume: equal scaling on both axes for a uniform squash.

## 2. Anticipation
- Hover states and button press (the "wind-up" before the click).
- Menu dropdowns, modal reveals, and toasts all "wind up" before exposing.

## 3. Staging
- One focal point per screen. The primary action leads the eye into the
  page.
- Hero beats animate in order — the most important thing first.

## 4. Straight Ahead / Pose to Pose
- **Pose to Pose:** `@keyframes` define clear poses; ideal for controlled,
  compositional animation.
- **Straight Ahead:** JS/timeline-driven frame-by-frame; good for
  reactive, causal motion (a progress bar filling after a fetch).

## 5. Follow Through and Overlapping
- Elements keep moving after the action that caused them (scroll-linked
  elements settle after the scroll stops).
- Staggered reveals: each list item animates after the previous.

## 6. Slow In and Slow Out
- Entrance: `ease-out`. Exit: `ease-in`. Custom curves via `cubic-bezier`.
- Keep motion on the compositor thread (`transform`, `opacity`) for 60fps.

## 7. Arcs
- UI motion should follow a logical arc; avoid straight-line, grid-locked
  paths.
- Slightly overshoot with a spring-like curve for "settling" — but not
  cartoonish.

## 8. Secondary Action
- A card opening: shadow grows, label lifts, hover ring expands — all at
  once, all supporting the primary action.

## 9. Timing
- Heavy things move slowly; light things fast.
- Micro-interactions: 100–300ms. Panels: 300–500ms. Match audio, speech,
  and music to the motion.

## 10. Exaggeration
- Functional UI: restraint. Decorative hero animation: freedom to
  overstate.

## 11. Solid Drawing
- Silhouette, contrast, and legibility; avoid "twins" — elements so
  mirrored they read as dead.

## 12. Appeal
- The interface must be pleasant, clear, and engaging — the
  "desirability" of the product.

## Quick checklist
- [ ] One focal point per screen
- [ ] Interactive elements show anticipation
- [ ] Easing applied (ease-out on entrance, ease-in on exit)
- [ ] Secondary motion supports the main action
- [ ] 60 fps — no jank
