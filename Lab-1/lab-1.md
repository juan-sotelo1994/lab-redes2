# Laboratorio de redes 2 
<p><code>Laboratorio 1 de redes 2</code></p>
<p>Realizado <code>Juan David Sotelo</code>

## 1.[Configurar el entorno de trabajo](#) ✔

<ol type="a">


<li>¿Cual es la dirección de red y de broadcast de un host que tiene una ip 192.168.10.10/30 .? </li>

### Respuesta:

1. la direccion de broadcast es: 192.168.10.11<br>
2. la primera direccion ip es : 192.168.10.9 <br>
3. la utlima direccion ip es: 192.168.10.10 <br>
4. la direccionde subred es: 192.168.10.8/30<br>

<li>¿Cuantos clientes puede tener la sub red 172.16.0.0/22?.<</li>

### Respuesta:

<li> ¿Que clase y tipo de dirección es 10.10.10.0/24?.</li>

### Respuesta:

<li> ¿Que información se puede inferir de la dirección 169.254.255.200/26?.</li>

### Respuesta:

<li>¿Que información se puede inferir de la dirección 169.254.255.200/26?.</li>

### Respuesta:

## 2. [Caracterización de los adaptadores del compu](#) ✔
|parametro||valor|
|--|:--:|--:|
|Número de adaptadores Físicos|-->|2|
|Número de adaptadores Virtuales|-->|0|
|Tipo de Adaptador principal|-->|ethernet-W-fi|
|Fabricante del Adaptador principal|-->|Intel Corporation|
|Código MAC del fabricante|-->|28-80-23-D4-78-44|
|MAC|-->|80-86-F2-7C-2E-BE|


## 3. [Caracterización de la red Interna](#) ✔
|Parámetro|Valor|
|--|--:|
|__Subnet__|192.168.10.0/24|
|IPv4|192.168.10.128|
|Subnet Mask decimal|24|
|Subnet Mask octetos|255.255.255.0|
|Número de direcciones de Host|254|
|Rango de direcciones de Host|192.168.10.100-199|
|IP Broadcast|192.168.10.255|
|Server DHCP inicial |192.168.10.100| 
|Server DHCP final |192.168.10.199| 
|Server DNS|8.8.8.8|

## 3. [Caracterización de la red provedor](#) ✔
|Parámetro|Valor|
|--|--:|
|__Subnet__|192.168.1.0/24|
|IPv4|192.168.1.2|
|Subnet Mask decimal|24|
|Subnet Mask octetos|255.255.255.255|
|Número de direcciones de Host|2|
|Rango de direcciones de Host|192.168.125.25-26|
|IP Broadcast|192.168.125.25|
|Server DHCP inicial |inactivo| 
|Server DNS|8.8.8.8|
|Server DNS|8.8.4.4|



## 4. [Caracterización de la puerta de enlace](#) ✔
|Parámetro|Valor|
|--|--:|
|Número de Entradas en la tabla ARP |10|
|IPv4 Gateway|192.168.10.1|
|MAC Gateway|98-da-c4-63-c7-8e|
|ISP|Sistemas Palacios|
|[IP Publica][5]|8.242.185.21|
|Sistema Autónomo|AS264646|

## 5. [Retardo de la red](#) ✔
|Servidor|IP|Tiempo promedio/ms|
|--|--|--|
|DNS Google|8.8.8.8|18ms|
|DNS Google|8.8.4.4|15ms|
|DNS Cloudflare|1.1.1.1|15ms|
|OpenDNS|208.67.222.222|126ms|
|OpenDNS|208.67.220.220|121ms|
|Alternate DNS|	76.76.19.19|16ms|
|Alternate DNS|	76.223.122.150|17ms|
|DNS Quad9|9.9.9.9|18ms|
|AdGuard DNS|94.140.14.14|130ms|
|AdGuard DNS|94.140.15.15|130ms|

## 6. [Capacidad del canal](#) ✔
|Servidor|Ping/ms|Down/MB|Up/MB|
|--|:--:|--:|--:|
|[speed test][1]|21|24.05|24.14|
|[Netflix][2]|32|80|60|
|[Claro][3]|14  |24.9|24.8|
|[nperf][4]|18.00|24.67|24.57|


## 7. [Distancia desde el host](#) ✔
|Servidor|Ping/ms|Numero de Saltos|
|--|:--:|--:|
|google.com|17|13|
|GMail.com|21|13|
|YouTube.com|18|18|
|dns.google|38|18|
|aws.amazon.com|15|17|
|portal.azure.com|15|13|
|login.live.com|98|20|
|Facebook.com|10|13|
|c.ns.WhatsApp.net|132|14|
|claro.com.co|151|12|
|platzi.com|75|15|
|rappi.com.co|145|30|


## 8. [Diagrama de Red](#) ✔
- Realice un diagrama topológico de la red que le ofrece conectividad a internet.
- Incluya todos los detalles de la red de area local a la que se encuentra conectado.
- Incluya los saltos conocidos incluyendo el equipo de borde de su ISP.

## 9. [Preguntas de conocimiento](#) ✔
1. Cual es la dirección de red y de broadcast de un host que tiene una ip 192.168.10.10/30.
1. Cuantos equipos o.
1. Incluya los saltos conocidos incluyendo el equipo de borde de su ISP.