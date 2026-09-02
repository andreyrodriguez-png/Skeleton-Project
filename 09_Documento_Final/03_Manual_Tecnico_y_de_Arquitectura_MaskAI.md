# MANUAL TÉCNICO Y DE ARQUITECTURA DEL SISTEMA - MASK AI
**Versión del Documento:** 1.0  
**Proyecto:** Mask AI  
**Audiencia:** Desarrolladores, Arquitectos de Software, Auditores Técnicos  

---

## 1. Arquitectura de Módulos y Dependencias
El proyecto está estructurado como una aplicación Android multi-módulo desacoplada:

```
                       +-------------------------+
                       |        :app             |
                       +-------------------------+
                        /     |            |    \
                       v      v            v     v
        +---------------+ +-----------+ +------------+ +-------------+
        | :feature-chat | | :feature- | | :feature-  | | :feature-   |
        |               | |  experts  | |  aiengine  | |  backup     |
        +---------------+ +-----------+ +------------+ +-------------+
               \              |            |              /
                v             v            v             v
        +------------------------------------------------------------+
        |                        :core-domain                        |
        |       (Use Cases, Domain Models, Repository Contracts)     |
        +------------------------------------------------------------+
                                      |
                                      v
        +------------------------------------------------------------+
        |                         :core-data                         |
        |   (Room Entities, DAOs, SQLCipher Helper, Retrofit APIs)   |
        +------------------------------------------------------------+
                                      |
                                      v
        +------------------------------------------------------------+
        |                       :core-security                       |
        |      (Android Keystore, AES-GCM Engine, PBKDF2 Derivation) |
        +------------------------------------------------------------+
```

---

## 2. Tecnologías y Librerías Principales
- **Lenguaje:** Kotlin 2.0.0 con soporte de Coroutines y Flow.
- **UI Framework:** Jetpack Compose con Material Design 3.
- **Inyección de Dependencias:** Dagger Hilt 2.51.
- **Persistencia Local:** Room Database 2.6.1 + SQLCipher 4.5.4 para cifrado AES-256 en reposo.
- **Motor Local de IA:** MediaPipe LLM Inference SDK (Google) / C++ NDK bindings para modelos GGUF.
- **Networking:** Retrofit 2.11 + OkHttp 4.12 con soporte de Server-Sent Events (SSE).
- **Criptografía:** Java Cryptography Extension (JCE) + Android KeyStore System (AES-256-GCM / PBKDF2WithHmacSHA256).
- **Testing:** JUnit 5, MockK, Robolectric, Compose Testing Tool.
- **Calidad y Seguridad:** SonarQube Scanner Gradle Plugin, OWASP ZAP DAST Runner.
