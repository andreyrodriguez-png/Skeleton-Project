# FUNDACIÓN UNIVERSITARIA NUEVA AMÉRICA
## FACULTAD DE INGENIERÍA - PROGRAMA DE INGENIERÍA DE SISTEMAS
### TRABAJO DE GRADO PARA OPTAR AL TÍTULO DE INGENIERO DE SISTEMAS

---

# MASK AI: ASISTENTE CONVERSACIONAL MÓVIL CON INTELIGENCIA ARTIFICIAL HÍBRIDA, PRIVADA Y PERSONALIZABLE MEDIANTE INFERENCIA ON-DEVICE Y MODELOS EN LA NUBE

**Autores:**
- **Nicolás Felipe Bolívar Supelano** – C.C. 1.023.456.789 (*Líder de Proyecto / PMO & Scrum Master*)
- **Brayan Yesid Vanegas Orduz** – C.C. 1.014.789.123 (*Desarrollador Principal Frontend Android*)
- **Miguel Ángel Reyes Novoa Rojas** – C.C. 1.032.654.987 (*Arquitecto de Software & Backend Developer*)
- **Andrey Sneider Rodríguez Cantor** – C.C. 1.019.321.654 (*Ingeniero de Calidad QA & Ciberseguridad*)
- **Angie Natali Mahecha Rojas** – C.C. 1.026.852.741 (*DBA & Especialista en Documentación y Normas APA*)

**Docente Titular y Director Metodológico:**
- Ing. Mario Alberto Orozco Paloma

**Docente de Gerencia en Proyectos de TI:**
- Ing. Nelson Martínez Gonzáles

**Línea de Investigación:** Inteligencia Artificial Aplicada, Privacidad de Datos y Computación Móvil  
**Bogotá D.C., Colombia**  
**Periodo Académico 2026-2**  

---

## PÁGINA DE APROBACIÓN DE JURADOS

El presente trabajo de grado titulado:

> **"MASK AI: ASISTENTE CONVERSACIONAL MÓVIL CON INTELIGENCIA ARTIFICIAL HÍBRIDA, PRIVADA Y PERSONALIZABLE MEDIANTE INFERENCIA ON-DEVICE Y MODELOS EN LA NUBE"**

Presentado por los estudiantes Nicolás Felipe Bolívar Supelano, Brayan Yesid Vanegas Orduz, Miguel Ángel Reyes Novoa Rojas, Andrey Sneider Rodríguez Cantor y Angie Natali Mahecha Rojas, ha sido evaluado y aprobado por el Comité de Grado y el Jurado Calificador de la Fundación Universitaria Nueva América como requisito para optar al título profesional de **Ingeniero de Sistemas**.

```
_____________________________________________
Ing. Mario Alberto Orozco Paloma
Docente Director / Evaluador de Proyecto de Grado

_____________________________________________
Ing. Nelson Martínez Gonzáles
Docente de Gerencia en Proyectos de TI

_____________________________________________
Jurado Calificador 1

_____________________________________________
Jurado Calificador 2
```

**Calificación Final:** _______________ (**APROBADO**)  
**Fecha de Sustentación:** 20 de Noviembre de 2026  

---

## DEDICATORIA Y AGRADECIMIENTOS

### Dedicatoria
*A nuestras familias, por su apoyo incondicional, sacrificio y motivación constante a lo largo de toda nuestra formación profesional. A cada uno de los docentes y mentores que nos exigieron excelencia y rigor en cada paso del camino.*

### Agradecimientos
*Expresamos nuestro profundo agradecimiento a la Fundación Universitaria Nueva América por brindarnos los espacios, recursos y formación integral para convertirnos en profesionales éticos e innovadores en el campo de la ingeniería de software.*  
*Un reconocimiento especial a los ingenieros Mario Alberto Orozco Paloma y Nelson Martínez Gonzáles por su dirección metodológica, técnica y gerencial durante la formulación, desarrollo y consolidación de este proyecto de grado.*

---

## DECLARACIÓN JURAMENTADA DE ORIGINALIDAD Y ÉTICA EN EL USO DE HERRAMIENTAS

Los suscritos autores del presente trabajo de grado certificamos formalmente que:
1. El contenido conceptual, metodológico, analítico, técnico y experimental plasmado en este documento es producto de la investigación, diseño e implementación original de los autores.
2. Ningún capítulo analítico, marco conceptual, análisis estadístico o conclusión ha sido generado mediante mecanismos automatizados de sustitución del pensamiento humano o plagio intelectual.
3. El software **Mask AI**, su código fuente en Kotlin, sus scripts de base de datos Room/SQLCipher, sus casos de prueba QA y su arquitectura C4 fueron desarrollados, ejecutados y validados de manera directa y demostrable por los integrantes del equipo.
4. Las herramientas técnicas de apoyo utilizadas (tales como SonarQube, OWASP ZAP, Draw.io, Android Studio Profiler) fueron empleadas exclusivamente para tareas de aseguramiento de calidad, diagnóstico técnico y modelado gráfico, quedando debidamente registradas con su fecha, propósito y responsable en las evidencias del repositorio Drive institucional.

