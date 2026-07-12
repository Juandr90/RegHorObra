# Control de jornada — Parte de horas

Webapp para fichar entrada/salida, consultar el historial y exportar un Excel
con la misma estructura que el parte de horas original (Horario, Jornada,
Trabajadores, Partidas, Observaciones).

Es una única página (`index.html`), sin backend ni build. Los datos se
guardan en el `localStorage` del navegador donde la abras, así que **solo
son visibles en ese navegador y ese dispositivo** (no se sincronizan entre
móvil y ordenador, ni entre navegadores distintos).

## Icono en pantalla de inicio

La carpeta `icons/` y el archivo `manifest.webmanifest` ya están enlazados
desde `index.html`. Si subes el repositorio tal cual (con la carpeta
`icons/` incluida), al abrir la web desde el móvil y elegir
"Añadir a pantalla de inicio" (Android/Chrome) o "Añadir a pantalla de
inicio" desde el botón compartir (iPhone/Safari), se usará automáticamente
el icono rojo y negro que nos pasaste, sin pasos extra.

## Cómo publicarla gratis con GitHub Pages

1. Crea un repositorio nuevo en GitHub (puede ser público o privado).
2. Sube estos archivos y carpetas a la raíz del repositorio: `index.html`,
   `manifest.webmanifest`, la carpeta `icons/` completa, y este `README.md`.
   Puedes hacerlo desde la web de GitHub con "Add file → Upload files"
   (arrastra también la carpeta `icons`), o por terminal:
   ```bash
   git init
   git add .
   git commit -m "Primera versión del parte de horas"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/TU_REPOSITORIO.git
   git push -u origin main
   ```
3. En GitHub, entra en **Settings → Pages** del repositorio.
4. En "Build and deployment" → "Source", elige **Deploy from a branch**.
5. En "Branch", selecciona `main` y la carpeta `/ (root)`, y pulsa **Save**.
6. Espera 1-2 minutos. GitHub te dará una URL del tipo:
   `https://TU_USUARIO.github.io/TU_REPOSITORIO/`
7. Abre esa URL: ya puedes fichar desde el móvil o el ordenador.

## Notas importantes

- **Los datos son locales al navegador.** Si borras el historial/caché del
  navegador, o usas "modo incógnito", perderás los registros. Para no
  perder nada, exporta a Excel de vez en cuando desde la pestaña
  "Exportar Excel" (te descarga un `.xlsx`).
- Si quieres ficharlo desde varios dispositivos y que todos vean lo mismo,
  esta versión no lo permite: haría falta una base de datos en algún
  servidor. Dímelo si te interesa y lo montamos.
- El sitio funciona sin conexión salvo por dos recursos externos: la
  tipografía (Google Fonts) y la librería para generar el Excel (SheetJS,
  vía CDN). Si algún día dejan de estar disponibles, el resto de la app
  sigue funcionando salvo la exportación.
