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
"Añadir a pantalla de inicio" se usará automáticamente el icono rojo y
negro, sin pasos extra.




## Notas importantes

- **Los datos son locales al navegador.** Si borras el historial/caché del
  navegador, o usas "modo incógnito", perderás los registros. Para no
  perder nada, exporta a Excel de vez en cuando desde la pestaña
  "Exportar Excel" (te descarga un `.xlsx`).
- Si quieres ficharlo desde varios dispositivos y que todos vean lo mismo,
  esta versión no lo permite: haría falta una base de datos en algún
  servidor.
- El sitio funciona sin conexión salvo por dos recursos externos: la
  tipografía (Google Fonts) y la librería para generar el Excel (SheetJS,
  vía CDN). Si algún día dejan de estar disponibles, el resto de la app
  sigue funcionando salvo la exportación.
