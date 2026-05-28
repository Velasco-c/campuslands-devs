# Solución de profesor: Control de inventario streetwear

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const prendas = [
  { nombre: "hoodie negro", talla: "M", stock: 3, ventasSemana: 8 },
  { nombre: "cargo pants", talla: "L", stock: 10, ventasSemana: 4 },
  { nombre: "oversize tee", talla: "S", stock: 2, ventasSemana: 5 }
];

const reporte = prendas.map((prenda) => {
  const reposicion = Math.max(prenda.ventasSemana * 2 - prenda.stock, 0);
  return {
    ...prenda,
    bajoStock: prenda.stock < 5,
    reposicion
  };
});

console.table(reporte);
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
