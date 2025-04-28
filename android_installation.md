# Instalación de Android Studio en Linux Mint

Esta guía detalla los pasos para instalar Android Studio en tu sistema Linux Mint. Android Studio es el entorno de desarrollo integrado (IDE) oficial para el desarrollo de aplicaciones para la plataforma Android.

## Pasos de Instalación

Sigue estos pasos para instalar Android Studio en tu Linux Mint:

### 1. Descargar Android Studio

1.  Abre tu navegador web y ve a la página oficial de descarga de Android Studio: [https://developer.android.com/studio](https://developer.android.com/studio)
2.  Haz clic en el botón "Descargar Android Studio".
3.  Lee y acepta los términos y condiciones.
4.  Descarga el archivo `.tar.gz` de Android Studio para Linux.

### 2. Extraer el Archivo Descargado

1.  Abre tu terminal. Puedes hacerlo presionando `Ctrl + Alt + T`.
2.  Navega hasta el directorio donde se guardó el archivo descargado (generalmente la carpeta `Descargas`).
    ```bash
    cd Descargas
    ```
3.  Extrae el contenido del archivo `.tar.gz`. Reemplaza `android-studio-VERSION-linux.tar.gz` con el nombre exacto del archivo que descargaste.
    ```bash
    tar -xzf android-studio-VERSION-linux.tar.gz
    ```
    Esto creará una nueva carpeta llamada `android-studio` en el directorio actual.

### 3. Ejecutar el Script de Instalación

1.  Navega hasta el directorio `bin` dentro de la carpeta `android-studio` que se acaba de extraer.
    ```bash
    cd android-studio/bin
    ```
2.  Ejecuta el script de instalación `studio.sh`.
    ```bash
    ./studio.sh
    ```
    Esto iniciará el asistente de configuración de Android Studio.

### 4. Completar el Asistente de Configuración

1.  **Importar Configuraciones Previas (Opcional):** Si has instalado Android Studio antes, se te preguntará si deseas importar configuraciones previas. Elige la opción adecuada o selecciona "No importar configuraciones" si es una instalación nueva. Haz clic en "OK".
2.  **Enviar Estadísticas de Uso:** Se te preguntará si deseas compartir datos de uso con Google para ayudar a mejorar Android Studio. Elige la opción que prefieras y haz clic en "Siguiente".
3.  **Tipo de Instalación:** Elige el tipo de instalación. "Estándar" es recomendado para la mayoría de los usuarios. Haz clic en "Siguiente".
4.  **Tema de la Interfaz de Usuario:** Elige entre los temas "Darcula" (oscuro) o "IntelliJ Light" (claro). Haz clic en "Siguiente".
5.  **Componentes del SDK:** El asistente mostrará los componentes del SDK de Android que se instalarán. Asegúrate de que "Android SDK" esté seleccionado. También puedes optar por instalar el "Android Virtual Device" si planeas usar emuladores. Haz clic en "Siguiente".
6.  **Configuración del Emulador (Si se seleccionó):** Si elegiste instalar el "Android Virtual Device", se te pedirá que configures la memoria asignada. Ajusta según tus recursos y haz clic en "Siguiente".
7.  **Verificar Configuración:** Revisa la configuración de la instalación. Si todo es correcto, haz clic en "Siguiente".
8.  **Descargar y Instalar:** Haz clic en "Finalizar" para comenzar la descarga e instalación de los componentes necesarios. Este proceso puede llevar algún tiempo dependiendo de tu conexión a internet.
9.  **Finalizar:** Una vez que la instalación se complete, haz clic en "Finalizar".

### 5. Iniciar Android Studio

Ahora puedes iniciar Android Studio desde el menú de aplicaciones de Linux Mint. Busca "Android Studio" y haz clic para ejecutarlo.

## Pasos Post-Instalación (Recomendado)

* **Actualizar el SDK de Android:** Una vez que Android Studio esté abierto, ve a "Configure" (en la pantalla de bienvenida o en "File" > "Settings") y selecciona "SDK Manager". Aquí puedes actualizar las plataformas y herramientas del SDK de Android a las últimas versiones disponibles.
* **Crear un Dispositivo Virtual Android (AVD):** Si planeas probar tus aplicaciones en un emulador, ve a "Configure" > "AVD Manager" y crea un nuevo dispositivo virtual con las especificaciones deseadas.
