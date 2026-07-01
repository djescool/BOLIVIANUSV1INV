# FINTECH - Android Web App

Esta es la versión nativa de la aplicación FINTECH para Android, basada en el diseño de pantallas web existente.
La aplicación está configurada para cargar de forma nativa los archivos HTML y sentirse como una app real.

## Características:
- **Pantalla completa (AMOLED Black):** Adaptada para aprovechar pantallas de móviles como POCO X8 PRO MAX sin mostrar barras de direcciones. Aprovecha colores `#000000` para ahorrar batería.
- **Sin conexión externa:** Todas las vistas cargan de los `assets` nativos, no requiere acceso a internet a dominios externos para evitar vulnerabilidades de inyección y ahorrar datos.
- **Fluidez y aceleración:** Aceleración por GPU activada, y control de zoom / bounce effects (overscroll) desactivado.
- **Haptics:** Sutil vibración al presionar botones (usando interfaces nativas).

## Instrucciones para Modificar y Compilar

1. **Requisitos:**
   - Android Studio (versión reciente que soporte Gradle 8+).
   - JDK 17 o superior.

2. **Modificar las Vistas:**
   - Los archivos de diseño HTML/CSS/JS se encuentran en: `app/src/main/assets/www/`.
   - Puedes editar cualquiera de estos archivos; la app los actualizará de forma instantánea al compilar.
   - El punto de entrada es `index.html`.

3. **Recompilar el APK (Terminal):**
   - Asegúrate de estar en el directorio raíz del proyecto.
   - Ejecuta:
     ```bash
     ./gradlew assembleDebug
     ```
   - El APK generado lo encontrarás en `app/build/outputs/apk/debug/app-debug.apk`.
   - Puedes copiarlo directamente usando: `cp app/build/outputs/apk/debug/app-debug.apk FINTECH.apk`

4. **Recompilar con Android Studio:**
   - Abre el directorio raíz del proyecto en Android Studio.
   - Modifica el código HTML en la carpeta assets.
   - Presiona `Build > Build Bundle(s) / APK(s) > Build APK(s)`.
   - O simplemente presiona "Run" (▶) para instalar la app directo en tu teléfono conectado.

## Encontrar el APK listo
Un APK listo para instalar está directamente en la raíz de este repositorio, llamado `FINTECH.apk`.
Descárgalo, envíalo a tu dispositivo móvil e instálalo (asegúrate de permitir orígenes desconocidos).
