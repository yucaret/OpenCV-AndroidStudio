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

Y al final debe de quedar de la siguiente manera y luego debes de sincronizar, hasta este momento no debe de existir errores:

![androidstudio-vistasobuildgradle 2](https://user-images.githubusercontent.com/31372472/44688669-90cc9b80-aa1a-11e8-8c86-b2242fb7fef2.png)

- 8) Luego debes de ir a File --> Project Structure, dentro de este vamos a realizar 3 configuraciones.

![androidstudio-file-projectstructure](https://user-images.githubusercontent.com/31372472/44690671-50bce700-aa21-11e8-87f2-cdbb9ebab346.png)

En la Primera vamos a configurar la dirección del NDK, primero nos colocamos en "SDK Location" y vamos a la sección de "Android NDK Location", allí modificamos la ruta a la direccion de NDK que decargamos inicialmente, en mi caso la ruta es "C:\android-ndk-r16b" y le damos "OK".

![androidstudio-file-projectstructure-ndklocation](https://user-images.githubusercontent.com/31372472/44690682-51557d80-aa21-11e8-9937-8ebf662f7b7d.png)

![androidstudio-file-projectstructure-ndklocation 2](https://user-images.githubusercontent.com/31372472/44690681-51557d80-aa21-11e8-9a61-8ed4cc1bbfb7.png)

Para validar esta modificacion abrimos "gradle.properties" y vemos que en el archivo estan las modificaciones.

![androidstudio-file-projectstructure-app-dependencies 5](https://user-images.githubusercontent.com/31372472/44690678-51557d80-aa21-11e8-8efa-42028b70a209.png)

Luego en la Segunda configuración abrimos nuevamente el "Project Structure" y vamos a "Modules" y seleccionamos "App"; dentro de esta vamos a la pestaña de "Properties" y cambiamos el "Compile SDK Version" con la versión de Android que elegimos para nuestro proyecto, en mi caso es el "Andorid 3.0".

![androidstudio-file-projectstructure-app-properties 1](https://user-images.githubusercontent.com/31372472/44690679-51557d80-aa21-11e8-92aa-6c40147aa520.png)

![androidstudio-file-projectstructure-app-properties 2](https://user-images.githubusercontent.com/31372472/44690680-51557d80-aa21-11e8-82e9-1c33ef160729.png)

Finalmente como Tercera configuración vamos a la pestaña de "Dependencies", damos click en el "+" y luego seleccionamos "3 Module Dependency" y elegimos el OpenCV

![androidstudio-file-projectstructure-app-dependencies 1](https://user-images.githubusercontent.com/31372472/44690673-50bce700-aa21-11e8-9649-f745f94d6de8.png)

![androidstudio-file-projectstructure-app-dependencies 2](https://user-images.githubusercontent.com/31372472/44690674-50bce700-aa21-11e8-935a-823f8098c9e8.png)

![androidstudio-file-projectstructure-app-dependencies 3](https://user-images.githubusercontent.com/31372472/44690675-50bce700-aa21-11e8-9ed6-651d51f242d1.png)

![androidstudio-file-projectstructure-app-dependencies 4](https://user-images.githubusercontent.com/31372472/44690676-50bce700-aa21-11e8-8d70-b17ded76a739.png)

A partir de allí saldrán errores que se solucionaran con los siguientes pasos.

- 9) Ahora vamos a crear la nueva carpeta de librerias de OpenCV, para ello seleccionamos la vista de proyectos, luego nos dirigimos a la ruta de archivos "..../app/src/main", luego damos click derecho en "main" y vamos a "New --> Folder --> JNI Folders", alli le damos click al checkbox "Change Folder Location" y luego en "New Folder Location" colocamos lo siguiente "src/main/jniLibs/", es allí donde creamos la nueva carpeta de librerias con nombre "jniLibs" y le damos "Finish".

![androidstudio-new-folder-gnifolder 1](https://user-images.githubusercontent.com/31372472/44692320-fb380880-aa27-11e8-9a49-34f72297b24d.png)

![androidstudio-new-folder-gnifolder 2](https://user-images.githubusercontent.com/31372472/44692207-7220d180-aa27-11e8-8abf-c633a7428c94.png)

![androidstudio-new-folder-gnifolder 3](https://user-images.githubusercontent.com/31372472/44692208-7220d180-aa27-11e8-82a4-f37f26f4f49e.png)

- 10) Ahora copiamos la estructura de archivos del OpenCV en la nueva carpeta "jniLibs", vamos a la ruta donde decargamos el OpenCV inicialmente, en mi caso la ruta es "C:\OpenCV-android-sdk\opencv-342-android-sdk\sdk\native\libs" y allí copiamos todas las carpetas que estan dentro, luego vamos al Android Studio, a la nueva carpeta "jniLibs" y pegamos, nos saldra una pantallita a la que le daremos OK.

![jnilibs 1](https://user-images.githubusercontent.com/31372472/44692969-15bfb100-aa2b-11e8-9816-3e338b7cd9e1.png)

![jnilibs 2](https://user-images.githubusercontent.com/31372472/44692970-16584780-aa2b-11e8-98ce-c39a84b27f27.png)

![jnilibs 3](https://user-images.githubusercontent.com/31372472/44692972-16584780-aa2b-11e8-9f76-aa63ecf7d303.png)
