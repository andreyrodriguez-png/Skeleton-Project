# DIAGRAMAS DE SECUENCIA Y FLUJOS OPERATIVOS
**Proyecto:** Mask AI  

---

## 1. Flujo de Inferencia Local On-Device

```
Usuario         UI (Compose)        ChatViewModel        InferenceOrchestrator      LocalEngine (NDK)      Room (SQLCipher)
   |                  |                    |                       |                        |                      |
   |-- 1. Prompt ---->|                    |                       |                        |                      |
   |                  |-- 2. onSendMsg --->|                       |                        |                      |
   |                  |                    |-- 3. GetContext ----->|                        |                      |
   |                  |                    |                       |-- 4. Query History --->|                      |
   |                  |                    |                       |<-- 5. Return msgs -----|                      |
   |                  |                    |-- 6. streamLocal() -->|                        |                      |
   |                  |                    |                       |-- 7. tokenize & run -->|                      |
   |                  |                    |                       |<-- 8. Token Stream ----|                      |
   |                  |<-- 9. Emit State --|                       |                        |                      |
   |<-- 10. Render ---|                    |                       |                        |                      |
   |                  |                    |                       |-- 11. Save Message -------------------------->|
```

---

## 2. Flujo de Exportación de Respaldo Cifrado AES-256-GCM

```
Usuario           BackupScreen         BackupViewModel        CryptoBackupEngine        Room Database
   |                    |                     |                       |                       |
   |-- 1. Click Export >|                     |                       |                       |
   |-- 2. Input Pass -->|                     |                       |                       |
   |                    |-- 3. export(pass) ->|                       |                       |
   |                    |                     |-- 4. dumpAllData() -------------------------->|
   |                    |                     |                       |<-- 5. JSON Raw Payload|
   |                    |                     |-- 6. encryptPayload ->|                       |
   |                    |                     |                       |-- 7. Derive PBKDF2    |
   |                    |                     |                       |-- 8. AES-GCM Encrypt  |
   |                    |                     |<-- 9. .maskbackup Bin |                       |
   |<-- 10. Share Sheet-|                     |                       |                       |
```
