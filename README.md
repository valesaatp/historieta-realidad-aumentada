# Historieta AR: El secreto de la computadora

## Archivos
- `index.html`: página web con cuatro escenas, diálogos y módulo de cámara AR.
- `img/escena1.png` a `img/escena4.png`: las cuatro ilustraciones que también funcionarán como marcadores.
- `comic.mind`: **debes generarlo** con el compilador de MindAR a partir de las cuatro ilustraciones.

## 1. Crear el repositorio
1. Entra a https://github.com/new
2. Nombre sugerido: `historieta-realidad-aumentada`
3. Selecciona **Public** y crea el repositorio.
4. En el repositorio, usa **Add file > Upload files**.
5. Sube `index.html`, la carpeta `img` completa y este `README.md`. Después pulsa **Commit changes**.

## 2. Generar los marcadores para la realidad aumentada
1. Abre el compilador de imágenes de MindAR: https://hiukim.github.io/mind-ar-js-doc/tools/compile/
2. Carga las cuatro imágenes PNG de la carpeta `img` en este orden: `escena1.png`, `escena2.png`, `escena3.png`, `escena4.png`.
3. Compila las imágenes y descarga el archivo resultante `.mind`.
4. Cámbiale el nombre exactamente a `comic.mind`.
5. En GitHub, abre el repositorio y sube `comic.mind` a la raíz (al mismo nivel que `index.html`).

El orden importa porque la página asocia el índice 0 a escena 1, índice 1 a escena 2, etc.

## 3. Publicar con GitHub Pages
1. En el repositorio, abre **Settings**.
2. En el menú lateral entra a **Pages**.
3. En **Build and deployment**, elige **Deploy from a branch**.
4. Selecciona la rama `main` y la carpeta `/(root)`.
5. Pulsa **Save**.
6. Espera unos minutos. La URL se verá aproximadamente así: `https://TU-USUARIO.github.io/historieta-realidad-aumentada/`.

## 4. Probar
- Abre el enlace público en el celular, preferiblemente en Chrome.
- Pulsa **Iniciar cámara AR** y acepta el permiso de cámara.
- Apunta la cámara a una de las ilustraciones (por ejemplo, impresa o abierta en otra pantalla).
- La experiencia muestra mensajes digitales; en la escena 3 aparece un pequeño robot 3D.

## Si no funciona
- Confirma que `comic.mind` está en la raíz junto a `index.html`.
- Confirma que compilaste las imágenes en el mismo orden.
- La cámara solo funciona en HTTPS (GitHub Pages sí lo proporciona) y requiere permiso.
- Prueba con buena iluminación y una ilustración nítida. No apuntes la cámara a la misma pantalla del celular: imprime la imagen o ábrela en otra pantalla.
- Si el repositorio es público, el contenido de la página también será accesible públicamente. No subas datos personales.

## Nota técnica
GitHub Pages aloja archivos estáticos; la realidad aumentada se ejecuta en el navegador usando MindAR y A-Frame, cargados desde CDN. El archivo `comic.mind` no se incluye porque debe compilarse específicamente a partir de las cuatro imágenes finales.
