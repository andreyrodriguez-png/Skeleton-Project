# MATRIZ RACI DE ASIGNACIÓN DE RESPONSABILIDADES
**Proyecto:** Mask AI  
**Definición de Roles:**  
- **R (Responsible):** Quien realiza la actividad.  
- **A (Accountable):** Quien aprueba y rinde cuentas finales por el entregable.  
- **C (Consulted):** Quien aporta información clave o asesoría técnica.  
- **I (Informed):** Quien debe ser notificado del avance o resultado.  

---

## 1. Integrantes y Nomenclatura
- **NB:** Nicolás Felipe Bolívar Supelano (Líder / Gerente de Proyecto)
- **BV:** Brayan Yesid Vanegas Orduz (Desarrollador Frontend Kotlin / UI)
- **MR:** Miguel Ángel Reyes Novoa Rojas (Arquitecto de Software / Backend Dev)
- **AR:** Andrey Sneider Rodríguez Cantor (QA Lead / Especialista en Ciberseguridad)
- **AM:** Angie Natali Mahecha Rojas (DBA / Documentación y Calidad APA)

---

## 2. Matriz de Asignación por Entregable y Fase

| Fase / Entregable Principal | NB (PMO) | BV (Front) | MR (Back) | AR (QA/Sec) | AM (DB/Doc) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **1. INICIACIÓN Y GESTIÓN** | | | | | |
| Project Charter y Plan de Proyecto | **A / R** | C | C | C | C |
| Cronograma WBS y Seguimiento ClickUp | **A / R** | I | I | I | I |
| Presupuesto Detallado y Análisis PyG | **A / R** | C | C | C | C |
| Actas Semanales de Comité | **A** | I | I | I | **R** |
| **2. INVESTIGACIÓN Y REQUISITOS** | | | | | |
| Formulación del Problema y Justificación | **A** | C | C | C | **R** |
| Diseño y Aplicación de Encuestas (N=120) | C | **R** | C | C | **A / R** |
| Tabulación Estadística y Gráficas | I | C | C | C | **A / R** |
| Marco Teórico y Estado del Arte de SLMs | C | C | **A / R** | C | C |
| Especificación de Requisitos IEEE 830 | **A** | **R** | **R** | C | C |
| Historias de Usuario con Criterios Gherkin | **A** | **R** | **R** | C | C |
| Casos de Uso y Diagramas UML | C | **R** | **A / R** | C | C |
| **3. ARQUITECTURA Y DISEÑO TÉCNICO** | | | | | |
| Documento de Arquitectura de Software C4 | C | C | **A / R** | C | I |
| Diagramas Draw.io (Flujos y Secuencia) | I | C | **A / R** | I | I |
| Modelo Entidad-Relación y Esquema Room | I | C | C | C | **A / R** |
| Diseño de Motor Híbrido (Local / Cloud) | C | C | **A / R** | C | I |
| **4. DESARROLLO E IMPLEMENTACIÓN** | | | | | |
| Repositorio GitHub, GitFlow y CI/CD | C | C | **A / R** | C | I |
| Capa UI Jetpack Compose y Markdown Parser | I | **A / R** | C | I | I |
| Integración de Motor Local On-Device | I | C | **A / R** | C | I |
| Conectores API Cloud (OpenAI, Gemini, etc.) | I | C | **A / R** | C | I |
| Módulo de Perfiles y Memorias Independientes | I | **R** | **A / R** | I | C |
| Cifrado AES-256 y Exportación de Respaldos | C | I | **R** | **A / R** | C |
| **5. QA, UAT Y CIBERSEGURIDAD** | | | | | |
| Plan Maestro de Pruebas y Matriz de Casos | I | C | C | **A / R** | I |
| Pruebas Unitarias e Integración (82%+ Cobertura)| I | **R** | **R** | **A / R** | I |
| Auditoría OWASP Mobile y Escaneo ZAP | I | C | C | **A / R** | I |
| Análisis Estático SonarQube | I | C | C | **A / R** | I |
| Gestión y Verificación de Bugs (Bugs 01-10) | C | **R** | **R** | **A / R** | I |
| Despliegue de Ambiente UAT y Validación Usuario| **A** | C | C | **R** | C |
| **6. CIERRE Y DOCUMENTACIÓN FINAL** | | | | | |
| Consolidación Documento APA 7 (92+ págs) | **A** | C | C | C | **R** |
| Manual de Usuario Final | I | **A / R** | I | C | C |
| Manual Técnico y de Instalación | I | I | **A / R** | C | C |
| Presentaciones Semanales de los Martes | **A / R** | C | C | C | C |
| Sustentación Final ante Jurados | **A / R** | **R** | **R** | **R** | **R** |
