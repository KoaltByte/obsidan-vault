# SOC 
---
- Centro de operaciones de seguridad; núcleo encargado de monitorear, detectar, responder y prevenir incidentes de seguridad de una organización.
- Su objetivo principal es proteger los activos digitales, garantizar la continuidad del negocio y coordinar las acciones ante amenazas cibernéticas.

# Redes
---
- Una red conecta múltiples dispositivos que comparten información y recursos.
- Las redes varían de tamaño en función de la empresa.
- Su función principal es permitir una comunicación rápida y confiable mediante tecnologías como cableado, conexiones inalámbricas.
El SOC monitorea toda la actividad que sucede dentro de las redes.

## Redes corporativas
- Son redes que necesitan conectarse de manera global, para superar limitaciones geográficas.
- Los retos para este tipo redes globales es garantizar conexiones seguras y confiables, que permitan la transferencia sin interrupciones.
Las ``VPN's (Virtual Private Networks)`` Son utilizadas para unir redes que están en diferentes partes del mundo, creando conexiones seguras para el intercambio de información.
- Actualmente las empresas dependen de las redes para realizar sus operaciones diarias, una interrupción en la red resulta en perdida de la productividad, interrupción de servició y consecuencias económicas. 
Por lo anterior es importante mantener la red confiable y segura, así como tener planes de contingencia y monitoreo constante.

## Arquitectura cliente-servidor
- Diseñada para manejar una gran cantidad de clientes de manera simultánea. 
- Esta arquitectura permite:
	- Que los servidores centrales reciban, procesen y respondan solicitudes de múltiples clientes al mismo tiempo. 
	- Que haya flexibilidad y crecimiento, logrando una adaptación de la organización ante expansiones y entornos de red a gran escala.

# Modelo TCP/IP
---
- Base sobre la cual se diseñan y operan las redes de computadoras.
- Se compone de cuatro capas, cada una con funciones especificas que permiten la transmisión de datos del origen al destino.
- Cada capa tiene protocolos.

![Modelo TCP/IP|600](https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202022-01-26%20a%20la(s)%205.30.22%20p.m.-8d0a2556-7853-45b8-b910-7cc4aa4ab30f.jpg)

## 4. Aplicación
- Es la más cercana al usuario, sirve como interfaz entre las aplicaciones y la red.
- Define como los programas se comunican y establece las reglas de intercambio de información.
### Protocolos principales
- ``HTTP/HTTPS`` -> Navegación web segura.
- ``FTP`` -> Transferencia de archivos.
- ``SMTP`` -> Envió de correos electrónicos.
- ``DNS`` -> Resolución de nombres de dominio.

Cuando un usuario accede a www.google.com, el navegador utiliza:
1. DNS para traducir el nombre de dominio a una dirección IP.
2. HTTP/HTTPS para solicitar y recibir el contenido de la página web.
## 3. Transporte
- ==Garantiza la  comunicación== de extremo a extremo entre el dispositivo emisor y receptor.
- Administra el ==control de flujo==
- Realiza la segmentación de datos y la detección de errores.
### Protocolos
- ``TCP (Transmission Control Protocol)`` 
	- Confiable y orientado a la conexión.
	- Asegura que los datos lleguen completos y en el orden correcto.
	- Ejemplo: Navegar por un sitio web o descargar un archivo.
- ``UDP (User Datagram Protocol)
	- Más rápido que TCP pero sin control de errores.
	- Útil para transmisiones en tiempo real.
	- Ejemplo: Videollamadas.
- ``RTP (Real-Time Transport Protocol)
	- Optimizado para audio y vídeo en tiempo real.

Ejemplo práctico:
- ``TCP`` : Cuando se descarga un archivo desde un servidor FTP, TCP verifica que cada parte llegue correctamente antes de reconstruir el archivo, si una parte no llego se hace un reenvío. 
- ``UDP`` : En una  videollamada lo que importa es no tener retrasos por lo que si algunos paquetes se pierden, estos no se reenvían para evitar retrasos. 

## 2. Internet
- Encargada de direccionar y enrutar los paquetes a través de diferentes redes hasta llegar al destino.
### Protocolos
- ``IP (IPv4 /IPv6)`` -> Define y asigna las direcciones únicas para cada dispositivo en la red.
- ``ICMP`` ->Diagnostica y manda mensajes de error (comando ``ping``).
- ``ARP`` -> Traduce las direcciones IP a direcciones físicas ``(MAC)`` (Direccionamiento físico).
- ``RARP`` -> Hace una traducción inversa de MAC a IP.

Ejemplo práctico:
Cuando se hace ping a un servidor, ICMP se encarga de enviar los mensajes de prueba y recibir respuestas para verificar la conectividad.

## 1. Enlace o Acceso a la red
- Administra la conexión física entre dispositivos de la misma red.
- Controla el envió y la recepción de datos mediante la gestión de:
	- Encapsulación de la información en tramas.
	- Direccionamiento físico mediante MAC.
	- Detección de errores básicos en la transmisión.

Ejemplo:
- En una red domestica esta capa es la que maneja la comunicación entre la computadora y el router a través de Wi-Fi o cable.
- Cuando se envían datos a otro equipo dentro de la misma red, primero se usa la dirección MAC para asegurar que el paquete llegue de forma correcta. 

# Modelo OSI
---
El modelo OSI (Open System Interconnection) es un marco de referencia desarrollado por la ISO para entender y estandarizar la comunicación en las redes.

- Divide la comunicación en siete capas.
- Permite que diferentes dispositivos y tecnologías se comunique de manera organizada y compatible.
- Es esencial para:
	- Diseño eficiente y escalable de redes.
	- Desarrollo de protocolos de comunicación.
	- Solución de problemas de conectividad. 
![[OSI model.png | 500]]
# Tipos de redes
---
Las redes pueden tener diversas formas y estas se eligen en función de cada escenario, las necesidades especificas, factores como escalabilidad, tamaño y alcance geográfico. 
## PAN (Personal Area Network)
- Conecta dispositivos personales como telefónos, tables, PC.
- Alcance muy reducido (algunos metros).
- Conexión Bluetooth entre un celular y unos manos libres.
## LAN (Local Area Network)
- Conecta dispositivos dentro de un área pequeña como una casa u oficina.
- De uso común en redes de computadoras de empresas conectadas a un servidor central.
- Se implementa en empresas y redes domésticas.
## WLAN(Wireless Local Area Network)
- Similar a un LAN pero sin cables, utiliza Wi-Fi.
- Permite la movilidad dentro de un área determinada.
## MAN (Metropolitan Area Network)
- Cubre una mayor área geográfica como una ciudad entera. 
- Por ejemplo, la red de fibra óptica que conecta a las diferentes sedes de una empresa en la misma cd. 
## WAN (Wide Area Network)
- Es una red de gran alcance, puede cubrir países e incluso continentes.
- Internet es la red WAN más grande del mundo.
- La WAN es una red formada por varias LAN's
# Cliente / Servidor 
---
## Cliente
- Dispositivo o aplicación que ==solicita== servicios o recursos a un server.
- Puede ser una computadora, un celular o cualquier dispositivo conectado.
- Utiliza aplicaciones como navegadores web, clientes de e-mail o programas de transferencia de archivos. 
## Servidor
- Sistema que ==proporciona== los servicios, datos o recursos a múltiples clientes.
- Esta diseñado para manejar múltiples solicitudes de forma simultanea.
- Tipos:
	- Web server (páginas web)
	- Email server (correo electrónico)
	- File server (Archivos compartidos)
	- Database server (bases de datos)