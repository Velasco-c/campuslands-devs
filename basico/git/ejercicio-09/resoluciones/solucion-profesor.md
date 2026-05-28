# Solución de profesor: Trabajo con ramas sobre ramas en película sci-fi

> Esta respuesta es una guía de consulta. El estudiante debe intentar resolver el ejercicio antes de revisar esta solución.

## Enfoque recomendado

Lee el problema, identifica datos de entrada, proceso y salida esperada. Luego compara tu respuesta con esta guía y revisa diferencias de lógica, orden y validación.

## Comandos o pasos sugeridos

```bash
git checkout -b feature/catalogo-sci-fi
git commit -m "feat(git): crear catalogo sci-fi"
git checkout -b feature/catalogo-sci-fi/posters
git commit -m "feat(git): agregar referencias de posters"
git checkout feature/catalogo-sci-fi
git merge feature/catalogo-sci-fi/posters
git checkout dev
git merge feature/catalogo-sci-fi
```

## Criterio de revisión

- El estudiante trabaja desde su propia rama.
- Los commits tienen mensajes claros y siguen el estándar del repositorio.
- No se suben cambios directos a `main` ni `dev`.
- La evidencia muestra `git status`, `git log` o el PR cuando aplique.

## Respuesta esperada

Un archivo Markdown con los comandos usados, una breve explicación y evidencia de validación.
