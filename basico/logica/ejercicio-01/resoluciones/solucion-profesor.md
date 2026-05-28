# Solución de profesor: Ranking de escuadras battle royale

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const escuadras = [
  { nombre: "Nova", bajas: 8, posicion: 1, revividos: 2 },
  { nombre: "Titan", bajas: 10, posicion: 3, revividos: 1 },
  { nombre: "Eclipse", bajas: 4, posicion: 2, revividos: 3 }
];

function puntosPorPosicion(posicion) {
  if (posicion === 1) return 20;
  if (posicion === 2) return 14;
  if (posicion === 3) return 10;
  return 4;
}

const ranking = escuadras
  .map((escuadra) => ({
    ...escuadra,
    puntos: escuadra.bajas * 3 + puntosPorPosicion(escuadra.posicion)
  }))
  .sort((a, b) => b.puntos - a.puntos || b.bajas - a.bajas);

ranking.forEach((escuadra, index) => {
  console.log(`${index + 1}. ${escuadra.nombre} - ${escuadra.puntos} pts`);
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
