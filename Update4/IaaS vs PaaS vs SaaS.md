---
Fecha de creación: 2025-11-30 10:30
Fecha de Modificación: 2025-11-30 12:15
tags:
Tema: IaaS vs PaaS vs SaaS
---

## 📚 Idea/Concepto 
Los modelos de servicio cloud representan niveles progresivos de abstracción de la Pila de TI con trade-off inverso entre control y overhead administrativo. **IaaS (Infrastructure as a Service)** abstrae hardware físico y virtualización; el usuario (SysAdmin/IT Admin) gestiona OS, middleware, runtime, aplicación y datos, proveyendo máximo control con máximo overhead operativo. **PaaS (Platform as a Service)** abstrae hardware, virtualización, OS y middleware/runtime; el usuario (Developer) solo gestiona aplicación y datos, habilitando nativamente autoscaling y distribución mediante Application Gateway L7. **FaaS (Functions as a Service)** abstrae la gestión de aplicaciones completas; el usuario solo escribe funciones individuales de código ejecutadas por eventos, representando el máximo nivel de abstracción para código ejecutable, base del modelo Serverless. **BaaS (Backend as a Service)** provee servicios backend gestionados de terceros (Object Storage, Auth, DB); combinado con FaaS conforma la arquitectura Serverless completa, eliminando gestión de infraestructura. **SaaS (Software as a Service)** abstrae la pila completa; el usuario final consume aplicación terminada bajo suscripción, implementando Multi-tenancy para eficiencia de costos y escalabilidad. Cada modelo optimiza para diferentes necesidades: IaaS para control granular, PaaS para velocidad de desarrollo, FaaS/BaaS para arquitecturas event-driven sin gestión de servidores, SaaS para consumo inmediato.

## 📌 Puntos Claves
- **IaaS**: Abstrae hardware/virtualización; usuario gestiona OS+middleware+app+datos; máximo control/overhead
- **PaaS**: Abstrae hasta runtime; usuario gestiona solo app+datos; autoscaling nativo, enfoque developer
- **FaaS**: Abstrae gestión de apps; usuario escribe solo funciones event-driven; base de Serverless
- **BaaS**: Servicios backend gestionados (Storage, Auth, DB); complemento de FaaS
- **Serverless**: FaaS + BaaS = cero gestión de infraestructura
- **SaaS**: Pila completa abstraída; aplicación lista para consumir; multi-tenancy
- **Trade-off fundamental**: Control ↔ Overhead administrativo (relación inversa)
- **Selección**: IaaS (control), PaaS (velocidad), FaaS/BaaS (event-driven), SaaS (consumo inmediato)

## 🔗 Connections
- [[Virtual Private Cloud (VPC)]]
- [[Cloud Híbrido (Hybrid Cloud)]]
- [[Escalamiento horizontal y vertical en el cloud]]
- [[Arquitectura Orientada a Eventos]]
- [[Microservicios]]

## 💡 Personal Insight
Los modelos de servicio cloud no son opciones arbitrarias sino puntos en un espectro de abstracción con matemática económica clara: cada capa abstraída reduce OpEx operativo pero disminuye control granular. IaaS da máxima flexibilidad a cambio de gestionar toda la pila (patches, seguridad, escalamiento), apropiado cuando se requiere control total o workloads legacy. PaaS elimina undifferentiated heavy lifting, permitiendo que developers enfoquen en lógica de negocio, no en infraestructura. FaaS/BaaS representa el punto de inflexión: código completamente desacoplado de infraestructura, pagando solo por ejecuciones (no por capacidad ociosa), ideal para arquitecturas event-driven. SaaS cierra el ciclo: cero gestión técnica, puro consumo de funcionalidad. La selección no es preferencia sino optimización: ¿qué nivel de abstracción maximiza velocidad de entrega minimizando overhead según el contexto específico?

## 🧾 Recursos
