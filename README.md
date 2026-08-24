# Master IPTV

Reproductor IPTV web preparado para GitHub Pages y Android mediante Capacitor.

## Qué incluye

- TV, Películas y Series.
- M3U por URL HTTP/HTTPS o contenido pegado.
- Xtream Codes mediante servidor HTTP/HTTPS, usuario y contraseña.
- Categorías y buscador.
- Reproductor HLS/MP4 compatible con el navegador.
- Guardado local de fuentes en el dispositivo/navegador.
- Interfaz responsive con animaciones.
- GitHub Actions para publicar `www/` en GitHub Pages.
- Proyecto Capacitor para generar APK/AAB.

> Utiliza únicamente listas y servicios que tengas autorización para utilizar.

## 1. Subir a GitHub

Crea un repositorio, por ejemplo `master-iptv`, y sube todo el contenido de esta carpeta.

Después entra en:
Settings → Pages → Build and deployment → Source → GitHub Actions.

El workflow incluido publicará automáticamente la carpeta `www/`.

## 2. Probar en GitHub Pages

Después de que termine Actions, GitHub mostrará la URL de Pages en:
Settings → Pages.

## 3. Generar Android

Requisitos:
- Node.js LTS
- Android Studio
- Android SDK

En una terminal dentro del proyecto:

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

En Android Studio puedes ejecutar la aplicación o generar el APK.

También puedes usar:

```bash
npm run build:android
```

Para una versión distribuible conviene configurar firma de lanzamiento.

## Nota IPTV

Un navegador o WebView puede bloquear peticiones a servidores que no permitan CORS. Eso depende del servidor IPTV y no de GitHub Pages.

La versión actual deja el catálogo de series preparado, pero la pantalla de temporadas/episodios puede añadirse después con `get_series_info` de Xtream.
