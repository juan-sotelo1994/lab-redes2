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

[![1.png](https://i.postimg.cc/ZKPPTcrK/1.png)](https://postimg.cc/crHthf9V)

8. Configurar el [DHCP][dhcp] para que asigne 20 direcciones IP entre [G](#parámetros).200-[G](#parámetros).220.

[![1.png](https://i.postimg.cc/wMLrxmV8/1.png)](https://postimg.cc/BPZpMtkM)

9. Configurar la [WLAN][wlan] de nombre y [PSK](psk) "REDES_4[G](#parámetros)" para lograr conectividad inalámbrica.

[![1.png](https://i.postimg.cc/prrDqbm0/1.png)](https://postimg.cc/ctqgLzMY)

[![1.png](https://i.postimg.cc/wMRnZrPV/1.png)](https://postimg.cc/wRHWsw9y)

Escogimos el canal 1 debido a que tiene menos trafico para que la red no tenga conflicto con otras señales.

10. Realizar pruebas [PING][4_3] a DNS Cloudflare desde el dispositivo.

[![Whats-App-Image-2023-06-13-at-10-07-30-PM.jpg](https://i.postimg.cc/1RV0nPZt/Whats-App-Image-2023-06-13-at-10-07-30-PM.jpg)](https://postimg.cc/c6Zt2pCy)

11. Realizar pruebas [PING][4_3] a DNS Cloudflare desde el computador conectado por UTP.

[![1.png](https://i.postimg.cc/kGyY0dsW/1.png)](https://postimg.cc/rRK943vp)

12. Realizar pruebas [TRACEROUTE][4_4] a DNS Google desde el router.

[![1.png](https://i.postimg.cc/rwR27D6T/1.png)](https://postimg.cc/87GY6PPX)

13. Realizar pruebas [TRACEROUTE][4_4] a DNS Google desde el Computador conectado por UTP.
[![1.png](https://i.postimg.cc/5NDN7QcC/1.png)](https://postimg.cc/mtNshDgL)
14. Realizar pruebas [TRACEROUTE][4_4] a DNS Google desde un dispositivo conectado por WIFI.
[![1.png](https://i.postimg.cc/zvfbYyk1/1.png)](https://postimg.cc/r0vFSFbh)
15. Habilitar la gestión remota del dispositivo desde cualquier IP.
[![Whats-App-Image-2023-06-16-at-10-47-03-PM.jpg](https://i.postimg.cc/FK3N1hKk/Whats-App-Image-2023-06-16-at-10-47-03-PM.jpg)](https://postimg.cc/06kLBRD9)
16. Realizar un backup de la configuración del equipo.
[![Whats-App-Image-2023-06-16-at-10-47-12-PM.jpg](https://i.postimg.cc/YSKB5Txr/Whats-App-Image-2023-06-16-at-10-47-12-PM.jpg)](https://postimg.cc/RWRYfs8y)

>Router: [TP-LINK][4_5] -> reiniciar: [Con el Router encendido dejamos presionado el botón reset durante 10 segundos hasta  LED SYS/PWR parpadee rápidamente][4_1] acceder: [conectar con la cadena admin:admin@tplinkwifi.net][4_2]

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

[![Whats-App-Image-2023-06-23-at-7-24-57-PM.jpg](https://i.postimg.cc/hvg4h5f6/Whats-App-Image-2023-06-23-at-7-24-57-PM.jpg)](https://postimg.cc/R6sxDG1L)

1. [Reinicie][8_1] los dispositivos a la configuración de fabrica.

[![Whats-App-Image-2023-06-23-at-7-59-05-PM.jpg](https://i.postimg.cc/t4DBcZ3x/Whats-App-Image-2023-06-23-at-7-59-05-PM.jpg)](https://postimg.cc/BjL5LvwS)


[![Whats-App-Image-2023-06-23-at-7-59-05-PM-1.jpg](https://i.postimg.cc/d3dWN56s/Whats-App-Image-2023-06-23-at-7-59-05-PM-1.jpg)](https://postimg.cc/7JHMfMjd)

# tenemos otra forma de reiniciar el equipo




1. Conecte los equipo mediante un patchcord (latiguillo) al equipo y a internet.

[![Whats-App-Image-2023-06-23-at-7-41-18-PM.jpg](https://i.postimg.cc/kXKZTgYQ/Whats-App-Image-2023-06-23-at-7-41-18-PM.jpg)](https://postimg.cc/dLQ41wY3)

1. [Acceder][8_2] al dispositivo por el puerto 8291 via Winbox.
1. Cambiar el nombre del dispositivo para identificarlo.
1. Cambiar la contraseña del usuario "admin" a "Redes_2".
1. Configurar las [interfaces][8_3] y el [bridge][8_4] (conmutador) para dos redes (Interna y externa).
1. Agregar la [dirección][8_5] de la interfaz externa en el segmento necesario para acceder a internet.
1. Agregar la [dirección][8_5] del bridge (interna) con una IP privada, clase A.
1. Agregar un [Pool][8_6] en el segmento de la LAN que asigne direcciones entre [GG](#parámetros).100-[GG](#parámetros).200.
1. Configurar el [DHCP][dhcp] y las rutas estáticas necesarias para lograr conectividad de la red interna con internet.
1. Configurar la [WLAN][wlan] de nombre y [PSK](psk) "REDES_4[G](#parámetros)" para lograr conectividad inalámbrica.
1. Realizar pruebas de diagnostico [PING][8_7] y [TRACEROUTE][4_4] desde el router.
1. Realizar pruebas de diagnostico [PING][4_3] y [TRACEROUTE][4_4] desde un computador conectado via UTP.
1. Realizar pruebas de diagnostico [PING][4_3] y [TRACEROUTE][4_4] desde un computador conectado via WIFI.
1. Realizar un backup de la configuración del equipo.

>ROUTER: [MikroTik][8_5] -> reiniciar:[Con el botón de reset presionado encendemos el equipo. Dejamos presionado el botón reset durante 2-3 segundos hasta que veamos parpadear alguno de los LEDs de servicio][8_1] Acceder:[instale winbox y acceda por la pestaña "Neighbors" Login:admin y Password:admin][8_2]

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