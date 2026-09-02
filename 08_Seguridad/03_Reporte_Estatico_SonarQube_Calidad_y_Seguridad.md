# REPORTE ESTÁTICO DE CALIDAD DE CÓDIGO Y SEGURIDAD - SONARQUBE
**Proyecto:** Mask AI  
**Herramienta:** SonarQube Community Edition v10.4  
**Fecha de Análisis:** 10 de Octubre de 2026 | **Quality Gate:** **PASSED (APROBADO)**  

---

## 1. Métricas Consolidadas del Calidad de Código
- **Bugs (Defectos de Código):** **0** (Rating A)
- **Vulnerabilities (Vulnerabilidades de Seguridad):** **0** (Rating A)
- **Security Hotspots (Puntos Críticos de Seguridad):** **0 Abiertos** (100% de Puntos Críticos Auditados y Remediados)
- **Code Smells (Deuda Técnica):** **6 menores** (Deuda técnica total: 42 minutos / Rating A)
- **Coverage (Cobertura de Pruebas Unitarias):** **82.4%** (Superando el umbral institucional del 80%)
- **Duplicated Lines (Duplicación de Código):** **1.2%** (Sobre 8.420 líneas de código en Kotlin y C++)

---

## 2. Remediación de Security Hotspots
1. *Hotspot 1 (Criptografía):* Generador de números aleatorios en `CryptoEngine`.  
   *Acción:* Se reemplazó `java.util.Random` por `java.security.SecureRandom` criptográficamente seguro.
2. *Hotspot 2 (Redes):* Permiso de tráfico en claro.  
   *Acción:* Se forzó `cleartextTrafficPermitted=false` en `network_security_config.xml`.
