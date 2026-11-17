# Turno de Sombra 3D

Prototipo de terror 3D original para Android hecho en HTML y Three.js. La imagen de referencia se usa solo para inspiración general de ambiente; personajes, escenario y materiales son propios del prototipo, no assets oficiales de FNAF.

## Juego actual
- Exploración en primera persona de oficina, pasillos laterales y acceso a comedor.
- Controles táctiles: joystick, deslizar para mirar, linterna, esconderse, compuertas y cambio de cámaras.
- Batería que se gasta con linterna y compuertas.
- Animatrónico original con máscara y ojos luminosos, que avanza hacia la oficina.
- Empaquetado Cordova. El HUD queda superpuesto al visor 3D.

## APK Android
GitHub Actions tiene un workflow manual, sin builds automáticos en cada push: **Actions → Android APK → Run workflow**. Descarga `Turno-de-Sombra-debug-APK` desde el artefacto del run cuando finalice.

## Build local
Node 20, Java 17 y Android SDK: `npm install`, `npx cordova platform add android@13`, `npx cordova build android --debug`.

## Nota de estado
Este es un primer prototipo de escenario y mecánicas; no afirmar prueba visual o táctil en teléfono hasta instalarlo y probarlo allí.
