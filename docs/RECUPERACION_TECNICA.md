# Recuperación técnica — fuente histórica avanzada

## Fuente exacta consultada

- Repositorio: `CA0SC0RP/art-Design-Music`
- Rama: `feature/living-paper-engine-foundation`
- HEAD observado al consultar GitHub: `2734257ca0515c98637689b4a906c4ad0da9dfe9`
- Fecha de consulta: 2026-11-02.

## Estado del editor

El árbol de archivos de esta rama contiene el prototipo `prototype/character-editor-v01/` con `index.html`, `ik-solver.js`, `mesh-model.js`, `mesh-skinning.js`, `project-io.js` y `rig-geometry.js`. También hay pruebas separadas para interacción, IK, malla, skinning, geometría y serialización.

El prototipo documenta versión v0.9.33. El historial incluye correcciones de validación de mallas, pesos, matrices, transformaciones jerárquicas, mensajes de error y entrada táctil/puntero. La última validación explícita de editor citada en el estado histórico fue CI #116 para v0.9.31: 93 pruebas superadas. Las versiones posteriores deben volver a validarse.

## Estado de Creative Control

Archivos localizados:
- `creative-control/adapter.js`
- `creative-control/capability-registry.js`
- `creative-control/proposal-validator.js`
- `creative-control/preview-state.js`
- `creative-control/contracts/action-proposal.schema.json`
- `creative-control/contracts/synchronization-protocol.md`

La documentación registra:
- contexto serializado e inmutable;
- catálogo de capacidades del editor;
- validación de propuestas contra el contexto y límites;
- simulación y vista previa sobre una copia temporal del proyecto;
- bloqueo de ejecución y ausencia de mutación en esta etapa.

CI #139 registró 110 pruebas superadas y 0 fallidas para la etapa de preview. El siguiente tramo —aprobación humana ligada a una propuesta, ejecución transaccional, undo y chat— requiere verificar su estado actual antes de implementarlo.

## Estado del motor experimental

La rama incluye `living-paper-engine/` con PixiJS y módulos de escenario, geometría, rigging, deformación, elasticidad, capas, volumen, cantos y colisiones, además de pruebas. La auditoría del 1 de noviembre recomienda reutilizar gradualmente el escenario, transformaciones y algunas abstracciones genéricas, sin imponer los módulos específicos de papel al editor de personajes.

## Estado de validación

La documentación histórica deja pendiente:
- inspección visual del editor en Safari de iPad;
- validación real de gestos touch y mouse;
- revisión visual de uniones y deformaciones de malla;
- prueba de rendimiento y estabilidad en el dispositivo;
- confirmación de CI sobre el HEAD exacto que se vaya a migrar.

## Precaución

Esta auditoría se basa en el árbol y documentos del commit consultado. No equivale a ejecutar el código ni a certificar su estado en el Codespace del usuario. El repositorio fuente permanece intacto.
