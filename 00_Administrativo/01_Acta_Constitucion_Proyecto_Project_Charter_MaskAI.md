# ACTA DE CONSTITUCIÓN DEL PROYECTO (PROJECT CHARTER)
**Proyecto:** Mask AI - Asistente Conversacional Móvil con Inteligencia Artificial Híbrida, Privada y Personalizable  
**Institución:** Fundación Universitaria Nueva América  
**Programa Académico:** Ingeniería de Sistemas  
**Asignatura:** Proyecto de Grado / Gerencia en Proyectos de TI  
**Docente Director:** Ing. Mario Alberto Orozco Paloma / Nelson Martínez Gonzáles  
**Fecha:** 19 de Agosto de 2026 | Versión: 1.0  

---

## 1. Información General del Proyecto
| Campo | Detalle |
| :--- | :--- |
| **Nombre del Proyecto** | Mask AI: Asistente Conversacional Móvil con Inteligencia Artificial Híbrida, Privada y Personalizable |
| **Código del Proyecto** | PGA-2026-MASKAI-01 |
| **Gerente de Proyecto** | Nicolás Felipe Bolívar Supelano |
| **Patrocinadores / Autores** | Nicolás Felipe Bolívar Supelano, Brayan Yesid Vanegas Orduz, Miguel Ángel Reyes Novoa Rojas, Andrey Sneider Rodríguez Cantor, Angie Natali Mahecha Rojas |
| **Fecha de Inicio Oficial** | 05 de Agosto de 2026 |
| **Fecha Estimada de Cierre** | 20 de Noviembre de 2026 |

---

## 2. Propósito y Justificación del Proyecto
El auge acelerado de los Modelos Masivos de Lenguaje (LLMs) ha transformado la interacción con la información digital. Sin embargo, la gran mayoría de soluciones comerciales operan bajo arquitecturas cerradas en la nube, imponiendo riesgos críticos de privacidad, fuga de propiedad intelectual, dependencia de conectividad constante a Internet y costos recurrentes elevados. Al mismo tiempo, los modelos pequeños de lenguaje (SLMs) ejecutables en el borde (*on-device AI*) han alcanzado niveles de madurez computacional que permiten inferencias locales eficientes en hardware móvil.

**Mask AI** nace para cerrar esta brecha mediante una solución móvil híbrida para Android (Kotlin), permitiendo a los usuarios alternar dinámicamente entre motores de inferencia locales (garantizando 100% de privacidad y funcionamiento offline) y APIs de vanguardia en la nube (OpenAI, Anthropic Claude, Google Gemini, Ollama remoto). Además, incorpora un sistema modular de "Máscaras" (Perfiles de Expertos) con memorias conversacionales estrictamente aisladas, procesamiento de archivos de código fuente y respaldos cifrados con AES-256-GCM.

---

## 3. Objetivo General y Objetivos Específicos (SMART)
### 3.1 Objetivo General
Desarrollar durante el periodo académico 2026-2 la aplicación móvil **Mask AI** para dispositivos Android utilizando Kotlin y arquitectura limpia (MVVM), integrando servicios de inteligencia artificial locales configurables y modelos en la nube mediante APIs parametrizables, junto con perfiles de expertos con memoria contextual independiente, procesamiento seguro de archivos de código y mecanismos de respaldo encriptado, con el propósito de proporcionar a estudiantes, investigadores y desarrolladores una plataforma conversacional híbrida, privada, flexible y orientada a la soberanía de datos.

### 3.2 Objetivos Específicos
1. **OE1 (Investigación y Requisitos):** Investigar el estado del arte en inferencia de SLMs móviles y motores on-device (*MediaPipe LLM / llama.cpp / ONNX Runtime*), caracterizando los requerimientos técnicos y funcionales mediante instrumentos estadísticos aplicados a una muestra representativa de desarrolladores y usuarios académicos ($N=120$).
2. **OE2 (Diseño y Arquitectura):** Diseñar una arquitectura de software desacoplada bajo el patrón MVVM y Clean Architecture, integrando un motor orquestador híbrido de IA, un modelo entidad-relación optimizado en Room/SQLite con cifrado SQLCipher y un gestor de contextos de memoria independiente por perfil.
3. **OE3 (Construcción e Implementación):** Implementar la aplicación nativa en Kotlin con Jetpack Compose, integrando conectores REST/gRPC seguros para APIs cloud y el motor de inferencia local en el dispositivo, incorporando visualizadores de sintaxis para código y analizadores de documentos.
4. **OE4 (Aseguramiento de Calidad y Ciberseguridad):** Validar la solución mediante pruebas unitarias, de integración, pruebas de estrés de inferencia y pruebas de aceptación de usuario (UAT), aplicando auditorías de seguridad bajo el estándar OWASP Mobile Top 10 y análisis estático con SonarQube.

---

