## Apartado: Mejoras implementadas (resumen técnico)

Resumen
- Se añadió un efecto de interacción en `.menu1 a`: elevación y ligera escala combinadas con un brillo holográfico cyan.
- Se introdujeron variables CSS para facilitar la personalización de colores y tipografía base.

Variables CSS (uso)
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

Transiciones y optimización (código relevante)
```css
transition: transform .25s cubic-bezier(.2,.9,.2,1), box-shadow .25s ease, border-color .25s ease;
will-change: transform, box-shadow;
transform-origin: center;
```
- Propósito: controlar la animación (duración y easing) y permitir optimizaciones de renderizado.
- Detalle: `transform` usa cubic-bezier para una aceleración ágil; `will-change` sugiere al motor que optimice `transform` y `box-shadow`; `transform-origin: center` garantiza escala simétrica.

Efecto en estado `:hover` (código relevante)
```css
transform: translateY(-6px) scale(1.04);
box-shadow:
  0 14px 30px rgba(0,255,255,0.12),
  0 0 14px rgba(0,255,255,0.30);
border-color: rgba(0,255,255,0.9);
```
- Propósito: aplicar la interacción visual al pasar el cursor (hover/focus).
- Detalle: `translateY` y `scale` producen elevación y aumento ligero; `box-shadow` en dos capas separa la percepción de profundidad (sombra desplazada) del brillo cromático (glow cyan); `border-color` se tiñe para reforzar el acento.

Consideraciones rápidas
- Rendimiento: animar `transform` y `box-shadow` es eficiente si se usa `will-change` de forma limitada.
- Accesibilidad: añadir `@media (prefers-reduced-motion: reduce)` y estilos para `:focus-visible` es recomendable.

(Valores y opacidades pueden ajustarse para afinar intensidad y velocidad del efecto.)
