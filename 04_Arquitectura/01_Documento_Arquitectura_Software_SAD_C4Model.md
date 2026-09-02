# DOCUMENTO DE ARQUITECTURA DE SOFTWARE (SAD) - MODELO C4
**Proyecto:** Mask AI  
**Estilo Arquitectural:** Clean Architecture + MVVM + Micro-Motores Desacoplados  
**Plataforma Objetivo:** Android 10+ (Kotlin Nativo)  

---

## 1. Nivel 1: Diagrama de Contexto del Sistema

```
                                  +-----------------------+
                                  |    USUARIO FINAL      |
                                  | (Estudiante / Dev)    |
                                  +-----------------------+
                                              |
                                              | 1. Interactúa, envía prompts,
                                              |    archivos y gestiona máscaras
                                              v
                              +-------------------------------+
                              |       SISTEMA MASK AI         |
                              |  (Aplicación Móvil Android)   |
                              +-------------------------------+
                                  |                       |
            2a. Inferencia Cloud  |                       | 2b. Inferencia Local
            (HTTPS / TLS 1.3)     |                       | (Memoria compartida / NDK)
                                  v                       v
               +----------------------+       +-----------------------+
               |  PROVEEDORES CLOUD   |       |   MOTOR LOCAL ON-DEV  |
               | - OpenAI / Gemini    |       | - GGUF INT4 Runtime   |
               | - Claude / Ollama    |       | - MediaPipe LLM       |
               +----------------------+       +-----------------------+
```

---

## 2. Nivel 2: Diagrama de Contenedores

```
+-----------------------------------------------------------------------------------------+
| SISTEMA MASK AI (DISPOSITIVO MÓVIL ANDROID)                                             |
|                                                                                         |
|  +-----------------------------------------------------------------------------------+  |
|  | CAPA DE PRESENTACIÓN (Jetpack Compose UI)                                         |  |
|  | - ChatScreen (Stream de mensajes, visor de código Markdown, selector de máscaras)  |  |
|  | - ExpertManagementScreen (CRUD de máscaras, ajuste de temperatura y System Prompts)|  |
|  | - SettingsScreen (Gestión de API Keys, selección de modelos y respaldos)          |  |
|  +-----------------------------------------------------------------------------------+  |
|                                            | (StateFlow / Eventos)                       |
|                                            v                                             |
|  +-----------------------------------------------------------------------------------+  |
|  | CAPA DE DOMINIO (Clean Architecture Use Cases)                                    |  |
|  | - SendMessageUseCase, StreamInferenceUseCase, ManageExpertsUseCase               |  |
|  | - ProcessFileUseCase, ExportEncryptedBackupUseCase, ImportBackupUseCase          |  |
|  +-----------------------------------------------------------------------------------+  |
|                                            |                                             |
|                    +-----------------------+-----------------------+                     |
|                    |                                               |                     |
|                    v                                               v                     |
|  +-----------------------------------+           +-----------------------------------+  |
|  | CAPA DE DATOS (Room + SQLCipher)  |           | CAPA DE INFERENCIA HÍBRIDA (IA)   |  |
|  | - ExpertDao, MessageDao, ChatDao  |           | - LocalInferenceEngine (C++/NDK)  |  |
|  | - EncryptedSharedPreferences      |           | - CloudInferenceAdapter (Retrofit)|  |
|  | - Cifrado AES-256 en reposo       |           | - PromptOrchestrator & Tokenizer  |  |
|  +-----------------------------------+           +-----------------------------------+  |
+-----------------------------------------------------------------------------------------+
```
