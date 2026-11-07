# netTime · Presentación interactiva

Presentación web para **netTime**, una app que enseña a autónomos y repartidores cuánto ganan de verdad, no solo lo que facturan.

**Verla en directo:** https://pablofranb.github.io/nettime-presentacion/

## Qué contiene

1. **El problema.** Un gráfico de rosco parte de 100 € facturados y, en cada paso, quita un trozo: gastos (−27 €), cuota de autónomos (−7 €) e IRPF (−10 €). La cifra del centro baja contando hasta los 56 € que quedan de verdad.
2. **Lo que ya existe.** Pablo acaba el turno y pregunta «¿Cuánto he ganado hoy?». La libreta, la app de facturas y la gestoría le responden en un chat, pero solo saben lo facturado o se lo dicen tarde. netTime responde al momento: te quedan 100,80 €.
3. **Cómo te ayuda.** «Apuntas. Ves. Decides.» contado con un único móvil que cambia de pantalla: cerrar el turno, ver el neto con su desglose y descubrir qué día rinde más.

## Controles

| Acción | Tecla |
|---|---|
| Avanzar | → · Espacio · Av Pág · mando de presentación · clic |
| Retroceder | ← · Re Pág · Mayús + clic |
| Pantalla completa | F |
| Pantalla en negro | B |

## Cómo está hecha

- Un único archivo `index.html`, sin frameworks ni dependencias que instalar: HTML, CSS y JavaScript puros.
- Un escenario fijo de 1920×1080 que se escala a cualquier pantalla con `transform: scale()`, así se ve igual en el portátil y en el proyector.
- Cada escena tiene varios **estados**. Al avanzar, JavaScript cambia el estado y CSS anima la transición (`transition`) entre uno y otro.
- El rosco es un SVG: cada trozo es un `<circle>` cuyo arco se dibuja con `stroke-dasharray` y `stroke-dashoffset`.
- El mando funciona porque, para el ordenador, es un teclado que envía flechas o Av Pág / Re Pág, y la página escucha esas teclas.
- Los bocadillos del chat simulan que alguien escribe (los tres puntos) antes de responder, y el móvil «teclea» los datos del turno carácter a carácter con temporizadores de JavaScript.
- Iconos: [Lucide](https://lucide.dev) (licencia ISC). Tipografía: Outfit (Google Fonts).
