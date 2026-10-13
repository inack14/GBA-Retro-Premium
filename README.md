# GBA Retro Premium (Android)

Proyecto Android para emulación GBA mediante EmulatorJS. No incluye ROMs. La primera carga del núcleo requiere internet.

## Obtener el APK sin Android Studio (desde el teléfono)

Este proyecto incluye una compilación en la nube mediante GitHub Actions. No puedo generar ni adjuntar un APK ya compilado desde este entorno porque no dispone de Android SDK/Gradle ni acceso a una cuenta de compilación. Sigue estos pasos desde el navegador del teléfono:

1. Descarga `GBA_Retro_Premium_CloudBuild.zip` y descomprímelo con el administrador de archivos.
2. Entra a https://github.com/new e inicia sesión o crea una cuenta.
3. Crea un repositorio llamado `GBA-Retro-Premium`. Puede ser privado.
4. Sube los archivos y carpetas del proyecto descomprimido, incluida la carpeta oculta `.github/workflows`. Si la web móvil no permite subir carpetas completas, activa la opción de sitio de escritorio. También puedes crear el archivo `.github/workflows/android-apk.yml` con el contenido incluido en el ZIP.
5. Abre la pestaña **Actions** del repositorio. Habilita workflows si GitHub lo solicita.
6. Selecciona **Build GBA Retro Premium APK** y pulsa **Run workflow** si no se inició automáticamente.
7. Espera a que la ejecución termine con marca verde. Abre esa ejecución, baja a **Artifacts** y descarga `GBA-Retro-Premium-debug-apk`.
8. Descomprime el ZIP del artefacto en tu teléfono. Toca `app-debug.apk` para instalarlo. Si Android lo solicita, permite temporalmente instalar apps desde ese navegador o administrador de archivos.

## Requisitos y uso

- Android 6.0 o posterior recomendado.
- Internet para descargar EmulatorJS desde su CDN.
- ROMs `.gba` propias o que tengas derecho a usar.
- Abre la app, toca **Abrir ROM** y elige el archivo del juego.
- Los controles táctiles los proporciona EmulatorJS. Usa su menú para funciones de estado si las llamadas rápidas no están disponibles.

## Funciones y limitaciones

- Selector de ROM, pantalla inmersiva, filtros visuales y selector de velocidad.
- Guardar/cargar estado y velocidad dependen de las APIs disponibles en la versión del núcleo EmulatorJS.
- El APK de Actions es una compilación de depuración (`debug`), útil para instalar y probar en tu teléfono, no para distribución comercial.
- No incluye ROMs comerciales. La emulación depende de recursos remotos de EmulatorJS y puede dejar de funcionar si cambia su CDN o API.
