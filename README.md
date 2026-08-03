# ✈️ Avioncito de Papel — Modo Infinito

Un juego estilo *Flappy Bird*, pero con un avioncito de papel. Vuela sin parar, dispara a las naves enemigas, esquiva los tubos y trata de superar tu mejor puntuación.

Jugable directamente en el navegador, sin necesidad de instalar nada.

## 🎮 Cómo jugar

- **Clic / toque en la pantalla / ESPACIO** → volar y disparar a la vez
- **Flechas del teclado** → control direccional libre:
  - `↑` subir
  - `↓` bajar
  - `←` retroceder
  - `→` avanzar
- **Tecla `X`** → disparar (sin volar)
- **Botón ⏸ / tecla `P` / `Escape`** → pausar la partida
- Botones en pantalla `VOLAR` y `🔫` → controles táctiles para celular

No hay niveles ni mundos distintos: es un solo escenario infinito. Cada 10 puntos aparece una nave enemiga más resistente que da puntos extra si la derribas. La dificultad sube poco a poco mientras más puntos consigues.

## 📱 Instalarlo como app en el celular (sin verse como página web)

Este juego es una **PWA (Progressive Web App)**: una vez publicado con GitHub Pages (ver más abajo), puedes agregarlo a la pantalla de inicio de tu celular y se abrirá **a pantalla completa, como una app**, sin barra de direcciones ni íconos del navegador.

### En iPhone (Safari)
1. Abre el enlace del juego en **Safari** (tiene que ser Safari, no Chrome, para que funcione el ícono de instalación).
2. Toca el botón de **compartir** (el cuadrito con la flecha hacia arriba).
3. Baja y toca **"Agregar a pantalla de inicio"** (Add to Home Screen).
4. Confirma el nombre y toca **"Agregar"**.
5. Listo: aparecerá un ícono del avioncito en tu pantalla de inicio. Al abrirlo, el juego se abre a pantalla completa, sin ninguna barra ni enlace visible, igual que una app normal.

### En Android (Chrome)
1. Abre el enlace del juego en **Chrome**.
2. Toca el menú de **tres puntos** (⋮) arriba a la derecha.
3. Toca **"Agregar a pantalla de inicio"** o **"Instalar aplicación"** (el texto varía según la versión de Chrome).
4. Confirma.
5. El ícono del avioncito quedará en tu pantalla de inicio y el juego abrirá en modo pantalla completa, como una app instalada.

## 🚀 Cómo subir este proyecto a GitHub y activar la página (GitHub Pages)

### 1. Crea el repositorio en GitHub
1. Entra a [github.com](https://github.com) e inicia sesión.
2. Haz clic en el botón **"New"** (Nuevo repositorio), arriba a la izquierda o en el ícono **+** de la esquina superior derecha → **"New repository"**.
3. Ponle un nombre, por ejemplo: `avioncito-de-papel`.
4. Déjalo en **Public** (público) para poder usar GitHub Pages gratis.
5. **No** marques la opción de agregar README (ya tienes uno en este repositorio).
6. Haz clic en **"Create repository"**.

### 2. Sube los archivos
La forma más fácil, sin usar la terminal:
1. En la página de tu nuevo repositorio, haz clic en **"uploading an existing file"** (o el botón **"Add file" → "Upload files"**).
2. Arrastra el archivo `index.html` (y el `README.md` si quieres) a la ventana del navegador.
3. Baja hasta el final y haz clic en **"Commit changes"**.

Si prefieres usar la terminal (con Git instalado):
```bash
git init
git add .
git commit -m "Primer commit: Avioncito de Papel"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/avioncito-de-papel.git
git push -u origin main
```
(Reemplaza `TU-USUARIO` por tu nombre de usuario de GitHub y `avioncito-de-papel` por el nombre real que le pusiste al repositorio.)

### 3. Activa GitHub Pages
1. En tu repositorio, ve a la pestaña **"Settings"** (Configuración).
2. En el menú de la izquierda, haz clic en **"Pages"**.
3. En **"Build and deployment"** → **"Source"**, selecciona **"Deploy from a branch"**.
4. En **"Branch"**, elige **`main`** y la carpeta **`/ (root)`**.
5. Haz clic en **"Save"**.
6. Espera uno o dos minutos. GitHub te mostrará un enlace tipo:
   ```
   https://TU-USUARIO.github.io/avioncito-de-papel/
   ```
7. ¡Listo! Ese enlace ya es tu juego publicado y jugable desde cualquier navegador o celular.

## 📁 Contenido del repositorio

```
avioncito-de-papel/
├── index.html              ← el juego completo (HTML, CSS y JavaScript)
├── manifest.json           ← configuración de la app (nombre, ícono, modo pantalla completa)
├── sw.js                   ← service worker (permite que funcione offline y se instale bien)
├── icons/
│   ├── icon-192.png        ← ícono para Android
│   ├── icon-512.png        ← ícono grande para Android / splash screen
│   ├── maskable-512.png    ← ícono adaptable (Android "maskable icon")
│   ├── apple-touch-icon.png← ícono para "Agregar a pantalla de inicio" en iPhone
│   └── favicon-32.png      ← ícono pequeño para la pestaña del navegador
├── README.md                ← este archivo, con las instrucciones
└── LICENSE                   ← licencia MIT (uso libre)
```

## 🛠️ Notas técnicas

- El juego funciona como una **PWA (Progressive Web App)**: incluye `manifest.json` y un ícono de avioncito de papel, para que se pueda instalar en la pantalla de inicio de iPhone y Android y se abra en pantalla completa, sin verse como una página web.
- Incluye un `sw.js` (service worker) básico que permite que el juego cargue incluso sin conexión, una vez visitado por primera vez.
- No depende de librerías externas ni de un servidor backend, por lo que funciona perfectamente con GitHub Pages, Netlify, Vercel o cualquier hosting estático (debe servirse por **https**, que es justo lo que hace GitHub Pages, para que la instalación como app funcione correctamente).
- La pantalla se adapta automáticamente al tamaño y orientación del dispositivo (horizontal o vertical), incluyendo el "notch" de los iPhone más recientes.
- La puntuación más alta se guarda solo mientras la pestaña o la app esté abierta (no hay guardado permanente entre sesiones).

## 📄 Licencia

Este proyecto se distribuye bajo la licencia MIT. Eres libre de usarlo, modificarlo y compartirlo.
