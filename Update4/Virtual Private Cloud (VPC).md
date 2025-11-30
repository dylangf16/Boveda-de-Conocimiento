---
Fecha de creación: 2025-11-30 09:15
Fecha de Modificación: 2025-11-30 10:30
tags:
Tema: Virtual Private Cloud (VPC)
---

## 📚 Idea/Concepto 
**Virtual Private Cloud (VPC)** es una red virtual lógicamente aislada dentro de la infraestructura cloud, donde se definen espacios de direccionamiento IP privados, subredes y enrutamiento personalizado. El filtrado de tráfico se gestiona mediante Network Security Groups (NSG) a nivel de subred/interfaz y Application Security Groups (ASG) para segmentación por roles de carga de trabajo. La VPC habilita arquitecturas híbridas conectando recursos cloud con infraestructura On-Premise mediante VPN Gateway o conexiones dedicadas, y está limitada a una región geográfica; para multiregión se requiere VNet Peering o VPN Gateway. Integra servicios PaaS de forma segura mediante Private Endpoints, eliminando exposición pública. La distribución de tráfico se implementa con Load Balancer (Capa 4, TCP/UDP) o Application Gateway (Capa 7, HTTP/HTTPS con terminación SSL). La conectividad saliente a Internet se controla mediante NAT Gateway e IPs públicas estáticas/dinámicas. Es fundamental para aislamiento de seguridad, control granular de conectividad y extensión de la red corporativa hacia la nube.

## 📌 Puntos Claves
- **Definición**: Red virtual lógicamente aislada con direccionamiento IP privado personalizado
- **Segmentación de red**: Subredes para organización lógica de recursos
- **Control de tráfico**: NSG (nivel subred/interfaz) y ASG (segmentación por roles)
- **Conectividad híbrida**: VPN Gateway o conexiones dedicadas a On-Premise
- **Limitación geográfica**: Confinada a una región; multiregión requiere VNet Peering/VPN
- **Integración PaaS**: Private Endpoints para servicios sin exposición pública
- **Distribución de tráfico**: Load Balancer (L4) o Application Gateway (L7 con SSL)
- **Conectividad saliente**: NAT Gateway con IPs públicas estáticas/dinámicas

## 🔗 Connections
- [[Cloud Híbrido (Hybrid Cloud)]]
- [[Public IP en el cloud]]
- [[IaaS vs PaaS vs SaaS]]
- [[Arquitectura Microkernel]]
- [[Arquitectura Orientada a Eventos]]

## 💡 Personal Insight
La VPC es el fundamento arquitectónico que transforma el cloud de un espacio público compartido a una extensión segura de la red corporativa. La capacidad de definir topologías de red personalizadas con control granular mediante NSG y ASG es lo que permite implementar arquitecturas zero-trust en la nube. Los Private Endpoints representan un cambio paradigmático: eliminan la necesidad de exponer servicios PaaS públicamente, cerrando vectores de ataque mientras mantienen la conveniencia del cloud. La conectividad híbrida no es solo una característica técnica, sino el puente que permite migraciones graduales y arquitecturas distribuidas que respetan restricciones regulatorias sin sacrificar elasticidad.

## 🧾 Recursos
