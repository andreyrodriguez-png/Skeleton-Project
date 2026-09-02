# REPORTE DINÁMICO DE SEGURIDAD DAST - OWASP ZAP
**Proyecto:** Mask AI  
**Herramienta:** OWASP Zed Attack Proxy (ZAP) v2.14.0  
**Alcance:** Adaptadores de Comunicación REST / gRPC y Endpoints de Streaming  

---

## 1. Resumen Ejecutivo del Escaneo
- **Alertas de Nivel Alto (High Risk):** **0**
- **Alertas de Nivel Medio (Medium Risk):** **0**
- **Alertas de Nivel Bajo (Low Risk):** **1** (Cabecera de caché en endpoints de streaming - Justificada por diseño de stream en tiempo real)
- **Alertas Informativas:** **3** (Uso de TLS 1.3 verificado, cabeceras CORS de proveedores validadas)

---

## 2. Verificación de Seguridad en Conectores Cloud
- **Prueba de Inyección de Cabeceras:** Inmune (Uso de librerías tipadas OkHttp 4.12).
- **Prueba de Escuchas MitM:** Inmune (Certificados SSL válidos con verificación estricta de cadenas de confianza).
- **Prueba de Exposición de Credenciales en URL:** Inmune (Todas las API Keys viajan exclusivamente en la cabecera HTTP `Authorization: Bearer <token>`).
