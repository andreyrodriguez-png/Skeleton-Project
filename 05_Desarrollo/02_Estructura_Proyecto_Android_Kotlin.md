# ESTRUCTURA TÉCNICA DEL PROYECTO ANDROID (MODULAR KOTLIN)
**Proyecto:** Mask AI  

---

## Árbol de Directorios del Código Fuente

```
app/
├── src/
│   ├── main/
│   │   ├── java/com/nuevaamerica/maskai/
│   │   │   ├── core/
│   │   │   │   ├── common/             # Extensiones, utilitarios y constantes globales
│   │   │   │   ├── data/               # Entidades Room, DAOs, SQLiteCipher OpenHelper
│   │   │   │   ├── di/                 # Módulos de inyección Dagger Hilt
│   │   │   │   ├── domain/             # Modelos de dominio e interfaces de repositorios
│   │   │   │   └── security/           # KeystoreHelper, AESCryptoEngine, Sanitizer
│   │   │   ├── feature/
│   │   │   │   ├── chat/               # ChatScreen, ChatViewModel, MarkdownParser
│   │   │   │   ├── experts/            # ExpertScreen, ExpertViewModel, ExpertAdapter
│   │   │   │   ├── aiengine/           # LocalInferenceEngine, CloudApiAdapters
│   │   │   │   ├── backup/             # BackupScreen, BackupRestoreEngine
│   │   │   │   └── settings/           # ApiKeyConfigScreen, SettingsViewModel
│   │   │   ├── ui/
│   │   │   │   ├── components/         # Botones personalizados, SyntaxBlock, Dialogs
│   │   │   │   └── theme/              # Color, Type, Theme Material 3
│   │   │   └── MainActivity.kt         # Punto de entrada y NavHost Compose
│   │   ├── res/                        # Drawables, strings, mipmap, xml config
│   │   └── AndroidManifest.xml         # Permisos y configuración de aplicación
│   └── test/                           # Pruebas Unitarias JUnit 5 y MockK
│   └── androidTest/                    # Pruebas de Integración y UI Compose
├── build.gradle.kts                    # Configuración de dependencias a nivel de módulo
└── proguard-rules.pro                  # Reglas de ofuscación R8/ProGuard
```
