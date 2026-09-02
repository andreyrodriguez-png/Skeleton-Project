# MANUAL TÉCNICO DE INSTALACIÓN, COMPILACIÓN Y CONFIGURACIÓN
**Proyecto:** Mask AI  
**Destinatarios:** Ingenieros de Sistemas, Desarrolladores de Software y Evaluadores Técnicos  

---

## 1. Clonación del Repositorio y Configuración Inicial
1. Clonar el repositorio desde GitHub:
   ```bash
   git clone https://github.com/nueva-america-projects/mask-ai-android.git
   cd mask-ai-android
   ```
2. Crear el archivo `local.properties` en la raíz del proyecto para definir la ruta del Android SDK:
   ```properties
   sdk.dir=C:\Users\Usuario\AppData\Local\Android\Sdk
   ```

---

## 2. Configuración de Modelos Locales GGUF
Para habilitar la inferencia local sin conexión:
1. Descargar el modelo cuantizado `phi-3-mini-4k-instruct.Q4_K_M.gguf` (~1.9 GB).
2. Conectar el dispositivo móvil Android mediante depuración USB (*ADB*).
3. Transferir el binario del modelo a la memoria interna privada de la aplicación:
   ```bash
   adb push phi-3-mini-4k-instruct.Q4_K_M.gguf /sdcard/Android/data/com.nuevaamerica.maskai/files/models/
   ```

---

## 3. Compilación y Generación del Paquete APK
- **Compilar APK de Desarrollo (DEV):**
  ```bash
  ./gradlew assembleDebug
  ```
  *Ubicación de salida:* `app/build/outputs/apk/debug/app-debug.apk`

- **Compilar APK Firmado para Pruebas de Usuario (UAT / Release):**
  ```bash
  ./gradlew assembleRelease
  ```
  *Ubicación de salida:* `app/build/outputs/apk/release/mask-ai-v1.0.0-release.apk`
