# La Ultimita, app web para iPhone y Android

Funciona en el navegador y se instala en la pantalla de inicio. No necesita Claude, ni App Store, ni Google Play. Tampoco necesita internet para verse: las tipografías (Inter y Barlow Condensed) vienen incluidas en esta carpeta.

## A. Publicarla (una sola vez, unos 10 minutos; es más fácil desde un computador)
1. Crea una cuenta gratis en github.com.
2. Toca "+" > New repository. Nombre: `ultimita`. Marca Public. Create repository.
3. Toca "uploading an existing file" y suelta TODOS los archivos de esta carpeta (los archivos, no la carpeta): index.html, data.json, sw.js, manifest.webmanifest, los 3 íconos .png, los 5 archivos .woff y los 2 de texto. Commit changes.
4. Entra a Settings > Pages. En Source elige "Deploy from a branch", rama `main`, carpeta `/ (root)`, y Save.
5. En 1 o 2 minutos aparece la dirección `https://TU-USUARIO.github.io/ultimita/`. Ese es el link para los jugadores.

Si ya la tenías publicada: sube y reemplaza todos los archivos. Antes de reemplazar `data.json`, expórtalo desde la app (Editar > Exportar archivo) por si publicaste cambios que no quieres perder, y pásaselo a Claude.

Instalarla en el celular:
- iPhone: abrir el link en Safari > Compartir > Agregar a pantalla de inicio.
- Android: abrir el link en Chrome > menú de tres puntos > Instalar app (o Agregar a pantalla principal).

## B. Modo editor (solo el DT)
1. En la app, arriba a la derecha, abre el selector "Soy..." y elige "DT (cuerpo técnico)". Aparece el botón "Editar" y la app entra directo en modo edición. La app recuerda tu elección en ese dispositivo. Si eliges a un jugador, la edición se apaga.
2. Para publicar necesitas un token de GitHub: tu foto > Settings > Developer settings > Personal access tokens > Fine-grained tokens > Generate new token. En Repository access elige "Only select repositories" y `ultimita`. En Repository permissions pon Contents: Read and write. Genera el token y cópialo.
3. En la app: Editar > Configurar GitHub. Escribe `TU-USUARIO/ultimita` y pega el token.
4. Edita y toca "Publicar cambios". Los jugadores ven el cambio en 1 o 2 minutos, al abrir o recargar la app.

Sin token: toca "Exportar archivo" y reemplaza `data.json` en el repositorio (Add file > Upload files).

Importante sobre quién puede editar: la opción "DT" no tiene clave. Un jugador que la elija en su teléfono podría mover cosas, pero solo en su propio teléfono: lo que ven los demás cambia únicamente cuando se publica `data.json`, y eso exige el token de GitHub, que solo tienes tú. Si quieres que además pida una clave para entrar como DT, se puede agregar.

### Qué puedes editar
**Pestaña Partido** (con "Editar" activado):
- Datos del partido: rival, fecha, hora, lugar y esquema rival (por ejemplo 1-3-3-1).
- Titulares: elige quién juega en cada posición.
- Fichas libres: arrastra con el dedo a nuestros jugadores y, con "Ver rival", también las fichas rojas del rival. Los botones "Mover nuestros" y "Mover rival" bloquean una de las dos para poder agarrar una ficha que quedó debajo de otra. "Restablecer" vuelve a la posición original. Las posiciones se guardan por separado para "Con balón" y "Sin balón".

**Pestaña Jugadas** (con "Editar" activado):
- "+ Agregar jugada" crea una jugada nueva; "Editar jugada" abre las existentes.
- Cada jugada puede tener varios pasos ("+ Paso" copia las posiciones del paso actual). En cada paso mueves las fichas y escribes un texto corto.
- Herramientas: Mover (fichas y balón), Flecha (movimiento, línea punteada), Pase (línea continua), Etiqueta (cambia el texto de una ficha) y Borrar (ficha, balón o flecha).
- "Flechas desde el paso anterior" dibuja solas las flechas de lo que se movió respecto al paso anterior.
- "+ Jugador" y "+ Rival" agregan fichas; las fichas del rival son rojas.
- "Reproducir" anima la jugada paso a paso. Los jugadores la ven con "Anterior", "Siguiente" y "Reproducir".
- Las jugadas que traía la app (estructuras, repliegue, recuperación y basculaciones) siguen marcadas "Borrador" hasta que las apruebes con "Listo".

Todo queda guardado en tu dispositivo mientras editas y se sube al repositorio al tocar "Publicar cambios".

## C. Tabla, fixture y datos del partido
Los carga Claude. Pásale los datos y el `data.json` actual, y te devuelve uno actualizado para subir al repositorio. Si no le das el actual, se pierden los cambios que hayas publicado desde la app.

## Avisos
- El repositorio es público: cualquiera con el link puede ver nombres, asistencia y jugadas. Un repositorio privado con Pages requiere un plan de pago de GitHub (verifica las condiciones vigentes).
- El token da permiso de escritura sobre ese repositorio. Queda guardado solo en tu teléfono. No lo compartas; si lo pierdes, bórralo en GitHub.
- Los nombres de los menús de GitHub cambian de vez en cuando.
- Las tipografías Inter y Barlow Condensed se incluyen bajo licencia SIL Open Font License (ver `LICENCIAS-FUENTES.txt`).
- Probado en un navegador de escritorio simulando un teléfono: edición de fichas, jugadas con pasos y flechas, animación y modo sin conexión. No se probó en teléfonos reales: la publicación a GitHub, la instalación en pantalla de inicio ni el uso con el dedo (arrastrar en pantalla táctil).

## Instrucciones por posición
En la pestaña Partido, bajo la alineación, cada jugador ve las instrucciones de su posición abiertas (elige su nombre en «Soy…»). Quien no elige nombre las ve todas.
El DT las edita con «Soy… → DT»: una instrucción por línea, con el formato «Momento: texto». Se publican igual que el resto de los datos.
