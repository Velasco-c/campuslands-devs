# Solución de profesor: Presupuesto de estudio de animación 3D

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const escenas = [
  { nombre: "Intro ciudad", horasModelado: 10, horasRender: 8, artistas: 3 },
  { nombre: "Persecucion", horasModelado: 18, horasRender: 16, artistas: 4 },
  { nombre: "Cierre", horasModelado: 6, horasRender: 4, artistas: 2 }
];

function costoEscena(escena) {
  return escena.horasModelado * 40000 + escena.horasRender * 25000 + escena.artistas * 120000;
}

const costos = escenas.map((escena) => ({ ...escena, costo: costoEscena(escena) }));
const total = costos.reduce((suma, escena) => suma + escena.costo, 0);
const costosas = costos.filter((escena) => escena.costo > 1000000);
const mayor = [...costos].sort((a, b) => b.costo - a.costo)[0];

console.table(costos);
console.log({ total, costosas, mayor });
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
