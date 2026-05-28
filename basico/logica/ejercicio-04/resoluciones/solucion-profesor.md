# Solución de profesor: Control de líneas MOBA

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const jugadores = [
  { rol: "top", kills: 5, deaths: 2, assists: 8, oro: 12800, objetivos: 1 },
  { rol: "jungla", kills: 3, deaths: 0, assists: 12, oro: 11900, objetivos: 5 },
  { rol: "mid", kills: 9, deaths: 3, assists: 6, oro: 14200, objetivos: 2 }
];

const analisis = jugadores
  .map((jugador) => ({
    ...jugador,
    kda: (jugador.kills + jugador.assists) / Math.max(jugador.deaths, 1),
    economia: jugador.oro >= 12000 ? "fuerte" : "baja",
    alerta: jugador.objetivos < 2 ? "mejorar control de objetivos" : "ok"
  }))
  .sort((a, b) => b.kda - a.kda);

console.table(analisis);
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
