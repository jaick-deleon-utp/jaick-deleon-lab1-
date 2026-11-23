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

### 1. Verificación de conectividad
Se asignaron direcciones IP estáticas y se comprobó la comunicación entre
PC1 (192.168.1.10) y PC2 (192.168.1.11) mediante el comando `ping`:

​```
C:\> ping 192.168.1.11

Pinging 192.168.1.11 with 32 bytes of data:
Reply from 192.168.1.11: bytes=32 time<1ms TTL=128
Reply from 192.168.1.11: bytes=32 time<1ms TTL=128
Reply from 192.168.1.11: bytes=32 time<1ms TTL=128
Reply from 192.168.1.11: bytes=32 time<1ms TTL=128

Ping statistics for 192.168.1.11:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss)
​```

### 2. Análisis de tráfico
| Protocolo | Filtro usado | Observación |
|-----------|--------------|-------------|
| ARP  | `arp`  | PC1 envió una solicitud broadcast para descubrir la MAC de PC2, y PC2 respondió con su dirección MAC. |
| ICMP | `icmp` | Se observaron 4 pares de paquetes Echo Request / Echo Reply correspondientes al ping. |
| TCP  | `tcp`  | Se identificó el establecimiento de conexión (SYN, SYN-ACK, ACK). |

📸 Evidencia: `img/wireshark.png`

### 3. Hallazgos
- La comunicación en la red local funcionó sin pérdida de paquetes (0 %).
- ARP siempre precede al primer ICMP, porque el host necesita conocer la MAC destino.
- El tráfico sin cifrar es visible para quien capture en la red, lo que muestra
  por qué importa proteger las comunicaciones.

## 🧠 Conclusiones

Este laboratorio me permitió comprender cómo se comunican dos dispositivos en una
red local y cómo se puede observar ese proceso paquete por paquete. Aprendí que
una verificación de conectividad tan simple como un `ping` involucra varios
protocolos (ARP e ICMP) trabajando en conjunto.

También entendí que el análisis de paquetes es una habilidad base en
ciberseguridad: permite diagnosticar fallas, detectar tráfico anómalo y
reconocer qué información viaja expuesta en una red. Además, documentar el
laboratorio en GitHub me ayudó a practicar el control de versiones y a construir
un registro verificable de mi aprendizaje.

**Próximos pasos:** ampliar la topología con VLANs, aplicar listas de control de
acceso (ACL) y analizar protocolos como DNS y HTTP.
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
