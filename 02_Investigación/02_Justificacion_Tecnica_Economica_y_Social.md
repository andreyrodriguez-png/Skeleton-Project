# JUSTIFICACIÓN TÉCNICA, ECONÓMICA, SOCIAL Y ACADÉMICA
**Proyecto:** Mask AI  

---

## 1. Justificación Técnica
Desde la perspectiva de la ingeniería de software y la computación móvil, **Mask AI** aborda la evolución hacia el cómputo en el borde (*Edge Computing / Edge AI*). Los avances recientes en técnicas de cuantización de pesos neuronales (AWQ, GPTQ y cuantización por bloques en formato GGUF a 4 y 8 bits) permiten que modelos con parámetros de 1B a 3.8B (como Phi-3 Mini, Gemma 2B, Llama 3.2 1B/3B) ejecuten inferencias con alta fidelidad sintáctica directamente sobre chipsets móviles ARM64 (mediante CPU NEON y aceleración por GPU/NPU OpenCL/Vulkan). 

La integración de una arquitectura híbrida desacoplada permite que el dispositivo opere de forma autónoma cuando no hay conectividad o cuando se procesa información confidencial, transfiriendo tareas de alta complejidad analítica a APIs en la nube mediante un orquestador transparente. El uso de **Kotlin**, **Jetpack Compose**, **Clean Architecture** y la librería criptográfica **SQLCipher** garantiza un producto de alto rendimiento, modular y con los más altos estándares de la industria móvil.

---

## 2. Justificación Económica
El acceso a servicios comerciales de IA en la nube bajo esquemas de suscripción individual suele oscilar entre $20 USD y $30 USD mensuales por plataforma ($80.000 a $120.000 COP/mes). Para una institución educativa, empresa o estudiante, pagar múltiples suscripciones resulta inviable. 

**Mask AI** optimiza dramáticamente estos costos al:
- Permitir el uso ilimitado de modelos locales sin costo por token o consumo de datos móviles.
- Permitir la configuración de API keys bajo esquema *Pay-As-You-Go* (donde 1.000 tokens de entrada cuestan fracciones de centavo de dólar).
- Reducir el consumo de ancho de banda móvil hasta en un 65% para tareas rutinarias de asistencia.

---

## 3. Justificación Social y Ética
En el contexto colombiano, el derecho fundamental al *Habeas Data* y la protección de datos personales consagrados en la **Ley 1581 de 2012** exigen que los ciudadanos mantengan el control sobre el destino de su información. Mask AI democratiza el acceso a la inteligencia artificial garantizando que comunidades académicas, profesionales del derecho, ingenieros y usuarios comunes puedan utilizar herramientas de última generación sin entregar sus secretos industriales, proyectos de grado o datos personales a servidores extranjeros.

---

## 4. Justificación Académica
Para el programa de Ingeniería de Sistemas de la Fundación Universitaria Nueva América, este proyecto evidencia la articulación de múltiples áreas de conocimiento del núcleo profesional:
- **Ingeniería de Software:** Levantamiento de requisitos bajo estándar IEEE 830, modelado UML, C4 Model y metodologías ágiles Scrum.
- **Inteligencia Artificial:** Inferencia local, cuantización, embeddings y orquestación de prompts.
- **Bases de Datos:** Diseño relacional, normalización, optimización de queries y seguridad en reposo con SQLCipher.
- **Ciberseguridad:** Auditoría bajo OWASP Mobile Top 10, análisis estático de código y criptografía simétrica AES-256.
