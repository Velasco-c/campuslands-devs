# Solución de profesor: Diagnóstico rápido de mecánica

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Solución sugerida

```js
function diagnosticar(sintomas) {
  const catalogo = {
    "no enciende": "revisar bateria, bujia y sistema de encendido",
    vibra: "revisar balanceo, llantas y soportes",
    "pierde aceite": "revisar empaques, retenes y torque de tornillos",
    "frena poco": "revisar pastillas, liquido de frenos y disco"
  };

  return sintomas.map((sintoma) => ({
    sintoma,
    recomendacion: catalogo[sintoma] || "hacer inspeccion general"
  }));
}

console.table(diagnosticar(["vibra", "frena poco"]));
```

## Por qué funciona

- Usa datos estructurados en arreglos y objetos.
- Aplica filtros, cálculos, condicionales o ciclos según el problema.
- Genera una salida verificable y fácil de leer.

## Cómo compararla con tu solución

- Tu solución puede tener nombres diferentes, pero debe producir resultados equivalentes.
- Revisa si manejaste casos límite como valores en cero, listas vacías o empates.
- Evalúa si tus nombres de variables explican el contexto del problema.
