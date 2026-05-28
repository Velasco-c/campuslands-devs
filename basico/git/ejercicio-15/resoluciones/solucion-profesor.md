# Solución de profesor: Checklist final de flujo profesional

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Comandos o pasos sugeridos

```bash
git checkout dev
git pull origin dev
git checkout -b alumno/nombre-apellido/ejercicio-15
resolver ejercicio
git status
git add basico/git/ejercicio-15/resoluciones/nombre-apellido.md
git commit -m "feat(git): resolver ejercicio 15"
git push -u origin alumno/nombre-apellido/ejercicio-15
abrir PR hacia dev
```

## Criterio de revisión

- El estudiante trabaja desde su propia rama.
- Los commits tienen mensajes claros y siguen el estándar del repositorio.
- No se suben cambios directos a `main` ni `dev`.
- La evidencia muestra `git status`, `git log` o el PR cuando aplique.

## Respuesta esperada

Un archivo Markdown con los comandos usados, una breve explicación y evidencia de validación.
