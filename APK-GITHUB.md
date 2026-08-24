# Crear el APK de Master IPTV desde GitHub

## 1. Subir los archivos

Sube todo el contenido de este proyecto a la rama `main` de tu repositorio.

## 2. Abrir Actions

En GitHub entra en:

Actions → Build Master IPTV APK

Pulsa:

Run workflow

## 3. Esperar la compilación

Cuando termine en verde:

Build Master IPTV APK → el trabajo `build-apk` → Artifacts

Descarga:

`Master-IPTV-debug`

Dentro estará:

`app-debug.apk`

Ese APK es una compilación de prueba para Android.

## 4. Para una versión de publicación

El APK de debug sirve para instalar y probar. Para publicar una aplicación formalmente se recomienda crear una firma propia y generar un APK/AAB de release.

## Nota

El workflow crea el proyecto Android automáticamente con Capacitor, por lo que no hace falta subir la carpeta `android/` al repositorio.

No guardes contraseñas IPTV, tokens ni claves privadas en el repositorio.
