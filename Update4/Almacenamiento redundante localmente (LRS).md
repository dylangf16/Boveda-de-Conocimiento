---
Fecha de creación: 2025-11-30 11:30
Fecha de Modificación: 2025-11-30 13:15
tags:
Tema: Almacenamiento redundante localmente (LRS)
---

## 📚 Idea/Concepto 
**Locally Redundant Storage (LRS)** replica datos sincrónicamente tres veces dentro de un único centro de datos (datacenter) en la misma región, distribuyendo las réplicas en dispositivos físicos separados (servidores, racks). Ofrece un SLA de durabilidad de 11 nueves (99.999999999 %) anual, protegiendo contra fallas de hardware individual (discos, servidores, racks) pero vulnerable a fallos de sitio completo (incendios, inundaciones). No garantiza Alta Disponibilidad (HA) multizona. **Ventajas**: Mínimo costo y máximo rendimiento (baja latencia por proximidad física, replicación síncrona garantiza consistencia inmediata). **Limitación crítica**: Sin protección contra falla de datacenter completo. Se contrasta con alternativas de mayor resiliencia: Zone-Redundant Storage (ZRS) y Geo-Redundant Storage (GRS). LRS es adecuado para datos no críticos, datos reconstituibles, entornos de desarrollo/prueba, o cuando se combina con estrategias de backup externas. Para datos críticos de producción se recomienda ZRS o GRS según requisitos de disponibilidad y RPO.

## 📌 Puntos Claves
- **Replicación**: 3 copias síncronas en un único datacenter
- **Distribución física**: Servidores y racks separados dentro del sitio
- **SLA durabilidad**: 11 nueves (99.999999999%) anual
- **Protección**: Fallas de hardware individual (discos, servidores, racks)
- **Vulnerabilidad**: Fallos de datacenter completo (incendios, inundaciones)
- **Ventajas**: Mínimo costo, máximo rendimiento, baja latencia, consistencia inmediata
- **Limitación**: Sin HA multizona, sin protección contra falla de sitio
- **Uso adecuado**: Datos no críticos, reconstituibles, dev/test, con backups externos
- **Alternativas**: ZRS (multizona) o GRS (multirregión) para producción crítica

## 🔗 Connections
- [[Almacenamiento redundante en zona (ZRS)]]
- [[Almacenamiento geo-redundante (GRS)]]
- [[Virtual Private Cloud (VPC)]]
- [[Disponibilidad de la aplicación]]
- [[Trade off en el diseño y arquitectura de software]]

## 💡 Personal Insight
LRS representa el trade-off fundamental en almacenamiento cloud: costo/rendimiento vs resiliencia. Las 3 réplicas síncronas dentro de un datacenter ofrecen protección suficiente contra fallas de hardware cotidianas (discos mueren, servidores fallan, racks pierden energía), pero el punto único de falla es el sitio completo. La replicación síncrona garantiza consistencia perfecta sin lag, crítico para workloads sensibles a consistencia. El rendimiento es óptimo: latencia mínima por proximidad física de réplicas. Pero la vulnerabilidad a desastres de sitio (incendios, inundaciones, cortes eléctricos masivos) lo hace inapropiado para datos críticos sin backups adicionales. LRS es perfecto para: caches (reconstituibles), entornos de desarrollo (tolerantes a pérdida), logs procesados (no críticos). Para producción crítica, el pequeño costo incremental de ZRS o GRS compra resiliencia exponencialmente mayor.

## 🧾 Recursos
