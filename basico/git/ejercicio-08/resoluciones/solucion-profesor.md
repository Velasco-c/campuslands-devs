# Solución de profesor: Conflicto simple en playlist musical

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Comandos o pasos sugeridos

```bash
git checkout -b playlist-a
editar playlist.md linea 1
git commit -am "feat(git): ajustar playlist version a"
git checkout dev
git checkout -b playlist-b
editar la misma linea
git commit -am "feat(git): ajustar playlist version b"
git checkout dev
git merge playlist-a
git merge playlist-b
resolver marcas <<<<<<< ======= >>>>>>>
git add playlist.md
git commit -m "fix(git): resolver conflicto de playlist"
```

## Criterio de revisión

- El estudiante trabaja desde su propia rama.
- Los commits tienen mensajes claros y siguen el estándar del repositorio.
- No se suben cambios directos a `main` ni `dev`.
- La evidencia muestra `git status`, `git log` o el PR cuando aplique.

## Respuesta esperada

Un archivo Markdown con los comandos usados, una breve explicación y evidencia de validación.
