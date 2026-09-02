# ESPECIFICACIÓN FORMAL DE CASOS DE USO UML
**Proyecto:** Mask AI  

---

## CU-01: Gestionar Perfiles de Expertos (Máscaras)
- **Actores:** Usuario Final.
- **Precondiciones:** La aplicación debe estar instalada y ejecutándose en el dispositivo.
- **Flujo Principal:**
  1. El usuario accede al menú lateral y selecciona la opción "Gestionar Máscaras".
  2. El sistema consulta la base de datos local y despliega la lista de perfiles existentes.
  3. El usuario pulsa el botón flotante "Nueva Máscara".
  4. El sistema presenta el formulario de configuración (Nombre, Rol, System Prompt, Temperatura, Avatar).
  5. El usuario diligencia los campos y presiona "Guardar".
  6. El sistema valida los datos, inserta el registro en la tabla `expert_profiles` de Room y retorna confirmación visual.
- **Flujos Alternativos:**
  - *4a. Campos obligatorios vacíos:* El sistema resalta los campos requeridos en color rojo e impide el guardado.
- **Postcondiciones:** La nueva máscara queda disponible de inmediato para iniciar conversaciones especializadas.

---

## CU-02: Procesar Inferencia Híbrida (Local / Nube)
- **Actores:** Usuario Final, Motor On-Device, APIs Cloud (OpenAI/Claude/Gemini/Ollama).
- **Precondiciones:** Existe una conversación activa asociada a una máscara determinada.
- **Flujo Principal:**
  1. El usuario escribe un mensaje en la barra de texto (con o sin archivo adjunto) y pulsa "Enviar".
  2. El sistema recupera el System Prompt de la máscara y los últimos $k$ mensajes de la conversación activa.
  3. El sistema verifica el motor de inferencia seleccionado (Local vs Nube).
  4. *Rama Local:* El sistema envía los tokens al runtime on-device (*MediaPipe / llama.cpp*), el cual genera el streaming en tiempo real.
  5. *Rama Cloud:* El sistema establece una conexión HTTPS segura con el endpoint del proveedor y transmite el stream de tokens.
  6. El sistema renderiza el texto progresivamente en la UI con formato Markdown.
  7. Al finalizar la generación, el sistema persiste el mensaje del usuario y la respuesta en la base de datos Room.
- **Flujos Alternativos:**
  - *5a. Fallo de red en modo Cloud:* Si la conexión expira (timeout > 15s), el sistema notifica el error y ofrece la opción de "Reintentar con Motor Local Offline".
- **Postcondiciones:** El historial contextual de la máscara se actualiza atómicamente.

---

## CU-03: Exportar e Importar Respaldos Cifrados
- **Actores:** Usuario Final.
- **Precondiciones:** Acceso al módulo de configuración de seguridad.
- **Flujo Principal (Exportación):**
  1. El usuario selecciona "Exportar Respaldo".
  2. El sistema solicita la definición de una contraseña maestra de cifrado.
  3. El sistema serializa las tablas de la base de datos a formato JSON estructurado.
  4. El motor criptográfico deriva una clave mediante PBKDF2 y cifra el payload con AES-256-GCM.
  5. El sistema empaqueta el archivo `.maskbackup` y abre el menú de almacenamiento para guardarlo localmente o en la nube personal.
- **Postcondiciones:** El archivo de respaldo queda protegido y no puede abrirse sin la contraseña maestra.
