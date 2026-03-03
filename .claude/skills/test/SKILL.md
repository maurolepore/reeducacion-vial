---
name: test
description: Genera exámenes de práctica de reeducación vial (20 preguntas multiple choice). Usar cuando el usuario quiera practicar para el examen, repasar temas, o pida un test/examen de práctica. Fuentes disponibles: manual Sistemas Reid, manual Creando Conciencia, preguntas CABA.
---

# Examen de Reeducación Vial

Genera exámenes de práctica para el curso de reeducación vial de CABA (recuperación de 4 puntos).

## Al comenzar

1. Preguntar fuente: 
  - Reeducacion vial: 
    - manual Reid, 
    - manual Creando Conciencia, 
  - Examen de conducir de CABA: 
    - Manual CABA, 
    - simulador (simulador-test-de-conducir/src/data/
2. Explicar formato:
   - 20 preguntas, 4 a la vez
   - Responder: `a, b, c, d`
   - Resultados al final
   - Usar `*` para notas (ej: `* explicar este concepto`)
3. Leer `backlog.md` e incluir preguntas pendientes
4. Leer `practica.md` y listar los temas ya preguntados en exámenes anteriores
5. Seleccionar preguntas en este orden de prioridad:
   - **Primero:** temas en backlog (errores previos) — repetir hasta que se acierten
   - **Segundo:** temas nuevos no aparecidos en practica.md — explorar áreas menos obvias del manual
   - **Tercero (si no hay suficientes):** reciclar los más antiguos de practica.md

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
3. **Actualizar backlog.md:**
   - Agregar errores nuevos (evitar duplicados)
   - Eliminar preguntas respondidas correctamente
4. **Registrar en practica.md** con timestamp descendente

## Archivos

- `practica.md` - Historial de exámenes
- `backlog.md` - Errores pendientes de repasar (mismo directorio)
- Manuales en directorio raíz del proyecto
