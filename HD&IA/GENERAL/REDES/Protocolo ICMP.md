# Qué es?
---
- **ICMP (Internet Control Message Protocol)** es un protocolo de la capa de red usado por dispositivos (routers, hosts) para **informar errores y realizar diagnósticos** sobre la entrega de paquetes IP. No transporta datos de usuario como TCP/UDP — su objetivo es **señalizar** problemas y ayudar a herramientas de red (por ejemplo `ping` o `traceroute`).
- Opera **encima de IP** (es parte del conjunto TCP/IP). Para IPv4 se usa **ICMP**, y para IPv6 existe **ICMPv6** (que además incorpora funciones adicionales como descubrimiento de vecinos).
- Pertenece a la capa 3 del modelo OSI

# Propósito
---
- **Reportar errores**: p. ej. destino inalcanzable, tiempo de vida (TTL) excedido, fragmentación necesaria.
- **Diagnóstico**: p. ej. `Echo Request` / `Echo Reply` que usa `ping`.
- **Control de ruta**: redirigir tráfico (ICMP Redirect) o informar sobre MTU (Path MTU Discovery).
# Mensajes ICMP comunes
---
- **Echo Request (Type 8)** / **Echo Reply (Type 0)** → usado por `ping`.
- **Destination Unreachable (Type 3)** → indica que no se puede entregar el paquete (códigos: host unreachable, port unreachable, fragmentation needed, etc.).
- **Time Exceeded (Type 11)** → TTL llegó a 0 (útil para `traceroute`).
- **Redirect (Type 5)** → pide al host que cambie su ruta para esa red.
- **Fragmentation Needed (part of Destination Unreachable)** → informa sobre MTU para Path MTU Discovery.

# Ejemplos 
---
- `ping 8.8.8.8` → envía Echo Requests; si recibes Echo Replies, el host es reachable y puedes medir latencia.
- `traceroute ejemplo.com` → usa TTL incrementales; cuando cada salto responde con **Time Exceeded** revela la ruta.
# Limitaciones de seguridad
---
- **No es confiable para transportar datos** ni para establecer sesiones; es informativo.
- **Vulnerabilidades**: puede usarse en ataques (ICMP flood / ping flood, Smurf) o para reconocimiento.
- **Buenas prácticas de red**:
    - **Filtrar** o **rate-limit** ICMP en perímetros (firewall) según política: permitir tipos necesarios (p. ej. `Destination Unreachable`, `Time Exceeded`) y limitar Echo para diagnósticos.
    - No bloquear totalmente ICMP si necesitas Path MTU Discovery y diagnósticos — bloquearlo puede causar problemas de conectividad.