#**PRÁCTICA DE COMANDOS DE RED EN WINDOWS Y LINUX I**

**Objetivo**

La siguiente práctica está destinada a comprender algunos comandos importantes que son de gran utilidad en la administración de una red. 

**Material necesario**

Necesitaremos dos máquinas virtuales o reales. Una con un sistema operativo Windows y otra con Linux.

***1. Comando `ipconfig` (Windows)***

Este comando nos permite ver datos relacionados con la configuración de red de nuestro equipo. Algunas de sus principales opciones son:

***`ipconfig /all`***  -> Nos muestra información más detallada del adaptador de red.

***`ipconfig /release`*** -> Libera las configuración asignada por dhcp.

***`ipconfig /renew`*** -> Solicita al servidor DHCP la renovación de una configuración de red.

***`ipconfig /displaydns`*** -> Muestra el contenido de la caché DNS de nuestro equipo.

***`ipconfig /flushdns`*** -> Borra la caché DNS de nuestro equipo.

**Ejercicios**

+ Use el comando ***`ipconfig /all`*** para ver la dirección MAC de tu equipo.  Y la siguiente aplicación <http://coffer.com/mac_find/> para rellenar la siguiente tabla.

![resultado](img/2023-01-10_09-27.png)

|Dirección IP v4|172.18.13.11| 
| - | - |
|Máscara|255.255.0.0|
|Gateway|172.18.0.1|
|MAC|08-00-27-F1-20-EF|
|Fabricante|cadmus computer systems|
|Dirección IP v6|fe80::ad13:6840:6ebb%10/64|
|Servidores DNS|8.8.8.8|
|Tiempo de concesión de la IP||
|Nombre del adaptador de red|Ethernet|

+ Liberar la configuración IP del adaptador con ***`ipconfig /release`*** y a continuación volver a usar el comando ***`ipconfig`*** . ¿Cuál es la ip ahora?
![resultado](img/2023-01-10_09-31.png)
la nueva ip es 169.254.110.187

+ Ejecutar el comando ***`ipconfig /renew`*** solicitando una renovación de dirección IP. A continuación volver a ejecutar ***`ipconfig`*** . ¿Cuál es la nueva ip?
![resultado](img/2023-01-10_09-32.png)
la nueva ip es 172.18.99.111

+ Ejecutar el comando ***`ipconfig /displaydns`*** y comprobar la información que contiene la caché DNS de tu equipo. Ejecuta ahora el comando ***`ipconfig /flushdns`** y después muestra otra vez el contenido de la caché DNS. ¿Qué información muestra ahora? ¿Qué ha ocurrido?*



