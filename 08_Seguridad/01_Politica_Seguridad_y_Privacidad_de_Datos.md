# POLÍTICA DE SEGURIDAD Y PRIVACIDAD DE DATOS (PRIVACY BY DESIGN)
**Proyecto:** Mask AI  
**Marco Legal:** Ley 1581 de 2012 (Colombia) / Principios RGPD (UE)  

---

## 1. Principios Rectores
1. **Privacidad por Defecto y por Diseño (*Privacy by Design*):** Toda la información conversacional, configuraciones y perfiles residen de forma predeterminada en el almacenamiento local del dispositivo del usuario.
2. **Telemetría Cero:** La aplicación Mask AI no recopila, rastrea ni transmite telemetría, estadísticas de uso, registros de actividad ni identificadores de hardware a servidores centrales.
3. **Cero Retención en Tránsito:** Las consultas enviadas a proveedores cloud utilizan conexiones HTTPS directas desde el cliente móvil hacia los endpoints de los proveedores sin servidores intermediarios propietarios.
4. **Cifrado de Extremo a Extremo en Reposo:** La base de datos SQLite se protege mediante claves criptográficas de 256 bits generadas en el hardware seguro del terminal.
