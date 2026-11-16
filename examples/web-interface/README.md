# Web Interface — example

A component library animated with the 12 principles: buttons, cards,
modal, navigation, and page transitions.

## Component overview

| Component | Principles at work |
|---|---|
| Button | Squash and Stretch (press), Anticipation (hover) |
| Card | Staging (focus), Follow Through (stagger) |
| Modal | Staging, Timing, Appeal |
| Navigation | Staging, Arcs |
| Page transitions | Slow In & Slow Out, Arcs |

## Demo checklist

Run each component through the evaluation suite in `evaluations/test-cases.md`.

### Button

- **Press:** compresses, then springs — squash and stretch.
- **Hover:** a preparatory lift — anticipation.

### Card

- **Open:** the card slides with a slight overshoot (slow-in/out + arcs);
  the list follows in stagger (follow-through).

### Modal

- **Open:** a light dims, then the card rises (staging + timing).
- **Close:** the card shrinks and the light fades (slow-in/out).

## Files

```
web-interface/
├── README.md
└── components.md        # detailed component breakdown
```

## How to test

1. Open the component set in the browser.
2. Run `evaluations/test-cases.md` T1–T12 against each component.
3. Record scores in `templates/estudo-de-principios.md`.
