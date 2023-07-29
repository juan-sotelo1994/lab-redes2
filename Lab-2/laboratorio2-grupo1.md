# Telematica

# Practica de laboratorio 01

## Objetivos

### Objetivo General
Proporcionar el conocimiento y generar las habilidades necesarias en la configuración y gestión de dispositivos de redes.

### Objetivos Específicos:
- Conocer los números necesarios para configurar el direccionamiento de una red de area local.  

---

## Parámetros:
Para todos los efectos:
* la letra G  de se reemplaza por el número de grupo de laboratorio.
* la letra C  de se reemplaza por el ultimo número de cédula del estudiante.


## 1. [Configurar el entorno de trabajo](#) ✔
1. Cree si no existe el repositorio [__"REDES-2"__][1_2] en su cuenta de github. ✔
1. Agregue un archivo llamado [__"laboratorio_2.md"__][1_2] a este repositorio. ✔
1. Invite a los compañeros de grupo como colaboradores en este repositorio. ✔
1. Documente cada uno de los items a continuación con capturas de pantalla y código . ✔


## 2. [Preguntas reflexivas de ambientación](#) ✔

<ol type="a">
<li>¿Como se llama la interfaz donde se conecta los cables UTP.?</li>
   
   ### Respuesta:
     Adaptador de Ethernet Conocido como puerto de internet.

