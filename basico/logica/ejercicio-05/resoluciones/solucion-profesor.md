# Solución de profesor: Tabla de fútbol sala

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const equipos = [
  { nombre: "Furia", victorias: 4, empates: 1, derrotas: 0, golesFavor: 22, golesContra: 10 },
  { nombre: "Norte", victorias: 4, empates: 0, derrotas: 1, golesFavor: 18, golesContra: 8 },
  { nombre: "Barrio", victorias: 2, empates: 2, derrotas: 1, golesFavor: 16, golesContra: 13 }
];

const tabla = equipos
  .map((equipo) => ({
    ...equipo,
    puntos: equipo.victorias * 3 + equipo.empates,
    diferencia: equipo.golesFavor - equipo.golesContra
  }))
  .sort((a, b) => b.puntos - a.puntos || b.diferencia - a.diferencia);

tabla.forEach((equipo, index) => {
  console.log(`${index + 1}. ${equipo.nombre} | ${equipo.puntos} pts | DG ${equipo.diferencia}`);
});
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
