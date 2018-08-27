# Como configurar OpenCV en Android Studio para Windows de 64 bits

Configuración de OpenCV 3.4.2 (64 bits) en Android Studio 3.1.4 (64 Bits) para Windows 7, 10 o más de 64 bits.

## Requerimientos:

- Descargar OpenCV para windows de 64 bits (versiones 3.X.X) para Android (Android Pack): https://opencv.org/releases.html , descomprimirlo y colocarlo en la raiz de "C:" (para mayor facilidad).
- Descargar e Instalar Android Studio para Windows de 64 bits: https://developer.android.com/studio/
- Descargar NDK para windows de 64 bits: https://developer.android.com/ndk/downloads/?hl=es-419 , descomprimirlo y colocarlo en la raiz de "C:" (para mayor facilidad).

## Previo:

Previo a la configuración deben de tener bien parametrizado el SDK en Android Studio, para ello deben de realizar dentro de Android Studio lo siguiente:
- a) Ingresar a "File --> Setting".
- b) Ir a la sección de "System Settings".
- c) En la Pestaña de "SDK Platforms" deben de tener instaladas las versiones de Android con la que desean desarrollar su App, en mi caso tengo todas las versiones superiores a la 3.0 (Honeycomb), ver imagen.

![androidstudio-settings-systemsettings-sdkplatforms](https://user-images.githubusercontent.com/31372472/44683648-899e9100-aa0c-11e8-8405-95160e9464b9.png)

- d) Luego configurar "SDK Tools", en mi caso tengo todas las opciones activas, pero las necesarias son las que se encuentran resaltadas, ver imagen.

![androidstudio-settings-systemsettings-sdktools](https://user-images.githubusercontent.com/31372472/44684655-40037580-aa0f-11e8-9c9b-f38e8c5cba42.png)

## Pasos:

- 1) Crear el Proyecto.

![androidstudio-newproject](https://user-images.githubusercontent.com/31372472/44685662-a1c4df00-aa11-11e8-8f95-5c7555efa75e.png)

- 2) Nombrarlo, en ese caso se llama "OpenCVConfiguration".

![androidstudio-createandroidproject](https://user-images.githubusercontent.com/31372472/44685833-0bdd8400-aa12-11e8-8b19-f02ad5da7f86.png)

- 3) Seleccionar el tipo de Dispositivo; en mi caso, para mis proyectos, utilizo la versión 4.0 de Android, esto quiere decir que todos los dispositivos con esa versión o con con versiones actuales van a poder utilizar mi App.

![androidstudio-targetandroiddevices](https://user-images.githubusercontent.com/31372472/44685957-56f79700-aa12-11e8-82ed-91772b17cfaf.png)

- 4) Creamos la Activity (que viene a ser la pantalla principal del App), en este caso la coloco como en blanco, damos siguiente, dejamos los valores por defecto y click en finalizar para que se cree el proyecto.

![androidstudio-addanactivitytomobile](https://user-images.githubusercontent.com/31372472/44685993-7393cf00-aa12-11e8-9238-844947bf655b.png)

![androidstudio-createanewemptyactivity](https://user-images.githubusercontent.com/31372472/44686017-84dcdb80-aa12-11e8-9998-0491aea5b324.png)

- 5) Luego de que el proyecto es creado ingresamos a "File --> New  --> Import Module", en este punto vamos a importar los módulos del "OpenCV" para java.

![androidstudio-file-new-importmodule](https://user-images.githubusercontent.com/31372472/44686966-7fcd5b80-aa15-11e8-8603-de91283a861e.png)

- 6) A continuación nos mostrará la pantalla en donde debemos colocar la ruta de los modulos del OpenCV, en mi caso la ruta es la siguiente: "C:\OpenCV-android-sdk\opencv-342-android-sdk\sdk\java"; luego de indicar la ruta, el sistema automaticamente colocará el módulo con la versión de OpenCV que descargaste inicialmente y luego le damos siguiente.

![androidstudio-file-new-importmodule 1](https://user-images.githubusercontent.com/31372472/44686986-8d82e100-aa15-11e8-8107-4b3cbcc51ca1.png)

![androidstudio-file-new-importmodule 2](https://user-images.githubusercontent.com/31372472/44686999-95db1c00-aa15-11e8-9067-51e37bfd48cc.png)

![androidstudio-file-new-importmodule 3](https://user-images.githubusercontent.com/31372472/44687000-95db1c00-aa15-11e8-90d9-60cef5378e55.png)

Aquí quitamos todos los check de reemplazo de jars y damos finalizar.

![androidstudio-file-new-importmodule 4](https://user-images.githubusercontent.com/31372472/44687001-95db1c00-aa15-11e8-9de1-7f08462af57c.png)

Como resultado el sistema te mostrara un resumen de los importado.

![androidstudio-file-new-importmodule 5](https://user-images.githubusercontent.com/31372472/44687002-9673b280-aa15-11e8-9389-f9fae27076af.png)

- 7) Después de importar los módulos vamos a configurar los "build.gradle" del "App" y del "OpenCV", primero colocamos la vista en formato "Android", desplegamos "Gradle Scripts" y allí encontraremos los dos archivos que vamos a modificar.

![androidstudio-vistasobuildgradle](https://user-images.githubusercontent.com/31372472/44688651-89a58d80-aa1a-11e8-89ba-8b558bb62ef4.png)

Lo que vamos hacer es copiar los valores que se encuentra en el "build.gradle (Module App)" en el "build.gradle (Module OpenCV)"

![androidstudio-vistasobuildgradle 1](https://user-images.githubusercontent.com/31372472/44688668-90cc9b80-aa1a-11e8-8a5d-490d4e4f616b.png)

Y al final debe de quedar de la siguiente manera:

![androidstudio-vistasobuildgradle 2](https://user-images.githubusercontent.com/31372472/44688669-90cc9b80-aa1a-11e8-8c86-b2242fb7fef2.png)

