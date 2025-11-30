---
Fecha de creación: 2025-11-30 10:00
Fecha de Modificación: 2025-11-30 11:45
tags:
Tema: Escalamiento horizontal y vertical en el cloud
---

## 📚 Idea/Concepto 
**Escalamiento Vertical (scaling up)** aumenta la capacidad de una sola instancia agregando CPU/RAM mediante ajuste de VM, pero tiene límites físicos y costo prohibitivo en niveles altos. **Escalamiento Horizontal (scaling out)** agrega múltiples instancias para distribuir carga, habilitado por virtualización que permite réplica rápida de VMs, requiriendo Load Balancer (L4) o Application Gateway (L7) para distribución eficiente del tráfico. El horizontal proporciona alta disponibilidad y elasticidad, pero introduce sobrecarga operativa (OpEx) por complejidad de orquestación de clústeres distribuidos. Requiere arquitecturas stateless o almacenamiento compartido externo (Redis); alternativamente, session affinity en L7 puede simplificar temporalmente el manejo de estado. Para bases de datos, se implementa mediante replicación (read replicas) o sharding. El cloud ofrece autoscaling nativo en servicios PaaS (App Services) y FaaS, permitiendo aprovisionamiento/desaprovisionamiento dinámico basado en métricas (CPU, memoria, solicitudes). El horizontal es más costo-eficiente y resiliente, siendo la estrategia preferida en arquitecturas cloud nativas.

## 📌 Puntos Claves
- **Vertical (scaling up)**: Aumentar CPU/RAM de instancia única; límites físicos y costos altos
- **Horizontal (scaling out)**: Agregar instancias múltiples; requiere Load Balancer/Application Gateway
- **Trade-off**: Horizontal ofrece HA y elasticidad pero aumenta OpEx por complejidad
- **Requisito arquitectónico**: Aplicaciones stateless o almacenamiento compartido (Redis)
- **Alternativa temporal**: Session affinity en L7 para manejo de estado
- **Bases de datos**: Read replicas para lectura, sharding para escritura
- **Autoscaling nativo**: PaaS y FaaS proveen elasticidad automática basada en métricas
- **Estrategia preferida**: Horizontal por costo-eficiencia y resiliencia

## 🔗 Connections
- [[Virtual Private Cloud (VPC)]]
- [[IaaS vs PaaS vs SaaS]]
- [[Arquitectura Microkernel]]
- [[Arquitectura Orientada a Eventos]]
- [[Disponibilidad de la aplicación]]

## 💡 Personal Insight
El escalamiento horizontal vs vertical representa la diferencia entre pensamiento monolítico y distribuido. Vertical es intuitivo pero fundamentalmente limitado: eventualmente alcanzas el hardware más potente disponible y los costos se vuelven exponenciales. Horizontal requiere un cambio mental: aceptar que múltiples instancias débiles superan una instancia fuerte, pero esto exige arquitecturas stateless o externalización de estado. El autoscaling nativo en PaaS/FaaS no es solo conveniencia operativa sino ventaja económica fundamental: pagas solo por capacidad activamente utilizada, convirtiendo CapEx fijo en OpEx variable que sigue la demanda. La preferencia por horizontal no es dogma sino matemática: mejor costo, mejor resiliencia (fault tolerance), mejor elasticidad.

## 🧾 Recursos
