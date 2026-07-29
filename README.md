# Elios Matrix — canal de actualizaciones

Repo público **solo para releases/updates** (no es el código fuente completo).

## Cómo publicar una versión nueva

1. Sube el instalador/zip en **Releases** (tag `vX.Y.Z`).
2. Actualiza `updates/manifest.json`:
   - `version` = misma versión (ej. `1.0.1`)
   - `downloadUrl` = URL del asset o de la release
   - `notes` = changelog corto
3. Actualiza `updates/newest.txt` con la misma versión (una línea).

La app consulta `updates/manifest.json` al arrancar y al pulsar **Update**.