[![v4-460px-Connect-an-Ethernet-Cable-to-a-Laptop-Step-2.jpg](https://i.postimg.cc/8k9B5yfX/v4-460px-Connect-an-Ethernet-Cable-to-a-Laptop-Step-2.jpg)](https://postimg.cc/Hj07v92b)
    
<li>¿Que significa POE IN y POE OUT en una interfaz?.</li>

  ### Respuesta:

  ## Poe input 
  significa que el router o dispositivos puede tomar energía de la fuente de PoE y brindar energia desde su mismo puerto utilizando su propia alimentacion de energia.

  ## Poe output
   significa que el router o dispositivo necesita de una fuente alterna para enviar la energia por el medio que se va a usar. 


[![poe2.jpg](https://i.postimg.cc/qvKy4cxC/poe2.jpg)](https://postimg.cc/hXSf0dwS) 

<li>¿Que utilidad tiene la interfaz USB en los Enrutadores?.</li>

  ### Respuesta:

Podemos usar el puerto USB en un Enrutador para los Siguientes fines:

 ✔ Conectar una impresora USB, y así podrá ser usada por todos los dispositivos de esa red.
 
 ✔ Conectar un pendrive o disco duro y usarlo como almacenamiento compartido en la red, por ejemplo vía FTP o SMB.

 ✔ Conectar un sistema de videovigilancia.

 ✔Actualización del firmware.
 
 <li>¿Que utilidad tiene la interfaz SFP en los Enrutadores?.</li>
  
  ### Respuesta: 
 Los puertos SFP permiten que los switches Gigabit se conecten a una amplia variedad de cables de fibra óptica y Ethernet para extender la funcionalidad de conmutación a través de la red.

Los SFP son equipos de entrada/salida intercambiable en caliente, utilizados principalmente en switches de red y de almacenamiento; Permiten que el switch se conecte a cables de fibra óptica de diferentes tipos – incluyendo modos monomodo y multimodo – y velocidades (1 Gbps, 10Gbps, 40Gbps y 100Gbps), o incluso cables de cobre Ethernet, como CAT5e y CAT6.

[![SFP-SWITCH-1.png](https://i.postimg.cc/7LWVm1Ds/SFP-SWITCH-1.png)](https://postimg.cc/v15fmV4f)

<li>¿Que tipos de interface Ethernet se pueden encontrar en los Enrutadores?.</li>

 ### Respuesta:

 Tenemos tre tipos de interfaces de red que encontramos en un enrutador:

  ## Ethernet: 
  Es una interfaz de red de área local (LAN) que utiliza el protocolo Ethernet para permitir la transmisión de datos entre dispositivos conectados a la misma red.

  ##  WAN (Wide Area Network):
  Es una interfaz de red de área amplia que se utiliza para conectar redes a distancia. Las interfaces WAN se utilizan para conectar redes LAN a Internet o a otras redes LAN en diferentes locaciones.

  ## Wi-Fi: 
  Es una interfaz inalámbrica que permite la transmisión de datos a través de ondas de radio. Los dispositivos Wi-Fi pueden utilizarse para conectar dispositivos a una red LAN o para establecer una conexión de red inalámbrica.
</ol>


## 3. [Caracterizar el CPE TP-LINK](#) ✔
|Parámetro||Valor|
|--|:--:|--:|
|Marca|-->|Tp-Link|
|Referencia|-->|TL-WR940N|
|Velocidad de la CPU|-->|580 MHz 32-bit|
|Tamaño de la memoria RAM|-->|32 MiB|
|Sistema Operativo|-->||
|Tipo de WIFI|-->|Wi-Fi 4 IEEE 802.11n/b/g 2.4 GHz|
|Voltaje DC|-->|9V ⎓ 0.6 A|

## 4. [Configurar básica de CPE TP-LINK](#) ✔
1. Conecte los equipos a la red eléctrica.

  Conectamos el Equipo a la corriente electrica. <br>

[![Whats-App-Image-2023-06-13-at-6-53-41-PM.jpg](https://i.postimg.cc/pdVz4rRk/Whats-App-Image-2023-06-13-at-6-53-41-PM.jpg)](https://postimg.cc/DSDSb2Wb)

2. [Reiniciar][4_1] el dispositivo a la configuración de fabrica.

  Reiniciamos el equipo Presionando el boton que tiene en su parte trasera con el fin de reestablecerlo a su configuracion de fabrica.
[![Whats-App-Image-2023-06-13-at-6-53-40-PM-1.jpg](https://i.postimg.cc/Vk2PHrqP/Whats-App-Image-2023-06-13-at-6-53-40-PM-1.jpg)](https://postimg.cc/Hr0NrLv6)
3. Conectar el equipo mediante un patchcord (latiguillo) al equipo y a internet.

Nos conectamos por medio de un patchcord para garantizar la conexion mas estable a nuestro equipo, con el cual haremos la configuracion. 

[![Whats-App-Image-2023-06-13-at-6-53-40-PM.jpg](https://i.postimg.cc/Y2XrzSsM/Whats-App-Image-2023-06-13-at-6-53-40-PM.jpg)](https://postimg.cc/DmX327hM)

Al momento de conectar el patchcord debemos hacerlo en los puertos que sean de LAN, esto hace que podamos ingresar al dispositivo y no tengamos problema alguno. en este caso los puertos de LAN los identificamos por su color naranja.

[![Whats-App-Image-2023-06-13-at-6-53-39-PM.jpg](https://i.postimg.cc/28sVn613/Whats-App-Image-2023-06-13-at-6-53-39-PM.jpg)](https://postimg.cc/crcxSdMN)

Conectamos el otro extremo del cable a nuestro equipo en la interfas de Ethernet, dado el caso no tengamos esta interfaz podemos configurarlo por medios inalambricos(WI-FI)


4. [Acceder][4_2] al dispositivo via protocolo http desde el navegador web.

ya conectados al dispositivo ingresamos a nuestro navegador de preferencia y digitamos en la barra del buscador la siguiente direccion = 
# 192.168.0.1

[![Whats-App-Image-2023-06-13-at-6-55-13-PM.jpg](https://i.postimg.cc/zvp48347/Whats-App-Image-2023-06-13-at-6-55-13-PM.jpg)](https://postimg.cc/H8c6tWY8)

Esto nos llevara a una ventana de inicio de sesion en las cuales nos pedira unas credenciales, las cuales son Admin como usuario y como Password admin (estos valores son predeterminados de fabrica cuando el equipo es nuevo o ha sido reiniciado).

[![Whats-App-Image-2023-06-13-at-6-57-01-PM.jpg](https://i.postimg.cc/Qx9qXFLM/Whats-App-Image-2023-06-13-at-6-57-01-PM.jpg)](https://postimg.cc/HVmMzskG)

Ingresando al equipo encontramos esta interface que nos permite entrar a toda la configuracion de nuestro router.

5. Cambiar el nombre del dispositivo para identificarlo.

nos dirijimos al menu y ingresamos por la opcion de red la cual nos dirije a la siente ventana con la cual podemos cambiar el nombre a nuestro dispositivo para identificarlo en la red LAN.

[![Whats-App-Image-2023-06-13-at-9-07-46-PM.jpg](https://i.postimg.cc/d0XzQ4wx/Whats-App-Image-2023-06-13-at-9-07-46-PM.jpg)](https://postimg.cc/p9f0qQ9f)

6. Configurar la direccionamiento WAN para lograr conectividad con la red externa.

[![Whats-App-Image-2023-06-13-at-9-31-09-PM.jpg](https://i.postimg.cc/25b28YH4/Whats-App-Image-2023-06-13-at-9-31-09-PM.jpg)](https://postimg.cc/3yhgnsQR)

[![Whats-App-Image-2023-06-13-at-9-32-40-PM.jpg](https://i.postimg.cc/bY9cj0Sq/Whats-App-Image-2023-06-13-at-9-32-40-PM.jpg)](https://postimg.cc/pyr1fFBS)

7. Configurar la direccionamiento LAN con una IP privada, clase C para lograr conectividad con la red interna.

Configuramos la ip de nuestro router para tener un propio segmento de ips para trabajar.

[![1.png](https://i.postimg.cc/ZKPPTcrK/1.png)](https://postimg.cc/crHthf9V)

8. Configurar el [DHCP][dhcp] para que asigne 20 direcciones IP entre [G](#parámetros).200-[G](#parámetros).220.

Asignamos un segmento de red determinado con el componente DHCP para tener asignado desde la ip 192.168.30.200 hasta 192.168.30.220, para tener la capacidad de 20 equipos conectados.

[![1.png](https://i.postimg.cc/wMLrxmV8/1.png)](https://postimg.cc/BPZpMtkM)


9. Configurar la [WLAN][wlan] de nombre y [PSK](psk) "REDES_4[G](#parámetros)" para lograr conectividad inalámbrica.

En este apartqado cambiamos la configuracion del nombre la red inalámbrica al igual que la region y posteriormente lo que es el canal en donde vamos a trabajar, en este caso vamos a utilizar el canal numero 1
[![1.png](https://i.postimg.cc/prrDqbm0/1.png)](https://postimg.cc/ctqgLzMY)

Tambien cambiamos lo que es la clave de acceso para tener una conexion mas segura como el formato WPA2 para mayor proteccion para las conexiones seguras.

[![1.png](https://i.postimg.cc/wMRnZrPV/1.png)](https://postimg.cc/wRHWsw9y)

Escogimos el canal 1 debido a que tiene menos trafico para que la red no tenga conflicto con otras señales.

10. Realizar pruebas [PING][4_3] a DNS Cloudflare desde el dispositivo.

[![Whats-App-Image-2023-06-13-at-10-07-30-PM.jpg](https://i.postimg.cc/1RV0nPZt/Whats-App-Image-2023-06-13-at-10-07-30-PM.jpg)](https://postimg.cc/c6Zt2pCy)

11. Realizar pruebas [PING][4_3] a DNS Cloudflare desde el computador conectado por UTP.

Realizamos un ping a los servidores de Cloudflare para verificar la conexion a la red de internet con una conexion fija por medio de cable utp.

[![1.png](https://i.postimg.cc/kGyY0dsW/1.png)](https://postimg.cc/rRK943vp)

12. Realizar pruebas [TRACEROUTE][4_4] a DNS Google desde el router.

Realizamos el mismo proceso del ping esta vez desde la conexion wi-fi para comparar velocidades.

[![1.png](https://i.postimg.cc/rwR27D6T/1.png)](https://postimg.cc/87GY6PPX)

13. Realizar pruebas [TRACEROUTE][4_4] a DNS Google desde el Computador conectado por UTP.

Realizamos un tracer para identificar cuantos saltos realiza  para llegar a los servidores de googles. 

[![1.png](https://i.postimg.cc/5NDN7QcC/1.png)](https://postimg.cc/mtNshDgL)

14. Realizar pruebas [TRACEROUTE][4_4] a DNS Google desde un dispositivo conectado por WIFI.

Esta prueba la realizamos desde otro computador conectado a la red que hemos creado para el laboratorio.

[![1.png](https://i.postimg.cc/zvfbYyk1/1.png)](https://postimg.cc/r0vFSFbh)

15. Habilitar la gestión remota del dispositivo desde cualquier IP.

Habilitamos la gestion remota en nuestro router con el puerto 8076 para cuando tengamos que conectarnos desde otra parte de la red podamos hacerlo con la ip de puerta de enlace mas el puerto que le hemos asignado. 

[![1.png](https://i.postimg.cc/QdLrk1Sw/1.png)](https://postimg.cc/2VxJCqs7)

16. Realizar un backup de la configuración del equipo.

Nos vamos al apartado de heraamientas de sistema, y ingresamos al submenu y nos dirijimos a soporte y restablecer, donde podemos generar nuestra copia de seguridad para guardar la configuracion previa que hemos hecho.

[![1.png](https://i.postimg.cc/WzxbZ49v/1.png)](https://postimg.cc/p5YHbPbG)

Haciendo esto vamos a tener una ventana emergente con la cual vamos a ubicar donde vamos a guardar nuestra copia de seguridad.

[![Whats-App-Image-2023-06-16-at-10-47-12-PM.jpg](https://i.postimg.cc/YSKB5Txr/Whats-App-Image-2023-06-16-at-10-47-12-PM.jpg)](https://postimg.cc/RWRYfs8y)



## 5. [Caracterizar la ONT HUAWEI](#) ✔
|Parámetro||Valor|
|--|:--:|--:|
|Marca|-->||
|Referencia|-->||
|Velocidad de la CPU|-->||
|Tamaño de la memoria RAM|-->||
|Sistema Operativo|-->||
|Tipo de WIFI|-->||
|Voltaje DC|-->||

## 6. [Configurar básica de ONT HUAWEI](#) ✔
1. Conecte los equipos a la red eléctrica.
1. [Reinicie][6_1] los dispositivos a la configuración de fabrica.
1. Conecte los equipo mediante un patchcord (latiguillo) al equipo y a internet.
1. [Acceder][6_2] al dispositivo via protocolo http desde el navegador web.
1. Configurar la direccionamiento LAN con una IP privada, clase B para lograr conectividad con la red interna.
1. Configurar el [DHCP][dhcp] para que asigne 50 direcciones IP entre [GG](#parámetros).150-[GG](#parámetros).200.
1. Reservar una IP fija en la red interna para la MAC del un computador (Servidor).
1. Configurar la [WLAN][wlan] de nombre y [PSK](psk) "REDES_4[G](#parámetros)" para lograr conectividad inalámbrica.
1. Realizar pruebas [PING][4_3] a la puerta de enlace desde el computador conectado por UTP (Servidor).
1. Realizar pruebas [PING][4_3] a la puerta de enlace desde el computador conectado por WIFI (Cliente).
1. Realizar pruebas [PING][6_3] a la puerta de enlace desde un teléfono Movil conectado por WIFI.
1. Listar los dispositivos por tipo que aparecen en "DHCP Information".
1. Mapear el puerto 80 del router para que redirija a un servicio [Python][6_4] en un computador.
1. Verificar que se puede acceder al servicio (pagina web) desde los dos clientes (móvil y PC).
1. Habilitar la gestión remota del dispositivo desde cualquier IP.
1. Realizar un backup de la configuración del equipo.

>ONT: [HUAWEI][6_5] -> reiniciar:[Con el Router encendido dejamos presionado el botón reset durante 2 segundos hasta  hasta que los LEDs se apaguen][6_1] acceder: [conectar con la cadena user:twtvu@192.168.1.1][6_2]

## 7. [Caracterizar el router MikroTik](#) ✔
|Parámetro||Valor|
|--|:--:|--:|
|Marca|-->|Mikrotik|
|Referencia|-->|RB951Ui-2HnD|
|Velocidad de la CPU|-->|	600 MHz-AR9344-DC3A|
|Tamaño de la memoria RAM|-->|128 MB|
|Sistema Operativo|-->|RouterOS V 7.9.2|
|Tipo de WIFI|-->|	802.11b/g/n|
|Voltaje DC|-->|8 V - 30 V|

## 8. [Configurar básica de router MikroTik](#) ✔
1. Conecte los equipos a la red eléctrica.

Tenemos nuestro equipo mikrotik a la corriente.

[![Whats-App-Image-2023-06-23-at-7-24-57-PM.jpg](https://i.postimg.cc/hvg4h5f6/Whats-App-Image-2023-06-23-at-7-24-57-PM.jpg)](https://postimg.cc/R6sxDG1L)


1. [Reinicie][8_1] los dispositivos a la configuración de fabrica.

Vamos a reiniciar el equipo de la manera manual usando un clip, o un desarmador de punta fina.

Paso a seguir vamosa insertarlo en el boton de reset pero antes debemos tener desconectado el equipo.

[![Whats-App-Image-2023-06-23-at-7-59-05-PM.jpg](https://i.postimg.cc/t4DBcZ3x/Whats-App-Image-2023-06-23-at-7-59-05-PM.jpg)](https://postimg.cc/BjL5LvwS)

Luego conectamos el equipo a la corriente sin dejar de presionar el boton de reset, para saber que tenemos el equipo reiniciado el equipo va a sonar y van a parpadear las luces, en ese caso debemos dejar de presionar el boton.

[![Whats-App-Image-2023-06-23-at-7-59-05-PM-1.jpg](https://i.postimg.cc/d3dWN56s/Whats-App-Image-2023-06-23-at-7-59-05-PM-1.jpg)](https://postimg.cc/7JHMfMjd)

# tenemos otra forma de reiniciar el equipo

1. Conecte los equipo mediante un patchcord (latiguillo) al equipo y a internet.

[![Whats-App-Image-2023-06-23-at-7-41-18-PM.jpg](https://i.postimg.cc/kXKZTgYQ/Whats-App-Image-2023-06-23-at-7-41-18-PM.jpg)](https://postimg.cc/dLQ41wY3)

ingresamos al router, esto es factible si conocemos la clave. 
(lo podemos hacer por medio de winbox o la direccion ip)

[![2.png](https://i.postimg.cc/HxRxWP7m/2.png)](https://postimg.cc/jw6KZcX3)

ya dentro del sistema del router nos dirijimos al apartado de new terminal 

[![3.png](https://i.postimg.cc/ZRBbQFsM/3.png)](https://postimg.cc/ygKCg9Hm)

y vamos a digitar en la consola el siguiente comando system reset.

[![Whats-App-Image-2023-07-20-at-10-04-02-AM.jpg](https://i.postimg.cc/Wzx8sQk0/Whats-App-Image-2023-07-20-at-10-04-02-AM.jpg)](https://postimg.cc/V0BnRZ4N)

ya con este comando digitado vamos a confirmar con la Y para aceptar el reseteo del systema. 

[![Whats-App-Image-2023-07-20-at-10-03-46-AM.jpg](https://i.postimg.cc/tTKDjKPW/Whats-App-Image-2023-07-20-at-10-03-46-AM.jpg)](https://postimg.cc/xJPLGF61)

1. [Acceder][8_2] al dispositivo por el puerto 8291 via Winbox.

Ingresamos al router por medio de la aplicacion de mikrotik, escogemos nuestro router(en caso de tener mas routers mikrotik con el vamos a trabajar tiene la ip 192.168.88.1).

[![11.png](https://i.postimg.cc/6qcQxG1Z/11.png)](https://postimg.cc/30yhgWhr)

1. Cambiar el nombre del dispositivo para identificarlo.

Vamos a cambiar el nombrer de nuestro dispositivo para tener la certeza de cual equipo vamos a configurar.

[![Whats-App-Image-2023-07-20-at-10-05-28-AM.jpg](https://i.postimg.cc/X71MMJqC/Whats-App-Image-2023-07-20-at-10-05-28-AM.jpg)](https://postimg.cc/F7SC3hjr)

1. Cambiar la contraseña del usuario "admin" a "Redes_2".

Al ingresar nuestro router nos pedira el cambio de contraseña de la sesion administrador, esto con el fin de tener seguridad en nuestro equipo. 

[![13.jpg](https://i.postimg.cc/SR9xjvsW/13.jpg)](https://postimg.cc/fSwNr5YL)

1. Configurar las [interfaces][8_3] y el [bridge][8_4] 
(conmutador) para dos redes (Interna y externa).

Vamos a identificar las interfaces con las que trabajaresmos, recordemos que en mikrotik podemos escoger que puerto utilizaremos como WAN o LAN Y Wi-Fi.

[![1.png](https://i.postimg.cc/MTPWN7Fj/1.png)](https://postimg.cc/TLbMWDGR)

Ingresamos a la interfas del bridge para la creacion del mismo ya que no tenenomos ningun puerto asignado a el bridge.

[![brig1.png](https://i.postimg.cc/SKf3tmvX/brig1.png)](https://postimg.cc/XZXsr633)

Creamos el bridge con las interfaces LAN Y Wi-Fi para que tengan el mismo direccionamiento ip.

[![brgi2.png](https://i.postimg.cc/mD6d0kNr/brgi2.png)](https://postimg.cc/KkBrTZWX)  

Vamos a escoger que interfaces vamos a ir agregando a el bridge.

[![agregar-brig.png](https://i.postimg.cc/wMmS2D8z/agregar-brig.png)](https://postimg.cc/0K9W2MyX)

Al finalizar vamosa  tener una lista de los puertos que se han agregado satisfactoriamente.

[![agregados1.png](https://i.postimg.cc/JhzvgfVP/agregados1.png)](https://postimg.cc/TKBt5HPD)

1. Agregar la [dirección][8_5] de la interfaz externa en el segmento necesario para acceder a internet.

ya aqui podemos configurar los servicios, iniciando con la configuracion del dhcp en el bridge que hemos creado posteriormente. 

[![dchp-server.png](https://i.postimg.cc/NfwzZxvF/dchp-server.png)](https://postimg.cc/RqXdHKFx)

Ya configurado el Bridge nos va a pedir el direcionamiento al cual vamos a darle la conexion.

[![drireccionamiento-dhcp.png](https://i.postimg.cc/FRTHwK7s/drireccionamiento-dhcp.png)](https://postimg.cc/2bBYZrQP)

Configuramos los servicios de DNS del proveedor de internet 

[![servidor-dns.png](https://i.postimg.cc/FsyHQGfB/servidor-dns.png)](https://postimg.cc/Lnsptt3t)

Tambien vamos a configurar el tiempo de asignacion para las direcciones ip, ya que cuando un equipo se desconecte poder asignarle esa ip a otro dispositivo vamos a poner el intervalo de tiempo para ello. 

[![tiempo-para-ips.png](https://i.postimg.cc/G3kCBtcB/tiempo-para-ips.png)](https://postimg.cc/kDXZznR9)


1. Agregar la [dirección][8_5] del bridge (interna) con una IP privada, clase A.

Este paso lo vamos hacer de manera automatica con DHCP setup que etsa en los servicios de dhcp server con esto vamos hacer una configuracion rapida y correcta.

[![dchp-server.png](https://i.postimg.cc/NfwzZxvF/dchp-server.png)](https://postimg.cc/RqXdHKFx)


1. Agregar un [Pool][8_6] en el segmento de la LAN que asigne direcciones entre [GG](#parámetros).100-[GG](#parámetros).200.

Para agragar nuestro pool podemos hacerlo de dos formas la primera en el menu de nuestro router mikrotik nos ubicamos en el apartado de ip y ingresamos a la opcion pool. 

ya hecho el despliegue de esta opcion tenemos que poner un nombre a nuestro pool, seguido de la direccion ip de nuestro segmento y vamos a cambiar el utlimo digito para nuestro segmento de trabajo.

[![pool2.png](https://i.postimg.cc/nhgG7Hk5/pool2.png)](https://postimg.cc/rDG4227C)

La otra forma como podemos hacerlo es por medio de la opcion DHCP Server que se encuentra en el menu en la opcion ip, dando las opciones adecuadas para la conectividad podemos configurar de igual manera el pool siendo la manera mas rapida de hacerlo.

[![pool.png](https://i.postimg.cc/8c5Z4Fgd/pool.png)](https://postimg.cc/dkbRtV1D)


1. Configurar el [DHCP][dhcp] y las rutas estáticas necesarias para lograr conectividad de la red interna con internet.
 
Ya con el dchp-server y dhcp cliente listos y configurados tenemos nuestra red lista para conectanos a internet, solo nos falta una ultima configuracion para que esto sea posible.

[![dhcp-conf.png](https://i.postimg.cc/RZ16X4Qq/dhcp-conf.png)](https://postimg.cc/sMXg2FLR)

Vamos a cuadrar la firma de firewall que nos es necesaria para tener el acceso a internet 

[![firewall.png](https://i.postimg.cc/3NM0tR64/firewall.png)](https://postimg.cc/k6c54n7q)


Vamos a crear el nuevo firewall en el formato que vamos a trabajar y el puerto por el cual vamos a tener comunicacion el cual es el WAM.

[![newfirewall.png](https://i.postimg.cc/qqLB2vdd/newfirewall.png)](https://postimg.cc/vx4dsMBP)

En las acciones vamos a configurarlos como enmascarado para que tenga la mascara de nuestro proveedor y asi poder tener internet. 

[![firewall2.png](https://i.postimg.cc/zGfvSKB2/firewall2.png)](https://postimg.cc/hfHKKJVV)



1. Configurar la [WLAN][wlan] de nombre y [PSK](psk) "REDES_4[G](#parámetros)" para lograr conectividad inalámbrica.

Vamos a cambiar la configuracion del apartado de wlan iniciando por el modo en el que vamos a trabajar que sera en ap bridge, seguido de la frecuencia en la que vmoas a trabajar que es de 2,5 GHz. 

la frecuencia la vamos a manejar automatica para que pueda evaluar en que canal hay menor trafico de red, el SSID vamos a trabajar con el nombre de REDES_4G.

[![wifii.png](https://i.postimg.cc/gJr0gG0b/wifii.png)](https://postimg.cc/ftnZLnX8)

Luego vamos a cambiar la seguridad para asignarle una contraseña con las caracteristicas de WPA Y WPA2 para una seguridad fuerte de igual manera la contraseña que vamos a asignar tendra caracteres especiales para tener una seguridad mejor.

[![WIFISEGURIDAD.png](https://i.postimg.cc/KYGwTNGR/WIFISEGURIDAD.png)](https://postimg.cc/NKndqRrc)

Ya podemos ver que la señal esta disponible.

[![se-al.png](https://i.postimg.cc/SN65R56W/se-al.png)](https://postimg.cc/zVfpPxPB)

1. Realizar pruebas de diagnostico [PING][8_7] y [TRACEROUTE][4_4] desde el router.

[![ping.png](https://i.postimg.cc/vmc3rSV2/ping.png)](https://postimg.cc/gwbVds43)

[![tracer-1.png](https://i.postimg.cc/JhMRtZHh/tracer-1.png)](https://postimg.cc/K1q6HKNX)

1. Realizar pruebas de diagnostico [PING][4_3] y [TRACEROUTE][4_4] desde un computador conectado via UTP.

[![ping.png](https://i.postimg.cc/MK64c5dN/ping.png)](https://postimg.cc/F16G8ytV)

[![tracer.png](https://i.postimg.cc/yYLG0RGd/tracer.png)](https://postimg.cc/6yGzX8tJ)

1. Realizar pruebas de diagnostico [PING][4_3] y [TRACEROUTE][4_4] desde un computador conectado via WIFI.

[![ipp.png](https://i.postimg.cc/wTQjd9BJ/ipp.png)](https://postimg.cc/N5Lc6qmf)

[![trracer.png](https://i.postimg.cc/RZPCNGKZ/trracer.png)](https://postimg.cc/YvWBP6d5)


1. Realizar un backup de la configuración del equipo.

para hacer una copia de la configuracion de nuestro router, nos vamos al apartado de files en el menu del router mikrotik.  

[![1.png](https://i.postimg.cc/nLyxx83x/1.png)](https://postimg.cc/2q7Mdtp9)

Ya en la siguiente ventana le vamos a dar click en la opcion de backup, y se desplegara una ventana donde pondremos el nombre de la backup que vamos a hacer. 

Despues de hacer esto podemos arrastrar el archivo generado en nuestro router al escritorio de nuestra pc para guardarlo en un lugar seguro.

[![back.png](https://i.postimg.cc/FRCjzZJh/back.png)](https://postimg.cc/r0WdY5JH)

## 9. [Diagrama de Red](#) ✔
- Realice un diagrama topológico de cada uno de los casos de estudio.
- Incluya todos los detalles de la red de area local a la que se encuentra conectado.
- Incluya los saltos conocidos incluyendo el equipo de borde de su ISP.

## 10. [Preguntas de conocimiento](#) ✔
1. ¿Que diferencias hay entre cada una de las implementaciones? (Ventajas y Desventajas)
1. ¿Que diferencias existe en el retardo via WIFI vs el retardo via UTP? (Justifique)
1. ¿Cual es la puerta de enlace a internet? ¿Cual es la ruta por defecto? En el punto (8)
1. ¿Existe diferencia en las trazas hacia los DNS en internet, para cada medio de transmisión y dispositivo? (Justifique)

[psk]:https://es.wikipedia.org/wiki/Pre-shared_key
[dhcp]:https://es.wikipedia.org/wiki/Protocolo_de_configuraci%C3%B3n_din%C3%A1mica_de_host
[wlan]:https://es.wikipedia.org/wiki/Red_de_%C3%A1rea_local_inal%C3%A1mbrica
[4_1]:https://www.tp-link.com/ar/support/faq/497/
[4_2]:https://static.tp-link.com/res/down/doc/TL-WR840N(ES)_V2_QIG.pdf
[4_3]:https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ping
[4_4]:https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/tracert
[4_5]:https://www.tp-link.com/co/home-networking/wifi-router/tl-wr840n/
[6_1]:https://consumer.huawei.com/co/support/content/es-us15855743/
[6_2]:https://forum.huawei.com/enterprise/es/%C2%BFc%C3%B3mo-iniciar-sesi%C3%B3n-en-ont-de-huawei/thread/636939-100243
[6_3]:https://play.google.com/store/apps/details?id=com.lipinic.ping&hl=es_419&gl=US
[6_4]:https://docs.python.org/3.10/library/http.server.html
[6_5]:https://support.huawei.com/enterprise/es/access-network/echolife-hg8546m-pid-21465065
[8_1]:https://wiki.mikrotik.com/wiki/Manual:Reset
[8_2]:https://wiki.mikrotik.com/wiki/Manual:Winbox
[8_3]:https://wiki.mikrotik.com/wiki/Manual:Interface/Ethernet
[8_4]:https://wiki.mikrotik.com/wiki/Manual:Interface/Bridge
[8_5]:https://wiki.mikrotik.com/wiki/Manual:IP/Address
[8_6]:https://wiki.mikrotik.com/wiki/Manual:IP/Pools
[8_7]:https://wiki.mikrotik.com/wiki/Manual:Tools/Ping
[8_8]:https://wiki.mikrotik.com/wiki/Manual:Troubleshooting_tools

---
## Mas Recursos
- [Wiki Mikrotik](https://wiki.mikrotik.com/wiki/Main_Page) (Wiki)
- [Video-Curso Mikrotik](https://www.youtube.com/watch?v=SLAPzl-LSc0&list=PLf0g2cV4iCkH19_UhaVt0vDn1f9ObumjF) (Wiki)
- [Direccionamiento IP](https://es.wikipedia.org/wiki/Direcci%C3%B3n_IP) (Wikipedia)
- [Calculadora IP](https://www.calculator.net/ip-subnet-calculator.html) (Wikipedia)

---
## Evaluación y rúbrica
- Fecha máximo entrega: 05 de Mayo de 2023
- Hora de entrega: 11:59pm	
- Nota máxima: 5.0 
- Número de actividades: 10
- Valor de cada actividad: 0.5
- Ponderación: 20%
- $\color{#DD69DD}{\text{...Carpe Diem}}$