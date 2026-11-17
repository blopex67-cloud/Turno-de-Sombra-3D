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

## Actualización visual y de juego
- Modelo robot animado CC0 de Quaternius incorporado como Collada; se conserva el animatrónico procedural como respaldo mientras se verifica el modelo importado.
- Material PBR Concrete 047 A a 1K (base color, normal y roughness) en muros y piso.
- Sonidos OGG 48 kHz: ambiente industrial, drone, compuertas, cadenas y criatura.
- Movimiento con colisiones de límites, escritorio y mobiliario del comedor; los botones abren/cierran las compuertas laterales.
- HUD original de vigilancia con feed tipo CCTV, mapa de cámaras seleccionable, rótulo, scanlines y retícula.
- Consultar `ATTRIBUTIONS.md` para las licencias CC0, CC BY 4.0 y MIT.

### Correcciones posteriores basadas en capturas
- Quitada la placa de piso que estaba debajo de todos los pisos de zona; ahora el suelo se tesela con rectángulos complementarios y sin superficies coplanares, evitando el parpadeo/z-fighting y las franjas grises.
- Recortadas de nuevo las texturas aportadas, limpiando bordes del atlas; mipmaps y filtrado anisotrópico activados.
- Colisión axis-by-axis contra paredes, mesas, sillas, mostradores de cocina, baño, escenario, entrada, puertas y animatrónico; atravesar diagonalmente obstáculos ya no los salta.
- El animatrónico Quaternius/CC0 incluye clips de Collada `Robot_Idle`, `Robot_Walking`, `Robot_Running` y otros; el cargador conserva los nombres. Permanece en el escenario y cambia idle/caminar según su estado.
