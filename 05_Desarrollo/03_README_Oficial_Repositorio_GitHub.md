# Mask AI - Asistente Conversacional Móvil con IA Híbrida

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Kotlin](https://img.shields.io/badge/Kotlin-2.0.0-blue)
![Android SDK](https://img.shields.io/badge/SDK-29%20to%2034-orange)
![Security](https://img.shields.io/badge/OWASP-Passed-green)
![License](https://img.shields.io/badge/License-MIT-blue)

**Mask AI** es una aplicación móvil nativa para Android desarrollada en **Kotlin** y **Jetpack Compose** que revoluciona la interacción con Inteligencia Artificial, proporcionando una arquitectura híbrida que combina modelos locales on-device (100% privados y desconectados) con APIs en la nube de alta potencia (OpenAI, Anthropic Claude, Google Gemini y servidores Ollama autoalojados).

---

## Características Principales
- 🔒 **Inferencia Local On-Device:** Ejecución de SLMs cuantizados (GGUF INT4 / MediaPipe) directamente en el hardware del teléfono, sin consumir datos ni enviar información al exterior.
- 🎭 **Perfiles de Expertos ("Máscaras"):** Configuración de múltiples asistentes especializados con prompts de sistema y memorias contextuales estrictamente aisladas.
- 💻 **Visor de Código con Resaltado Sintáctico:** Renderizado impecable de fragmentos de código (.kt, .py, .js, .json) con copiado rápido al portapapeles.
- 📂 **Ingesta de Archivos de Desarrollo:** Carga directa de scripts y documentos para análisis contextual por parte de la IA.
- 🛡️ **Seguridad Grado Militar:** Base de datos en reposo cifrada con **SQLCipher (AES-256)** y sistema de exportación/importación de respaldos protegidos con contraseña mediante **AES-256-GCM**.

---

## Requisitos de Entorno para Compilación
- **Android Studio:** Hedgehog | 2023.1.1 o superior (Recomendado Ladybug 2024.2+).
- **JDK:** Java Development Kit 17 (LTS).
- **Android SDK:** API Mínima 29 (Android 10.0), API Target 34 (Android 14.0).
- **Gradle:** 8.4+.

---

## Autores y Créditos Académicos
Proyecto de Grado desarrollado para la **Fundación Universitaria Nueva América** (Bogotá D.C., 2026):
- Nicolás Felipe Bolívar Supelano (*Líder de Proyecto / PMO*)
- Brayan Yesid Vanegas Orduz (*Frontend Developer*)
- Miguel Ángel Reyes Novoa Rojas (*Software Architect / Backend*)
- Andrey Sneider Rodríguez Cantor (*QA & Cybersecurity Lead*)
- Angie Natali Mahecha Rojas (*DBA & Documentation Lead*)
