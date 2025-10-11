---
Fecha de creación: 2025-10-11 14:02
Fecha de Modificación: 2025-10-11 11:15
tags:
Tema: Disponibilidad de la aplicación
---

## 📚 Idea/Concepto 
**Disponibilidad de la aplicación** es la capacidad del sistema para estar operativo y responder exitosamente cuando se necesita. Se mide bidimensionalmente: uptime (expresado en "nueves") y tasa de éxito (solicitudes exitosas / peticiones válidas). Se formaliza mediante SLAs/SLOs que establecen compromisos con el cliente. Las estrategias incluyen redundancia, resiliencia y recoverability (reduciendo MTTR), Automatización de Incidentes, y estrategias de mitigación. Su objetivo inverso es minimizar downtime y sus causas raíz. Se sustenta por Observabilidad (logging, métricas, traces) para detección inmediata de fallos, conectando con métricas de Site Reliability.

## 📌 Puntos Claves
- **Medición bidimensional**: Uptime ("nueves") + Tasa de éxito (requests exitosas/válidas)
- **Formalización**: SLAs (acuerdos) y SLOs (objetivos) con el cliente
- **Detección**: Observabilidad (logging, métricas, traces) para fallos inmediatos
- **Recuperación**: Resiliencia y Recoverability reduciendo MTTR
- **Automatización**: Incident response automatizado para cumplir SLAs
- **Causa raíz**: Minimizar downtime y sus causas mediante Site Reliability

## 🔗 Connections
- [[06_Despliegue e Infraestructura - Azure DevOps]]
- [[07_Mantenimiento - Monitoreo de Aplicación]]

## 💡 Personal Insight
La disponibilidad no es una métrica única sino un sistema integral donde uptime, tasa de éxito, observabilidad y recuperación rápida se entrelazan. Solo considerando todas las dimensiones se logra confiabilidad genuina que satisface compromisos con clientes.

## 🧾 Recursos