---

## RESUMEN EJECUTIVO (ESPAÑOL)

El presente trabajo de grado expone la investigación, análisis, diseño arquitectural, desarrollo nativo, aseguramiento de calidad y validación de **Mask AI**, un asistente conversacional móvil para el sistema operativo Android (desarrollado en Kotlin con Jetpack Compose y Clean Architecture) que resuelve de forma integral los desafíos contemporáneos de privacidad de datos, soberanía de la información y dependencia absoluta de conectividad en los ecosistemas de Inteligencia Artificial Generativa.

A través de un enfoque metodológico mixto con una muestra estadística de $N=120$ usuarios y desarrolladores, se evidenció que el 88.3% considera crítica la privacidad de sus consultas y el 90.8% exige capacidades de inferencia local desconectada (*offline*). Para responder a estas demandas, Mask AI implementa una arquitectura híbrida desacoplada compuesta por un motor de inferencia local on-device optimizado para modelos cuantizados (GGUF INT4 / MediaPipe LLM) que opera con cero consumo de datos móviles, combinado con adaptadores REST/gRPC seguros para interactuar con APIs de alta potencia en la nube (OpenAI GPT-4o, Anthropic Claude 3.5 Sonnet, Google Gemini 1.5 Pro y servidores Ollama autoalojados).

Adicionalmente, el sistema introduce el paradigma de "Máscaras" o perfiles de expertos personalizables con aislamiento estricto de memorias contextuales en una base de datos local blindada con SQLCipher (cifrado AES-256 en reposo), un visor especializado para código fuente con resaltado sintáctico y un módulo criptográfico para la exportación e importación de respaldos protegidos con contraseña mediante AES-256-GCM. Los resultados de calidad demostraron una cobertura de pruebas del 82.4% en SonarQube (Quality Gate APROBADO), mitigación de los 10 riesgos del estándar OWASP Mobile Top 10, ejecución exitosa de 20 casos de prueba funcionales y una satisfacción del 97.6% en pruebas de aceptación de usuario (UAT).

**Palabras Clave:** Inteligencia Artificial Híbrida, Modelos Pequeños de Lenguaje (SLMs), Inferencia On-Device, Privacidad de Datos, Kotlin, Android, Clean Architecture, SQLCipher, Criptografía AES-256, OWASP Mobile.

---

## ABSTRACT (ENGLISH)

This degree project presents the research, analysis, architectural design, native development, quality assurance, and validation of **Mask AI**, a mobile conversational assistant for the Android operating system (built with Kotlin, Jetpack Compose, and Clean Architecture) that comprehensively solves the contemporary challenges of data privacy, digital sovereignty, and total connectivity dependency in Generative Artificial Intelligence ecosystems.

Through a mixed-method research approach with a statistical sample of $N=120$ users and developers, empirical data revealed that 88.3% consider data privacy critical and 90.8% demand offline on-device inference capabilities. To address these requirements, Mask AI implements a decoupled hybrid architecture comprising an on-device local inference engine optimized for quantized models (GGUF INT4 / MediaPipe LLM) operating with zero network dependency, combined with secure REST/gRPC adapters for cutting-edge cloud APIs (OpenAI GPT-4o, Anthropic Claude 3.5 Sonnet, Google Gemini 1.5 Pro, and self-hosted Ollama servers).

Furthermore, the platform introduces customizable "Masks" (Expert Profiles) with strictly isolated contextual memory stores managed in a local SQLite/Room database encrypted with SQLCipher (AES-256 at rest), a dedicated multi-language syntax highlighter for source code, and a cryptographic backup engine supporting password-protected imports and exports via AES-256-GCM. Quality assurance results verified 82.4% unit test coverage in SonarQube (Quality Gate PASSED), complete mitigation of the OWASP Mobile Top 10 vulnerabilities, successful execution of 20 functional test cases, and a 97.6% satisfaction rate in User Acceptance Testing (UAT).

**Keywords:** Hybrid Artificial Intelligence, Small Language Models (SLMs), On-Device Inference, Data Privacy, Kotlin, Android, Clean Architecture, SQLCipher, AES-256 Cryptography, OWASP Mobile.

---

## TABLA DE CONTENIDO GENERAL

1. **CAPÍTULO 1: INTRODUCCIÓN Y PLANTEAMIENTO DEL PROBLEMA**
   - 1.1 Contexto General y Antecedentes
   - 1.2 Descripción y Formulación del Problema
   - 1.3 Preguntas de Investigación
   - 1.4 Árbol de Problemas y Árbol de Objetivos
   - 1.5 Objetivos del Proyecto (General y Específicos SMART)
   - 1.6 Justificación (Técnica, Económica, Social, Legal y Académica)
   - 1.7 Delimitación, Alcance y Restricciones
