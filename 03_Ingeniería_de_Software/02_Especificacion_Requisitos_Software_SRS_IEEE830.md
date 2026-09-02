# ESPECIFICACIÓN DE REQUISITOS DE SOFTWARE (SRS) - ESTÁNDAR IEEE 830
**Proyecto:** Mask AI: Asistente Conversacional Móvil con IA Híbrida  
**Versión:** 1.0 Oficial  
**Fecha:** 26 de Agosto de 2026  

---

## 1. Requisitos Funcionales (RF)

| ID | Nombre del Requisito | Descripción Detallada | Prioridad |
| :---: | :--- | :--- | :---: |
| **RF-01** | Selección de Motor de IA | El sistema debe permitir al usuario alternar en cualquier momento entre el motor local on-device y proveedores cloud (OpenAI, Claude, Gemini, Ollama). | **Alta (Must)** |
| **RF-02** | Gestión de Perfiles de Expertos | El sistema debe permitir crear, editar, duplicar y eliminar perfiles de expertos ("Máscaras"), definiendo nombre, rol, avatar, system prompt y temperatura. | **Alta (Must)** |
| **RF-03** | Aislamiento de Memoria Contextual | Cada perfil de experto debe almacenar y mantener su propio historial conversacional de forma estrictamente independiente y aislada. | **Alta (Must)** |
| **RF-04** | Interfaz de Chat con Streaming | La interfaz debe desplegar la respuesta del modelo palabra por palabra en tiempo real (*Server-Sent Events* o token stream). | **Alta (Must)** |
| **RF-05** | Renderizado de Markdown y Código | El sistema debe parsear y colorear bloques de código con resaltado de sintaxis para lenguajes populares (Kotlin, Python, Java, JS, JSON, C++). | **Alta (Must)** |
| **RF-06** | Botón de Copiado Rápido de Código | Cada bloque de código renderizado debe incluir un botón de acción rápida para copiar el contenido íntegro al portapapeles. | **Media (Should)** |
| **RF-07** | Ingesta de Archivos de Texto y Código| El usuario debe poder adjuntar archivos (.txt, .py, .kt, .json, .md) para ser leídos e incorporados al prompt como contexto de análisis. | **Alta (Must)** |
| **RF-08** | Inferencia Local Offline | El sistema debe ser capaz de procesar prompts y generar respuestas mediante un modelo SLM local sin requerir conexión a datos o Wi-Fi. | **Alta (Must)** |
| **RF-09** | Parametrización de Claves de API | La aplicación debe proveer una pantalla de configuración para ingresar, validar y almacenar de forma segura las API keys del usuario. | **Alta (Must)** |
| **RF-10** | Configuración de Servidor Ollama | El sistema debe permitir configurar la URL base y el nombre de modelo de una instancia personalizada de Ollama en red local o pública. | **Media (Should)** |
| **RF-11** | Búsqueda en Historial de Chats | El sistema debe incluir un buscador por texto para filtrar conversaciones pasadas por palabras clave o fechas. | **Media (Should)** |
| **RF-12** | Exportación de Respaldo Cifrado | El sistema debe permitir exportar todas las conversaciones, perfiles y configuraciones en un archivo comprimido cifrado con AES-256-GCM. | **Alta (Must)** |
| **RF-13** | Importación y Restauración de Respaldo| El usuario debe poder restaurar su información a partir de un archivo de respaldo ingresando la contraseña maestra de descifrado. | **Alta (Must)** |
| **RF-14** | Vaciado y Borrado Seguro | El usuario debe poder eliminar permanentemente una conversación o la totalidad de los datos locales mediante sobrescritura segura. | **Media (Should)** |
| **RF-15** | Control de Temperatura y Top-P | Cada experto debe permitir calibrar los hiperparámetros de muestreo (Temperatura de 0.0 a 1.0 y Top-P) para regular creatividad. | **Baja (Could)** |
| **RF-16** | Modo Oscuro / Claro Automático | La interfaz debe adaptarse dinámicamente al tema del sistema operativo Android y ofrecer alternancia manual. | **Media (Should)** |
| **RF-17** | Monitoreo de Recursos en Tiempo Real | Durante inferencia local, el sistema debe mostrar opcionalmente la tasa de tokens por segundo y memoria RAM utilizada. | **Baja (Could)** |
| **RF-18** | Manejo de Timeouts y Fallback | Si una API cloud no responde tras 15 segundos, el sistema debe sugerir reintentar o conmutar al motor local de respaldo. | **Alta (Must)** |

---

## 2. Requisitos No Funcionales (RNF)

| ID | Categoría | Criterio Específico | Métrica de Aceptación |
| :---: | :--- | :--- | :--- |
| **RNF-01** | **Rendimiento** | Tiempo de primera respuesta (*Time-to-First-Token*) en inferencia local. | $\le 1.8$ segundos en dispositivos con Snapdragon 7/8 series. |
| **RNF-02** | **Rendimiento** | Tasa sostenida de generación de tokens en modelo cuantizado INT4. | $\ge 6.0$ tokens por segundo en hardware ARM64. |
| **RNF-03** | **Seguridad** | Cifrado en reposo de la base de datos de la aplicación. | Cifrado AES-256 mediante SQLCipher sobre SQLite/Room. |
| **RNF-04** | **Seguridad** | Almacenamiento seguro de secretos y API keys. | Uso exclusivo de Android Keystore / EncryptedSharedPreferences. |
| **RNF-05** | **Compatibilidad** | Versiones del sistema operativo móvil soportadas. | Android 10 (API 29) hasta Android 14+ (API 34). |
| **RNF-06** | **Disponibilidad** | Capacidad operativa del motor local sin conexión. | 100% disponible sin conectividad de red activa. |
| **RNF-07** | **Usabilidad** | Diseño de interfaz de usuario intuitivo y accesible. | Adherencia estricta a directrices de Material Design 3 de Google. |
| **RNF-08** | **Mantenibilidad**| Cobertura de pruebas y arquitectura desacoplada. | Cobertura de código en pruebas unitarias $\ge 80\%$ en SonarQube. |
| **RNF-09** | **Integridad** | Consistencia de datos en operaciones de respaldo. | Validación obligatoria de integridad mediante hash SHA-256. |
| **RNF-10** | **Portabilidad** | Formato universal de exportación de datos. | Estructura JSON estándar estandarizada e interoperable. |
| **RNF-11** | **Eficiencia** | Consumo de memoria RAM en reposo (*idle state*). | $\le 85$ MB de memoria RAM cuando no hay inferencia activa. |
| **RNF-12** | **Robustez** | Tolerancia a fallos por desconexión en streaming. | Reanudación o cierre controlado sin caída forzada (*crash 0%*). |
