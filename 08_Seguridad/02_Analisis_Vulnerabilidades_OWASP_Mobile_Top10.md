# ANÁLISIS DE VULNERABILIDADES OWASP MOBILE TOP 10 (2024)
**Proyecto:** Mask AI  
**Auditor:** Andrey Sneider Rodríguez Cantor (Especialista en QA y Seguridad)  

---

| Categoría OWASP Mobile | Nivel de Riesgo Inicial | Mecanismo de Remediación e Implementación Técnica en Mask AI | Estado Final |
| :--- | :---: | :--- | :---: |
| **M1: Improper Credential Usage** | Alto | Las API keys se almacenan cifradas en Android Keystore con protección biométrica opcional; nunca se embeben en código fuente. | **MITIGADO** |
| **M2: Inadequate Supply Chain Security** | Medio | Verificación estricta de dependencias con Gradle Dependency Verification y bloqueo de hashes SHA-256 de librerías. | **MITIGADO** |
| **M3: Insecure Authentication/Authorization** | Medio | Uso de contraseña maestra con derivación PBKDF2 (65.536 rondas) para desbloqueo de respaldos locales. | **MITIGADO** |
| **M4: Insufficient Input/Output Validation** | Alto | Sanitización de inputs de usuario para prevenir Prompt Injections y validación tipada con Room para evitar SQL Injections. | **MITIGADO** |
| **M5: Insecure Communication** | Alto | Implementación obligatoria de TLS 1.3 con Network Security Config que prohíbe conexiones HTTP en texto claro. | **MITIGADO** |
| **M6: Inadequate Privacy Controls** | Crítico | Motor de inferencia local 100% offline para datos sensibles; ningún log enviado a servidores externos. | **MITIGADO** |
| **M7: Insufficient Binary Protections** | Medio | Ofuscación de clases y nombres de variables mediante ProGuard/R8 y stripping de símbolos de depuración en C++/NDK. | **MITIGADO** |
| **M8: Security Misconfiguration** | Medio | Atributos `android:allowBackup="false"` y `android:usesCleartextTraffic="false"` fijados estrictamente en el Manifiesto. | **MITIGADO** |
| **M9: Insecure Data Storage** | Crítico | Cifrado transparente de base de datos Room mediante SQLCipher con algoritmo AES-256 en modo CBC. | **MITIGADO** |
| **M10: Insufficient Cryptography** | Alto | Uso exclusivo de algoritmos criptográficos robustos estándar (AES-256-GCM, HMAC-SHA256, PBKDF2); descarte de MD5/DES. | **MITIGADO** |