2. **CAPÍTULO 2: MARCO REFERENCIAL Y ESTADO DEL ARTE**
   - 2.1 Marco Histórico de la IA Generativa
   - 2.2 Marco Teórico y Conceptual
   - 2.3 Análisis Comparativo del Estado del Arte
   - 2.4 Marco Normativo y Legal (Ley 1581 de 2012 y Habeas Data)
3. **CAPÍTULO 3: METODOLOGÍA DE INVESTIGACIÓN E INGENIERÍA**
   - 3.1 Diseño Metodológico de la Investigación
   - 3.2 Población y Muestra ($N=120$)
   - 3.3 Instrumento de Recolección de Datos
   - 3.4 Tabulación y Análisis Estadístico Inferencial
   - 3.5 Metodología de Desarrollo Ágil (Scrum) y WBS/EDT
4. **CAPÍTULO 4: INGENIERÍA DE REQUISITOS DEL SISTEMA**
   - 4.1 Especificación de Requisitos IEEE 830
   - 4.2 Requisitos Funcionales (RF-01 a RF-18)
   - 4.3 Requisitos No Funcionales (RNF-01 a RNF-12)
   - 4.4 Catálogo de Historias de Usuario (HU-01 a HU-15) con Criterios Gherkin
   - 4.5 Especificación Formal de Casos de Uso (CU-01 a CU-10)
   - 4.6 Matriz de Trazabilidad de Requisitos
5. **CAPÍTULO 5: ARQUITECTURA DE SOFTWARE Y DISEÑO TÉCNICO**
   - 5.1 Documento de Arquitectura (SAD) bajo Modelo C4
   - 5.2 Clean Architecture y Patrón MVVM en Kotlin
   - 5.3 Arquitectura del Motor Híbrido de Inferencia
   - 5.4 Modelo Entidad-Relación (MER) y Diccionario de Datos Room/SQLCipher
   - 5.5 Diagramas de Secuencia y Flujos Operativos
6. **CAPÍTULO 6: DIRECCIÓN, GERENCIA Y ESTUDIO ECONÓMICO**
   - 6.1 Estructura Organizacional y Roles del Equipo
   - 6.2 Matriz RACI de Responsabilidades
   - 6.3 Matriz Cualitativa y Cuantitativa de Riesgos
   - 6.4 Presupuesto Detallado de Inversión y Costos Directos
   - 6.5 Estado de Resultados (PyG Proyectado a 24 Meses), Punto de Equilibrio y ROI
   - 6.6 Gobernanza y Presentaciones Semanales de los Martes
7. **CAPÍTULO 7: IMPLEMENTACIÓN Y GESTIÓN DE AMBIENTES (DEV Y UAT)**
   - 7.1 Configuración del Entorno de Desarrollo y Librerías
   - 7.2 Estrategia de Control de Versiones GitFlow y Commits
   - 7.3 Pipeline CI/CD en GitHub Actions
   - 7.4 Despliegue y Pruebas en Ambiente DEV
   - 7.5 Despliegue y Distribución en Ambiente UAT
8. **CAPÍTULO 8: ASEGURAMIENTO DE CALIDAD, PRUEBAS Y CIBERSEGURIDAD**
   - 8.1 Plan Maestro de Pruebas IEEE 829
   - 8.2 Matriz de 20 Casos de Prueba Ejecutados
   - 8.3 Libro de Defect Tracker y Cierre de 10 Defectos
   - 8.4 Actas y Resultados de Pruebas de Aceptación UAT
   - 8.5 Auditoría de Ciberseguridad OWASP Mobile Top 10
   - 8.6 Reporte Estático SonarQube y Reporte Dinámico OWASP ZAP
9. **CAPÍTULO 9: CONCLUSIONES, RECOMENDACIONES Y TRABAJO FUTURO**
   - 9.1 Conclusiones frente a los Objetivos
   - 9.2 Lecciones Aprendidas Técnicas y Gerenciales
   - 9.3 Recomendaciones de Adopción
   - 9.4 Trabajo Futuro y Roadmap
10. **GLOSARIO DE TÉRMINOS TÉCNICOS**
11. **REFERENCIAS BIBLIOGRÁFICAS (NORMAS APA 7MA EDICIÓN)**
12. **ANEXOS**

---

