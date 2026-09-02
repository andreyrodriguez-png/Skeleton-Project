# OBJETIVOS DEL PROYECTO Y MATRIZ DE ALINEACIÓN METODOLÓGICA
**Proyecto:** Mask AI  

---

## 1. Objetivo General
Desarrollar durante el periodo académico 2026-2 la aplicación móvil **Mask AI** para dispositivos Android utilizando Kotlin y arquitectura limpia (MVVM), integrando servicios de inteligencia artificial locales configurables y modelos en la nube mediante APIs parametrizables, junto con perfiles de expertos con memoria contextual independiente, procesamiento seguro de archivos de código y mecanismos de respaldo encriptado, con el propósito de proporcionar a estudiantes, investigadores y desarrolladores una plataforma conversacional híbrida, privada, flexible y orientada a la soberanía de datos.

---

## 2. Objetivos Específicos y Metas Medibles

| ID | Objetivo Específico | Indicador de Logro | Meta Cuantificable | Entregable Asociado |
| :---: | :--- | :--- | :---: | :--- |
| **OE1** | Investigar el estado del arte de SLMs móviles y caracterizar requerimientos mediante encuestas estadísticas. | Porcentaje de respuestas analizadas y requisitos validados. | $N=120$ encuestas analizadas; SRS IEEE 830 aprobado al 100%. | Informe de Investigación y SRS v1.0 |
| **OE2** | Diseñar la arquitectura desacoplada MVVM/C4 y el modelo de datos relacional con cifrado SQLCipher. | Diagramas completados y validados en Draw.io. | 100% de diagramas C4, DER y flujos aprobados. | Documento SAD y Modelo DER |
| **OE3** | Construir la aplicación móvil nativa en Kotlin con Jetpack Compose e integrar motores locales y APIs Cloud. | Funcionalidades implementadas vs planificadas en Backlog. | 15 Historias de Usuario completadas; Build APK release v1.0.0. | Código fuente GitHub y APK funcional |
| **OE4** | Asegurar la calidad del software y la seguridad del sistema mediante pruebas unitarias, UAT y OWASP ZAP. | Cobertura de pruebas y vulnerabilidades críticas detectadas. | Cobertura $\ge 80\%$; 0 vulnerabilidades críticas OWASP. | Reporte QA, SonarQube y Actas UAT |

---

## 3. Matriz de Alineación (Problema - Objetivo - Entregable - Módulo)

```
[PROBLEMA IDENTIFICADO]           [OBJETIVO ESPECÍFICO]           [MÓDULO / ENTREGABLE]
Falta de privacidad y       --->  OE1 & OE3: Inferencia local  ---> Módulo Local GGUF On-Device
dependencia de la nube.           cuantizada sin Internet.        (Offline AI Engine).

Pérdida de contexto e       --->  OE2 & OE3: Perfiles expertos ---> Módulo de Máscaras y Memoria
historiales desorganizados.       con memoria aislada.            Aislada en Room/SQLCipher.

Dificultad para manejar     --->  OE3: Visor de código y       ---> Módulo de Procesamiento de Código
código fuente y archivos.         resaltado de sintaxis.          y Markdown Renderer.

Riesgo de pérdida de datos  --->  OE2 & OE4: Criptografía y    ---> Módulo de Seguridad, Cifrado
y falta de portabilidad.          respaldo seguro AES-256.        y Backup Engine.
```
