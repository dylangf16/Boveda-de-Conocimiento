---
Fecha de creación: 2025-11-30 12:30
Fecha de Modificación: 2025-11-30 14:20
tags:
Tema: Almacenamiento geo-redundante (GRS)
---

## 📚 Idea/Concepto 
**Geo-Redundant Storage (GRS)** replica datos a una región secundaria geográficamente distante (típicamente cientos de kilómetros) mediante replicación asíncrona. Protege contra fallas regionales completas (desastres naturales, cortes masivos) y es fundamental para estrategias de Disaster Recovery (DR). Es la estrategia predilecta para object storage a escala global (S3, Azure Blob Storage). **Características clave**: Replicación asíncrona (delay inherente resulta en RPO > 0, riesgo de pérdida de datos recientes); mantiene 3 réplicas en región primaria + 3 réplicas en región secundaria. Requiere failover manual o automatizado para activar región secundaria (RTO adicional) y necesita DNS geográfico (Traffic Manager, Route 53) para redirigir tráfico automáticamente. **Trade-offs**: Costos operativos continuos altos (ancho de banda y egress charges) y RPO > 0 (pérdida potencial de datos). Comparado con ZRS, GRS sacrifica consistencia inmediata por resiliencia geográfica. Para RPO=0 multirregional, existe GZRS (Geo-Zone-Redundant Storage) que combina ZRS en región primaria con replicación asíncrona a región secundaria.

## 📌 Puntos Claves
- **Replicación**: Asíncrona a región secundaria (cientos de kilómetros)
- **Protección**: Fallas regionales completas (desastres naturales, cortes masivos)
- **Configuración**: 3 réplicas región primaria + 3 réplicas región secundaria
- **RPO**: > 0 (delay asíncrono, riesgo pérdida de datos recientes)
- **Failover**: Manual o automatizado; requiere activación de región secundaria (RTO adicional)
- **DNS geográfico**: Traffic Manager/Route 53 para redirección automática
- **Trade-offs**: Costos altos (ancho de banda, egress), RPO no-cero
- **Uso principal**: Disaster Recovery, object storage global (S3, Blob Storage)
- **GZRS**: Variante con ZRS primario + GRS = RPO=0 regional + resiliencia geográfica

## 🔗 Connections
- [[Almacenamiento redundante localmente (LRS)]]
- [[Almacenamiento redundante en zona (ZRS)]]
- [[Cloud Híbrido (Hybrid Cloud)]]
- [[Public IP en el cloud]]
- [[Disponibilidad de la aplicación]]
- [[Trade off en el diseño y arquitectura de software]]

## 💡 Personal Insight
GRS representa la resiliencia máxima contra desastres catastróficos: replicar cientos de kilómetros asegura que ningún evento regional (terremotos, huracanes, apagones masivos) destruya todos los datos. Pero la replicación asíncrona introduce un trade-off fundamental: RPO > 0 significa que existe una ventana temporal donde datos escritos en región primaria aún no llegaron a secundaria, y si la primaria falla completamente en ese instante, esos datos se pierden irrecuperablemente. Los costos son significativos: ancho de banda continuo entre regiones y egress charges acumulan rápidamente a escala. El failover no es instantáneo: requiere detectar falla primaria, activar secundaria, y propagar cambios DNS, agregando minutos a RTO. GRS es indispensable para DR de datos críticos donde tolerancia a pérdida regional supera preocupación por RPO no-cero. Para workloads que requieren RPO=0 Y protección geográfica, GZRS es la solución: combina consistencia local (ZRS) con resiliencia regional (replicación asíncrona), aunque a costo premium.

## 🧾 Recursos