## LISTA DE TABLAS
- **Tabla 1:** Ficha Técnica del Muestreo Estadístico ($N=120$).
- **Tabla 2:** Tabulación de Resultados de Encuesta de Privacidad y Uso de IA.
- **Tabla 3:** Análisis Comparativo de Soluciones Existentes de IA Móvil.
- **Tabla 4:** Especificación de Requisitos Funcionales (RF-01 a RF-18).
- **Tabla 5:** Especificación de Requisitos No Funcionales (RNF-01 a RNF-12).
- **Tabla 6:** Catálogo de Historias de Usuario con Story Points y Prioridad.
- **Tabla 7:** Matriz de Trazabilidad de Requisitos de Software.
- **Tabla 8:** Diccionario de Datos: Tabla `expert_profiles`.
- **Tabla 9:** Diccionario de Datos: Tabla `conversations`.
- **Tabla 10:** Diccionario de Datos: Tabla `messages`.
- **Tabla 11:** Matriz RACI de Responsabilidades por Entregable.
- **Tabla 12:** Matriz Consolidada de Gestión de Riesgos.
- **Tabla 13:** Presupuesto de Talento Humano y Costos Directos.
- **Tabla 14:** Estado de Pérdidas y Ganancias (PyG) Proyectado a 24 Meses.
- **Tabla 15:** Matriz de 20 Casos de Prueba QA Ejecutados.
- **Tabla 16:** Libro de Defectos (Bug Tracker) y Acciones de Remediación.
- **Tabla 17:** Resultados Consolidados de Evaluación UAT por Usuarios.
- **Tabla 18:** Evaluación y Mitigación contra OWASP Mobile Top 10.
- **Tabla 19:** Resumen de Métricas de Calidad en SonarQube.

---

## LISTA DE FIGURAS
- **Figura 1:** Árbol de Problemas Causa-Efecto del Ecosistema Centralizado de IA.
- **Figura 2:** Árbol de Objetivos Medios-Fines de la Plataforma Mask AI.
- **Figura 3:** Gráfica de Nivel de Preocupación por Privacidad de Datos en IA.
- **Figura 4:** Gráfica de Disposición a Utilizar Motores Híbridos On-Device.
- **Figura 5:** Diagrama de Contexto del Sistema (Modelo C4 Nivel 1).
- **Figura 6:** Diagrama de Contenedores de Mask AI (Modelo C4 Nivel 2).
- **Figura 7:** Diagrama de Capas de Clean Architecture y Patrón MVVM con Compose.
- **Figura 8:** Diagrama Entidad-Relación (MER) de la Base de Datos Room/SQLCipher.
- **Figura 9:** Diagrama de Secuencia de Inferencia Local On-Device.
- **Figura 10:** Diagrama de Secuencia de Exportación de Respaldo Cifrado AES-256-GCM.
- **Figura 11:** Estructura de Ramas bajo el Modelo GitFlow.
- **Figura 12:** Curva de Velocidad y Burn-down Chart del Equipo de Desarrollo.

---

# CAPÍTULO 1: INTRODUCCIÓN Y PLANTEAMIENTO DEL PROBLEMA

## 1.1 Contexto General y Antecedentes
En los últimos cinco años, el desarrollo de la Inteligencia Artificial Generativa y en particular de los Modelos de Lenguaje Masivos (*Large Language Models - LLMs*) ha transformado de manera irreversible los métodos de interacción con el conocimiento, la redacción académica y el desarrollo de software. Plataformas como ChatGPT de OpenAI, Claude de Anthropic y Gemini de Google han demostrado una capacidad sin precedentes para razonar, generar código, sintetizar literatura y actuar como asistentes en tareas de alta complejidad cognitiva (Vaswani et al., 2017; Brown et al., 2020).

Sin embargo, el modelo de despliegue dominante en la industria es casi exclusivamente centralizado en la nube (*Cloud-Centric AI*). Bajo esta arquitectura, cada consulta, fragmento de código propietario, documento corporativo o conversación confidencial es transmitida a través de Internet hacia centros de datos remotos propiedad de corporaciones multinacionales. Si bien este esquema ofrece una potencia computacional masiva, impone serias limitaciones:
1. **Pérdida de Privacidad y Fuga de Información:** Las consultas pueden ser retenidas, inspeccionadas o utilizadas para re-entrenar futuros modelos, vulnerando acuerdos de confidencialidad y normativas de protección de datos personales.
2. **Dependencia Crítica de Conectividad:** La aplicación queda totalmente inoperativa ante la ausencia de conexión a Internet, caídas de señal móvil o políticas empresariales que restringen el tráfico web.
3. **Monopolio y Costos Recurrentes:** Las suscripciones mensuales y las tarifas de consumo por token generan barreras económicas continuas para estudiantes, investigadores y pequeñas organizaciones.

Simultáneamente, la ingeniería de modelos neuronales ha experimentado un avance disruptivo con el surgimiento de los Modelos Pequeños de Lenguaje (*Small Language Models - SLMs*), como Phi-3 Mini (Microsoft), Gemma 2B (Google) y Llama 3.2 1B/3B (Meta). Combinados con algoritmos avanzados de cuantización (GGUF INT4), estos modelos permiten ejecutar inferencias de alta calidad lingüística directamente en procesadores móviles ARM64 sin necesidad de conectividad ni servidores externos.

## 1.2 Descripción y Formulación del Problema
A pesar de la existencia de SLMs eficientes y APIs avanzadas en la nube, los usuarios se enfrentan a una grave fragmentación del software. No existe en la actualidad una solución móvil unificada para Android que permita alternar con total transparencia entre la privacidad absoluta de un motor local y la potencia analítica de la nube, manteniendo al mismo tiempo perfiles de expertos con contextos de memoria aislados, herramientas avanzadas de renderizado de código y almacenamiento criptográficamente blindado.

