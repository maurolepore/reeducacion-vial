# Educación y Reeducación Vial - CABA

Información sobre el sistema de scoring y recuperación de puntos en Buenos Aires. Incluye un skill para generar exámenes de práctica de reeducación vial, con los manuales de las dos empresas que ofrecen entrenamiento (Sistemas Reid y Creando Conciencia). Bonus: también puede generar exámenes para el examen de manejo normal (no de reeducación).

## Contenido

| Archivo | Descripción |
|---------|-------------|
| `README.md` | Cómo recuperar puntos (pago voluntario, reeducación, caducidad) |
| `simulador-test-de-conducir/src/data/*` | Data del simulador de examen CABA |

## Skills

```
skills/
└── test/
    ├── SKILL.md              # Genera exámenes de práctica (reeducación o licencia)
    └── references/
        ├── manual_reid_curso-de-reeducacion-vial.md
        ├── manual_creandoconciencia_curso-de-reeducacion-vial.md
        ├── manual_caba_examen-de-conduccion.md
        └── examen-real.md    # Preguntas recordadas del examen real
```

Datos del usuario se guardan en `~/.local/share/reeducacion-vial/` (practica.md, backlog.md).
