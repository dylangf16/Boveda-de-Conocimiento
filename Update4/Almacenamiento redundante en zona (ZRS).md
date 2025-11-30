---
Fecha de creación: 2025-11-30 12:00
Fecha de Modificación: 2025-11-30 13:45
tags:
Tema: Almacenamiento redundante en zona (ZRS)
---

## 📚 Idea/Concepto 
**Zone-Redundant Storage (ZRS)** replica datos sincrónicamente en tres zonas de disponibilidad (Availability Zones) separadas físicamente (típicamente 5-25 km) dentro de la misma región. Cada zona es un datacenter con infraestructura independiente (energía, refrigeración, red), protegiendo contra fallas de zona completa. Ofrece SLA de durabilidad de 11 nueves (99.999999999 %) anual. **Características clave**: Replicación síncrona (garantiza consistencia inmediata y RPO=0), SLA de disponibilidad superior (típicamente 99.99% o superior) y habilita Alta Disponibilidad (HA) multizona dentro de la región. **Trade-offs**: Latencia de escritura ligeramente mayor que LRS por confirmación síncrona en sitios separados y costo incremental mayor que LRS por distribución geográfica y tráfico de red continuo inter-zona. **Requisitos arquitectónicos**: Las aplicaciones deben configurar Load Balancers zone-aware o múltiples endpoints de red para failover automático a AZ diferente en caso de falla de zona activa. ZRS es ideal para aplicaciones críticas de producción que requieren HA regional con RPO=0 y pueden tolerar latencia de escritura ligeramente mayor.

## 📌 Puntos Claves
- **Replicación**: 3 copias síncronas en 3 Availability Zones (5-25 km separación)
- **Infraestructura**: Cada AZ es datacenter independiente (energía, refrigeración, red)
- **Protección**: Fallas de zona completa (datacenter individual)
- **SLA durabilidad**: 11 nueves (99.999999999%) anual
- **Consistencia**: Síncrona, RPO=0 (sin pérdida de datos)
- **Disponibilidad**: SLA típicamente 99.99%+ (HA multizona regional)
- **Trade-offs**: Latencia escritura mayor que LRS; costo incremental por distribución/tráfico
- **Requisito arquitectónico**: Load Balancers zone-aware o múltiples endpoints para failover automático
- **Uso ideal**: Aplicaciones críticas de producción con requisito de HA regional y RPO=0

## 🔗 Connections
- [[Almacenamiento redundante localmente (LRS)]]
- [[Almacenamiento geo-redundante (GRS)]]
- [[Escalamiento horizontal y vertical en el cloud]]
- [[Disponibilidad de la aplicación]]
- [[Trade off en el diseño y arquitectura de software]]

## 💡 Personal Insight
ZRS es el punto óptimo para aplicaciones críticas de producción que operan dentro de una región: elimina el punto único de falla de LRS (datacenter completo) sin el RPO no-cero de GRS. La replicación síncrona a través de Availability Zones (datacenters físicamente separados con infraestructura independiente) garantiza que ningún desastre localizado cause pérdida de datos. El RPO=0 es garantía matemática: todas las escrituras confirman solo después de replicarse a las 3 zonas. El trade-off de latencia es inevitable: confirmar escrituras a través de distancias de 5-25 km introduce microsegundos adicionales comparado con LRS, pero esto es imperceptible para la mayoría de aplicaciones. El requisito de Load Balancers zone-aware no es complejidad gratuita sino necesidad arquitectónica: sin failover automático entre zonas, ZRS solo protege datos pero no disponibilidad de acceso. Para workloads críticos regionales, ZRS es la elección correcta: mejor que LRS en resiliencia, mejor que GRS en consistencia.

## 🧾 Recursos
