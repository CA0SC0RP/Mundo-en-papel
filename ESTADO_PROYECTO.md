# Estado del proyecto — Mundo en Papel

**Última actualización:** 2026-11-02  
**Estado:** recuperación documental completada en esta rama; auditoría y migración de código pendientes.

## Repositorio nuevo

- Destino: [CA0SC0RP/Mundo-en-papel](https://github.com/CA0SC0RP/Mundo-en-papel).
- Rama base: `main`, que conserva el README inicial.
- Rama de trabajo documental: `docs/base-continuidad-y-migracion`.
- Esta rama contiene documentos de continuidad y referencias; todavía no contiene el motor ni el editor migrado.

## Objetivo vigente

Desarrollar un estudio para crear microhistorias y cortometrajes animados con estética artesanal de papel recortado, con una duración orientativa inicial de alrededor de un minuto. La prioridad funcional es completar el editor de personajes, después escenas y animación, timeline, renderizado/exportación local y, más adelante, el reproductor Android TV.

## Dirección de producto aprobada

- ToonSquid para iPad como referencia principal de capacidades, organización y flujo; no clonarlo.
- Interfaz propia, limpia, moderna y fluida, diseñada para touch y compatible con mouse/puntero.
- Simplificar el alcance; no dividir el producto en cuatro subprogramas grandes.
- Reutilizar el editor de personajes y Creative Control existentes.
- Herramientas avanzadas mediante paneles contextuales y opcionales.
- Música, diálogo y efectos como recursos de la historia, no como reproductor de paisajes musicales en loop.

## Hallazgo importante: el repositorio anterior tiene ramas más avanzadas que main

La auditoría inicial del repositorio anterior debe tomar como fuente prioritaria la rama histórica:

`CA0SC0RP/art-Design-Music — feature/living-paper-engine-foundation`

HEAD observado al consultar GitHub: `2734257ca0515c98637689b4a906c4ad0da9dfe9`.

La rama `main` del repositorio anterior no contiene todo el trabajo reciente. No migrar desde `main` sin comparar las ramas y confirmar los archivos.

## Inventario técnico de la rama avanzada

En `feature/living-paper-engine-foundation` se localizaron:

- Editor articulado de personajes v0.9.x en `prototype/character-editor-v01/`, con archivos separados para IK, geometría, malla, skinning y guardado/carga de proyectos.
- Pruebas de editor, IK, mallas, skinning, geometría y serialización.
- Creative Control: adaptador de solo lectura, registro de capacidades, esquema de propuestas, validador y vista previa aislada.
- Motor experimental PixiJS en `living-paper-engine/`, con módulos de geometría, deformación, rigging, capas, volumen y colisiones.
- Prototipo de estudio `prototype/caricature-studio-v01/`.
- Cinco prototipos de escena anteriores `prototype/level-01` a `level-05`.
- Documentación actualizada de dirección, auditoría de reutilización, Codespaces y render local.

## Estado registrado en la rama avanzada

La documentación de esa rama registra:

- Editor de personajes: versión v0.9.33 en el último registro consultado.
- CI #116: 93 pruebas superadas, 0 fallidas para la versión v0.9.31.
- Creative Control: registro de capacidades, validación estructurada de propuestas y vista previa creativa aislada no mutante.
- CI #139: 110 pruebas superadas, 0 fallidas para la etapa de vista previa creativa.
- La ejecución de CI valida lógica y estructura; no sustituye la prueba visual y táctil real en Safari/iPad.
- La inspección visual y táctil en Safari/iPad seguía pendiente en los registros consultados.

Estos resultados son históricos y deben repetirse sobre el commit exacto que se decida migrar. No asumir que el HEAD actual coincide con el commit de cada ejecución de CI.

## Límites: no declarar como terminado

No hay evidencia suficiente para afirmar que ya están terminados:
- editor completo listo para producción;
- integración de todos los subsistemas del motor;
- timeline narrativa;
- editor/secuenciador completo de escenas;
- render y exportación de vídeo local;
- exportación 4K/HDR verificada en iPad;
- compatibilidad certificada con Safari, Chrome, Firefox y Opera en iPad;
- flujo completo de Creative Control con aprobación, ejecución transaccional, undo y chat.

## Próximos pasos

1. Abrir el Codespace del repositorio nuevo en la rama `docs/base-continuidad-y-migracion`.
2. Comparar el repositorio histórico en la rama `feature/living-paper-engine-foundation` y revisar sus commits.
3. Ejecutar pruebas y revisar los archivos actuales sin alterar el repositorio original.
4. Auditar primero editor de personajes y Creative Control; conservar el motor PixiJS como laboratorio reutilizable, no imponerlo como núcleo sin evaluación.
5. Migrar por módulos a una rama de trabajo nueva y comprobar el funcionamiento desde el iPad.

## Registro de esta etapa

- Documentación de continuidad creada en una rama separada.
- Se identificó una rama histórica más avanzada que `main`; la migración se debe basar en esa revisión, no en la rama `main` antigua.
- El repositorio anterior permanece intacto.
- No se han copiado todavía código ni imágenes binarias al repositorio nuevo.
