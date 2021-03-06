## Nivel enlace de datos

- En el **modelo OSI** es nivel 2
- En el **modelo TCP** es nivel acceso a la red

### Funciones
- Permitir que las capas superiores accedan a los medios
- Aceptar paquetes de nivel 2 y empaquetarlos en frames
- Preparación de datos de red para el nivel físico
- Controlar cómo se colocan y reciben los medios
- Intercambio de frames entre nodos de un medio

### Servicios

- Entramado (aka. frames)
- Acceso al enlace usando MAC Access
- Entrega confiable
- Control de flujo
- Detección de errores
- Corrección de errores

### Half-duplex (HDX)

- Ambos datos pueden transmitir y recibir datos pero no al mismo tiempo.
- Usado en **topologías bus** de Ethernet anteriores y en **WLAN**

### Half-duplex (HDX)

- Ambos datos pueden transmitir y recibir datos pero no al mismo tiempo.
- Usado en **topologías bus** de Ethernet anteriores y en **WLAN**

### Full-duplex (FDX)

- Ambos dispositivos pueden transmitir y recibir en el mismo medio al **mismo tiempo**.
- Los switches operan en **FDX** pero podrían operar en **HDX** si se conectan a un **HUB**

### Logical Link Control (LLC)

- Se comunica con el nivel 3 y encapsula dichos niveles
- Está estandarizado por el **IEEE 802.2**

### Media Access Control (MAC)

- Define los procesos que accesan al medio
- Tiene diferentes estándares, dependiendo del medio.
  - **Ethernet**: IEEE 802.3
  - **Token ring**: IEEE 802.5
  - **Wifi**: IEEE 802.11
  - **Bluetooth**: IEEE 802.15
- Los protocolos de nivel 2 especifican la encapsulación del frame

### Topologías físicas 
- WAN
  - Punto a punto
  - Hub and Spoke (Estrella)
  - (Mesh) Malla
- LAN
  - Estrella
  - Estrella extendida
  - Bus
  - Anillo

### CSMA/CD (Carrier Sense Multiple Access / Collision Detection)

- Usadas por ethernet hubs y anteriores basadas en topología bus
- Funciona con **HDX**
- Inspirado en ALOHANet
- Si llega a haber colisiones los hosts esperan un tiempo, para volver a enviar datos

### CSMA/CA (Carrier Sense Multiple Access / Collision Avoidance)

- Se usa en las WLANs estandarizadas por IEEE 802.11
- No tiene como objetivo detectar colisiones, sino evitarlas. Para esto, espera un tiempo antes que de intentar transmitir nuevamente la información.

### Estructura de trama de Ethernet

- Dirección fuente (6 bytes)
- Dirección destino (6 bytes)
- Campo de tipo (2 bytes)
- Comprobación de Redundancia Cíclica (CRC) (4 bytes). Detecta errores
- Preámbulo (8 bytes). Puras A's y al final una B

### Técnicas de detección de errores

- Comprobación de paridad
- Forward Error Correction
- CRC

### Protocolo IEEE 802.1Q

- Es el protocolo utilizado para crear redes virtuales
- Estrucutura
  - Pri (3 **bits**)
  - CFI (1 **bit**)
  - ID (3 **nibbles**)
  - Type (2 **bytes**)