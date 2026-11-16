# 12 Principles of Animation — UI/UX Design

The 12 principles are the grammar of good UI motion. This guide applies
them to product design.

## 1. Squash and Stretch
- Buttons depress on click; inputs react to focus with a subtle scale.
- Touch targets: the feedback should feel immediate.

## 2. Anticipation
- Navigation states, toggles, and cards show a preparatory movement before
  the main action.

## 3. Staging
- Visual hierarchy: the primary action is the first thing to animate and
  the most prominent element on screen.

## 4. Straight Ahead / Pose to Pose
- UI panels open with pose-to-pose from a defined start to a stable end.
- Sheets and drawers, tooltips, and status badges follow this.

## 5. Follow Through and Overlapping
- Staggered list items; tooltips follow the cursor; a panel follows its
  trigger after the trigger is released.

## 6. Slow In and Slow Out
- `ease-out` for entry (nothing races in).
- `ease-in` for exit (things calm down).
- Keep motion on the compositor thread (transform, opacity).

## 7. Arcs
- Dragging an element, opening a menu, or expanding a panel: follow arcs,
  not rigid grid-locked paths.

## 8. Secondary Action
- A toggle: the switch moves, the label changes color, the icon rotates —
  a coordinated secondary action.

## 9. Timing
- 60 fps target.
- Micro-interactions: 100–300ms.
- Panels and transitions: 300–500ms.
- The 70ms rule for touch feedback.

## 10. Exaggeration
- A press can be crisp; a pull-to-refresh can be exaggerated slightly.

## 11. Solid Drawing
- Silhouette, contrast, and spacing; cramped UI lacks "solidness."

## 12. Appeal
- The interface is pleasant, intuitive, and feels "right" — the appeal of
  the product.

## Quick checklist
- [ ] One focal point per screen
- [ ] Interactive elements show anticipation
- [ ] Easing applied (ease-out on entrance, ease-in on exit)
- [ ] Staggered secondary motion
- [ ] 60 fps on target devices
