# Estado del proyecto — Mundo en Papel

**Última actualización:** 2026-11-02  
**Estado:** fase de recuperación, inventario y preparación de la base de trabajo.

## Estado verificado del repositorio nuevo

- Repositorio: [CA0SC0RP/Mundo-en-papel](https://github.com/CA0SC0RP/Mundo-en-papel).
- Rama base: `main`.
- La rama de documentación actual es `docs/base-continuidad-y-migracion`.
- Antes de esta rama, `main` contenía únicamente un README mínimo.
- Esta rama incorpora documentos de continuidad; todavía no contiene el motor ni el prototipo migrado.

## Objetivo vigente

Desarrollar un estudio para crear microhistorias y cortometrajes animados de papel, con duración orientativa de alrededor de un minuto. El producto debe permitir crear personajes, escenas, animación y exportar el resultado desde iPad.

## Decisiones vigentes

- Interfaz y capacidades de animación tomando ToonSquid para iPad como referencia principal, sin clonarlo.
- Interfaz limpia, fluida y táctil; compatibilidad también con mouse y puntero.
- Simplificar el alcance y evitar cuatro subprogramas separados.
- Reutilizar el editor de personajes y Creative Control existentes, después de auditarlos.
- Prioridad del editor de personajes antes de ampliar escenas y timeline.
- Música como banda sonora, diálogo y efectos; no como reproductor de paisajes musicales en loop.
- Mantener el lenguaje visual de papel recortado, capas, bordes físicos, sombras y profundidad artesanal.

## Inventario histórico localizado en el repositorio anterior

Se verificó que `CA0SC0RP/art-Design-Music` contiene, al menos en su rama `main` consultada:

- Documentación raíz: `ARQUITECTURA.md`, `BITACORA.md`, `ESTADO_PROYECTO.md`, `INSTRUCCIONES_PARA_IA.md` y `README.md`.
- `creative-control/README.md`, `creative-control/adapter.js` y un contrato de sincronización.
- Prototipo `prototype/character-editor-v01/index.html`.
- Pruebas `tests/editor-input.test.js` y `tests/test_contrato_v2.py`.
- Documentos sobre contrato de capas, validación, producción por capas, dirección artística y partitura audiovisual.
- Imagen maestra histórica `cuadro_vivo_mountains_that_breathe_master_4k.png`.

Este inventario confirma que hay material recuperable; **no confirma** que todo ese material corresponda al alcance actual ni que funcione en el estado presente.

## Qué no debe darse por implementado

No declarar como terminados sin auditoría y pruebas actuales:
- motor de animación integrado;
- deformación y rigs completos;
- timeline final;
- editor de escenas;
- render/exportación local;
- aplicación Android TV;
- compatibilidad completa con iPad Safari y mouse;
- integración total de Creative Control.

Los resultados históricos de pruebas y las propuestas del antiguo proyecto deben volver a ejecutarse y revisarse en el código que se migre.

## Próximos pasos

1. Inspeccionar el README, dependencias, archivos y funcionamiento del prototipo de personajes.
2. Auditar Creative Control y sus contratos.
3. Identificar código reutilizable y dependencias/licencias.
4. Diseñar una migración incremental a este repositorio, preservando el repositorio anterior.
5. Ejecutar el prototipo en Codespaces y probarlo desde el iPad.
6. Registrar resultados verificables antes de comenzar nuevas funciones.

## Registro de cambios de esta etapa

- Se creó la rama `docs/base-continuidad-y-migracion` desde `main`.
- Se preparó documentación inicial de continuidad y recuperación.
- No se modificó ni eliminó el repositorio anterior.
- No se copiaron todavía binarios ni código del repositorio anterior.
