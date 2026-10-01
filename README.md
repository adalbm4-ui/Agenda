# Agenda Dandy + Asistente IA (local)

Agenda personal de una sola página (`index.html`). No requiere instalación ni
servidor: ábrela en el navegador o súbela a GitHub Pages tal cual.

## ¿Qué hace el asistente?

Todo el "cerebro" vive dentro de `index.html`, en JavaScript puro, y **no hace
ninguna petición de red**: no necesita API key, no envía tus datos a ningún
servicio y funciona sin internet.

### 1. Captura rápida en lenguaje natural
Escribes como hablas y la IA decide a qué módulo va cada cosa:

| Escribes | Se guarda |
|---|---|
| `Pagar la luz $800 el viernes 18:00` | Gasto en Finanzas, $800, fecha viernes, rubro Hogar |
| `Recuérdame llamar a mamá a las 7 de la noche` | Recordatorio 19:00 en Agenda |
| `Vendí $1500 de fragancias` | Venta en Finanzas |
| `Tarea urgente: enviar la cotización` | Tarea con prioridad alta |
| `Leer 20 páginas todas las noches` | Hábito |
| `Juan me debe $500 del pedido` | Adeudo "por cobrar" a nombre de Juan |
| `reunión con Ana el lunes a las 10:30` | Evento en Calendario |

Entiende fechas relativas (hoy, mañana, pasado mañana, el viernes, el 15 de
marzo, en 3 días, próximo lunes), horas (`18:00`, `7am`, `a las 8`, `de la
noche`), montos (`$800`, `1,250.50`, `800 pesos`), prioridades (urgente,
importante, sin prisa) y rubros de gasto (Comida, Transporte, Hogar, Salud,
Trabajo, Ocio, Educación).

Antes de guardar muestra **qué entendió y con qué seguridad**. Si se equivoca,
eligues el tipo correcto y **aprende**: la próxima vez que escribas algo
parecido lo clasificará bien.

### 2. Plan del día priorizado
Junta tus recordatorios, eventos y tareas y arma una sola línea de tiempo:
primero lo vencido, después lo que toca **ahora** y luego cada tarea encajada
en tus huecos libres reales. La prioridad se calcula con la prioridad que
tú pusiste, los días que lleva pendiente y las palabras de urgencia.

### 3. Detección de patrones
Revisa tus propios datos y avisa de cosas como:
- gastos de hoy por encima o por debajo de tu promedio diario,
- proyección de cierre del mes y comparación con el mes anterior,
- ritmo necesario para llegar a tu meta de ventas,
- días de caja restantes según tu gasto diario,
- gastos "hormiga" que suman más de lo que parecen,
- hábitos en riesgo, rachas y el día de la semana que más fallas,
- tareas que llevan días sin cerrarse,
- recordatorios vencidos y huecos libres sin aprovechar.

Cada aviso se puede descartar (vuelve a aparecer a los 3 días).

### 4. Chat que actúa sobre tu agenda
Preguntas: *¿cuánto gasté hoy?*, *¿cómo voy con la meta?*, *¿qué sigue?*,
*dame un resumen*, *¿cómo van mis hábitos?*, *consejo*.

Acciones: *terminé la tarea de enviar cotización*, *gasté 320 en gasolina*,
*recuérdame cerrar la cortina a las 8 de la noche*. Todo lo que crea se puede
deshacer con un botón.

## Dónde vive cada cosa

- Un único archivo: `index.html` (~6.400 líneas, HTML + CSS + JS).
- Los datos siguen en `localStorage` bajo las mismas claves de siempre
  (`dia-agenda-v1`, `dandy-tasks-v1`, `dandy-finance-v1`, …).
- La memoria del asistente está en `dandy-ia-v1` y **también se incluye en la
  copia de seguridad** (exportar/importar y Google Drive), junto con el resto
  de tus datos.

## Atajos

- Botón ✨ en la esquina superior derecha: abre el asistente.
- Pestaña **IA** en la barra de navegación.
- Enter en el campo de captura: interpreta y guarda.
