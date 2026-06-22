# Autogestor

App para gestionar vehículos y analizar costos: combustible, gastos, mantenimiento y backup. Funciona 100% en el navegador (localStorage), sin backend.

## Publicar en GitHub Pages

1. Creá un repositorio nuevo (puede ser privado o público).
2. Subí estos archivos a la raíz del repo: `index.html`, `manifest.json`, `sw.js`, `icon.svg`, `icon-192.png`, `icon-512.png`.
3. En el repo: **Settings → Pages → Source → Deploy from a branch**, elegí la rama `main` y la carpeta `/ (root)`.
4. Esperá 1-2 minutos. Tu app va a estar en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

## Instalar como app en el celular (Android Chrome)

Abrí la URL en Chrome → menú (⋮) → **Agregar a pantalla de inicio** / **Instalar app**. Queda con ícono propio y abre en pantalla completa.

## Datos y backup

- Todo se guarda en el `localStorage` del navegador donde la uses. Si cambiás de celular, reinstalás Chrome, o navegás en modo incógnito, **no vas a ver los datos anteriores**.
- Por eso: usá la pestaña **Backup** para exportar un `.json` cada vez que agregues información importante, y guardalo en Drive, email, etc.
- Para restaurar (mismo dispositivo nuevo o después de borrar datos), usá **Importar** en la misma pestaña.
- Si usás la app en más de un celular para el mismo auto, no se sincronizan solos — tenés que exportar de uno e importar en el otro manualmente.

## Sobre los intervalos de mantenimiento

Los ítems del "plan estándar" (cambio de aceite, neumáticos, bujías, etc.) usan intervalos genéricos de referencia, no datos específicos de tu modelo exacto — la app no tiene una base de datos de fabricantes. Editá los km/meses de cada ítem según el manual de tu vehículo para que las alertas sean precisas.

## Estructura de archivos

```
index.html      → la app completa (HTML+CSS+JS)
manifest.json   → metadata para instalar como PWA
sw.js           → service worker (uso offline básico)
icon.svg        → ícono vectorial
icon-192.png    → ícono PNG 192x192
icon-512.png    → ícono PNG 512x512
```
