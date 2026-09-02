# MATRIZ DE TRAZABILIDAD DE REQUISITOS DE SOFTWARE
**Proyecto:** Mask AI  

---

| Objetivo Específico | Requisito Funcional (SRS) | Historia de Usuario | Caso de Uso | Módulo de Arquitectura | Caso de Prueba QA |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **OE1 / OE3** | RF-01, RF-08 | HU-01 | CU-02 | `feature-ai-engine / LocalEngine` | CP-01, CP-08 |
| **OE2 / OE3** | RF-02, RF-03 | HU-02, HU-03 | CU-01 | `feature-experts / RoomDatabase` | CP-02, CP-03 |
| **OE3** | RF-04, RF-05, RF-06 | HU-04 | CU-02 | `feature-chat / ComposeUI` | CP-04, CP-05 |
| **OE3** | RF-07 | HU-05 | CU-02 | `feature-chat / FileParser` | CP-06 |
| **OE2 / OE4** | RF-12, RF-13 | HU-06 | CU-03 | `feature-backup / CryptoEngine` | CP-07, CP-12 |
| **OE4** | RF-09, RNF-04 | HU-01 | CU-02 | `core-security / KeyStore` | CP-09, CP-14 |
| **OE4** | RNF-01, RNF-02 | HU-01 | CU-02 | `feature-ai-engine / Benchmarks`| CP-10, CP-11 |
| **OE4** | RNF-03, RNF-09 | HU-06 | CU-03 | `core-data / SQLCipherHelper` | CP-13, CP-15 |
