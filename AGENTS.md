# Reac Studio — Landing

## Qué es cada archivo
- **Impulso.dc.html** — TODO el diseño (markup + lógica). Es el único archivo que se edita.
- **support.js** — runtime que hace funcionar el formato. NO lo leas ni lo edites (es código generado, gasta tokens al pedo).

## Cómo previsualizar
Abrí `Impulso.dc.html` directamente en el navegador (doble clic o Live Server en VS Code). No necesita build ni servidor.

## Estructura interna de Impulso.dc.html
El archivo tiene 3 partes dentro de `<x-dc>`:
1. `<helmet>` — fuentes, `@keyframes` y estilos globales (animaciones de carga, reveal-on-scroll, hover).
2. El **template** (HTML con estilos inline) — todas las secciones: hero parallax, estadísticas, servicios, bento, panel/dashboard, proceso, FAQ, testimonios, contacto, footer.
3. La **clase `Component`** (al final, en `<script data-dc-script>`) — estado y lógica: parallax, navbar al scroll, sliders, toggles, animación del título letra por letra, IntersectionObserver de los reveals.

## Notas
- Las imágenes del hero parallax y las fuentes se cargan desde CDN (necesita internet la primera vez).
- Las animaciones respetan `prefers-reduced-motion`: si tu sistema tiene "reducir movimiento" activado, NO vas a ver el movimiento (el contenido aparece igual).
- Para gastar los mínimos tokens: editá solo los bloques puntuales que se pidan; no releas todo el archivo ni `support.js` en cada cambio.
