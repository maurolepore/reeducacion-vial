---
name: reeducacion-vial
description: "Genera exámenes de práctica de reeducación vial (20 preguntas multiple choice). Usar cuando el usuario quiera practicar para el examen, repasar temas, o pida un test/examen de práctica. Fuentes disponibles: manual Sistemas Reid, manual Creando Conciencia, preguntas CABA."
---

# Examen de Reeducación Vial

Genera exámenes de práctica para el curso de reeducación vial de CABA (recuperación de 4 puntos).

## Archivos

Material de referencia (distribuido con el skill):
- `references/manual_reid_curso-de-reeducacion-vial.md`
- `references/manual_creandoconciencia_curso-de-reeducacion-vial.md`
- `references/manual_caba_examen-de-conduccion.md`
- `references/examen-real.md` — preguntas recordadas del examen real
- `simulador-test-de-conducir/src/data/` (en raíz del repo, solo disponible si se clonó el repo)

Datos del usuario (en `~/.local/share/reeducacion-vial/`):
- `practica.md` — historial de exámenes
- `backlog.md` — errores pendientes de repasar

Si los archivos de usuario no existen, crear el directorio y los archivos con esta estructura:

practica.md:
```
# Registro de Práctica - Reeducación Vial
## Historial de Exámenes (orden cronológico descendente)
## Progreso General
| Examen | Fecha | Fuente | Score | % |
|--------|-------|--------|-------|---|
```

backlog.md:
```
# Backlog - Preguntas a Repasar
## Pendientes
| ID | Tema | Respuesta incorrecta | Respuesta correcta | Fuente | Fecha agregada |
|----|------|---------------------|-------------------|--------|----------------|
## Resueltas
| ID | Tema | Fecha resuelta |
|----|------|----------------|
```

## Al comenzar

1. Preguntar fuente:
  - Reeducacion vial:
    - manual Reid,
    - manual Creando Conciencia,
  - Examen de conducir de CABA:
    - Manual CABA,
    - simulador (simulador-test-de-conducir/src/data/, solo si se clonó el repo)
2. Explicar formato:
   - 20 preguntas, 4 a la vez
   - Responder: `a, b, c, d`
   - Resultados al final
   - Usar `*` para notas (ej: `* explicar este concepto`)
3. Informar al usuario: "Tu progreso se guarda en `~/.local/share/reeducacion-vial/`"
4. Leer `~/.local/share/reeducacion-vial/backlog.md` e incluir preguntas pendientes
5. Leer `~/.local/share/reeducacion-vial/practica.md` y listar los temas ya preguntados en exámenes anteriores
6. Leer `references/examen-real.md` para conocer temas del examen real
7. Seleccionar preguntas en este orden de prioridad:
   - **Primero:** temas en backlog (errores previos) — repetir hasta que se acierten
   - **Segundo:** temas de `examen-real.md` — priorizar lo que realmente se toma en el examen
   - **Tercero:** temas nuevos no aparecidos en practica.md — explorar áreas menos obvias del manual
   - **Cuarto (si no hay suficientes):** reciclar los más antiguos de practica.md

## Durante

- 20 preguntas, 4 a la vez
- Mezclar orden (no seguir secuencia del manual)
- Buscar activamente temas poco explorados del manual (no siempre los mismos "clásicos")
- 3 opciones por pregunta (a, b, c)
- Variar posición de respuesta correcta
- No mostrar resultados parciales

## Al finalizar

1. **Discutir notas** marcadas con `*`
2. **Mostrar resultados:**
   - Tabla resumen (fecha, total, correctas, %, fuente)
   - Tabla de errores (tema, respuesta dada, correcta)
3. **Actualizar `~/.local/share/reeducacion-vial/backlog.md`:**
   - Agregar errores nuevos (evitar duplicados)
   - Eliminar preguntas respondidas correctamente
4. **Registrar en `~/.local/share/reeducacion-vial/practica.md`** con timestamp descendente