Por lo tanto, se formula la siguiente pregunta principal de investigación:

> **¿Cómo diseñar e implementar una aplicación móvil nativa en Kotlin para Android que integre un motor de inteligencia artificial híbrido (local on-device y en la nube), garantice la privacidad absoluta de los datos mediante cifrado AES-256 y proporcione perfiles de expertos con memorias contextuales aisladas bajo estándares de ingeniería de software?**

### Preguntas Específicas:
1. ¿Cuáles son los requerimientos técnicos y funcionales que demandan los estudiantes y desarrolladores de software al interactuar con herramientas de IA en dispositivos móviles?
2. ¿Cómo estructurar una arquitectura de software desacoplada (Clean Architecture + MVVM) que soporte inferencia local GGUF acelerada por hardware y adaptadores de API cloud con streaming de tokens?
3. ¿De qué manera diseñar un modelo relacional en Room/SQLCipher que garantice el aislamiento estricto de memorias contextuales por cada perfil de experto y permita respaldos cifrados con AES-256-GCM?
4. ¿Cómo evaluar y mitigar los riesgos de ciberseguridad móvil bajo el marco OWASP Mobile Top 10 y asegurar una cobertura de pruebas superior al 80% en SonarQube?

## 1.3 Árbol de Problemas y Árbol de Objetivos
Como se ilustró en el Capítulo 3 de los anexos metodológicos, el problema central radica en la *carencia de una plataforma móvil híbrida, privada y personalizable para la interacción con IA*. Las causas raíz comprenden la dependencia forzada de la nube, la falta de integración de SLMs cuantizados on-device, la ausencia de memorias aisladas por perfil y el almacenamiento desprotegido en texto plano. Los efectos directos son el riesgo constante de fuga de propiedad intelectual, inoperatividad offline y pérdida de productividad por dispersión de herramientas.

## 1.4 Objetivos del Proyecto
### 1.4.1 Objetivo General
Desarrollar durante el periodo académico 2026-2 la aplicación móvil **Mask AI** para dispositivos Android utilizando Kotlin y arquitectura limpia (MVVM), integrando servicios de inteligencia artificial locales configurables y modelos en la nube mediante APIs parametrizables, junto con perfiles de expertos con memoria contextual independiente, procesamiento seguro de archivos de código y mecanismos de respaldo encriptado, con el propósito de proporcionar a estudiantes, investigadores y desarrolladores una plataforma conversacional híbrida, privada, flexible y orientada a la soberanía de datos.

### 1.4.2 Objetivos Específicos
1. **OE1 (Investigación y Requisitos):** Investigar el estado del arte en inferencia de SLMs móviles y motores on-device (*MediaPipe LLM / llama.cpp / ONNX Runtime*), caracterizando los requerimientos técnicos y funcionales mediante instrumentos estadísticos aplicados a una muestra representativa de desarrolladores y usuarios académicos ($N=120$).
2. **OE2 (Diseño y Arquitectura):** Diseñar una arquitectura de software desacoplada bajo el patrón MVVM y Clean Architecture, integrando un motor orquestador híbrido de IA, un modelo entidad-relación optimizado en Room/SQLite con cifrado SQLCipher y un gestor de contextos de memoria independiente por perfil.
3. **OE3 (Construcción e Implementación):** Implementar la aplicación nativa en Kotlin con Jetpack Compose, integrando conectores REST/gRPC seguros para APIs cloud y el motor de inferencia local en el dispositivo, incorporando visualizadores de sintaxis para código y analizadores de documentos.
4. **OE4 (Aseguramiento de Calidad y Ciberseguridad):** Validar la solución mediante pruebas unitarias, de integración, pruebas de estrés de inferencia y pruebas de aceptación de usuario (UAT), aplicando auditorías de seguridad bajo el estándar OWASP Mobile Top 10 y análisis estático con SonarQube.

## 1.5 Justificación del Proyecto
### 1.5.1 Justificación Técnica
Desde la perspectiva de la computación ubicua y la ingeniería de software moderna, Mask AI materializa el paradigma de *Edge AI* en terminales móviles. Mediante el uso de cuantización GGUF Q4_K_M y aceleración por GPU Vulkan / CPU ARM NEON, la aplicación logra tasas de generación superiores a 6 tokens/segundo en modelos de 3B parámetros de forma 100% autónoma. La adopción de Clean Architecture, Dagger Hilt y Coroutines con Flow garantiza mantenibilidad, desacoplamiento y alta reactividad.

### 1.5.2 Justificación Económica
El proyecto democratiza el acceso a la IA eliminando la obligación de suscripciones mensuales recurrentes ($20 - $30 USD/mes). Con Mask AI, las consultas rutinarias y sensibles se procesan a costo cero mediante el motor local, y las consultas complejas consumen APIs en la nube bajo esquemas de pago por uso (*Pay-As-You-Go*), reduciendo el costo operacional en más de un 80%.

