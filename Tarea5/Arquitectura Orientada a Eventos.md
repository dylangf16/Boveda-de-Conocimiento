---
Fecha de creación: 2025-11-09 13:52
Fecha de Modificación: 2025-11-09 14:18
tags:
Tema: Arquitectura Orientada a Eventos
---

## 📚 Idea/Concepto 
**Arquitectura Orientada a Eventos (EDA)** es un estilo de arquitectura asíncrona distribuida donde los componentes (productores y consumidores) reaccionan a **eventos** (declaraciones inmutables de hechos pasados), distinguiéndose de **comandos** (solicitudes de acción futura), sin invocación directa, materializando el principio de Bajo Acoplamiento. La comunicación se gestiona mediante un Event Backbone o broker intermediario. Existen dos topologías: modelo con Mediador/Orquestador (controla flujo) y modelo con Broker (broadcast sin control central). El registro (log) de eventos proporciona reproducibilidad, historia del stream y, en **Event Sourcing**, actúa como fuente de verdad para reconstruir estado. Los consumidores deben diseñarse con **idempotencia** para gestionar duplicación de mensajes. El desacoplamiento habilita alta escalabilidad, pero introduce **Consistencia Eventual** y requiere **Transacciones Compensatorias** para coordinación distribuida.

## 📌 Puntos Claves
- **Naturaleza**: Arquitectura asíncrona distribuida con comunicación indirecta
- **Eventos vs Comandos**: Hechos pasados inmutables vs. solicitudes futuras
- **Desacoplamiento**: Sin invocación directa, materializando Bajo Acoplamiento
- **Topologías**: Mediador/Orquestador (control centralizado) vs. Broker (broadcast descentralizado)
- **Event Log**: Reproducibilidad, historia del stream, fuente de verdad (Event Sourcing)
- **Idempotencia**: Requerida en consumidores para manejar duplicación segura
- **Trade-offs**: Alta escalabilidad vs. Consistencia Eventual y Transacciones Compensatorias

## 🔗 Connections
- [[03_Arquitectura y Diseño - Microservicios]]
- [[Broker en arquitecturas Event Driven]]
- [[Acoplamiento en desarrollo de software]]
- [[Trade off en el diseño y arquitectura de software]]

## 💡 Personal Insight
EDA representa un cambio paradigmático: de invocaciones síncronas acopladas a reacciones asíncronas desacopladas. La distinción entre eventos (hechos inmutables) y comandos (intenciones futuras) no es semántica sino arquitectónica fundamental. El Event Log transforma el sistema de estado mutable a historia inmutable reproducible, pero el precio es aceptar Consistencia Eventual y diseñar con idempotencia desde el inicio. Es arquitectura para sistemas que priorizan escalabilidad y resiliencia sobre consistencia inmediata.

## 🧾 Recursos
