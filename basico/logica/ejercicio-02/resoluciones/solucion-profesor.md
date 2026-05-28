# Solución de profesor: Inventario táctico de shooter

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const armas = [
  { nombre: "Vandal-X", tipo: "rifle", municion: 45, rareza: "epica" },
  { nombre: "Ghost-9", tipo: "pistola", municion: 18, rareza: "comun" },
  { nombre: "Longshot", tipo: "francotirador", municion: 30, rareza: "rara" }
];

const disponibles = armas.filter((arma) => arma.municion >= 30);

function esRecomendada(arma) {
  return arma.rareza === "rara" || arma.rareza === "epica";
}

const resumen = disponibles.map((arma) => ({
  nombre: arma.nombre,
  tipo: arma.tipo,
  municion: arma.municion,
  recomendada: esRecomendada(arma)
}));

console.table(resumen);
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