## 4. Alcance del Proyecto
### 4.1 Lo que Incluye el Proyecto (In-Scope)
- Aplicación móvil nativa para el sistema operativo Android (versiones 10.0 a 14.0+, API 29+).
- Interfaz gráfica moderna construida con Jetpack Compose y Material Design 3.
- Módulo de Inferencia Híbrida:
  - Motor local on-device basado en formatos cuantizados (GGUF / INT4 / INT8).
  - Adaptadores API para proveedores en la nube (OpenAI GPT-4o, Anthropic Claude 3.5 Sonnet, Google Gemini 1.5 Pro, servidor Ollama autoalojado).
- Sistema de Perfiles de Expertos ("Máscaras"):
  - Creación, edición, parametrización de System Prompts y temperatura.
  - Almacenamiento y aislamiento estricto de memorias conversacionales independientes.
- Módulo de Gestión de Código y Archivos:
  - Ingesta de archivos (.txt, .pdf, .py, .kt, .js, .json, .md).
  - Renderizado de Markdown y resaltado de sintaxis multilenguaje con botón de copiado rápido.
- Módulo de Seguridad y Respaldos:
  - Cifrado de base de datos local con SQLCipher (AES-256).
  - Generación, importación y exportación de respaldos cifrados con contraseña maestra.
- Despliegue en ambientes DEV y UAT con trazabilidad continua en GitHub y ClickUp.

### 4.2 Lo que NO Incluye el Proyecto (Out-of-Scope)
- Entrenamiento o ajuste fino (*fine-tuning*) de modelos fundacionales desde cero (se utilizan modelos preentrenados y cuantizados).
- Versión para sistemas operativos iOS o entorno Web (reservadas para roadmap futuro).
- Comercialización o pasarela de pagos integrada en la fase académica.
- Infraestructura de servidores propietarios físicos (se usa cloud serverless y ejecución cliente local).

---

## 5. Cronograma de Hitos Principales
| Hito | Descripción | Fecha Límite | Responsable |
| :--- | :--- | :--- | :--- |
| **M1: Formulación y SRS** | Entrega de charter, encuestas, marco teórico, SRS IEEE 830, arquitectura y presupuesto (Corte 1). | 08/09/2026 | Líder / Todos |
| **M2: Core Engine & DEV** | Repositorio GitHub activo, motor de inferencia local/nube integrado, base de datos Room estructurada. | 29/09/2026 | Devs / DBA |
| **M3: Release UAT & QA** | Despliegue de APK en ambiente UAT, ejecución de 20 casos de prueba, reporte OWASP ZAP y SonarQube (Corte 2). | 13/10/2026 | QA / Seguridad |
| **M4: Optimización y Cierre** | Remediación de bugs, pruebas de usuario final con actas de validación, manuales técnico y de usuario. | 03/11/2026 | Equipo Completo |
| **M5: Entrega Final y Demo** | Documento académico APA 7 consolidado (92-147 págs), APK final release firmada, demo funcional y sustentación ante comité (Corte 3). | 20/11/2026 | Líder / Todos |

---

## 6. Presupuesto Preliminar y Recursos
- **Inversión Total Estimada:** $ 24.850.000 COP (Incluye horas de ingeniería, infraestructura cloud DEV/UAT, licencias de desarrollo, dispositivos de prueba y costos operativos).
- **Financiamiento:** Recursos propios del equipo de desarrollo y créditos cloud académicos.

---

## 7. Supuestos y Restricciones
### 7.1 Supuestos
- Los integrantes del equipo mantendrán una dedicación mínima de 15 horas semanales al proyecto.
- Los dispositivos móviles de prueba cuentan con procesadores ARM64 y mínimo 6 GB de memoria RAM para soportar inferencia local.
- Las APIs en la nube mantendrán compatibilidad y cuotas disponibles para las pruebas de integración.

### 7.2 Restricciones
- Duración fija del semestre académico (16 semanas de trabajo intensivo).
- Prohibición estricta de adquisición de servidores físicos on-premise; uso exclusivo de arquitectura cliente y servicios serverless/APIs.
- Política institucional de no uso de IA para la elaboración intelectual del trabajo académico.

---

## 8. Firmas de Aprobación y Compromiso
| Integrante | Rol en el Proyecto | Firma / Conformidad |
| :--- | :--- | :--- |
| **Nicolás Felipe Bolívar Supelano** | Director del Proyecto / Líder PMO | APROBADO |
| **Brayan Yesid Vanegas Orduz** | Desarrollador Principal Frontend | APROBADO |
| **Miguel Ángel Reyes Novoa Rojas** | Arquitecto de Software / Backend Dev | APROBADO |
| **Andrey Sneider Rodríguez Cantor** | Ingeniero de QA y Ciberseguridad | APROBADO |
| **Angie Natali Mahecha Rojas** | DBA / Especialista en Documentación | APROBADO |
