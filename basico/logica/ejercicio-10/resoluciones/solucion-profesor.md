# Solución de profesor: Maratón de películas de miedo

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const peliculas = [
  { titulo: "La Senal", duracionMin: 100, sustos: 14, rating: 7.8 },
  { titulo: "Pasillo 13", duracionMin: 110, sustos: 20, rating: 8.1 },
  { titulo: "Sombra Final", duracionMin: 130, sustos: 16, rating: 6.9 },
  { titulo: "Noche Fria", duracionMin: 120, sustos: 18, rating: 7.4 }
];

let minutos = 0;
const seleccion = [];

for (const pelicula of peliculas.filter((item) => item.rating >= 7)) {
  if (minutos + pelicula.duracionMin <= 360) {
    seleccion.push(pelicula);
    minutos += pelicula.duracionMin;
  }
}

const sustos = seleccion.reduce((total, pelicula) => total + pelicula.sustos, 0);
console.table(seleccion);
console.log({ minutos, sustos });
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