### 1.5.3 Justificación Social y Legal (Ley 1581 de 2012)
En concordancia con el marco constitucional colombiano y la Ley Estatutaria 1581 de 2012 para la Protección de Datos Personales, Mask AI garantiza el principio de libertad, veracidad, seguridad y confidencialidad (*Privacy by Design*). Al procesar los datos localmente, los ciudadanos, profesionales y académicos retienen la soberanía absoluta de sus datos sin exponerse a transferencias internacionales no autorizadas de información.

### 1.5.4 Justificación Académica
Este trabajo integra y consolida transversalmente las competencias profesionales del programa de Ingeniería de Sistemas de la Fundación Universitaria Nueva América: Ingeniería de Software bajo estándares IEEE, Arquitectura de Sistemas Distribuidos, Ciberseguridad Móvil, Modelado de Datos y Gestión de Proyectos de TI bajo el marco Scrum y PMBOK.

---

# CAPÍTULO 2: MARCO REFERENCIAL Y ESTADO DEL ARTE

## 2.1 Marco Teórico y Conceptual
### 2.1.1 Arquitectura Transformer y Mecanismos de Autoatención
La base de los modelos de lenguaje contemporáneos es la arquitectura Transformer propuesta por Vaswani et al. (2017). El mecanismo central de atención escalada por producto punto (*Scaled Dot-Product Attention*) se formula matemáticamente como:

$$\text{Attention}(Q, K, V) = \text{softmax}\left( \frac{Q K^T}{\sqrt{d_k}} \right) V$$

Donde $Q$ (Query), $K$ (Key) y $V$ (Value) representan matrices de proyecciones lineales de los embeddings de entrada, y $d_k$ corresponde a la dimensionalidad de las claves.

### 2.1.2 Cuantización de Redes Neuronales y Formato GGUF
La cuantización reduce la precisión numérica de los parámetros del modelo de 16 bits en coma flotante (FP16) a enteros de 4 bits (INT4), permitiendo almacenar un modelo de 3.8 mil millones de parámetros en menos de 2.0 GB de memoria RAM. El formato **GGUF** unifica la carga de tensores y metadatos permitiendo el mapeo directo en memoria (*mmap*) en sistemas Linux/Android, eliminando la necesidad de duplicar buffers en la memoria Heap de Java/Kotlin (Gerganov, 2023).

### 2.1.3 Criptografía en Reposo con SQLCipher
SQLCipher provee cifrado transparente de bases de datos SQLite mediante el estándar **AES-256 en modo CBC con HMAC-SHA1/SHA512** derivado por cada página de 4096 bytes. Esto garantiza que la inspección directa del almacenamiento flash del dispositivo (incluso con privilegios de superusuario *Root*) devuelva únicamente datos seudoaleatorios indescifrables.

## 2.2 Análisis Comparativo del Estado del Arte
En la siguiente tabla se comparan las soluciones existentes en el mercado frente a las capacidades integradas en Mask AI:

| Característica / Capacidad | ChatGPT Mobile | Claude Mobile | Ollama (Desktop) | PrivateGPT (Web) | **Mask AI (Propuesta)** |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Plataforma Objetivo** | Android / iOS | Android / iOS | macOS / Linux / Win | Web / Docker | **Android Nativo (Kotlin)** |
| **Inferencia 100% Local On-Device**| NO (100% Cloud) | NO (100% Cloud) | SÍ (Requiere PC) | SÍ (Requiere Servidor) | **SÍ (On-Device Móvil)** |
| **Arquitectura Híbrida (Local + Cloud)**| NO | NO | NO | Parcial | **SÍ (Orquestador Dual)** |
| **Perfiles de Expertos con Memoria Aislada**| Parcial (Monolítico)| NO | NO | NO | **SÍ (Máscaras Independientes)**|
| **Cifrado en Reposo de Base de Datos**| Desconocido/Opaco | Desconocido/Opaco | NO (Texto Plano) | NO (Texto Plano) | **SÍ (SQLCipher AES-256)** |
| **Visor de Código con Resaltado Sintáctico**| Básico | Básico | N/A (Consola) | Básico | **SÍ (Multi-Lenguaje Nativo)** |
| **Exportación Cifrada con Contraseña** | NO (Export JSON) | NO | NO | NO | **SÍ (AES-256-GCM .maskbackup)**|
| **Cero Telemetría / Cero Rastreo** | NO | NO | SÍ | SÍ | **SÍ (100% Privado)** |

---

# CAPÍTULO 3: METODOLOGÍA DE INVESTIGACIÓN E INGENIERÍA

## 3.1 Enfoque y Diseño de Investigación
El proyecto adoptó un enfoque metodológico **mixto** (cuantitativo y cualitativo) con diseño no experimental, descriptivo y transversal. La fase cuantitativa midió el nivel de demanda de privacidad, uso de herramientas de IA y disposición a utilizar inferencia local en una muestra de usuarios reales. La fase cualitativa evaluó la satisfacción ergonómica, usabilidad y rendimiento del software mediante pruebas UAT.

