# Mapa de recuperación y migración

## Repositorios

- Nuevo destino: [CA0SC0RP/Mundo-en-papel](https://github.com/CA0SC0RP/Mundo-en-papel).
- Fuente histórica: [CA0SC0RP/art-Design-Music](https://github.com/CA0SC0RP/art-Design-Music).
- Rama histórica prioritaria para auditar: `feature/living-paper-engine-foundation`.
- HEAD observado de esa rama: `2734257ca0515c98637689b4a906c4ad0da9dfe9`.

El repositorio anterior debe permanecer intacto. La migración será selectiva, con revisión de compatibilidad, dependencias y licencias. No tomar `main` del repositorio anterior como fuente completa: tiene menos archivos que la rama avanzada.

## Inventario histórico localizado en la rama avanzada

| Recurso | Ubicación anterior | Tratamiento |
|---|---|---|
| Editor articulado | `prototype/character-editor-v01/` | Prioridad de auditoría y posible migración |
| Prueba de estudio | `prototype/caricature-studio-v01/` | Revisar como prototipo de flujo, no editor completo |
| Creative Control | `creative-control/` | Recuperar adaptador, registro, validador, preview y contratos |
| Motor PixiJS | `living-paper-engine/` | Conservar como laboratorio; extraer solo componentes compatibles |
| Pruebas | `tests/` | Migrar junto con el código y repetirlas |
| Cinco prototipos ambientales | `prototype/level-01` a `level-05` | Archivo histórico visual/técnico; no núcleo del producto |
| Documentación reciente | `docs/` y `living-paper-engine/` | Revisar antes de copiar; algunos documentos están archivados |
| Imagen maestra 4K | `cuadro_vivo_mountains_that_breathe_master_4k.png` | Conservar como referencia histórica; no modificar |

## Hallazgos técnicos concretos

### Editor de personajes

El prototipo avanzado v0.9.x contiene:
- piezas y jerarquías de personaje;
- pivotes, transformación y límites articulares;
- biblioteca de poses y expresiones;
- mallas editables, pesos e influencias;
- skinning y geometría de rig;
- IK 2D;
- importación/exportación JSON;
- controles Pointer Events y objetivos táctiles de al menos 44 px.

Estas capacidades se verificaron por lectura de código y documentación. La calidad de interacción y representación debe comprobarse en navegador real, especialmente Safari en iPad.

### Creative Control

La rama avanzada incluye:
- adaptador de contexto y notificaciones de cambios;
- catálogo de capacidades detectadas;
- esquema y validador de propuestas;
- simulación no mutante;
- vista previa temporal aislada.

El registro consultado mantiene la ejecución de acciones de IA deshabilitada. Aprobación humana, commit transaccional, undo y chat persistente no deben darse por terminados sin comprobar implementación posterior.

### Motor PixiJS

Existe un laboratorio con escenario, transformaciones, trayectorias, articulaciones y módulos especializados de papel (capas, pliegues, deformación, volumen, cantos y contacto). La auditoría histórica recomienda separar el núcleo genérico de escena/render de los módulos específicos de materialidad de papel. No es todavía el editor de personajes ni un producto integrado.

## Pruebas históricas registradas

- Editor v0.9.31: CI #116, 93 pruebas aprobadas, 0 fallidas.
- Creative Control con preview aislada: CI #139, 110 pruebas aprobadas, 0 fallidas.

Son resultados registrados en la documentación histórica, no una garantía del HEAD actual. Repetirlos sobre el commit exacto que se migre. Las pruebas automatizadas no certifican funcionamiento táctil/visual en Safari/iPad.

## Orden de recuperación

1. Inspeccionar el prototipo de personajes y sus módulos locales.
2. Revisar sus pruebas, scripts de CI y dependencias.
3. Inspeccionar Creative Control y distinguir lectura, propuesta, preview y ejecución real.
4. Revisar el estudio de caricaturas v0.1 y compararlo con la dirección simplificada actual.
5. Auditar el motor PixiJS y decidir qué componentes genéricos conviene extraer.
6. Preparar una migración por módulos, conservando rutas de origen y commits.
7. Ejecutar pruebas y abrir el resultado en Codespaces desde iPad.
8. Registrar problemas, compatibilidad, licencias y decisiones antes de ampliar el alcance.

## Qué no migrar automáticamente

- El reproductor de cuadros ambientales como arquitectura central.
- El flujo antiguo de loops musicales.
- Las coordenadas, capas o esquemas exclusivos de Mountains That Breathe.
- Código sin revisar dependencias, licencias, seguridad y compatibilidad.
- Archivos grandes sin verificar tamaño e integridad.

## Imágenes

Las imágenes pueden documentarse y mostrarse mediante Markdown. Para que formen parte física del repositorio nuevo deben copiarse a `assets/references/`, conservando originales, procedencia y hash. La imagen maestra histórica sigue enlazada desde el repositorio anterior; todavía no se ha duplicado en este repositorio.

## Criterio de finalización de migración

Cada módulo migrado debe tener:
- commit de origen y ruta original;
- lista de archivos y dependencias;
- licencia y atribuciones revisadas;
- pruebas ejecutadas y resultado;
- cambios necesarios para el nuevo alcance;
- evidencia de ejecución y revisión táctil/mouse.
