# Mapa de recuperación y migración

## Repositorios

- Nuevo destino: [CA0SC0RP/Mundo-en-papel](https://github.com/CA0SC0RP/Mundo-en-papel).
- Fuente histórica: [CA0SC0RP/art-Design-Music](https://github.com/CA0SC0RP/art-Design-Music).

El repositorio anterior debe permanecer intacto. La migración será selectiva, con revisión de compatibilidad, dependencias y licencias.

## Inventario histórico localizado

| Recurso | Ubicación anterior | Tratamiento |
|---|---|---|
| Editor de personajes v0.1 | `prototype/character-editor-v01/index.html` | Auditar e intentar ejecutar antes de migrar |
| Creative Control | `creative-control/` | Revisar README, adaptador y contrato |
| Pruebas de interacción | `tests/editor-input.test.js` | Revisar dependencias y cobertura |
| Pruebas de contrato v2 | `tests/test_contrato_v2.py` | Histórico; evaluar si aplica al nuevo producto |
| Documentación raíz | `ARQUITECTURA.md`, `BITACORA.md`, `ESTADO_PROYECTO.md`, `INSTRUCCIONES_PARA_IA.md` | Archivo histórico; no copiar como verdad vigente |
| Imagen maestra | `cuadro_vivo_mountains_that_breathe_master_4k.png` | Preservar original; referencia visual histórica |
| Índice y esquema de obras | `works/index.json`, `works/work.schema.json` | Evaluar compatibilidad; no imponer al nuevo flujo sin revisión |

## Orden de recuperación

1. Leer el prototipo de personajes y determinar su estructura, dependencias y estado.
2. Leer Creative Control y su contrato de sincronización.
3. Revisar pruebas existentes y ejecutarlas sin modificar el original.
4. Comparar componentes con las necesidades actuales de Mundo en Papel.
5. Proponer un plan de migración por módulos, con rutas y pruebas.
6. Copiar únicamente los componentes aprobados a una rama de trabajo.
7. Verificar que el prototipo migrado se ejecuta en Codespaces y puede usarse desde iPad.

## Qué no migrar automáticamente

- La arquitectura de cuadros ambientales como arquitectura central.
- El antiguo reproductor musical o su flujo de loops.
- Coordenadas, capas o esquemas que solo servían a Mountains That Breathe.
- Código sin revisar dependencias, licencias, seguridad y compatibilidad.
- Archivos generados o binarios grandes sin verificar tamaño e integridad.

## Imágenes

Las imágenes pueden documentarse aquí y mostrarse en Markdown. Para que formen parte física del nuevo repositorio deben copiarse a una carpeta como `assets/references/` y subirse conservando el original, procedencia y hash. La imagen maestra histórica sigue enlazada desde el repositorio anterior; aún no se ha duplicado en este repositorio.

## Criterio de finalización de migración

Cada módulo migrado debe tener:
- commit de origen y ruta original;
- lista de archivos y dependencias;
- licencia y atribuciones revisadas;
- pruebas ejecutadas y resultado;
- cambios necesarios para el nuevo alcance;
- evidencia de ejecución y revisión táctil/mouse.
