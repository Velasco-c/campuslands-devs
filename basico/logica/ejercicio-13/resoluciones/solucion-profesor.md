# Solución de profesor: Estadísticas de torneo de pingpong

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const jugadores = [
  { nombre: "Leo", partidos: 10, victorias: 8, puntosFavor: 210, puntosContra: 160 },
  { nombre: "Sara", partidos: 9, victorias: 7, puntosFavor: 190, puntosContra: 155 },
  { nombre: "Max", partidos: 0, victorias: 0, puntosFavor: 0, puntosContra: 0 }
];

const ranking = jugadores
  .filter((jugador) => jugador.partidos > 0)
  .map((jugador) => ({
    ...jugador,
    winrate: Number(((jugador.victorias / jugador.partidos) * 100).toFixed(1)),
    diferencia: jugador.puntosFavor - jugador.puntosContra
  }))
  .sort((a, b) => b.winrate - a.winrate || b.diferencia - a.diferencia);

console.table(ranking);
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
