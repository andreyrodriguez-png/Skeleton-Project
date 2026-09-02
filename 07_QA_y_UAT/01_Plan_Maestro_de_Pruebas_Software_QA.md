# PLAN MAESTRO DE PRUEBAS DE SOFTWARE (QA MASTER TEST PLAN)
**Proyecto:** Mask AI  
**Estándar:** IEEE 829 (Software Test Documentation)  
**Líder de QA:** Andrey Sneider Rodríguez Cantor  

---

## 1. Alcance de las Pruebas
El aseguramiento de calidad de Mask AI abarca:
1. **Pruebas Unitarias (Unit Testing):** Lógica de negocio, serialización JSON, derivación de claves criptográficas y cálculo de ventanas de contexto en Kotlin con JUnit 5 y MockK.
2. **Pruebas de Integración:** Verificación de consultas Room sobre base de datos encriptada SQLCipher y adaptadores HTTP con MockWebServer.
3. **Pruebas de Interfaz de Usuario (UI Testing):** Interacción fluida de componentes Jetpack Compose mediante Compose UI Test Framework.
4. **Pruebas de Rendimiento y Estrés:** Medición de latencia de inferencia, consumo de memoria RAM y temperatura del hardware móvil con Android Profiler.
5. **Pruebas de Aceptación de Usuario (UAT):** Validación funcional con 15 evaluadores externos según casos de uso reales.
