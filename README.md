🌐 Proyecto de Interconexión Multi-Protocolo (RIP, OSPF, BGP e IPv6 Tunneling)
📌 Descripción General

Este proyecto simula una arquitectura de red empresarial distribuida, compuesta por múltiples sistemas autónomos (AS) interconectados mediante BGP, y redes internas que utilizan RIP y OSPF como protocolos de enrutamiento dinámico.

Además, se implementa tunelización IPv6 sobre infraestructura IPv4, permitiendo conectividad extremo a extremo entre redes IPv6 ubicadas en diferentes dominios.

El diseño fue desarrollado en Cisco Packet Tracer utilizando routers ISR4331, switches 2960 y servidores para servicios DNS y Web.

🏗️ Arquitectura del Proyecto

La topología está dividida en tres dominios principales:

🔶 1️⃣ Dominio RIP (AS 100)

Protocolo: RIP v2

Redes internas:

1.0.0.0

2.0.0.0

3.0.0.0

4.0.0.0

5.0.0.0

6.0.0.0

7.0.0.0

8.0.0.0

Conectividad IPv4 hacia otros AS mediante BGP

Implementación de red IPv6:

1000:a::/64

1000:b::/64

1000:c::/64

Tunelización IPv6 hacia el dominio OSPF

🟢 2️⃣ Dominio BGP (Backbone – AS 200, 300, 400)

Protocolo: BGP

AS implementados:

AS 100 (RIP)

AS 200

AS 300

AS 400

AS 500 (OSPF)

Redes del backbone:

9.0.0.0

10.0.0.0

11.0.0.0

12.0.0.0

13.0.0.0

Servidores:

www.toyota.com

www.nissan.com

DNS IPv4

El backbone actúa como proveedor de tránsito entre los dominios RIP y OSPF.

🔵 3️⃣ Dominio OSPF (AS 500)

Protocolo: OSPFv2

Redes internas:

14.0.0.0

15.0.0.0

16.0.0.0

17.0.0.0

18.0.0.0

19.0.0.0

20.0.0.0

21.0.0.0

Redes IPv6:

2000:a::/64

2000:b::/64

2000:c::/64

2000:d::/64

Servidores:

DNS IPv6

www.susuki.com

Este dominio mantiene conectividad completa con el backbone mediante BGP.

🌍 Segmentación de Red

Cada segmento de red está claramente identificado en el diagrama con su respectiva dirección IP (IPv4 o IPv6).
La segmentación incluye:

Redes LAN para usuarios finales

Redes de tránsito entre routers

Redes internas por protocolo

Segmentos IPv6 independientes

Enlaces de interconexión entre AS

🔄 Tunelización IPv6

Se implementó túnel IPv6 sobre IPv4 para permitir comunicación entre:

Red IPv6 del dominio RIP (1000::/64)

Red IPv6 del dominio OSPF (2000::/64)

Características:

Encapsulamiento IPv6 en IPv4

Conectividad extremo a extremo entre hosts IPv6

Uso de infraestructura IPv4 existente como red de transporte

Esto permite interoperabilidad entre redes IPv6 separadas geográficamente.

🖥️ Servicios Implementados

🌐 Servidores Web accesibles entre dominios

🧭 DNS IPv4

🧭 DNS IPv6

Resolución de nombres entre dominios

Comunicación inter-AS funcional

🔀 Protocolos Utilizados
Protocolo	Función
RIP v2	Enrutamiento interno en AS 100
OSPF	Enrutamiento interno en AS 500
BGP	Interconexión entre sistemas autónomos
IPv6	Direccionamiento moderno
Túnel IPv6 sobre IPv4	Conectividad entre dominios IPv6
🎯 Objetivos del Proyecto

Implementar una arquitectura multi-AS

Integrar múltiples protocolos de enrutamiento

Configurar BGP entre dominios

Implementar IPv6 en redes separadas

Configurar tunelización IPv6 sobre IPv4

Garantizar conectividad extremo a extremo

Integrar servicios DNS y Web

🧪 Pruebas Realizadas

✔️ Ping entre redes IPv4 de distintos AS

✔️ Resolución DNS entre dominios

✔️ Acceso a servidores web remotos

✔️ Comunicación IPv6 a través del túnel

✔️ Verificación de tablas de enrutamiento (RIP, OSPF y BGP)

🛠️ Tecnologías Utilizadas

Cisco Packet Tracer

Routers Cisco ISR4331

Switches Cisco 2960

Enrutamiento dinámico

BGP multi-AS

IPv6 + Tunelización