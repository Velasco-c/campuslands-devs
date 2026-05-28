# Solución de profesor: Gestor de personajes RPG

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const personajes = [
  { nombre: "Kael", clase: "mago", nivel: 12, ataque: 35, defensa: 10 },
  { nombre: "Runa", clase: "tanque", nivel: 15, ataque: 18, defensa: 42 },
  { nombre: "Zed", clase: "asesino", nivel: 9, ataque: 28, defensa: 8 }
];

function calcularPoder(personaje) {
  return personaje.nivel * 2 + personaje.ataque + personaje.defensa;
}

function sugerirMejora(personaje) {
  return personaje.ataque < personaje.defensa ? "entrenar ataque" : "entrenar defensa";
}

const reporte = personajes.map((personaje) => {
  const poder = calcularPoder(personaje);
  return {
    ...personaje,
    poder,
    estado: poder < 60 ? "necesita mejora" : "listo",
    sugerencia: poder < 60 ? sugerirMejora(personaje) : "mantener build"
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
