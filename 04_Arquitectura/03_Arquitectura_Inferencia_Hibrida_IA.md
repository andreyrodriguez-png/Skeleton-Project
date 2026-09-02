# ARQUITECTURA DEL MOTOR DE INFERENCIA HÍBRIDA (LOCAL & CLOUD)
**Proyecto:** Mask AI  

---

## 1. Motor Orquestador de Inferencia (AI Router & Engine)
El componente central `AIInferenceOrchestrator` actúa como un despachador inteligente que intercepta las solicitudes de chat y evalúa:
- **Motor Seleccionado por el Usuario:** (Local On-Device vs OpenAI vs Claude vs Gemini vs Ollama).
- **Estado de Conectividad:** Si el usuario seleccionó nube pero no hay conexión activa, sugiere degradación elegante (*graceful fallback*) al motor local.
- **Inyección Contextual:** Formatea el prompt con el System Prompt del experto y las últimas $k$ interacciones recuperadas de la base de datos Room.

---

## 2. Motor Local On-Device (GGUF / INT4 / NDK)
- **Formato de Modelo:** Modelos cuantizados en formato GGUF con cuantización simétrica de 4 bits (Q4_K_M).
- **Aceleración de Hardware:** Ejecución nativa ARM64 aprovechando instrucciones ARM NEON e interfaz GPU Vulkan para paralelizar el cálculo de productos punto en la atención Transformer.
- **Ciclo de Inferencia:**
  1. Tokenización del texto de entrada mediante vocabulario SentencePiece / BPE.
  2. Inicialización de la ventana de contexto KV-Cache.
  3. Bucle de generación autorregresiva token por token emitido mediante Kotlin `Flow<String>`.

---

## 3. Motor Cloud y Adaptadores de Streaming
- **Protocolo de Comunicación:** HTTP/2 con Server-Sent Events (SSE) a través de OkHttp y Retrofit.
- **Seguridad en Tránsito:** TLS 1.3 con Certificate Pinning para prevenir ataques Man-in-the-Middle (MitM).
- **Gestión de Claves:** Las API Keys nunca se concatenan en código; se recuperan dinámicamente desde el Android Keystore en el momento exacto de firmar las cabeceras HTTP.
