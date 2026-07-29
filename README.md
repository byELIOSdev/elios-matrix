# Elios Matrix — canal de actualizaciones

Repo público **solo para releases/updates**.

## Versionado

Formato **major.minor**: `1.0`, `1.1`, `2.0`.

## Cómo publicar (auto-update)

1. Publica un **Release** con tag `v1.1` y un asset **`.zip`**.
   - El zip debe contener el contenido del publish (el `.exe` + DLLs),
     en la raíz del zip o en una sola carpeta interior.
2. Actualiza `updates/manifest.json`:
   - `version`: `1.1`
   - `downloadUrl`: URL directa del `.zip` (browser_download_url) **o**
     la página de release (la app buscará el asset `.zip` en Releases).
   - `notes`: changelog corto
3. Actualiza `updates/newest.txt` con `1.1`.

La app descarga el zip a `%TEMP%`, reemplaza **in-place** la instalación
actual y se reinicia. **No** crea carpetas `1.0`, `1.1` junto al programa.
