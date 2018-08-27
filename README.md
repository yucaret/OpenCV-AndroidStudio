# Como configurar OpenCV en Android Studio para Windows de 64 bits

Configuración de OpenCV 3.4.2 (64 bits) en Android Studio 3.1.4 (64 Bits) para Windows 7, 10 o más de 64 bits.

## Requerimientos:

- Descargar OpenCV para windows de 64 bits (versiones 3.X.X) para Android (Android Pack): https://opencv.org/releases.html , descomprimirlo y colocarlo en la raiz de "C:" (para mayor facilidad).
- Descargar e Instalar Android Studio para Windows de 64 bits: https://developer.android.com/studio/
- Descargar NDK para windows de 64 bits: https://developer.android.com/ndk/downloads/?hl=es-419 , descomprimirlo y colocarlo en la raiz de "C:" (para mayor facilidad).

## Nota:

Previo a la configuración deben de tener bien parametrizado el SDK en Android Studio, para ello deben de realizar dentro de Android Studio lo siguiente:
- a) Ingresar a File--> Setting.
- b) Ir a la sección de "System Settings".
- c) En la Pestaña de "SDK Platforms" deben de tener instaladas las versiones de Android con la que desean desarrollar su App, en mi caso tengo todas las versiones superiores a la 3.0 (Honeycomb), ver imagen.

![androidstudio-settings-systemsettings-sdkplatforms](https://user-images.githubusercontent.com/31372472/44683648-899e9100-aa0c-11e8-8405-95160e9464b9.png)

- D) Luego configurar "SDK Tools", en mi caso tengo todas las opciones activas, pero las necesarias son las que se encuentran resaltadas, ver imagen.

![androidstudio-settings-systemsettings-sdktools](https://user-images.githubusercontent.com/31372472/44684655-40037580-aa0f-11e8-9c9b-f38e8c5cba42.png)
