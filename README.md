# 🔬 Laboratorio 1: Simulación de Redes Seguras

![Licencia](https://img.shields.io/badge/Licencia-MIT-green)
![Institución](https://img.shields.io/badge/UTP-FISC-purple)
![Estado](https://img.shields.io/badge/Estado-En%20desarrollo-yellow)

## 📌 Propósito
Simular una red local en Cisco Packet Tracer y capturar tráfico con Wireshark
para identificar protocolos (ARP, ICMP, TCP, DNS) y comprender los fundamentos
del análisis de paquetes en ciberseguridad.

## 🎓 Información académica
- **Universidad:** Universidad Tecnológica de Panamá (UTP) - FISC
- **Asignatura:** Sistemas Colaborativos
- **Facilitadora:** Hilda L. Quirós M.
- **Estudiante:** [Nombre del Estudiante]
- **Año:** 2026

## 🗺️ Topología
![Topología de red](img/topologia.png)

| Dispositivo | Interfaz | Dirección IP    | Máscara       |
|-------------|----------|-----------------|---------------|
| Router R1   | G0/0     | 192.168.1.1     | 255.255.255.0 |
| Switch SW1  | VLAN 1   | 192.168.1.2     | 255.255.255.0 |
| PC1         | NIC      | 192.168.1.10    | 255.255.255.0 |
| PC2         | NIC      | 192.168.1.11    | 255.255.255.0 |

## 🛠️ Herramientas utilizadas
- Cisco Packet Tracer
- Wireshark
- Git y GitHub

## 📋 Procedimiento
1. Construir la topología en Packet Tracer según el diagrama.
2. Asignar direcciones IP estáticas a cada dispositivo.
3. Verificar conectividad con `ping` entre PC1 y PC2.
4. Iniciar la captura en Wireshark sobre la interfaz correspondiente.
5. Filtrar y analizar paquetes (`icmp`, `arp`, `tcp`).
6. Documentar hallazgos y capturas de pantalla.

## 📊 Resultados
- Conectividad exitosa entre dispositivos (captura en `img/ping.png`).
- Identificación de tramas ARP e ICMP (captura en `img/wireshark.png`).

## 🧠 Conclusiones
[Escribe 2 o 3 líneas sobre lo que aprendiste.]

## 📁 Estructura del repositorio
​```
utp-redes-lab1/
├── img/            # Capturas y diagramas
├── docs/           # Informe o notas
├── LICENSE
├── .gitignore
└── README.md
​```

## 📄 Licencia
Distribuido bajo licencia MIT

## 📬 Contacto
- LinkedIn: https://www.linkedin.com/in/jaick-de-león-942550451?utm_source=share_via&utm_content=profile&utm_medium=member_android
- Correo: jaick.deleon@utp.ac.pa
