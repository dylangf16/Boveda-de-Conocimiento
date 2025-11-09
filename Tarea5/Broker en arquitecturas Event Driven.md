---
Fecha de creación: 2025-11-09 14:05
Fecha de Modificación: 2025-11-09 14:27
tags:
Tema: Broker en arquitecturas Event Driven
---

## 📚 Idea/Concepto 
**Broker** es el componente intermediario (middleware) en la topología Broker de EDA que materializa el principio de **Bajo Acoplamiento** gestionando distribución descentralizada de **eventos** (declaraciones inmutables de hechos pasados), diferenciados de **comandos** (solicitudes de acción futura), mediante broadcast simple sin coordinación central. Opera como light broker habilitando comunicación publicar/suscribir (pub/sub) entre productores y consumidores. Gestiona persistencia potencialmente permanente en el **Event Log**, diferenciándose de mensajería transitoria, permitiendo reproducibilidad y proporcionando historia del stream. La reproducibilidad del Event Log exige que los consumidores implementen **idempotencia** para manejar duplicación segura. Esta topología se elige para flujos simples sin orquestación central, acepta **Consistencia Eventual** como trade-off del desacoplamiento, y requiere **Transacciones Compensatorias** para coordinación distribuida.

## 📌 Puntos Claves
- **Rol**: Middleware intermediario en topología Broker de EDA
- **Función**: Distribución descentralizada mediante broadcast sin coordinación central
- **Patrón**: Publicar/Suscribir (pub/sub) entre productores y consumidores
- **Event Log**: Persistencia permanente para reproducibilidad e historia del stream
- **Idempotencia**: Requerida en consumidores por reproducibilidad del log
- **Escenario**: Flujos simples sin orquestación central
- **Trade-offs**: Consistencia Eventual y Transacciones Compensatorias necesarias

## 🔗 Connections
- [[Arquitectura Orientada a Eventos]]
- [[Acoplamiento en desarrollo de software]]
- [[Trade off en el diseño y arquitectura de software]]
- [[03_Arquitectura y Diseño - Microservicios]]

## 💡 Personal Insight
El Broker no es simplemente un bus de mensajes sino una infraestructura fundamental que habilita desacoplamiento temporal y espacial mediante persistencia del Event Log. La distinción con mensajería transitoria es crítica: no es comunicación efímera sino historia permanente reproducible. Esto transforma requisitos: los consumidores deben ser idempotentes por diseño, no por conveniencia. La topología Broker sacrifica orquestación centralizada por simplicidad y escalabilidad, aceptando conscientemente Consistencia Eventual como precio del desacoplamiento radical.

## 🧾 Recursos
