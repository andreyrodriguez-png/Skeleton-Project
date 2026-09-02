# GUIÓN Y ESTRUCTURA DE LA SUSTENTACIÓN FINAL ANTE EL COMITÉ DE GRADO
**Proyecto:** Mask AI: Asistente Conversacional Móvil con IA Híbrida, Privada y Personalizable  
**Institución:** Fundación Universitaria Nueva América  
**Tiempo Total de Sustentación:** 20 Minutos de Exposición + 10 Minutos de Preguntas del Jurado  

---

## 1. Guión y Distribución de Roles en la Sustentación

### Minuto 00:00 - 03:00 | Apertura y Planteamiento del Problema
- **Expositor:** Nicolás Felipe Bolívar Supelano (Líder / PMO)
- **Mensaje Clave:** "Los asistentes de IA actuales son cajas negras centralizadas que exigen entregar datos confidenciales y dependen 100% de la nube. Mask AI resuelve este dilema con un enfoque híbrido on-device y soberanía de datos".
- **Datos Estadísticos:** Presentación de la encuesta ($N=120$ donde el 88.3% exige privacidad estricta).

### Minuto 03:00 - 06:00 | Arquitectura de Software e Ingeniería
- **Expositor:** Miguel Ángel Reyes Novoa Rojas (Arquitecto de Software / Backend)
- **Mensaje Clave:** "Diseñamos una arquitectura limpia MVVM con Clean Architecture y micro-motores desacoplados. El motor local ejecuta modelos cuantizados GGUF INT4 con aceleración ARM NEON, mientras que la base de datos Room está blindada con SQLCipher AES-256".

### Minuto 06:00 - 10:00 | Demostración en Vivo (Live Demo)
- **Expositor:** Brayan Yesid Vanegas Orduz (Frontend Lead)
- **Pasos Demostrables en Vivo:**
  1. Activar Modo Avión en el teléfono Android.
  2. Enviar prompt técnico con código Python al perfil local: Demostración de generación offline y visor de sintaxis con copiado.
  3. Desactivar Modo Avión, conmutar a GPT-4o y mostrar streaming de tokens con Server-Sent Events.
  4. Demostrar el aislamiento estricto de contexto al cambiar entre máscaras de expertos.
  5. Exportar un archivo de respaldo `.maskbackup` protegido con contraseña maestra.

### Minuto 10:00 - 13:00 | Calidad, Ciberseguridad y DEV/UAT
- **Expositor:** Andrey Sneider Rodríguez Cantor (QA & Cybersecurity)
- **Mensaje Clave:** "Ejecutamos 20 casos de prueba funcionales con 100% de éxito, cerramos 10 de 10 bugs en el Defect Tracker, alcanzamos 82.4% de cobertura en SonarQube con Quality Gate APROBADO y mitigamos los 10 riesgos del OWASP Mobile Top 10".

### Minuto 13:00 - 16:00 | Gestión de Datos, Normas APA y Viabilidad Financiera
- **Expositor:** Angie Natali Mahecha Rojas (DBA / Documentación)
- **Mensaje Clave:** "El modelo de datos garantiza integridad referencial con eliminación en cascada. El estudio de pérdidas y ganancias (PyG) demuestra un punto de equilibrio con solo 167 usuarios Pro y un ROI del 2.101% en el primer año".

### Minuto 16:00 - 20:00 | Conclusiones, Lecciones Aprendidas y Cierre
- **Expositor:** Nicolás Bolívar y Equipo Completo
- **Agradecimientos y disponibilidad inmediata para la sesión de preguntas técnicas y gerenciales del comité.**
