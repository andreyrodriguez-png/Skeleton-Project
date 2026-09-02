# CATÁLOGO DE HISTORIAS DE USUARIO CON CRITERIOS GHERKIN
**Proyecto:** Mask AI  
**Metodología:** Marco Ágil Scrum / Sintaxis BDD (Behavior-Driven Development)  

---

## HU-01: Selección Dinámica del Motor de Inferencia
- **ID:** HU-01 | **Épica:** Motor Híbrido de IA | **Prioridad:** Alta (Must) | **Story Points:** 5
- **Enunciado:** *Como* usuario desarrollador, *quiero* alternar entre el motor de IA local y los servicios en la nube (OpenAI, Claude, Gemini, Ollama) desde el encabezado del chat, *para* decidir si priorizo la total privacidad offline o una mayor potencia de cómputo en la nube.
- **Criterios de Aceptación (Gherkin):**
  - **Escenario 1: Conmutación a Motor Local**
    - *Dado* que el usuario está en la pantalla de chat con conexión a Internet desactivada,
    - *Cuando* selecciona la opción "Motor Local (GGUF on-device)",
    - *Entonces* el sistema inicializa el runtime local y permite enviar mensajes sin requerir red.
  - **Escenario 2: Conmutación a API Cloud con validación de API Key**
    - *Dado* que el usuario selecciona "OpenAI GPT-4o",
    - *Cuando* no ha configurado su API Key previamente,
    - *Entonces* el sistema muestra un modal solicitando el ingreso de la clave y redirige a la pantalla de configuración segura.

---

## HU-02: Creación y Parametrización de Máscaras (Perfiles de Expertos)
- **ID:** HU-02 | **Épica:** Perfiles y Memoria | **Prioridad:** Alta (Must) | **Story Points:** 5
- **Enunciado:** *Como* estudiante de ingeniería, *quiero* crear un nuevo perfil de experto definiendo su nombre, avatar, System Prompt y temperatura, *para* recibir respuestas altamente especializadas en tareas de programación o matemáticas.
- **Criterios de Aceptación (Gherkin):**
  - **Escenario 1: Creación exitosa de perfil experto**
    - *Dado* que el usuario completa el formulario con Nombre="Experto Kotlin", SystemPrompt="Eres un arquitecto senior de Android...",
    - *Cuando* pulsa el botón "Guardar Máscara",
    - *Entonces* el nuevo perfil se almacena en la base de datos Room y aparece disponible en el menú selector de expertos.

---

## HU-03: Aislamiento Estricto de la Memoria Contextual
- **ID:** HU-03 | **Épica:** Perfiles y Memoria | **Prioridad:** Alta (Must) | **Story Points:** 8
- **Enunciado:** *Como* usuario profesional, *quiero* que las conversaciones mantenidas con un experto no interfieran ni se mezclen con el contexto de otro experto, *para* evitar respuestas confusas o contaminadas.
- **Criterios de Aceptación (Gherkin):**
  - **Escenario 1: Verificación de memoria aislada al alternar perfiles**
    - *Dado* que el usuario conversó sobre un proyecto en Python con el perfil "Python Dev",
    - *Cuando* cambia al perfil "Redactor Académico" y consulta "¿Qué proyecto estamos haciendo?",
    - *Entonces* el modelo responde que no posee contexto previo sobre dicho proyecto técnico y atiende según su propio rol.

---

## HU-04: Renderizado de Bloques de Código con Resaltado y Copiado
- **ID:** HU-04 | **Épica:** Visor de Código y UI | **Prioridad:** Alta (Must) | **Story Points:** 3
- **Enunciado:** *Como* programador, *quiero* ver el código generado con colores de sintaxis legibles y un botón de copiado de un solo toque, *para* transferir fragmentos de código rápidamente a mi entorno de desarrollo.
- **Criterios de Aceptación (Gherkin):**
  - **Escenario 1: Copiado rápido de bloque de código**
    - *Dado* que el asistente genera un bloque de código en lenguaje Kotlin,
    - *Cuando* el usuario presiona el botón "Copiar Código" ubicado en la esquina superior derecha del bloque,
    - *Entonces* el código se copia al portapapeles del sistema y se muestra un mensaje Toast "Código copiado".

---

## HU-05: Ingesta y Análisis de Archivos de Código
- **ID:** HU-05 | **Épica:** Gestión de Archivos | **Prioridad:** Alta (Must) | **Story Points:** 5
- **Enunciado:** *Como* desarrollador de software, *quiero* adjuntar archivos de código (.kt, .py, .js) a mi mensaje, *para* solicitar refactorizaciones, depuración de errores o explicaciones técnicas al asistente.
- **Criterios de Aceptación (Gherkin):**
  - **Escenario 1: Adjuntar archivo soportado**
    - *Dado* que el usuario pulsa el ícono de clip y selecciona un archivo `MainActivity.kt` de 45 KB,
    - *Cuando* envía la consulta "¿Cómo puedo optimizar este código?",
    - *Entonces* el contenido del archivo se procesa, se incluye en el payload de la consulta y el modelo responde analizando dicho código.

---

## HU-06: Exportación de Respaldo Cifrado con AES-256
- **ID:** HU-06 | **Épica:** Seguridad y Respaldos | **Prioridad:** Alta (Must) | **Story Points:** 8
- **Enunciado:** *Como* usuario preocupado por la seguridad, *quiero* generar un archivo de copia de seguridad protegido por contraseña maestra, *para* guardar mis conversaciones de forma segura o migrarlas a otro dispositivo.
- **Criterios de Aceptación (Gherkin):**
  - **Escenario 1: Exportación exitosa con contraseña fuerte**
    - *Dado* que el usuario ingresa una contraseña de 8 o más caracteres en el módulo de respaldos,
    - *Cuando* pulsa "Generar Copia de Seguridad",
    - *Entonces* el sistema genera un archivo binario `.maskbackup` cifrado con AES-256-GCM y permite compartirlo mediante el selector nativo de Android.
