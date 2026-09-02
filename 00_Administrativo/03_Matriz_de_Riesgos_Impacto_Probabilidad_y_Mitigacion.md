# MATRIZ DE GESTIÓN Y MITIGACIÓN DE RIESGOS
**Proyecto:** Mask AI  
**Metodología:** Análisis Cualitativo y Cuantitativo de Riesgos (PMBOK 7ma Edición)  
**Última Actualización:** 20 de Agosto de 2026  

---

## 1. Escala de Calificación de Riesgos
- **Probabilidad (P):** 1 (Muy Baja), 2 (Baja), 3 (Media), 4 (Alta), 5 (Muy Alta)
- **Impacto (I):** 1 (Insignificante), 2 (Menor), 3 (Moderado), 4 (Mayor), 5 (Catastrófico)
- **Nivel de Severidad (PxI):**
  - **1 a 5:** Riesgo Bajo (Verde)
  - **6 a 12:** Riesgo Medio (Amarillo)
  - **15 a 25:** Riesgo Crítico / Alto (Rojo)

---

## 2. Matriz Consolidada de Riesgos

| ID | Categoría | Descripción del Riesgo | P | I | PxI | Nivel | Estrategia | Plan de Mitigación | Responsable |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :--- | :--- |
| **RSK-01** | Técnico | Consumo excesivo de memoria RAM durante la inferencia local que cause cierre inesperado (*Out-of-Memory* crash) en dispositivos de gama media. | 4 | 4 | **16** | **Crítico** | Mitigar | Implementar cuantización extrema de modelos a 4 bits (GGUF Q4_K_M / INT4) y descarga de capas a memoria virtual dinámica. | Miguel Reyes |
| **RSK-02** | Técnico | Latencia elevada o caída en los servicios de APIs de IA en la nube (OpenAI / Gemini / Anthropic). | 3 | 3 | **9** | **Medio** | Mitigar | Implementar mecanismo de fallback automático al motor local y gestión de timeouts con reintentos exponenciales. | Brayan Vanegas |
| **RSK-03** | Ciberseguridad | Fuga de claves de API (*API Keys*) almacenadas en el cliente por ingeniería inversa del APK. | 3 | 5 | **15** | **Crítico** | Evitar | Utilizar Android Keystore con firma biométrica y ofuscación de código con ProGuard/R8 para variables de compilación. | Andrey Rodríguez |
| **RSK-04** | Datos | Corrupción de la base de datos local SQLite/Room durante el proceso de exportación o importación de respaldos. | 2 | 4 | **8** | **Medio** | Mitigar | Implementar transacciones atómicas Room con validación de checksum SHA-256 antes de restaurar cualquier base de datos cifrada. | Angie Mahecha |
| **RSK-05** | Gestión | Retraso en el cumplimiento de los hitos del cronograma por sobrecarga académica del equipo. | 3 | 4 | **12** | **Medio** | Mitigar | Sesiones diarias tipo Daily Scrum de 15 minutos en ClickUp, priorización MoSCoW estricta del Backlog y congelamiento de alcance. | Nicolás Bolívar |
| **RSK-06** | Calidad / QA | Fragmentación de versiones de Android (bugs de renderizado Compose en versiones 10 y 11 vs 14). | 3 | 3 | **9** | **Medio** | Mitigar | Batería de pruebas en emuladores y dispositivos físicos con matriz de compatibilidad desde API 29 hasta API 34. | Andrey Rodríguez |
| **RSK-07** | Arquitectura | Contaminación cruzada de memorias conversacionales entre diferentes perfiles de expertos. | 2 | 4 | **8** | **Medio** | Evitar | Diseño relacional con claves foráneas compuestas y consultas Room parametrizadas rígidamente por `expert_id`. | Miguel Reyes |
| **RSK-08** | Financiero | Agotamiento prematuro de créditos de API Cloud durante las sesiones de pruebas masivas de integración. | 2 | 3 | **6** | **Medio** | Mitigar | Utilización prioritaria del servidor local Ollama para pruebas internas de desarrollo y mockups en pruebas unitarias. | Nicolás Bolívar |
| **RSK-09** | Usabilidad | Experiencia de usuario deficiente por lentitud en el renderizado de bloques extensos de código con Markdown. | 3 | 2 | **6** | **Medio** | Mitigar | Uso de librerías nativas de parsing asíncrono y renderizado perezoso (*LazyColumn*) en Jetpack Compose. | Brayan Vanegas |
| **RSK-10** | Ciberseguridad | Inyección de prompts maliciosos (*Prompt Injection*) que comprometan el comportamiento del experto. | 3 | 3 | **9** | **Medio** | Mitigar | Sanitización previa de inputs de usuario, delimitación estricta de contexto y refuerzo de directivas en el System Prompt. | Andrey Rodríguez |

---

## 3. Protocolo de Monitoreo y Contingencia
- Revisión semanal obligatoria de la matriz en cada reunión de los martes.
- Umbral de activación de contingencia: Cualquier riesgo que supere severidad 12 requiere reunión extraordinaria de comité y reporte inmediato al docente.
