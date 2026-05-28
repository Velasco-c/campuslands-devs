# Solución de profesor: Merge de ranking de pingpong

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Comandos o pasos sugeridos

```bash
git checkout dev
git checkout -b feature/ranking-pingpong
crear ranking.md
git add ranking.md
git commit -m "feat(git): agregar ranking de pingpong"
git checkout dev
git merge feature/ranking-pingpong
git log --oneline --graph --all
```

## Criterio de revisión

- El estudiante trabaja desde su propia rama.
- Los commits tienen mensajes claros y siguen el estándar del repositorio.
- No se suben cambios directos a `main` ni `dev`.
- La evidencia muestra `git status`, `git log` o el PR cuando aplique.

## Respuesta esperada

Un archivo Markdown con los comandos usados, una breve explicación y evidencia de validación.
