# Telematics
<p><code>Fundamentos de Telemática</code></p>
<p>Creado por <code>GncDev</code> para explicar los fundamentos de los <code>Sistemas de comunicaciones</code> en los cursos de telemática y redes de computadores.</p>

# Practica de laboratorio 05 - Enrutamiento Dinámico OSPF

## Objetivos 

### Objetivo General
Proporcionar el conocimiento y generar las habilidades necesarias en la configuración y gestión de dispositivos de redes.

### Objetivos Específicos:
- Conocer configuraciones básicas de enrutamiento dinámico con MikroTik. :+1:

---

## Parámetros:
Para todos los efectos:
* la letra G  de se reemplaza por el número de grupo de laboratorio.
* la letra C  de se reemplaza por el ultimo número de cédula del estudiante..


## 1. [Configurar el entorno de trabajo](#) ✔
1. Cree si no existe el repositorio llamado <code>Redes-dos</code>.
1. Crear una carpeta en este repositorio llamado <code>Laboratorio-cinco</code>.
1. Invite a los compañeros de grupo como colaboradores en este repositorio.
1. Documente cada uno de los items a continuación con capturas de pantalla y código.

>Nota: recuerde que los [parámetros](#parámetros) son validos en todo el laboratorio.

[1_2]:https://github.com/GiancarloBenavides

## 2. [Preguntas reflexivas de ambientación](#) ✔

<ol type="a">
<li>¿Como funcionan los servidores HTTP?</li>
<li>¿Que son las interfaces virtuales y de loopback?.</li>
<li>¿Cual es el algoritmo y la métrica que implementa OSPF?.</li>
<li>¿Que diferencias hay entre RIP y OSPF?. (Ventajas y Desventajas)</li>
<li>¿Que diferencias hay entre un area OSPF y un sistema autónomo?.</li>

</ol>

## 3. [Configuración básica MikroTik-01](#) ✔
1. Conecte los equipos a la red eléctrica.

[![Whats-App-Image-2023-06-13-at-6-53-41-PM.jpg](https://i.postimg.cc/pdVz4rRk/Whats-App-Image-2023-06-13-at-6-53-41-PM.jpg)](https://postimg.cc/DSDSb2Wb)

1. [Reinicie][3_1] los dispositivos a la configuración de fabrica.

> /system reset no-defaults

1. Conecte la ultima interfaz [RJ45][rj45] del router al PC de configuración.

[![Whats-App-Image-2023-06-23-at-7-41-18-PM.jpg](https://i.postimg.cc/kXKZTgYQ/Whats-App-Image-2023-06-23-at-7-41-18-PM.jpg)](https://postimg.cc/dLQ41wY3)

1. [Acceder][3_2] al dispositivo por el puerto 8291 via WinBox.

[![2.png](https://i.postimg.cc/HxRxWP7m/2.png)](https://postimg.cc/jw6KZcX3)

1. Cambiar el nombre del dispositivo para [identificarlo][3_3] como <code>R1</code>.

> /system identity set name=R1

1. Etiquetar las [interfaces][3_4] a utilizar (2 WAN y una LAN).

> /interface comment ether1 comment="WAN M"

> /interface comment ether2 comment="WAN 2"

> /interface comment ether3 comment="LAN"

> /interface comment ether4 comment="LAN"

> /interface comment ether5 comment="LAN"

1. Agregar un [bridge][3_6] y sus interfaces para la red LAN.

> /interface bridge add name=bridge_lan

1. Agregar el direccionamiento para las dos redes externas WAN y la red interna LAN.
    1. Agregar la [dirección][5_1] de la interfaz externa que conecta con R2 en el segmento IP 10.1.1.0/24.

     > /ip address add address=10.1.1.1/24 interface=ether1

    > /ip address add address=10.1.1.100/24 interface=ether1

    1. Agregar la [dirección][5_1] de la interfaz externa que conecta con R3 en el segmento IP 10.3.1.0/24.
  
  > /ip address add address=10.3.1.1/24 interface=ether2

    1. Agregar la [dirección][5_1] del bridge (interna) con una IP 192.168.1.1 privada, clase C.

  > /ip address add address=192.168.1.1/24 interface=bridge_lan

1. Agregar un [Pool][5_2] en el segmento de la LAN que asigne direcciones entre 192.168.1.100-192.168.1.150.

 > /ip pool add name=pool_dhcp_lan ranges=192.168.1.100-192.168.1.150

1. Agregar un servidor [DHCP][5_3] y la información de puerta de enlace y DNS que enviara a los PC conectados a la LAN. 

 > /ip dhcp-server add name=dhcp_lan interface=bridge_lan address-pool=pool_dhcp_lan disabled=no

> /ip dhcp-server network add address=192.168.100.0/24 gateway=10.1.1.1 dns-server=8.8.8.8,2.2.2.2

1. Convertir a [estático][5_4] el arrendamiento DHCP para la MAC del PC de configuración.

 > /ip dhcp-server lease add address="192.168.100.10" client-id="R1" server="dhcp_lan" mac-address=[/ip dhcp-server lease get number=0 mac-address]


1. Agregar una regla NAT en el cortafuegos para garantizar el enrutamiento en sistemas de IP publica como internet.

 > /ip dns set servers=8.8.8.8,2.2.2.2 allow-remote-requests=yes
    1. Crear una regla [source NAT][5_5] en el cortafuegos para los paquetes IP que salen hacia la WAN.
    1. Agregar una acción para que la regla anterior permita enmascarar la ip de origen.

1. Agregar una regla NAT en el cortafuegos para mapear ([Port Forwarding][fwd]) un servicio web de la red LAN. 

    > /ip firewall nat add chain=srcnat action=masquerade out-interface="ether1"
    1. Crear una regla [destination NAT][5_6] para el protocolo TCP para los paquetes que llegan desde la WAN por el puerto HTTP 80 .

    > /ip firewall nat add chain=dstnat dst-port=80 protocol=tcp action=dst-nat to-address="192.168.100.10" to-port=8080

    1. Agregar una acción para que la regla anterior permita redirigir la solicitud a 192.168.1.10:8080.

    > /ip route add dst-address="192.168.100.10" gateway="10.1.1.1"
    1. levantar un [servicio Web][web] en el pc 192.168.1.10 en el puerto 8080

    

1. Agregar la [ruta por defecto][5_7] 0.0.0.0/0.

```bash
# El servidor HTTP DEV puede servir para ejecutar un servicio de prueba
# En Win32 para servir el contenido de la carpeta public en el puerto 8080
.\devd.exe -aol --port=8080 .\public
```

## 4. [Configurar enrutamiento MikroTik-01](#) ✔
1. Agregar una [dirección de bucle invertido][8_1] (Virtual) que esta siempre activa para identificar el router en la red OSPF.

    1. Crear un puente de red llamado "loopback"
    
    > /interface bridge add name="loopback"

    1. Agregar una dirección 10.255.255.1/32 a ese puente

    > /ip address add address="10.255.255.1/32" interface="loopback"
1. Habilitar una instancia [OSPF][8_2] identificada con la IP de "loopback"
 
 > /routing ospf instance set 0 router-id="10.1.1.1"


1. Agregar las [interfaces][8_3] que compartirán rutas OSPF y configurar las métricas.

 > /routing ospf interface add interface=ether1 cost=10 priority=0

 > /routing ospf interface add interface=ether2 cost=100 priority=1

1. Publicar las [redes][8_4] que las interfaces OSPF deben compartir en el area "Backbone" para que los tres router conozcan la ruta a los otros dos y a sus redes LAN.

 > /routing ospf network add network=10.3.1.100/24 area=backbone
 > /routing ospf network add network=10.1.1.100/24 area=backbone

1. Realizar pruebas de diagnostico [PING][8_5] y [TRACEROUTE][8_6] desde el router a los otros router.



[![11.jpg](https://i.postimg.cc/mDC6YpwM/11.jpg)](https://postimg.cc/DJfgFgRy)

[![22.jpg](https://i.postimg.cc/W4r7CFkc/22.jpg)](https://postimg.cc/nsF7QL23)


[![evidencia.jpg](https://i.postimg.cc/0yTsBf55/evidencia.jpg)](https://postimg.cc/TKJFynWB)

## 5. [Diagrama de Red](#) ✔
- Realice un diagrama topológico de cada uno de los casos de estudio.


[![diagrama3.png](https://i.postimg.cc/3RybQMtP/diagrama3.png)](https://postimg.cc/Kk25tWSN)


