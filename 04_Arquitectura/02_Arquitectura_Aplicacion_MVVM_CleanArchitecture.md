# ARQUITECTURA DE LA APLICACIÓN: CLEAN ARCHITECTURE Y PATRÓN MVVM
**Proyecto:** Mask AI  

---

## 1. Principios de Diseño
La arquitectura de Mask AI implementa rigurosamente los principios de **Clean Architecture** (Robert C. Martin) y el patrón oficial de Google **MVVM (Model-View-ViewModel)** con flujo unidireccional de datos (*UDF - Unidirectional Data Flow*):

1. **Independencia de Frameworks:** La lógica de negocio reside en la capa de dominio en Kotlin puro, sin acoplamiento con librerías de UI o del sistema operativo.
2. **Testabilidad:** Cada caso de uso y ViewModel puede ser sometido a pruebas unitarias aisladas mediante inyección de dependencias e interfaces mock.
3. **Inversión de Control (IoC):** Se utiliza **Dagger Hilt** para proveer instancias de repositorios, clientes HTTP y motores criptográficos.

---

## 2. Diagrama de Capas y Flujo Unidireccional de Datos (UDF)

```
   +-------------------------------------------------------------+
   |                        VISTA (UI)                           |
   |              Jetpack Compose Composables                    |
   +-------------------------------------------------------------+
               | User Events                   ^ UI State
               v (Click, Type, Submit)         | (StateFlow)
   +-------------------------------------------------------------+
   |                        VIEWMODEL                            |
   |         ChatViewModel / ExpertViewModel / BackupViewModel    |
   +-------------------------------------------------------------+
               | Execute                       ^ Domain Models /
               v Use Case                      | Flow<Result>
   +-------------------------------------------------------------+
   |                    CAPA DE DOMINIO                          |
   |           Use Cases / Interactors / Entidades Puras         |
   +-------------------------------------------------------------+
               | Call Repository               ^ Repository
               v Interface                     | Implementation
   +-------------------------------------------------------------+
   |                     CAPA DE DATOS                           |
   |     Data Sources: Room Encrypted DB, Retrofit APIs, NDK     |
   +-------------------------------------------------------------+
```
