# Solución de profesor: Laboratorio de fórmulas químicas

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const compuestos = [
  { nombre: "Agua", componentes: [{ simbolo: "H", gramos: 2 }, { simbolo: "O", gramos: 16 }] },
  { nombre: "Sal", componentes: [{ simbolo: "Na", gramos: 23 }, { simbolo: "Cl", gramos: 35.5 }] },
  { nombre: "Error", componentes: [{ simbolo: "X", gramos: 0 }] }
];

const reporte = compuestos.map((compuesto) => {
  const valido = compuesto.componentes.every((item) => item.gramos > 0);
  const masaTotal = compuesto.componentes.reduce((total, item) => total + item.gramos, 0);
  return { nombre: compuesto.nombre, valido, masaTotal };
});

console.table(reporte.filter((item) => item.valido));
console.table(reporte.filter((item) => !item.valido));
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
