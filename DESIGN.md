# DESIGN SYSTEM - Nexus Travel

## LAYOUTS CREATIVOS POR SECCIÓN

### Hero - Carrusel editorial
- Fullscreen con 3 destinos rotando
- Imagen ocupa pantalla completa con overlay gradiente
  desde abajo (negro 0% arriba → 60% abajo)
- Texto alineado abajo-izquierda como revista
- Destino en DM Mono uppercase pequeño
- Título enorme en Fraunces italic
- Transición: clip-path reveal de izquierda a derecha
- Indicadores: líneas horizontales que se llenan

### Grid de destinos - Layout Bento
- NO grid uniforme. Usar CSS Grid asimétrico:
  * 1 card grande (2 columnas, 2 filas) - destacado
  * 2 cards medianas verticales
  * 3 cards pequeñas horizontales
- Cada card tiene imagen, país, ciudad, precio badge
- Hover: zoom imagen + aparece botón "Explorar →"

### Sección experiencias - Scroll horizontal
- En desktop: scroll horizontal con cards anchas
- Cada card: imagen izquierda + texto derecha
- Categorías: Aventura, Playa, Cultural, Gastronomía
- Indicador de scroll: barra de progreso fina abajo

### Testimonios - Layout revista
- 1 testimonio grande featured con foto grande
- 2 testimonios secundarios más pequeños al lado
- Comillas tipográficas gigantes como elemento gráfico
- Fondo azul noche, texto claro

### Proceso reserva - Timeline horizontal
- 4 pasos conectados por línea que se anima al hacer scroll
- Número del paso: grande, outline, en DM Mono
- Icono SVG debajo del número
- Texto descriptivo abajo

## ANIMACIONES

### Reveal de texto (signature)
- Texto envuelto en div con overflow: hidden
- El texto sube desde abajo: translateY(100%) → 0
- Timing: 0.9s cubic-bezier(0.16, 1, 0.3, 1)
- Stagger 0.15s entre líneas

### Cards hover
- Imagen: transform scale(1.08), transition 0.6s ease
- Overlay: opacity 0 → 0.3
- Texto: translateY(8px) → 0
- Botón: aparece desde abajo

### Parallax suave
- Hero background: mueve al 0.3x del scroll
- Imágenes de sección: mueve al 0.15x del scroll

### Números
- Cuentan de 0 al valor con easing
- Fuente DM Mono, tamaño grande
- Se activan con IntersectionObserver

## IMÁGENES UNSPLASH - IDs por destino
- Machu Picchu: photo-1526392060635-9d6019884377
- Tokio: photo-1540959733332-eab4deabeeaf
- Santorini: photo-1570077188670-e3a8d69ac5ff
- Bali: photo-1537996194471-e657df975ab4
- París: photo-1502602898657-3e91760cbb34
- Nueva York: photo-1496442226666-8d4d0e62e6e9
- Hero 1: photo-1488085061387-422e29b40080
- Hero 2: photo-1476514525535-07fb3b4ae5f1
- Hero 3: photo-1530789253388-582c481c54b0

## RESPONSIVE
- Mobile: stack vertical, imágenes 100% ancho
- Tablet 768px: grid 2 columnas
- Desktop 1024px+: layouts asimétricos completos
- Tipografía hero: clamp(3rem, 7vw, 6.5rem)
- Scroll horizontal en mobile para experiencias