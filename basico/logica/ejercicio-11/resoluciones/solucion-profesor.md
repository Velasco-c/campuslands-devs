# Solución de profesor: Bitácora de viajes extremos

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const reservas = [
  { nombre: "Ana", destino: "Antigua", actividad: "paracaidismo", edad: 22, costoBase: 900 },
  { nombre: "Luis", destino: "Atitlan", actividad: "paracaidismo", edad: 17, costoBase: 850 },
  { nombre: "Mia", destino: "Semuc", actividad: "tour", edad: 16, costoBase: 300 }
];

function esValida(reserva) {
  return reserva.actividad !== "paracaidismo" || reserva.edad >= 18;
}

const aprobadas = reservas
  .filter(esValida)
  .map((reserva) => ({
    ...reserva,
    total: Number((reserva.costoBase * 1.12).toFixed(2))
  }));

console.table(aprobadas);
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
