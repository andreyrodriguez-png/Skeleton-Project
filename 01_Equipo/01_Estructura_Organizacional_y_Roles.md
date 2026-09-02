# ESTRUCTURA ORGANIZACIONAL Y DEFINICIÓN DE ROLES DEL EQUIPO
**Proyecto:** Mask AI  
**Institución:** Fundación Universitaria Nueva América  
**Programa:** Ingeniería de Sistemas  

---

## 1. Organigrama Funcional del Proyecto

```
                    +------------------------------------------+
                    |        DIRECTOR DE PROYECTO / PMO        |
                    |     Nicolás Felipe Bolívar Supelano      |
                    +------------------------------------------+
                                         |
         +-------------------------------+-------------------------------+
         |                               |                               |
+-------------------+           +-------------------+           +-------------------+
|  FRONTEND LEAD    |           |  ARQUITECTURA &   |           |  QA & SEGURIDAD   |
|   & UI DESIGN     |           |   BACKEND LEAD    |           |     ENGINEER      |
| Brayan Y. Vanegas |           |  Miguel A. Reyes  |           | Andrey Rodríguez  |
+-------------------+           +-------------------+           +-------------------+
                                         |
                                +-------------------+
                                |    DBA & LEAD     |
                                |   DOCUMENTATION   |
                                |  Angie N. Mahecha |
                                +-------------------+
```

---

## 2. Perfiles Profesionales y Responsabilidades Formales

### 2.1 Nicolás Felipe Bolívar Supelano
- **Rol Principal:** Director del Proyecto / Líder PMO & Scrum Master.
- **Responsabilidades:**
  - Planificación general del proyecto, control del cronograma y gestión del alcance.
  - Administración del workspace de ClickUp (gestión de sprints, backlog, asignación de tareas).
  - Liderazgo de las presentaciones gerenciales de los martes ante el comité docente.
  - Gestión de riesgos, bloqueos y control de cambios en la arquitectura o presupuesto.
  - Consolidación del cumplimiento de los hitos evaluativos en los tres cortes académicos.

### 2.2 Brayan Yesid Vanegas Orduz
- **Rol Principal:** Desarrollador Principal Frontend Android (Kotlin).
- **Responsabilidades:**
  - Diseño e implementación de la interfaz gráfica de usuario con Jetpack Compose y Material 3.
  - Implementación del componente de chat fluido con soporte de streaming de texto (*SSE*).
  - Desarrollo del visor interactivo de código con resaltado de sintaxis multilenguaje y Markdown.
  - Construcción del selector de máscaras y pantalla de administración de perfiles expertos.
  - Integración de animaciones, accesibilidad y experiencia de usuario (UI/UX).

### 2.3 Miguel Ángel Reyes Novoa Rojas
- **Rol Principal:** Arquitecto de Software & Desarrollador Backend / Core AI Engine.
- **Responsabilidades:**
  - Diseño formal de la arquitectura de software (Clean Architecture + MVVM + C4 Model).
  - Integración técnica del motor de inferencia local (*MediaPipe LLM / llama.cpp / ONNX*).
  - Desarrollo de los adaptadores de API Cloud (OpenAI REST, Anthropic Claude, Gemini, Ollama).
  - Implementación del orquestador de prompts y balanceador dinámico de inferencias.
  - Configuración del pipeline de integración continua CI/CD en GitHub Actions.

### 2.4 Andrey Sneider Rodríguez Cantor
- **Rol Principal:** Ingeniero de Aseguramiento de Calidad (QA) y Ciberseguridad.
- **Responsabilidades:**
  - Elaboración y ejecución del Plan Maestro de Pruebas (unitarias, integración, rendimiento y UAT).
  - Gestión del libro de registro y ciclo de vida de defectos (*Defect / Bug Tracker*).
  - Auditoría de ciberseguridad sobre el aplicativo bajo el estándar OWASP Mobile Top 10.
  - Ejecución de escaneos estáticos en SonarQube y escaneos dinámicos con OWASP ZAP.
  - Conducción de las sesiones de validación y actas de aceptación de usuario UAT.

### 2.5 Angie Natali Mahecha Rojas
- **Rol Principal:** Administradora de Base de Datos (DBA) & Especialista en Documentación y Normas APA.
- **Responsabilidades:**
  - Modelado conceptual, lógico y físico de la base de datos (MER y entidades Room).
  - Implementación de la capa de persistencia cifrada con SQLCipher (AES-256).
  - Diseño e implementación del algoritmo de aislamiento estricto de memorias contextuales.
  - Consolidación y estricta aplicación de las Normas APA Séptima Edición en el documento maestro.
  - Levantamiento de actas de reunión semanales y control de versiones documentales en Drive.
