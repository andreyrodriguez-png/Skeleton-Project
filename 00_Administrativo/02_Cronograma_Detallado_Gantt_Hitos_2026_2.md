# CRONOGRAMA DETALLADO DEL PROYECTO (WBS / EDT Y GANTT)
**Proyecto:** Mask AI  
**Periodo Académico:** 2026-2 (16 Semanas)  
**Herramienta de Control:** ClickUp & GitHub Projects  

---

## 1. Estructura de Desglose del Trabajo (EDT / WBS)

```
1. PROYECTO MASK AI
├── 1.1 Fase de Iniciación e Investigación (Semanas 1 - 4)
│   ├── 1.1.1 Elaboración y aprobación del Project Charter
│   ├── 1.1.2 Diseño de instrumento de encuesta y muestreo (N=120)
│   ├── 1.1.3 Tabulación estadística, gráficas y análisis de requerimientos
│   ├── 1.1.4 Construcción del marco teórico y estado del arte de IA local/nube
│   └── 1.1.5 Elaboración del presupuesto preliminar y análisis PyG
├── 1.2 Fase de Ingeniería y Diseño de Arquitectura (Semanas 3 - 6)
│   ├── 1.2.1 Especificación de Requisitos de Software (SRS IEEE 830)
│   ├── 1.2.2 Redacción de Historias de Usuario con sintaxis Gherkin (HU-01 a HU-15)
│   ├── 1.2.3 Modelado de Casos de Uso y diagramas de interacción UML
│   ├── 1.2.4 Diseño de Arquitectura C4 (Contexto, Contenedores, Componentes)
│   └── 1.2.5 Modelado de Base de Datos MER y diseño relacional Room/SQLCipher
├── 1.3 Fase de Desarrollo DEV y Core Engine (Semanas 5 - 10)
│   ├── 1.3.1 Configuración de repositorio GitHub, GitFlow y CI/CD Pipelines
│   ├── 1.3.2 Implementación de Capa de Datos (Room, SQLCipher, SharedPreferences)
│   ├── 1.3.3 Implementación de Motor Local de IA (MediaPipe / GGUF on-device)
│   ├── 1.3.4 Implementación de Conectores Cloud (OpenAI, Gemini, Claude, Ollama)
│   ├── 1.3.5 Módulo de Perfiles de Expertos y Gestión de Memorias Aisladas
│   ├── 1.3.6 Interfaz gráfica Jetpack Compose, Markdown renderer y Syntax Highlighter
│   └── 1.3.7 Sistema de Exportación/Importación de Respaldos cifrados AES-256
├── 1.4 Fase de QA, UAT y Ciberseguridad (Semanas 9 - 13)
│   ├── 1.4.1 Ejecución de pruebas unitarias con JUnit y MockK (82%+ cobertura)
│   ├── 1.4.2 Despliegue de ambiente UAT y distribución de APK de validación
│   ├── 1.4.3 Ejecución de 20 casos de prueba funcionales y pruebas de estrés
│   ├── 1.4.4 Auditoría de Ciberseguridad OWASP Mobile Top 10 y escaneo OWASP ZAP
│   ├── 1.4.5 Análisis estático de código en SonarQube y cierre de Security Hotspots
│   └── 1.4.6 Ciclo de gestión, corrección y re-test de Bugs (BUG-01 a BUG-10)
└── 1.5 Fase de Cierre, Documentación y Sustentación (Semanas 14 - 16)
    ├── 1.5.1 Consolidación del Documento Final de Grado bajo Normas APA 7ma ed.
    ├── 1.5.2 Elaboración del Manual de Usuario Final y Manual Técnico
    ├── 1.5.3 Pruebas de aceptación de usuario UAT con actas firmadas
    ├── 1.5.4 Preparación del material audiovisual y guion de sustentación
    └── 1.5.5 Sustentación pública ante el Comité de Grado y entrega de release final
```

---

## 2. Cronograma de Actividades por Semana (Gantt Tabular)

| Sem. | Fechas | Corte | Actividad Principal | Responsable | Entregable Clave | % Avance Plan |
| :---: | :---: | :---: | :--- | :--- | :--- | :---: |
| **S01** | 05-09 Ago | C1 | Kick-off, asignación de roles, Project Charter y creación de Drive/ClickUp | Bolívar / Todos | Charter y Acta 01 | 6% |
| **S02** | 12-16 Ago | C1 | Aplicación de encuestas de mercado y estudio de privacidad en IA | Mahecha / Rodríguez | Base de 120 respuestas | 12% |
| **S03** | 19-23 Ago | C1 | Tabulación estadística, estado del arte de SLMs móviles y costeo PyG | Vanegas / Reyes | Gráficas e informe estadístico | 18% |
| **S04** | 26-30 Ago | C1 | Especificación de Requisitos IEEE 830 y catálogo de Historias de Usuario | Vanegas / Bolívar | SRS v1.0 y 15 Historias | 25% |
| **S05** | 02-06 Sep | C1 | Diagramas UML, arquitectura MVVM/C4 y MER de base de datos | Reyes / Mahecha | Modelos Draw.io y MER | 30% |
| **S06** | 09-13 Sep | **C1** | **Cierre Primer Corte:** Sustentación de Ingeniería, entrega documental Drive | **Equipo Completo** | **Entrega 1er Corte (30%)** | **35%** |
| **S07** | 16-20 Sep | C2 | Setup de proyecto Kotlin, GitFlow, GitHub Actions y estructura Room | Vanegas / Reyes | Repositorio activo y base local | 42% |
| **S08** | 23-27 Sep | C2 | Integración del motor de inferencia local y adaptadores de API cloud | Reyes / Vanegas | Inferencia local funcional | 50% |
| **S09** | 30 Sep-04 Oct | C2 | Construcción de UI Compose: chat, selector de máscaras y visor de código | Vanegas / Mahecha | UI interactiva completa | 60% |
| **S10** | 07-11 Oct | C2 | Despliegue en ambiente UAT, inicio de plan de pruebas QA y escaneo SonarQube | Rodríguez / Bolívar | Build APK UAT v0.8.0 | 70% |
| **S11** | 14-18 Oct | **C2** | **Cierre Segundo Corte:** Evidencias DEV/UAT, auditoría OWASP ZAP y bugs | **Equipo Completo** | **Entrega 2do Corte (30%)** | **75%** |
| **S12** | 21-25 Oct | C3 | Remediación de bugs identificados, optimización de memoria RAM y latencia | Reyes / Vanegas | Corrección BUG-01 a BUG-10 | 82% |
| **S13** | 28 Oct-01 Nov | C3 | Pruebas de aceptación UAT con usuarios externos y recolección de actas | Rodríguez / Bolívar | Actas UAT firmadas | 88% |
| **S14** | 04-08 Nov | C3 | Consolidación del Documento Final APA 7 (92+ págs) y manuales operativos | Mahecha / Todos | Borrador Documento Final | 94% |
| **S15** | 11-15 Nov | C3 | Ensayo general de sustentación, revisión de rúbrica y verificación de Drive | Bolívar / Todos | Diapositivas y demo lista | 98% |
| **S16** | 18-20 Nov | **C3** | **Cierre Tercer Corte:** Sustentación formal ante jurados y release v1.0.0 | **Equipo Completo** | **Entrega Final (40%)** | **100%** |
