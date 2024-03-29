# Telematics
<p><code>Fundamentos de Telemática</code></p>
<p>Creado por <code>GncDev</code> para explicar los fundamentos de los <code>Sistemas de comunicaciones</code> en los cursos de telemática y redes de computadores.</p>

# Practica de laboratorio 03 - Enrutamiento estático

## Objetivos 

### Objetivo General
Proporcionar el conocimiento y generar las habilidades necesarias en la configuración y gestión de dispositivos de redes.

### Objetivos Específicos:
- Conocer configuraciones básicas de enrutamiento estático con MikroTik. :+1:

---

## Parámetros:
Para todos los efectos:
* la letra G  de se reemplaza por el número de grupo de laboratorio.
* la letra C  de se reemplaza por el ultimo número de cédula del estudiante..


## 1. [Configurar el entorno de trabajo](#) ✔
1. Cree si no existe el repositorio llamado <code>Redes-dos</code>.
1. Crear una carpeta en este repositorio llamado <code>Laboratorio-tres</code>.
1. Invite a los compañeros de grupo como colaboradores en este repositorio.
1. Documente cada uno de los items a continuación con capturas de pantalla y código .

>Nota: recuerde que los [parámetros](#parámetros) son validos en todo el laboratorio.

## 2. [Preguntas reflexivas de ambientación](#) ✔

<ol type="a">
<li>¿Que es y como se configura la ruta por defecto?</li>
    
R/ Habitualmente la ruta por defecto es una ruta estática definida en el router de borde que tiene como próximo salto el router de acceso del ISP.

<li>¿Que es la distancia administrativa?.</li>

R/ la distancia administrativa de una ruta es cuando usa Rutas estáticas para hacer una copia de seguridad de una ruta IGP que existe actualmente. Esto normalmente se usa para abrir un enlace de respaldo cuando falla el primario.

<li>¿Que es una red directamente conectada y cual es su distancia administrativa?.</li>

R/ Una red directamente conectada es una red que se encuentra conectada físicamente a otro dispositivo o red sin la necesidad de pasar a través de enrutadores o dispositivos intermedios. Esto significa que los dispositivos en la red directamente conectada pueden comunicarse entre sí sin requerir la intervención de un enrutador para determinar la ruta correcta.

<li>¿Que es una ruta estática?.</li>

R/ Una ruta estática es una entrada de enrutamiento que se configura manualmente en un enrutador o dispositivo de red. En contraste con las rutas dinámicas, que se aprenden automáticamente mediante protocolos de enrutamiento, las rutas estáticas son creadas y mantenidas por un administrador de red.

<li>¿Que es una ruta dinámica?.</li>

R/ En el contexto de tecnologías de red y enrutamiento, el término "ruta dinámica" se refiere a una ruta que es determinada automáticamente por un protocolo de enrutamiento en lugar de ser configurada manualmente por un administrador de red. Estos protocolos de enrutamiento son utilizados en redes de computadoras para decidir cómo enviar los datos de un punto a otro a través de múltiples dispositivos interconectados, como routers y switches.

</ol>

## 3. [Configuración básica MikroTik-01](#) ✔
1. Conecte los equipos a la red eléctrica.

[![Whats-App-Image-2023-06-13-at-6-53-41-PM.jpg](https://i.postimg.cc/pdVz4rRk/Whats-App-Image-2023-06-13-at-6-53-41-PM.jpg)](https://postimg.cc/DSDSb2Wb)
 
1. [Reinicie][3_1] los dispositivos a la configuración de fabrica.

Vamos a reiniciar nuestro router con la configuracion de No Default configuration, para que nuestro router quede limpio y sin ninguna configuracion predeterminada. 

[![Whats-App-Image-2023-08-20-at-7-17-04-PM.jpg](https://i.postimg.cc/T3Dt21Cg/Whats-App-Image-2023-08-20-at-7-17-04-PM.jpg)](https://postimg.cc/PCdW2XG5)

1. Conecte la ultima interfaz [RJ45][rj45] del router al PC de configuración.

[![Whats-App-Image-2023-06-23-at-7-41-18-PM.jpg](https://i.postimg.cc/kXKZTgYQ/Whats-App-Image-2023-06-23-at-7-41-18-PM.jpg)](https://postimg.cc/dLQ41wY3)

1. [Acceder][3_2] al dispositivo por el puerto 8291 via Winbox.

[![2.png](https://i.postimg.cc/HxRxWP7m/2.png)](https://postimg.cc/jw6KZcX3)

1. Cambiar el nombre del dispositivo para [identificarlo][3_3] como <code>R1</code>.

Con el siguiente codigo vamos a darle un nombre a nuestro router, con el cual podemos identificarlo.

> /system identity set name=R1

1. Etiquetar las [interfaces][3_4] a utilizar (2 WAN y una LAN).

creamos la interfaz WAN m y le asignamos el primer puerto.

>  /interface comment ether1 comment="WAN M"

Luego creamos otra interfaz WAN en el segundo puerto 

> /interface comment ether2 comment="WAN 2" 


1. Agregar un [bridge][3_6] y sus interfaces para la red LAN.

> /interface bridge add name=bridge_lan

> /interface bridge port add bridge=bridge_lan interface=ether3

> /interface bridge port add bridge=bridge_lan interface=ether4

> /interface bridge port add bridge=bridge_lan interface=ether5 


1. Agregar el direccionamiento para las dos redes externas WAN y la red interna LAN.
    1. Agregar la [dirección][5_1] de la interfaz externa que conecta con R2 en el segmento IP 10.11.1.0/24.

 > /ip address add address=10.11.1.1/24 interface=ether1 

1. Agregar la [dirección][5_1] de la interfaz externa que conectara redes futuras en el segmento IP 10.10.1.0/24.

> /ip address add address=10.10.1.100/24 interface=ether2

1. Agregar la [dirección][5_1] del bridge (interna) con una IP 192.168.1.1 privada, clase C.

> /ip address add address=192.168.1.1/24 interface=bridge_lan

1. Agregar un [Pool][5_2] en el segmento de la LAN que asigne direcciones entre 192.168.1.100-192.168.1.200.

> /ip pool add name=pool_dhcp_lan ranges=192.168.1.100-192.168.1.200

1. Agregar un servidor [DHCP][5_3] y la información de puerta de enlace y DNS que enviara a los PC conectados a la LAN. 

> /ip dhcp-server add name=dhcp_lan interface=bridge_lan address-pool=pool_dhcp_lan disabled=no


> /ip dhcp-server network add address=192.168.1.0/24 gateway=192.168.1.1 dns-server=8.8.8.8,2.2.2.2

1. Agregar la [ruta por defecto][5_4] 0.0.0.0/0.

> /ip route add dst-address="0.0.0.0/0" gateway="10.10.1.1"

> /ip route add gateway=10.10.1.1

## 4. [Configurar enrutamiento MikroTik-01](#) ✔
1. Agregar las [rutas estáticas][8_1] necesarias para que los tres router conozcan la ruta a los otros dos.

> /ip address add address=10.11.1.100/24 interface=ether2

> /ip address add address=10.22.1.100/24 interface=ether2

1. Realizar pruebas de diagnostico [PING][8_2] y [TRACEROUTE][8_3] desde el router a los otros router.

[![11.jpg](https://i.postimg.cc/mDC6YpwM/11.jpg)](https://postimg.cc/DJfgFgRy)

[![22.jpg](https://i.postimg.cc/W4r7CFkc/22.jpg)](https://postimg.cc/nsF7QL23)


## 5. [Diagrama de Red](#) ✔
- Realice un diagrama topológico de cada uno de los casos de estudio.
- Incluya todos los detalles de la red de area local a la que se encuentra conectado.

[![diagrama.png](https://i.postimg.cc/GpQBSGjf/diagrama.png)](https://postimg.cc/sBMDMBqP)



## 6. [Preguntas de conocimiento](#) ✔
1. ¿Por qué desde un router no se puede ingresar a las redes LAN de los otros router?

    R/ Las redes LAN son segmentos locales de red en las que se conectan dispositivos dentro de una ubicación específica, como un hogar u oficina. Cada router tiene su propia red LAN, y estas redes están separadas en términos de direcciones IP y subredes. Por lo tanto, cuando intentas acceder a las redes LAN de otros routers desde un router específico, hay varias razones por las que eso generalmente no es posible

1. ¿Es posible lograr que los PC conectados a R1 encuentren la ruta a los PC conectados en R3?
 (procedimiento)

 R/ no es posible mirar los computadores de R3 debido a que se encuentran en una red aparte y el direccionamiento no nos permite mirarlos 
1. ¿Cual es la puerta de enlace a internet para R1?

    R/ la puerta de enlace es 10.11.1.1 para el Router 1

