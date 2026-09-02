# CONFIGURACIÓN DEL ESPACIO DE TRABAJO EN CLICKUP
**Proyecto:** Mask AI  
**Workspace:** `MaskAI-Engineering-NuevaAmerica`  
**Metodología:** Marco Ágil Scrum + Tableros Kanban de Flujo Continuo  

---

## 1. Estructura Jerárquica en ClickUp
```
Workspace: MaskAI-Engineering
└── Space: Core App Development (Android Kotlin)
    ├── Folder: 01_Primer_Corte_Ingenieria
    │   ├── List: Investigacion_y_Requisitos (Tareas de encuestas, estado del arte, SRS)
    │   └── List: Arquitectura_y_Diseno (Diagramas C4, DER, prototipos Figma)
    ├── Folder: 02_Segundo_Corte_DEV_UAT
    │   ├── List: Sprint_Backlog (Historias HU-01 a HU-15 en desarrollo)
    │   ├── List: QA_and_Bug_Tracking (Defectos BUG-01 a BUG-10)
    │   └── List: Ambientes_DEV_UAT (Despliegues y pruebas de integración)
    └── Folder: 03_Tercer_Corte_Entrega_Final
        ├── List: Documentacion_APA7_y_Manuales
        └── List: Sustentacion_y_Release_Final
```

---

## 2. Estados Personalizados del Flujo de Trabajo (Custom Statuses)
1. **`Backlog`** (Gris): Tarea identificada y priorizada pero no iniciada.
2. **`In Progress / En Desarrollo`** (Azul): Asignada a un desarrollador y en codificación activa.
3. **`Code Review / Revisión por Pares`** (Púrpura): Pull Request abierto en GitHub esperando aprobación.
4. **`QA / Testing DEV`** (Naranja): Desplegado en ambiente DEV para verificación de casos de prueba.
5. **`UAT Validation`** (Amarillo): Versión distribuida a usuarios de prueba para validación.
6. **`Closed / Done`** (Verde): Tarea completada con criterios de aceptación verificados y documentada.
