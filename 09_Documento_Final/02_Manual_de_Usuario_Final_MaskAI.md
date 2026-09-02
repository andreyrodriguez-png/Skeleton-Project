# MANUAL DE USUARIO FINAL - APLICACIÓN MÓVIL MASK AI
**Versión de la Aplicación:** 1.0.0 Release  
**Plataforma:** Android 10.0+ (APK)  
**Proyecto:** Mask AI - Asistente Conversacional Móvil con IA Híbrida  

---

## 1. Introducción y Bienvenida
Bienvenido a **Mask AI**, la primera aplicación móvil diseñada para brindarle control absoluto, privacidad total y máxima flexibilidad al interactuar con Inteligencia Artificial. Con Mask AI usted puede disfrutar de inferencia de modelos de lenguaje directamente en su teléfono celular sin conexión a Internet (100% privado y seguro) o conectarse a los modelos más avanzados de la nube (OpenAI, Claude, Gemini, Ollama) desde una misma interfaz fluida.

---

## 2. Requisitos Mínimos del Dispositivo
- **Sistema Operativo:** Android 10.0 (API 29) o superior (Recomendado Android 13 o 14).
- **Memoria RAM:** Mínimo 4 GB de RAM (Recomendado 6 GB u 8 GB para modelos locales).
- **Espacio Libre de Almacenamiento:** 500 MB para la app base + 2.0 GB si descarga un modelo local GGUF.
- **Procesador:** Arquitectura ARM64 (64 bits).

---

## 3. Guía de Instalación Rápida
1. Descargue el archivo de instalación `mask-ai-v1.0.0-release.apk` en su teléfono.
2. Abra el archivo y conceda el permiso "Instalar aplicaciones de fuentes desconocidas" si el sistema lo solicita.
3. Pulse **Instalar** y espere la confirmación.
4. Abra la aplicación desde el cajón de aplicaciones de su dispositivo.

---

## 4. Navegación y Uso de Funcionalidades Principales

### 4.1 Pantalla Principal de Chat
- **Barra Superior:** Muestra la Máscara activa y el selector de Motor de IA (Local vs Nube).
- **Área de Conversación:** Despliega el flujo de mensajes con soporte de streaming, texto enriquecido y colores en código.
- **Barra de Entrada:** Campo para escribir prompts, botón de adjuntar archivos (+) y botón de envío.

### 4.2 Selección y Conmutación de Motores de IA
1. En el encabezado superior del chat, pulse sobre el chip de motor activo (ej. "Motor Local").
2. Se desplegará un menú modal con las opciones disponibles:
   - **Motor Local (GGUF On-Device):** Ejecución 100% offline y privada en su hardware.
   - **OpenAI (GPT-4o / GPT-4o-mini):** Respuestas rápidas de alta potencia.
   - **Anthropic Claude (3.5 Sonnet):** Ideal para análisis profundo y redacción compleja.
   - **Google Gemini (1.5 Pro / Flash):** Excelente ventana de contexto.
   - **Ollama Local / Servidor Remoto:** Para conectar con su servidor propio en red local.

### 4.3 Gestión de Máscaras (Perfiles de Expertos)
1. Deslice el panel lateral izquierdo o pulse el ícono de menú (☰).
2. Seleccione **"Gestionar Máscaras"**.
3. Puede elegir entre las máscaras preinstaladas (*Programador Senior, Asistente de Redacción, Tutor Académico, Consultor Legal*) o pulsar el botón flotante **"+"** para crear una nueva.
4. Al crear una máscara, configure:
   - **Nombre:** Identificador del experto.
   - **Rol y Avatar:** Título y apariencia visual.
   - **Prompt de Sistema (System Prompt):** Instrucciones sobre cómo debe pensar y responder.
   - **Temperatura:** Deslizador de 0.0 (muy preciso/lógico) a 1.0 (muy creativo).
5. Pulse **"Guardar Máscara"**. Cada máscara mantendrá sus propias conversaciones y memoria independiente.

### 4.4 Visor de Código y Copiado Rápido
- Cuando el asistente genere bloques de código (Kotlin, Python, Java, JavaScript, C++, SQL, etc.), la aplicación aplicará automáticamente colores de sintaxis.
- En la esquina superior derecha del bloque de código encontrará el botón **"Copiar Código"**. Un solo toque copiará el fragmento limpio directamente a su portapapeles.

### 4.5 Ingesta de Archivos de Código y Documentos
1. En la barra de mensaje, pulse el ícono de clip (+).
2. Seleccione un archivo de su almacenamiento (.txt, .py, .kt, .json, .md).
3. El archivo se vinculará al mensaje. Escriba su consulta (ej. "¿Encuentra errores en esta función?") y pulse Enviar.

### 4.6 Copias de Seguridad Cifradas (Exportar / Importar)
1. Ingrese a **Ajustes > Seguridad y Respaldos**.
2. Para exportar: Pulse **"Exportar Respaldo Cifrado"**, defina una contraseña maestra segura y elija dónde guardar el archivo `.maskbackup`.
3. Para restaurar: Pulse **"Importar Respaldo"**, seleccione el archivo `.maskbackup` e ingrese la contraseña maestra. Todos sus chats y máscaras serán recuperados exactamente.
