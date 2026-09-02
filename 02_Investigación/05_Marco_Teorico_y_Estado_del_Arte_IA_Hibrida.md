# MARCO TEÓRICO Y ESTADO DEL ARTE DE IA HÍBRIDA EN DISPOSITIVOS MÓVILES
**Proyecto:** Mask AI  

---

## 1. Fundamentos Teóricos de Modelos de Lenguaje (LLMs y SLMs)
Los Modelos de Lenguaje Masivos (*Large Language Models - LLMs*) se basan en la arquitectura Transformer descrita originalmente por Vaswani et al. (2017), la cual fundamenta su capacidad de comprensión y generación en el mecanismo de autoatención (*Self-Attention*). En los últimos años, la necesidad de trasladar estas capacidades a dispositivos con recursos energéticos y de memoria limitados impulsó la creación de los Modelos Pequeños de Lenguaje (*Small Language Models - SLMs*), tales como **Phi-3 Mini (Microsoft)**, **Gemma 2B (Google)** y **Llama 3.2 1B/3B (Meta)**.

---

## 2. Técnicas de Cuantización y Formatos de Serialización (GGUF / INT4 / INT8)
La cuantización es el proceso matemático mediante el cual los pesos de una red neuronal, típicamente representados en precisión flotante de 32 o 16 bits (FP32 / FP16), se mapean a representaciones discretas de enteros de menor tamaño (INT8 o INT4). 

$$\text{Peso Cuantizado} = \text{round}\left( \frac{\text{Peso}_{FP32}}{\text{Escala}} \right) + \text{ZeroPoint}$$

El formato **GGUF (GPT-Generated Unified Format)** permite empaquetar tanto la estructura del modelo como sus metadatos y tensores cuantizados en un único archivo binario optimizado para ser mapeado en memoria (*mmap*) en sistemas operativos móviles, permitiendo que un modelo de 3 mil millones de parámetros reduzca su huella de RAM de ~6.5 GB a tan solo ~1.8 GB, haciéndolo viable en terminales Android contemporáneos.

---

## 3. Motores de Inferencia On-Device para Android
1. **MediaPipe LLM Inference (Google):** Framework optimizado para ejecutar modelos cuantizados sobre GPU móvil utilizando APIs Vulkan y OpenCL, ofreciendo alta velocidad de generación de tokens por segundo ($tokens/s$).
2. **llama.cpp / NDK C++:** Implementación minimalista en C/C++ puro sin dependencias externas, compilable para arquitecturas ARM64-v8a con soporte de extensiones vectoriales ARM NEON.
3. **ONNX Runtime Mobile:** Motor cross-platform respaldado por Microsoft con soporte de ejecución en aceleradores de hardware (NNAPI).

---

## 4. Gestión de Memoria Contextual y Aislamiento por Perfil
La memoria en sistemas conversacionales se define como la capacidad del sistema de retener el historial relevante para condicionar las generaciones subsecuentes:

$$P(W_t | W_{<t}, \text{SystemPrompt}, \text{HistorialContextual})$$

En **Mask AI**, cada "Máscara" o perfil experto posee una clave única ($ID_{perfil}$) en la base de datos local. El motor de contexto recupera exclusivamente los últimos $k$ intercambios vinculados a dicha clave, evitando la contaminación cruzada entre dominios temáticos distintos (ej. Desarrollo de Software vs. Asesoría Legal).

---

## 5. Criptografía Aplicada a Datos Móviles (SQLCipher y AES-256-GCM)
Para garantizar la confidencialidad de los historiales, Mask AI utiliza **SQLCipher**, una extensión de SQLite que proporciona cifrado transparente de 256 bits mediante el algoritmo **AES en modo CBC con HMAC-SHA1/SHA512** por página de datos. Para los archivos de respaldo exportables, se implementa **AES-256 en modo GCM (Galois/Counter Mode)**, garantizando simultáneamente confidencialidad e integridad criptográfica de extremo a extremo autenticada mediante un tag MAC de 128 bits.