+ Usar el navegador para ir a la web [https://www.w3schools.com]() y luego ejecutar el comando ***`ipconfig /displaydns`*** . Hacer una captura de pantalla donde se muestre que se ha cacheado la ip de ese nombre de dominio y pegarla aquí debajo.
![resultado](img/2023-01-12_09-26.png)


+ Borra la caché DNS con el comando ***`ipconfig /flushdns`*** y muestra una captura de pantalla en que se vea que ya no hay registros DNS en caché.
![resultado](img/2023-01-12_09-28.png)


***2. Comando `ifconfig` (Línux)***

Este comando nos permite mostrar la configuración IP de nuestra máquina y configurar algunos parámetros. Algunas opciones de interés son:

***`ifconfig  –a`*** -> Nos muestra la configuración de todas las tarjetas de red incluso las desactivadas.

***`ifconfig eth0 down`*** -> Desactiva una tarjeta de red llamada eth0. (También vale ***ifdown eth0***)

***`ifconfig eth0 up`*** -> Activa la tarjeta de red llamada eth1. (También vale ***ifup eth0***)

***`ifconfig eth0 192.168.1.1 netmask 255.255.255.192`*** -> Asigna una IP y una máscara a la tarjeta eth0.

**Ejercicios**

+ Ejecuta el comando ***`ifconfig`*** y rellena lo que puedas de la siguiente tabla.

![resultado](img/2023-01-12_09-31.png)

|Dirección IP v4|172.18.13.41|
| - | - |
|Máscara|255.255.0.0|
|Gateway|172.18.0.1|
|MAC|08:00:27:59:28:19|
|Fabricante||
|Dirección IP v6|fe80::c92:d97e:8257:b0e3|
|Servidores DNS|1.1.1.1|
|Tiempo de concesión de la IP||
|Nombre del adaptador de red|enp0s3|

+ Desactiva tu tarjeta de red con el comando ***`ifconfig eth0 down`***. A continuación, comprueba con un ***`ifconfig`*** que la tarjeta ya no aparece, se ha desactivado. Haz una captura de pantalla donde se vea que ya no está activada.
![resultado](img/2023-01-12_09-46.png)
![resultado](img/2023-01-12_09-51.png)

+ Usa el comando ***`ifconfig –a`*** para ver que la tarjeta está desactivada (pega una captura de pantalla debajo).
![resultado](img/2023-01-12_09-51.png)

+ Ahora activa la tarjeta con el comando ***`ifconfig eth0 up`*** y luego con el comando `ifconfig` comprueba que ya está habilitada (pega una captura de pantalla debajo).
![resultado](img/2023-01-12_09-51_1.png)

+ Usa el comando ***`ifconfig eth0 192.168.99.99 netmask 255.255.255.0`*** y pega una captura de pantalla que muestre que el adaptador de red se ha configurado correctamente.
![resultado](img/2023-01-13_08-18.png)

+ Usa el comando ***`ifconfig eth0 IP netmask Máscara`*** (con la configuración inicial de red) y pega una captura de pantalla que muestre que el adaptador de red se ha configurado correctamente.
![resultado](img/2023-01-13_08-20.png)

***3. Comando ping (Windows y Línux)***

Se usa para saber si hay comunicación entre equipos. Podría “no funcionar” en caso de que el ordenador al que hacemos el ping tenga un firewall que ignore nuestros mensajes. 

Algunas opciones para Windows/Linux son

***-n*** -> Indica el número de paquetes que se enviarán. ( ***-c*** en linux)

***-l*** -> establece el tamaño del mensaje que se envía. ( ***-s*** en linux)

***-t*** -> envía paquetes de manera indefinida hasta que lo paramos con “***ctrl+c***”

***-i*** -> establecemos el TTL del ping, es decir, el número de saltos que debe dar antes de que lo destruyan. ( ***-t*** en linux)

**Ejercicios**

+ Desde una máquina con línux ejecuta el comando ***`ping –s 100 –c 2  ip\_puertadeenlace`*** para que se envíen dos ecos de 100 bytes. Muestra una captura de pantalla con el resultado.



+ Desde una máquina con windows usa el comando ***`ping –i 2 ip\_puertadeenlace`*** para hacer un ping a nuestra puerta de enlace con un TTL igual a 2. 
![resultado](img/2023-01-13_08-38.png)

+ Luego haz un ping de las mismas características, pero a google ***`ping –i 2 www.google.es`*** Pega una captura de pantalla con el resultado y explica lo que ha pasado.
![resultado](img/2023-01-13_08-46.png)


+ El comando ping nos da información sobre el tiempo de latencia de una red. Haz un ping a nuestra puerta de enlace y luego a otro a [www.google.es](http://www.google.es/). Busca información de lo que es el tiempo de latencia y compara los tiempos de latencia en ambos casos. 
![resultado](img/2023-01-13_08-49.png)


***4. Comando route (Línux)***

Nos permite ver y configurar la tabla de rutas de nuestro equipo. Algunas opciones de uso son: 

***`route`*** -> Nos muestra la tabla de enrutamiento del equipo.
***`route del default gw ip_gateway`*** -> Borra la ruta por defecto.
***`route add default gw ip_gateway`*** -> Añade la puerta de enlace indicada para nuestro host.

**Ejercicios**

+ Usa el comando `route` para ver la puerta de enlace de tu equipo. ¿Cuál es tu puerta de enlace?


+ Borra la puerta de enlace usando el comando `route del default gw ip_gateway`. A continuación, ejecuta el comando `route` para comprobar que ya no hay puerta de enlace. Intenta navegar por internet y verás que tampoco puedes. Haz una captura de pantalla con la salida del comando `route` y del resultado de `ping 8.8.8.8` ¿Cómo interpretas el mensaje que te devuelve el `ping`?
![route](img/1.PNG)
![route](img/2.PNG)

El mensaje que me devuelve es porque no detecta una direccion para resolver. 

+ Vuelve a configurar la puerta de enlace usando el comando `route add default gw ip_gateway` y comprueba que ya ha vuelto la puerta de enlace con el comando `route`.
![route](img/3.PNG)


***5. Comando netstat (Línux y Windows)***

Nos muestra las conexiones que tiene nuestro host abiertas con la red. Algunas opciones para Linux son:

***-t*** → Muestra las conexiones tcp abiertas. (en windows -p tcp)
***-u*** → Muestra las conexiones udp abiertas. en windows -p udp)
***-a*** → Muestra los puertos que estén esperando conexiones (puertos en escucha). -n → Para que muestre solo información numérica.
***-s*** → Nos muestra estadísticas sobre nuestra conexión de red.
***-r*** → Nos muestra la tabla de enrutamiento de nuestro host.

**Ejercicios**

+ Abre una página web cualquiera y luego ejecuta el comando `netstat -t` para que nos muestre las conexiones que tenemos abiertas por tcp. Pon una captura de pantalla del resultado y explica lo que es cada una de las columnas que aparecen.
![route](img/4.PNG)

Protocolo:Indica el protocolo usado por el socket

Recibidos:Los paquetes que reciben

Enviados:Los paquetes que envian

direccion local:Direccion del equipo

direccion remota:Cuando navegas por internet esa dirección es la que detectan los sitios web que estás visitando

Estado:El tiempo que tar en conectarse 


+ Ahora espera unos segundos y vuelve a ejecutar `netstat -tn`. Comprobarás que algunas de las conexiones se han cerrado o están esperando para cerrarse. Además con la opción **-n** verás los resultados en formato numérico. Pon una captura de pantalla y explica la diferencia entre ***Established***, ***Time_wait*** y ***Close_Wait***.

![route](img/5.PNG)

***Established***: El estado se establecio correctamente 

***Time_wait***:El estado esta en estado de espera para ponder conectarse

***Close_Wait***:El tiempo de espera se cerro

+ Ejecuta ahora la orden `netstat -at` para que muestre las tanto las conexiones tcp abiertas como los puertos que están a la escucha. Copia una captura de pantalla donde se vean los puertos que tienes escuchando, explica qué significan los asteriscos en la columna ***“Foreign address”*** e investiga si tener esos puertos abiertos es normal o supone una amenaza.
![route](img/6.PNG)

quiere decir que la máquina local está esperando a que otra máquina remota envíe datos. No es peligroso tener los puertos de esa manera

+ Ejecuta el comando `netstat -s` para ver las estadísticas de red y haz una captura en la que se vean cuantos paquetes tcp has recibido y cuantos de ellos han sido erroneos.
![route](img/7.PNG)


***6. Comando arp (Línux y Windows)***

Se usa para mostrar y administrar la caché `ARP` de nuestro equipo. Las opciones más habituales son:

***`arp -a`*** → Muestra la tabla arp del host (en línux no hace falta el -a)
***`arp -d dirección_ip`*** → borra de la tabla la entrada indicada
***`arp -d *`*** → borra toda la tabla arp (el equivalente en linux: `ip neigh flush all`) 
***`arp -s direccion_ip direccion_mac`*** → crea una entrada en la tabla ARP

**Ejercicios**

+ Borra toda la caché ARP con el comando `arp -d *`. A continuación haz un ping a la puerta de enlace. Pon una captura de la tabla ARP en que se vea que solo está la puerta de enlace y su mac.
![route](img/8.PNG)

+ Ahora borra manualmente la entrada arp de la puerta de enlace con la orden `arp -d ip_puertadeenlace`. Luego introduce manualmente una mac falsa para la puerta de enlace en la tabla arp con el comando `arp -s ip_puertadeenlace aa:bb:cc:dd:ee:ff` Haz una captura de pantalla en que se vea el resultado del comando arp -a y de hacer un ping a google. Explica por qué ahora no hay internet.

+ Borra la entrada falsa de la tabla arp con el comando `arp -d ip_puertadeenlace`.

***7. Comando nslookup (Línux y Windows)***

Este comando nos da información sobre la resolución de nombres dns. Nos dice a quién le hacemos la consulta y qué respuesta nos da. Opciones principales:

***`nslookup dominio`*** → Consulta a nuestro servidor dns por el dominio indicado.
***`nslookup dominio ip_servidordns`*** → consulta al servidor dns indicado por el dominio.

**Ejercicios**

Averigua el nombre del servidor DNS de 
https://www.puertodelacruz.es . A continuación, ejecutamos el comando nslookup nombreServidorDNS y luego el comando `nslookup nombreServidorDNS 8.8.8.8`. Explica las causas de las diferencias que hay entre los resultados de las dos consultas.
![route](img/9.PNG)

La diferencia es que en la pagina web no detecta el dns y en el 8.8.8.8 si lo detecta