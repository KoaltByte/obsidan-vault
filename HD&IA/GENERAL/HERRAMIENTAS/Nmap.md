# ¿Qué es Nmap?
---

**Nmap** (Network **Map**per) es una herramienta de código abierto para **descubrimiento y auditoría de redes**. Se usa para:

- **Descubrir hosts** activos en una red.
- **Detectar puertos abiertos** en esos hosts.
- **Identificar servicios** (qué servicio corre en cada puerto) y, muchas veces, su **versión**.
- **Detectar el sistema operativo** (fingerprinting).
- **Ejecutar scripts** para detectar vulnerabilidades, configuraciones erróneas o recopilar info adicional.

# ¿Qué hace (funciones principales)?
---

1. **Host discovery** — ¿qué máquinas están arriba? (`-sn`, ping scan).
2. **Port scanning** — ¿qué puertos están abiertos? (`-p`, `-sS`, `-sT`, etc.).
3. **Service/version detection** — ¿qué servicio/version corre en esos puertos? (`-sV`).
4. **OS detection** — inferir sistema operativo (`-O`).
5. **Scripting** — Nmap incluye **NSE (Nmap Scripting Engine)** para comprobaciones desde simples hasta exploits/diagnóstico (`--script`).
6. **Salida/reporting** — distintos formatos para guardar resultados (`-oN`, `-oX`, `-oA`).
# Comandos básicos y qué hacen
---

1. Escaneo básico de un host:
``` bash
nmap 192.168.1.10
```
Busca puertos comunes y muestra si están abiertos/filtrados/cerrados.

2. Ping scan (solo descubre hosts, no escanea puertos):
``` bash
nmap -sn 192.168.1.0/24
```
Lista qué IPs responden en la subred.

3. Escaneo SYN (rápido y “sigiloso” — requiere permisos y privilegios):
``` bash
sudo nmap -sS 192.168.1.10
```
Envía SYN, espera SYN/ACK. No completa la conexión (half-open).

4. Detección de servicios y versiones:
``` bash
sudo nmap -sV 192.168.1.10
```
Intenta identificar el servicio y la versión en cada puerto abierto.

5. Detección de SO:
``` bash
sudo nmap -O 192.168.1.10
```
Intenta identificar el sistema operativo mediante fingerprinting.

6. Escaneo por puertos específicos:
``` bash
nmap -p 22,80,443 192.168.1.10
```

7. Escaneo de todos los puertos (1–65535):
``` bash
sudo nmap -p- 192.168.1.10
```

8. Escaneo “agresivo” (combina varias detecciones y scripts):
``` bash
sudo nmap -A 192.168.1.10
```
Equivale a `-sV -O --traceroute --script=default` (útil, pero ruidoso).

9. Usar scripts NSE (ejemplo: búsqueda de vulnerabilidades web):
```bash
sudo nmap --script vuln 192.168.1.10
```

10. Guardar resultados en varios formatos:
``` bash
nmap -oA resultado_scan 192.168.1.10
```
Crea `resultado_scan.nmap` (texto), `resultado_scan.xml` y `resultado_scan.gnmap`.

11. Evitar que haga ping previo (si el host bloquea ICMP):
``` bash
nmap -Pn 192.168.1.10
```
Asume que el host está activo y procede a escanear puertos.

12. Ajustar velocidad/timing:
``` bash
nmap -T4 192.168.1.10
```
`-T0` (muy lento/stealth) a `-T5` (muy rápido/noisy).

---

# Ejemplo de salida (interpretación rápida)
---

Salida típica:

```
PORT    STATE SERVICE VERSION
22/tcp  open  ssh     OpenSSH 7.2p2
80/tcp  open  http    Apache httpd 2.4.29
443/tcp open  ssl/http
```

- `PORT`: puerto y protocolo.
- `STATE`: open (abierto), closed (cerrado), filtered (filtrado por firewall).
- `SERVICE`: servicio detectado (ssh, http).
- `VERSION`: si Nmap pudo identificar la versión.

# Buenas prácticas y seguridad
---

- **Escanea solo sistemas autorizados.** Escanear redes/hosts sin permiso puede ser ilegal.
- Usa `-Pn` y timing con cuidado en entornos productivos: puede provocar alertas o interrumpir servicios.
- Si estás en una red de laboratorio (p. ej. Metasploitable + Kali), perfecto para practicar.
- Registra y guarda los resultados para análisis posteriores.

# Instalación rápida (Linux)
---

En Debian/Ubuntu:

```
sudo apt update
sudo apt install nmap
```

En Windows puedes descargar el instalador desde la web oficial o usar el paquete de Nmap que incluye Zenmap (GUI).

---

# Casos de uso típicos
---
- Auditoría de seguridad / pentesting.
- Inventario de servicios en la red.
- Detección de dispositivos no autorizados.
- Diagnóstico cuando un servicio no responde.
- Preparar un plan de pruebas (saber qué versiones y puertos existen).
