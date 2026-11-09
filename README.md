# netTime · Presentación interactiva

Presentación web para **netTime**, una app que enseña a autónomos y repartidores cuánto ganan de verdad, no solo lo que facturan.

**Verla en directo:** https://pablofranb.github.io/nettime-presentacion/

## Qué contiene

Las cifras son las del vídeo conceptual y la one-page: un turno de Pablo, taxista en Madrid, de **180 € en 11 horas**.

1. **El problema.** Un rosco parte de 180 € y en cada paso quita un trozo: gasolina (−42 €), cuota + seguro (−14 €) y reserva de IRPF (−20,60 €). La cifra del centro baja contando hasta los **103,40 €** que le quedan: **9,40 €/h limpios, no 16,36 €/h** como parecía.
2. **Lo que ya existe.** Pablo pregunta «¿Cuánto gano de verdad?». La libreta, la app de facturas y la gestoría le responden en un chat, pero solo saben lo facturado o se lo dicen tarde. NetTime responde al momento.
3. **Cómo te ayuda.** «Apuntas. Ves. Decides.» contado con un móvil que cambia de pantalla: apuntar la jornada, ver el neto con su desglose (y los 144 € apartados para Hacienda esta semana) y descubrir las franjas horarias que más rinden.
4. **Objetivo SMART.** Las cinco letras (específico, medible, alcanzable, relevante y temporal) se iluminan una a una mientras se explica el objetivo.
5. **Cierre.** Botón y código QR que llevan a la demo: https://jaacobgomez.github.io/nettime-demo/

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
