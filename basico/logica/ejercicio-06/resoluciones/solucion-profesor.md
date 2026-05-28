# Solución de profesor: Comparador de motos deportivas

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const motos = [
  { marca: "Yamaha", modelo: "R1", hp: 200, pesoKg: 201, mantenimientoMensual: 480000 },
  { marca: "Kawasaki", modelo: "H2", hp: 228, pesoKg: 238, mantenimientoMensual: 750000 },
  { marca: "BMW", modelo: "S1000RR", hp: 205, pesoKg: 197, mantenimientoMensual: 520000 }
];

const evaluadas = motos.map((moto) => ({
  ...moto,
  relacion: Number((moto.hp / moto.pesoKg).toFixed(3))
}));

const economicas = evaluadas.filter((moto) => moto.mantenimientoMensual < 500000);
const mejorPista = [...evaluadas].sort((a, b) => b.relacion - a.relacion)[0];
const mejorEconomica = [...economicas].sort((a, b) => b.relacion - a.relacion)[0];

console.log("Mejor para pista:", mejorPista);
console.log("Mejor economica:", mejorEconomica);
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
