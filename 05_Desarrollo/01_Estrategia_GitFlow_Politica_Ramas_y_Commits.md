# ESTRATEGIA DE CONTROL DE VERSIONES: GITFLOW Y CONVENCIONES DE COMMITS
**Proyecto:** Mask AI  
**Repositorio:** `https://github.com/nueva-america-projects/mask-ai-android`  

---

## 1. Estructura de Ramas Oficial
- **`main`:** Rama de producción. Solo código 100% probado, auditado y correspondiente a releases oficiales taggeados (ej. `v1.0.0`).
- **`develop`:** Rama troncal de integración diaria. Contiene el último avance estable de las funcionalidades del sprint.
- **`feature/*`:** Ramas para nuevas funcionalidades (ej. `feature/local-inference-engine`, `feature/markdown-syntax-highlighter`).
- **`bugfix/*`:** Ramas para solución de defectos encontrados en QA (ej. `bugfix/memory-leak-compose-lazycolumn`).
- **`release/*`:** Ramas de estabilización para corte y preparación de entregables (ej. `release/v0.8.0-corte2`).

---

## 2. Convenciones de Commits (Conventional Commits 1.0)
Formato obligatorio: `<tipo>(<alcance>): <descripción concisa en presente>`

### Tipos Permitidos:
- **`feat`:** Nueva funcionalidad para el usuario.
- **`fix`:** Corrección de un bug o defecto.
- **`docs`:** Cambios o adición de documentación en código o markdown.
- **`refactor`:** Refactorización de código sin cambio de comportamiento.
- **`test`:** Adición o corrección de pruebas unitarias o de integración.
- **`security`:** Parches o mejoras específicas de seguridad o criptografía.

### Ejemplos Reales del Proyecto:
- `feat(inference): integrate MediaPipe LLM on-device inference runner`
- `feat(security): implement SQLCipher AES-256 database encryption helper`
- `fix(chat): resolve out-of-memory exception when parsing large python files`
- `test(backup): add unit tests for AES-256-GCM backup encryption and restore`
