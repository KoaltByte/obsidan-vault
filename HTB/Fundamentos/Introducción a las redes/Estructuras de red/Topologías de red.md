- Una Topología de red es la d<mark style="background: #D2B3FFA6;">istribución física y lógica en la que se conectan los dispositivos</mark> en la red.
- En las topologías se incluyen componentes de red como switches, bridges y routers.
- Cada distribución tiene una función y asegura que todos los host puedan mantener una conexión lógica con los demás. 
- Las topologías determinan los componentes que se usan y los métodos de acceso a los medios de transmisión.
# Transmission medium layout
---
- Se refiere a la <mark style="background: #D2B3FFA6;">topología física de la red</mark>, que se utiliza para conectar dispositivos.
- En el caso de los medios conductores, se refiere al plan de cableado, la posición de cables y nodos, así como las conexiones entre nodos y el cableado.
# Logical topology
---
- Esta topología hace referencia a <mark style="background: #D2B3FFA6;">cómo actúan las señales en los medios de red</mark>, o como es que los datos se transmites a través de la red, desde un dispositivo hasta la conexión fisica con otros dispositivos. 

# Áreas de las topologías
---
## 1. Conexiones
![[Pasted image 20251020233326.png | 600]]

## Nodos - Controladores de interfaz de red (NIC)
![[Pasted image 20251020233422.png | 700]]
- Los nodos de red son los medios de transmisión o puntos de acceso, ya sean transmisores o receptores de señales.
- Un nodo puede estar conectado a una computadora, pero otros tienen solo un microcontrolador o no tienen dispositivo programable.

## Clasificación
- Podemos imaginar una topología como una forma virtual o `structure of a network`. Esta forma no se corresponde necesariamente con la disposición física real de los dispositivos en la red. Por lo tanto, estas topologías pueden ser `physical`o `logical`. Por ejemplo, las computadoras de una red `LAN`pueden estar dispuestas en círculo en una habitación, pero es muy improbable que tengan una topología de anillo real.
- Las topologías se dividen en ocho tipos básicos:
	1. Punto a punto
	2. Estrella
	3. Malla
	4. Hibrido
	5. Bus
	6. Anillo
	7. Árbol
	8. Cadena de margaritas
### Punto a punto
- La topología de red más simple, con una conexión dedicada entre dos hosts, es la `point-to-point`topología. En esta topología, solo existe un enlace físico directo entre dos dispositivos.
- Estos dos dispositivos pueden usar estas conexiones para comunicarse entre sí.
![[Pasted image 20251020233952.png | 400]]
### Bus 
- Todos los hosts están conectados mediante un medio de transmisión.
- Cada host tiene acceso al medio de transmisión y a las señales que se transmiten por él.
- <mark style="background: #D2B3FFA6;">No existe un componente de red central </mark>que controle los procesos.
- El medio de transmisión para esto puede ser, por ejemplo, un `coaxial`.
![[Pasted image 20251020234326.png | 500]]
### Estrella
- Mantiene una conexión con todos los hosts. 
- Cada host se conecta mediante un `Componente central de red` mediante un enlace independiente.
- Los componentes centrales suelen ser routers, switches o bridges, los cuales gestionan el forwarding funtion (La función de reenvío ) de los paquetes.
- Los componentes centrales reciben todos los paquetes de datos y los reenvían a su destino.
- El tráfico de datos en el componente central de la red puede ser muy alto, ya que todos los datos y conexiones pasan por él.
![[Pasted image 20251020234729.png | 550]]
### Anillo
- En esta topología cada host o nodo está conectado al anillo con dos cables:
	- Uno para las señales `incoming` (entrantes).
	- Uno para las señales `outgoing`  (salientes).
- Esto significa que un cable llega a cada host y otro sale.
- No suele requerir un componente de red activo.
- El <mark style="background: #D2B3FFA6;">control y el acceso al medio de transmisión se regulan mediante un protocolo</mark> al que se adhieren todas las estaciones.
- La información se transmite en una dirección de transmisión predeterminada. Normalmente, se accede al medio de transmisión secuencialmente de estación en estación mediante un sistema de recuperación desde la estación central o un `token`.
	- Un <mark style="background: #D2B3FFA6;">token </mark>es un patrón de bits que pasa continuamente por una red en anillo en una dirección, que funciona según el `claim token process` (Proceso de recuperación del toquen).
![[Pasted image 20251020235812.png | 500]]
### Malla
-  Aquí muchos nodos deciden sobre las conexiones físicas y el enrutamiento lógico, por lo tanto <mark style="background: #D2B3FFA6;">no se tiene una topología fija.</mark>
-   Existen dos estructuras básicas a partir del concepto básico:
	- `Fully meshed`: 
		- Cada host está conectado a todos los demás hosts de la red
		- Esta técnica se utiliza principalmente  en las `WAN` y `MAN` para garantizar una alta confiabilidad y un alto ancho de banda.
		- En esta configuración, nodos de red importantes, como enrutadores, podrían conectarse en red. Si un enrutador falla, los demás pueden seguir funcionando sin problemas y la red puede absorber la falla gracias a la gran cantidad de conexiones.
		- Cada nodo de una topología completamente en malla tiene las mismas funciones de enrutamiento y conoce los nodos vecinos con los que puede comunicarse en función de su proximidad a la puerta de enlace de la red y las cargas de tráfico.
	- `Partially meshed`:
		- Los puntos finales están conectados mediante una sola conexión.
		-  En este tipo de topología de red, algunos nodos se conectan a un solo nodo, y otros a dos o más mediante una conexión punto a punto.
![[Pasted image 20251021000409.png | 500]]
### Árbol
- Es es una topología de estrella extendida que las redes locales más extensas tienen en esta estructura.
- Esta topología se utiliza a menudo, por ejemplo, en grandes edificios empresariales.
- Existen tanto estructuras de árbol lógicas según el árbol de expansión (`spanning tree`) como físicas.
- Las redes modulares modernas, basadas en cableado estructurado con una jerarquía de concentradores, también tienen una estructura de árbol.
![[Pasted image 20251021000701.png | 500]]
### Híbrido
- Aquí se combinan dos o más topologías, de modo que la red resultante no presenta topologías estándar. Por ejemplo, una red de árbol puede representar una topología híbrida en la que las redes en estrella se conectan mediante redes de bus interconectadas.
- Una topología híbrida siempre se crea cuando <mark style="background: #D2B3FFA6;">dos diferentes</mark> topologías se interconectan topologías de red básicas.
![[Pasted image 20251021000909.png | 500]]
### Cadena de margaritas
- Varios hosts se conectan colocando un cable de un nodo a otro.
- Dado que esto crea una cadena de conexiones, también se conoce como configuración en cadena, en la que varios componentes de hardware se conectan en serie.
- La conexión en cadena se basa en la disposición física de los nodos, a diferencia de los procedimientos de token, que son estructurales pero pueden independizarse de la disposición física.
-  La señal se envía hacia y desde un componente al sistema informático a través de sus nodos anteriores.
![[Pasted image 20251021001050.png | 500]]

