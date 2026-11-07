# netTime · Presentación interactiva

Presentación web para **netTime**, una app que enseña a autónomos y repartidores cuánto ganan de verdad, no solo lo que facturan.

**Verla en directo:** https://pablofranb.github.io/nettime-presentacion/

## Qué contiene

1. **El problema.** Un gráfico de rosco parte de 100 € facturados y, en cada paso, quita un trozo: gastos (−27 €), cuota de autónomos (−7 €) e IRPF (−10 €). La cifra del centro baja contando hasta los 56 € que quedan de verdad.
2. **Lo que ya existe.** Libreta o Excel, apps de facturas y gestorías, puntuadas sobre 5 criterios, frente a netTime.
3. **Cómo te ayuda.** «Apuntas. Ves. Decides.»: neto por hora, Hacienda apartada y mejores turnos.

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
- Iconos: [Lucide](https://lucide.dev) (licencia ISC). Tipografía: Outfit (Google Fonts).