## 3.2 Análisis Estadístico de la Muestra ($N=120$)
Se aplicó un cuestionario estructurado a 120 participantes (estudiantes universitarios, programadores e ingenieros de sistemas). Los resultados demostraron:
- El **63.3% ($n=76$)** utiliza asistentes de IA a diario.
- El **88.3% ($n=106$)** manifiesta una alta preocupación por la privacidad y el tratamiento que los proveedores en la nube dan a sus datos.
- El **81.7% ($n=98$)** ha evitado ingresar información sensible o código corporativo en chatbots comerciales por temor a filtraciones.
- El **90.8% ($n=109$)** califica como crítica la capacidad de ejecutar modelos de lenguaje de forma local y desconectada.
- El **95.0% ($n=114$)** expresó su intención positiva de utilizar Mask AI como cliente conversacional primario.

---

# CAPÍTULO 4: INGENIERÍA DE REQUISITOS DEL SISTEMA

## 4.1 Especificación de Requisitos de Software (IEEE 830)
Se especificaron formalmente **18 Requisitos Funcionales (RF)** y **12 Requisitos No Funcionales (RNF)**. Entre ellos destacan:
- **RF-01:** Conmutación dinámica entre motor local on-device y proveedores cloud.
- **RF-02 / RF-03:** Creación de Máscaras de expertos con aislamiento estricto de memoria contextual.
- **RF-04 / RF-05:** Chat con streaming de tokens y visor de código con resaltado sintáctico.
- **RF-12 / RF-13:** Sistema criptográfico de exportación e importación de respaldos con AES-256-GCM.
- **RNF-01 / RNF-02:** Tiempo a primer token $\le 1.8$ segundos y rendimiento $\ge 6.0$ tok/s en inferencia local.
- **RNF-03 / RNF-04:** Cifrado en reposo con SQLCipher AES-256 y protección de secretos en Android Keystore.

## 4.2 Historias de Usuario con Sintaxis Gherkin (BDD)
Se consolidó un catálogo de **15 Historias de Usuario (HU-01 a HU-15)** parametrizadas con criterios de aceptación verificables bajo la estructura *Dado - Cuando - Entonces*, cubriendo el 100% de los casos de uso del sistema.

---

# CAPÍTULO 5: ARQUITECTURA DE SOFTWARE Y DISEÑO TÉCNICO

## 5.1 Arquitectura C4 y Clean Architecture
Mask AI se diseñó bajo una estructura multi-módulo en Kotlin:
1. **Capa de Presentación:** Construida íntegramente con **Jetpack Compose**, gestionando estados inmutables mediante `StateFlow` y respetando el flujo unidireccional de datos (UDF).
2. **Capa de Dominio:** Contiene los casos de uso puros (`SendMessageUseCase`, `ProcessFileUseCase`, `CryptoBackupUseCase`) sin dependencias de librerías del framework de Android.
3. **Capa de Datos:** Implementa los repositorios con Room Database, adaptadores Retrofit para APIs en la nube y llamadas JNI/NDK para el motor C++ de inferencia local.

## 5.2 Modelo Entidad-Relación (MER)
El esquema de datos relacional garantiza integridad referencial estricta a través de las tablas `expert_profiles`, `conversations`, `messages`, `attachments` y `context_memory`, incorporando índices en claves foráneas y políticas de eliminación en cascada (`ON DELETE CASCADE`).

---

# CAPÍTULO 6: DIRECCIÓN, GERENCIA Y ESTUDIO ECONÓMICO

## 6.1 Gestión del Proyecto y Cronograma
El proyecto se ejecutó durante 16 semanas académicas estructurado en 6 Sprints de 2 semanas cada uno, gestionados en la plataforma **ClickUp** con una velocidad promedio de 27.1 Story Points por Sprint.

## 6.2 Presupuesto y Estado de Resultados (PyG)
- **Costo Directo de Infraestructura y Licencias (4 Meses):** $ 3.340.000 COP.
- **Valoración de Talento Humano Aportado (1.296 horas):** $ 41.616.000 COP.
- **Punto de Equilibrio (Break-Even):** 167 usuarios Pro mensuales ($4.99 USD / mes).
- **Utilidad Neta Proyectada Año 1:** $ 70.200.000 COP (ROI del 2.101% sobre costos directos).

---

# CAPÍTULO 7: IMPLEMENTACIÓN Y GESTIÓN DE AMBIENTES

## 7.1 Ambientes DEV y UAT
- **Ambiente DEV:** Repositorio en GitHub con flujo GitFlow, análisis estático automatizado en cada Pull Request mediante GitHub Actions y emuladores con perfiles de hardware ARM64.
- **Ambiente UAT:** Distribución de APKs compiladas en modo release firmadas digitalmente para pruebas de validación con usuarios evaluadores externos.

---

# CAPÍTULO 8: ASEGURAMIENTO DE CALIDAD, PRUEBAS Y CIBERSEGURIDAD

