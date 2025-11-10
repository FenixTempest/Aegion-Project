## Section: Implemented improvements (technical summary)

Summary
- An interaction effect was added to `.menu1 a`: elevation and slight scaling combined with a cyan holographic glow.
- CSS variables were introduced to make it easier to customize colors and base typography.

CSS variables (usage)
```css
:root{
  --BGC: burlywood;
  --font1: 1.2rem "Fira Sans", sans-serif;
}

body{
  background-color: var(--BGC);
  font: var(--font1);
}
```

Transitions and optimization (relevant code)
```css
transition: transform .25s cubic-bezier(.2,.9,.2,1), box-shadow .25s ease, border-color .25s ease;
will-change: transform, box-shadow;
transform-origin: center;
```
- Purpose: to control the animation (duration and easing) and allow rendering optimizations.
- Detail: `transform` uses a cubic-bezier for a snappy acceleration; `will-change` hints to the engine to optimize `transform` and `box-shadow`; `transform-origin: center` ensures symmetric scaling.

Effect in `:hover` state (relevant code)
```css
transform: translateY(-6px) scale(1.04);
box-shadow:
  0 14px 30px rgba(0,255,255,0.12),
  0 0 14px rgba(0,255,255,0.30);
border-color: rgba(0,255,255,0.9);
```
- Purpose: to apply the visual interaction on cursor hover (hover/focus).
- Detail: `translateY` and `scale` produce elevation and a slight increase; the two-layer `box-shadow` separates the perception of depth (offset shadow) from the chromatic glow (cyan glow); `border-color` is tinted to reinforce the accent.

Quick considerations
- Performance: animating `transform` and `box-shadow` is efficient if `will-change` is used sparingly.
- Accessibility: adding `@media (prefers-reduced-motion: reduce)` and styles for `:focus-visible` is recommended.

(Values and opacities can be adjusted to fine-tune the intensity and speed of the effect.)
