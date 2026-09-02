# PLANTEAMIENTO DEL PROBLEMA Y ÁRBOL DE PROBLEMAS
**Proyecto:** Mask AI  
**Línea de Investigación:** Inteligencia Artificial Aplicada, Privacidad de Datos y Computación Móvil  

---

## 1. Descripción del Problema
En la actualidad, la adopción masiva de herramientas de Inteligencia Artificial Generativa y Modelos de Lenguaje Masivos (LLMs) ha transformado radicalmente los flujos de trabajo en el ámbito académico, profesional y de desarrollo de software. Sin embargo, este paradigma predominante presenta problemáticas críticas que limitan su uso seguro, eficiente y personalizado:

1. **Centralización Extrema y Riesgos de Privacidad:** Las plataformas comerciales líderes (ej. ChatGPT, Claude, Gemini Web) requieren transmitir la totalidad de los datos, código propietario, consultas sensibles y documentos a servidores centrales de terceros. Esto expone a los usuarios a riesgos de filtración, incumplimiento de leyes de protección de datos (como la Ley 1581 de 2012 en Colombia y el RGPD europeo) y pérdida de control sobre su información.
2. **Dependencia Total de Conectividad a Internet:** La incapacidad de ejecutar tareas básicas de procesamiento conversacional o análisis de texto de manera desconectada (offline) genera una vulnerabilidad operativa ante fallas de red, zonas rurales o políticas corporativas con firewalls restrictivos.
3. **Fragmentación y Falta de Interoperabilidad:** Los usuarios que requieren interactuar con múltiples proveedores de IA se ven forzados a alternar constantemente entre distintas aplicaciones y sitios web, lo que fragmenta el historial de conversaciones, dispersa el conocimiento y encarece la gestión.
4. **Ausencia de Aislamiento Contextual Personalizado:** Las interfaces convencionales manejan historiales monolíticos donde los roles y áreas de conocimiento se mezclan con frecuencia, generando respuestas inconsistentes y pérdida de especificidad técnica.
5. **Dificultades en la Gestión Técnica de Código y Respaldos:** La mayoría de clientes móviles carecen de herramientas especializadas para renderizar bloques extensos de código con sintaxis resaltada, importar archivos de proyectos y generar respaldos encriptados portables.

---

## 2. Árbol de Problemas (Causa - Efecto)

```
                                      [ EFECTOS / CONSECUENCIAS ]
 +---------------------------------------------------------------------------------------------------+
 | - Pérdida de soberanía digital y riesgo constante de fuga de información confidencial o código.   |
 | - Inoperatividad en entornos sin conexión a Internet o con conectividad inestable.                |
 | - Pérdida de productividad por dispersión de herramientas, chats desorganizados y memorias mixtas.|
 | - Costos recurrentes elevados e imposibilidad de portar o respaldar la información de forma segura|
 +---------------------------------------------------------------------------------------------------+
                                                  ▲
                                                  │
                               +-------------------------------------+
                               |         PROBLEMA CENTRAL            |
                               |  Inexistencia de una plataforma     |
                               |  móvil unificada, híbrida y privada |
                               |  para la interacción con múltiples  |
                               |  motores de IA y gestión de         |
                               |  memorias contextuales seguras.     |
                               +-------------------------------------+
                                                  ▲
                                                  │
                                     [ CAUSAS RAÍZ / ORIGEN ]
 +---------------------------------------------------------------------------------------------------+
 | 1. Arquitecturas móviles cerradas dependientes al 100% de la nube de proveedores comerciales.     |
 | 2. Falta de integración de modelos de lenguaje pequeños (SLMs) cuantizados on-device en Android.  |
 | 3. Inexistencia de un sistema de perfiles ("Máscaras") con memorias conversacionales aisladas.    |
 | 4. Carencia de estándares de cifrado local en reposo (AES-256) para historiales y respaldos.      |
 +---------------------------------------------------------------------------------------------------+
```

---

## 3. Árbol de Objetivos (Medios - Fines)

```
                                         [ FINES / IMPACTO ]
 +---------------------------------------------------------------------------------------------------+
 | - Garantizar la total privacidad y soberanía de los datos sensibles mediante inferencia local.    |
 | - Brindar continuidad operativa offline para consultas técnicas y procesamiento de código.        |
 | - Maximizar la productividad mediante perfiles especializados con contextos independientes.       |
 | - Proporcionar portabilidad y seguridad absoluta de la información mediante respaldos cifrados.  |
 +---------------------------------------------------------------------------------------------------+
                                                  ▲
                                                  │
                               +-------------------------------------+
                               |         OBJETIVO GENERAL            |
                               |  Desarrollar la aplicación móvil    |
                               |  Mask AI en Kotlin para Android con |
                               |  motor híbrido de IA (Local/Nube),  |
                               |  perfiles con memoria aislada y     |
                               |  seguridad criptográfica AES-256.   |
                               +-------------------------------------+
                                                  ▲
                                                  │
                                     [ MEDIOS / COMPONENTES ]
 +---------------------------------------------------------------------------------------------------+
 | 1. Implementación de motor on-device cuantizado (GGUF INT4 / MediaPipe LLM Inference).            |
 | 2. Integración de adaptadores REST para APIs cloud (OpenAI, Gemini, Claude, Ollama).              |
 | 3. Base de datos Room encriptada con SQLCipher y aislamiento contextual por perfil experto.       |
 | 4. Visor nativo con resaltado de código y sistema de importación/exportación de respaldos.        |
 +---------------------------------------------------------------------------------------------------+
```