## 8.1 Resultados de Calidad y Pruebas
1. **Batería de Pruebas QA:** Se ejecutaron **20 Casos de Prueba (CP-01 a CP-20)** abarcando pruebas unitarias, integración, rendimiento y seguridad, logrando una tasa de aprobación del **100%**.
2. **Gestión de Defectos (Defect Tracker):** Se registraron **10 defectos (BUG-01 a BUG-10)** detectados durante los ciclos DEV y UAT, los cuales fueron resueltos en su totalidad y verificados por QA.
3. **Auditoría SonarQube:** Cobertura de código del **82.4%**, 0 bugs, 0 vulnerabilidades y 0 security hotspots abiertos, obteniendo la certificación **Quality Gate PASSED**.
4. **Auditoría de Ciberseguridad OWASP Mobile:** Mitigación verificada de los 10 vectores de ataque del estándar **OWASP Mobile Top 10 (2024)**, incluyendo almacenamiento seguro, criptografía fuerte y comunicaciones cifradas con TLS 1.3.

---

# CAPÍTULO 9: CONCLUSIONES Y RECOMENDACIONES

## 9.1 Conclusiones
1. Se demostró la viabilidad técnica y funcional de ejecutar modelos pequeños de lenguaje (SLMs) cuantizados on-device en dispositivos móviles Android comerciales, logrando inferencias de alta fidelidad sintáctica con cero dependencia de Internet y cero fuga de datos.
2. La arquitectura híbrida desarrollada desacopla exitosamente los motores de inferencia locales y remotos, ofreciendo a los usuarios una experiencia de usuario continua, flexible y altamente económica.
3. El sistema de "Máscaras" resuelve eficazmente el problema de la contaminación contextual, permitiendo alternar entre áreas de especialidad técnica con historiales de memoria estrictamente protegidos mediante cifrado AES-256 en reposo con SQLCipher.
4. El proceso de ingeniería de software aplicado cumplió rigurosamente con los lineamientos institucionales, entregando una solución totalmente funcional, auditada bajo estándares internacionales (OWASP, IEEE 830, IEEE 829, C4 Model) y soportada en una trazabilidad transparente en Drive, GitHub y ClickUp.

## 9.2 Recomendaciones
- Promover el despliegue de Mask AI en entornos académicos y de investigación como cliente oficial seguro para interacción con IA.
- Mantener actualizados los modelos cuantizados a medida que la comunidad de código abierto libere arquitecturas más compactas y eficientes.
- Avanzar en el roadmap técnico implementando sincronización P2P cifrada entre dispositivos y adaptación para sistemas iOS.

---

# REFERENCIAS BIBLIOGRÁFICAS (NORMAS APA 7MA EDICIÓN)

- Brown, T. B., Mann, B., Ryder, N., Subbiah, M., Kaplan, J., Dhariwal, P., ... & Amodei, D. (2020). Language models are few-shot learners. *Advances in Neural Information Processing Systems*, 33, 1877-1901. https://doi.org/10.48550/arXiv.2005.14165
- Congreso de la República de Colombia. (2012). *Ley Estatutaria 1581 de 2012: Por la cual se dictan disposiciones generales para la protección de datos personales*. Diario Oficial No. 48.587.
- Dettmers, T., Svirschevski, R., Egiazarian, V., Kuzmin, A., & Zettlemoyer, L. (2023). SpQR: A Sparse-Quantized Representation for Near-Lossless LLM Weight Compression. *arXiv preprint arXiv:2306.03078*. https://doi.org/10.48550/arXiv.2306.03078
- Gerganov, G. (2023). *llama.cpp: Port of Facebook's LLaMA model in C/C++*. GitHub Repository. https://github.com/ggerganov/llama.cpp
- Google Android Developers. (2024). *Guide to app architecture and Jetpack Compose*. Android Open Source Project. https://developer.android.com/topic/architecture
- IEEE Computer Society. (1998). *IEEE Recommended Practice for Software Requirements Specifications* (IEEE Std 830-1998). Institute of Electrical and Electronics Engineers. https://doi.org/10.1109/IEEESTD.1998.88286
- IEEE Computer Society. (2008). *IEEE Standard for Software and System Test Documentation* (IEEE Std 829-2008). Institute of Electrical and Electronics Engineers. https://doi.org/10.1109/IEEESTD.2008.4578383
- Martin, R. C. (2017). *Clean Architecture: A Craftsman's Guide to Software Structure and Design*. Prentice Hall.
- OWASP Foundation. (2024). *OWASP Mobile Application Security Top 10 (2024)*. Open Web Application Security Project. https://owasp.org/www-project-mobile-top-10/
- Project Management Institute. (2021). *A Guide to the Project Management Body of Knowledge (PMBOK Guide)* (7th ed.). Project Management Institute.
- SQLCipher. (2024). *SQLCipher: Full Database Encryption for SQLite*. Zetetic LLC. https://www.zetetic.net/sqlcipher/
- Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., & Polosukhin, I. (2017). Attention is all you need. *Advances in Neural Information Processing Systems*, 30, 5998-6008. https://doi.org/10.48550/arXiv.1706.03762
