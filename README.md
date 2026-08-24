# Master IPTV v2

Versión 2 de Master IPTV, preparada para GitHub Pages y Android con Capacitor.

## Novedades v2

- TV en vivo.
- Películas.
- Series con temporadas y episodios para Xtream Codes.
- Favoritos.
- Historial.
- Buscador.
- Categorías.
- Múltiples listas guardadas.
- M3U por URL o contenido pegado.
- Xtream Codes por HTTP/HTTPS.
- Reproductor HLS/MP4.
- Interfaz responsive.
- Workflow de GitHub Pages actualizado a las versiones actuales de las acciones.

## GitHub Pages

En el repositorio:
Settings → Pages → Source → GitHub Actions.

Cada push a `main` vuelve a publicar `www/`.

## Android

Instala Node.js LTS y Android Studio. Después:

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

Desde Android Studio puedes generar un APK o AAB.

## Importante

Las credenciales de Xtream se guardan localmente en el dispositivo mediante `localStorage`; no se envían a Master IPTV. No pongas credenciales reales dentro del código del repositorio.

Los servidores IPTV deben permitir las peticiones necesarias desde navegador/WebView. Algunos servidores bloquean CORS.

Usa únicamente listas y servicios que tengas autorización para utilizar.
