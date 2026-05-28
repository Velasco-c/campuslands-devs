# Solución de profesor: Playlist para entrenamiento de kickboxing

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
const canciones = [
  { titulo: "Round One", artista: "KZ", bpm: 142, duracionSeg: 210 },
  { titulo: "Explode", artista: "NOVA", bpm: 168, duracionSeg: 185 },
  { titulo: "Warm Flow", artista: "BeatLab", bpm: 128, duracionSeg: 240 }
];

function intensidad(bpm) {
  if (bpm >= 160) return "explosiva";
  if (bpm >= 140) return "alta";
  return "media";
}

const playlist = canciones
  .filter((cancion) => cancion.bpm > 135)
  .map((cancion) => ({ ...cancion, intensidad: intensidad(cancion.bpm) }));

const duracionTotal = playlist.reduce((total, cancion) => total + cancion.duracionSeg, 0);
console.table(playlist);
console.log("Duracion total en minutos:", (duracionTotal / 60).toFixed(1));
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
