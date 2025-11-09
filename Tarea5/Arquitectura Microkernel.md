---
Fecha de creación: 2025-11-09 14:16
Fecha de Modificación: 2025-11-09 14:38
tags:
Tema: Arquitectura Microkernel
---

## 📚 Idea/Concepto 
**Arquitectura Microkernel** es un patrón de arquitectura monolítica relativamente simple donde el Core system contiene solo la funcionalidad mínima esencial, eliminando la **complejidad ciclomática** (ramificaciones if/else, switch) del sistema principal para mejorar su mantenibilidad. Las funcionalidades adicionales se implementan como módulos plug-in independientes que exponen un **contrato** definiendo su comportamiento, datos de entrada y datos de salida. El núcleo utiliza un Registro (Registry) que mantiene información sobre qué plug-ins están disponibles y cómo contactarlos mediante sus contratos. Este patrón mejora la extensibilidad (agregar funcionalidades sin modificar el core), aumenta la Testabilidad (probar módulos aisladamente), y se usa para separar código volátil del código estable. Ejemplos: Eclipse IDE, navegadores con extensiones, sistemas operativos como QNX.

## 📌 Puntos Claves
- **Estructura**: Core system mínimo + módulos plug-in independientes
- **Core**: Solo funcionalidad esencial, sin complejidad ciclomática (if/else, switch)
- **Plug-ins**: Contratos definiendo comportamiento, entrada y salida
- **Registro (Registry)**: Mantiene disponibilidad y acceso a plug-ins
- **Beneficios**: Extensibilidad (agregar sin modificar core), Testabilidad (aislamiento)
- **Separación**: Código volátil (plug-ins) del código estable (core)
- **Ejemplos**: Eclipse IDE, navegadores, sistemas operativos (QNX)

## 🔗 Connections
- [[Cohesión en desarrollo de software]]
- [[Acoplamiento en desarrollo de software]]
- [[05_Pruebas - Pruebas Unitarias]]
- [[04_Implementación - Estándares de Programación]]

## 💡 Personal Insight
El Microkernel materializa el principio Open/Closed: abierto a extensión (plug-ins), cerrado a modificación (core). La eliminación de complejidad ciclomática del core no es cosmética sino estratégica: transforma ramificaciones frágiles en extensiones componibles. El Registry es el puente entre estabilidad y volatilidad, permitiendo que el código estable permanezca intacto mientras funcionalidades cambiantes se agregan o remueven dinámicamente. Es arquitectura para sistemas donde la extensibilidad predecible es más valiosa que la flexibilidad arbitraria.

## 🧾 Recursos
