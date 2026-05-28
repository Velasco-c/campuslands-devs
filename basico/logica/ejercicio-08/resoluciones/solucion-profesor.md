# Solución de profesor: Catálogo de hiperdeportivos

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const autos = [
  { marca: "Bugatti", modelo: "Chiron", ceroACien: 2.4, precioUSD: 3200000, unidades: 500 },
  { marca: "Koenigsegg", modelo: "Jesko", ceroACien: 2.5, precioUSD: 3000000, unidades: 125 },
  { marca: "Ferrari", modelo: "SF90", ceroACien: 2.5, precioUSD: 530000, unidades: 2000 }
];

const rapidos = autos
  .filter((auto) => auto.ceroACien < 3)
  .map((auto) => ({
    ...auto,
    exclusividad: auto.unidades < 500 ? "extrema" : "alta"
  }))
  .sort((a, b) => a.ceroACien - b.ceroACien);

const precioPromedio = autos.reduce((total, auto) => total + auto.precioUSD, 0) / autos.length;

console.table(rapidos.slice(0, 3));
console.log("Precio promedio:", precioPromedio);
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
