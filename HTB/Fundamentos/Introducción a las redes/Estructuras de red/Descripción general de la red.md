- Una red permite que dos computadoras se comuniquen entre sí. Existe una amplia gama de redes `topologias`(malla, árbol, estrella). 
- La mayoría de las redes usan una máscara `/24` de subred, tanto que muchos evaluadores de penetración configuran esta máscara de subred <mark style="background: #D2B3FFA6;">(255.255.255.0)</mark> sin comprobarlo. La red <mark style="background: #D2B3FFA6;">/24 permite que los ordenadores se comuniquen entre sí siempre que los tres primeros octetos de una dirección IP sean iguales (p. ej., 192.168.1.xxx)</mark>.

# Internet
---
- Internet se basa en muchas redes subdivididas, como se muestra en el ejemplo y marcadas como " `Home Network`" y " `Company Network`" .

![[Pasted image 20251020222215.png | 600]]
## Aspectos a considerar para el diagrama 
1. El servidor web debe estar en una [[DMZ Zona Desmilitarizada]], ya que los clientes en internet pueden iniciar comunicaciones con el sitio web, lo que aumenta su probabilidad de ser comprometido. Al ubicarlo en una <mark style="background: #D2B3FFA6;">red independiente</mark>, los administradores pueden implementar protecciones de red entre el servidor web y otros dispositivos.
2. Las estaciones de trabajo deberían estar en su propia red y, idealmente, <mark style="background: #D2B3FFA6;">cada estación debería tener una regla de firewall basada en host</mark> que le impida comunicarse con otras estaciones de trabajo. Si una estación de trabajo está en la misma red que un servidor, los ataques de red `spoofing`se `man in the middle`convierten en un problema mucho mayor.
3. El <mark style="background: #D2B3FFA6;">conmutador y el enrutador deben estar en una "Red de Administración".</mark> Esto evita que las estaciones de trabajo interfieran en la comunicación entre estos dispositivos.
4.  <mark style="background: #D2B3FFA6;">Los teléfonos IP deben estar en su propia red</mark>. Por razones de seguridad, esto evita que las computadoras puedan interceptar la comunicación. Además de la seguridad, los teléfonos son únicos en el sentido de que la latencia/retardo es significativo. Al ubicarlos en su propia red, los administradores de red pueden priorizar su tráfico para evitar una latencia alta con mayor facilidad.
5. Las <mark style="background: #D2B3FFA6;">impresoras deberían estar en su propia red</mark>. Puede parecer extraño, pero es prácticamente imposible proteger una impresora.


Imaginemos que queremos visitar el sitio web de una empresa desde nuestro " " `Home Network`. En ese caso, intercambiamos datos con el sitio web de la empresa ubicado en su " " `Company Network`. Al igual que al enviar correo o paquetes, conocemos la dirección a la que deben dirigirse. La <mark style="background: #D2B3FFA6;">dirección del sitio web o Uniform Resource Locator( URL)</mark> que introducimos en nuestro navegador también se conoce como <mark style="background: #D2B3FFA6;">Fully Qualified Domain Name( FQDN).</mark>

## URL vs FQDN
- FQDN: Sólo especifica la dirección ("El edificio"). 
> [!example] 
>  www.hackthebox.eu
- URL: Además de especificar el "Edificio", también especifica "el piso, la oficina, el buzón y el destinatario del paquete"
> [!example] 
> https://www.hackthebox.eu/example?floor=2&office=dev&employee=17 
