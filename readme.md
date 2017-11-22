#EJERCICIO DE REDES#

----------


## He realizado un ejercicio con Cisco Packet Tracer, en el cual he creado cinco redes con las siguientes características: ##

## RED 1 ##
Tres subredes (VLSM), una que soporta 100 host, otra que soporta 30 y por último una para 6 host. Sólo esta última puede salir fuera. Cada una tiene cuatro ordenadores conectados.
Para calcular la red 1
Calculo a partir del número de host que va a tener cada una:


-  Los host encontrados.
-  La dirección de red de cada host.
-  La máscara de red. 
-  La 1ª dirección IP de cada red.
-  La última dirección IP .
-  El Broatcast.


![Calculo red 1](http://lengmarjorge.webcindario.com/imagenes/calculoredes.jpg)

Una vez calculado configuro cada una de las subredes con los resultados obtenidos.



**La subred 1** de clase C tiene 3 ordenadores con IP fija que puede ir desde la 192.168.0.1 hasta la 192.168.0.126 con máscara de red 255.255.255.128, en esta red he puesto tres ordenadores con la siguiente configuración

![](http://lengmarjorge.webcindario.com/imagenes/subred1.jpg)

En esta imagen podemos ver la configuración de uno de sus ordenadores:

![](http://lengmarjorge.webcindario.com/imagenes/subred1-1.jpg)

**La subred 2** de clase C tiene 3 ordenadores con IP fija que puede ir desde la 192.168.0.129 hasta la 192.168.0.158 con máscara de red 255.255.255.224, en esta red he puesto tres ordenadores con la siguiente configuración

![](http://lengmarjorge.webcindario.com/imagenes/subred2.jpg)

En esta imagen podemos ver la configuración de uno de sus ordenadores:

![](http://lengmarjorge.webcindario.com/imagenes/subred2-1.jpg)

**La subred 3** de clase C tiene 3 ordenadores con IP fija que puede ir desde la 192.168.0.161 hasta la 192.168.0.166 con máscara de red 255.255.255.166, en esta red he puesto tres ordenadores con la siguiente configuración.

![](http://lengmarjorge.webcindario.com/imagenes/subred3.jpg)

Esta red tiene puerta de enlace 192.168.0.163 ya que puede salir fuera
En esta imagen podemos ver la configuración de uno de sus ordenadores:

![](http://lengmarjorge.webcindario.com/imagenes/subred3-1.jpg)

## RED 2 ##

Una red con 8 ordenadores con DHCP:

Esta red la he dotado de un servidor con DHCP configurado para que administre a los ordenadores de una red de clase C desde la IP 192.168.1.1 hasta la 192.168.1.245, con máscara de red 255.255.255.0
La configuración del servidor es:

![](http://lengmarjorge.webcindario.com/imagenes/red2-1.jpg)

La configuración del DHCP:

![](http://lengmarjorge.webcindario.com/imagenes/red2-2.jpg)

Y la de uno de los ordenadores conectados a la red:

![](http://lengmarjorge.webcindario.com/imagenes/red2-3.jpg)

Por lo tanto nos quedaría así la red 2:

![](http://lengmarjorge.webcindario.com/imagenes/red2.jpg)

## RED 3 ##
Una red con 4 ordenadores con DHCP:

Esta red es similar a la descrita anteriormente, la he dotado de un servidor con DHCP configurado para que administre la red de clase C desde la IP 192.168.3.1 hasta la 192.168.3.245, con máscara de red 255.255.255.0 
La configuración del servidor es:

![](http://lengmarjorge.webcindario.com/imagenes/red3-1.jpg)

La configuración del DHCP:

![](http://lengmarjorge.webcindario.com/imagenes/red3-2.jpg)

Y la de uno de los ordenadores conectados a la red:

![](http://lengmarjorge.webcindario.com/imagenes/red3-3.jpg)

Por lo tanto nos quedaría así la red 2:

![](http://lengmarjorge.webcindario.com/imagenes/red3.jpg)

## RED 4 ##

Red con	4 ordenadores con IP fija, un punto de enlace con 5 ordenadores con DHCP.
En esta he montado 4 ordenadores en la red de clase C 192.168.2.X y máscara de red 255.255.255.0
La configuración de uno de ellos sería:

![](http://lengmarjorge.webcindario.com/imagenes/red4-1.jpg)

Para las direcciones DCHP he montado un servidor con la siguiente configuración:

![](http://lengmarjorge.webcindario.com/imagenes/red4-2.jpg)

![](http://lengmarjorge.webcindario.com/imagenes/red4-3.jpg)

Por lo tanto uno de los ordenadores con DCHP quedaría con la siguiente configuración:

![](http://lengmarjorge.webcindario.com/imagenes/red4-4.jpg)

Y la red 4 tendría esta forma:

![](http://lengmarjorge.webcindario.com/imagenes/red4.jpg)

## RED 5 ##

5 Ordenadores con IP fija:
Esta red es muy similar a la primera que he descrito cada uno de los ordenadores tendría una IP fija dentro de la red de clase C 192.168.4.X y máscara de red 255.255.255.0, la configuración de uno de ellos es:

![](http://lengmarjorge.webcindario.com/imagenes/red5-1.jpg)

Y esta red quedaría así:


![](http://lengmarjorge.webcindario.com/imagenes/red5.jpg).


    Una vez configuradas las redes voy a proceder a conectarlas mediante cuatro  router.


![](http://lengmarjorge.webcindario.com/imagenes/router.jpg)
> 
> **El router 1** conecta la red 1 y su configuración es:

![](http://lengmarjorge.webcindario.com/imagenes/router1.jpg)

La dirección de red 192.168.0.162 lo conecta con la red 1 y la 192.168.20.1 con el cable de serie del router 2.
> 
> **El router 2** conecta la red 2 y su configuración es:

![](http://lengmarjorge.webcindario.com/imagenes/router2.jpg)

La dirección de red 192.168.1.10 lo conecta con la red 2, la 192.168.20.2 con el cable de serie del router 1 y la 192.168.21.1 con el router 3.

> 
> **El router 3** conecta la red 3 y los servidores WEB y DNS, que describiremos posteriormente, su configuración es:

![](http://lengmarjorge.webcindario.com/imagenes/router3.jpg)

La dirección de red 192.168.3.19 lo conecta con la red 3, la 192.168.10.1 con los servidores, la 192.168.21.2 con el cable de serie del router 2 y la 192.168.22.1 con el router 4.

> 
> **El router 4** conecta la red 4 y 5, su configuración es:

![](http://lengmarjorge.webcindario.com/imagenes/router4.jpg)

La dirección de red 192.168.2.2 lo conecta con la red 4, la 192.168.4.2 con la red 5 y la 192.168.22.2 con el cable de serie del router 3.

`Por último he montado tres servidores web que alojan tres páginas`
`diferentes y un servidor DNS para resolver los nombres de estas páginas, `
`todos conectados al router 3 como ya he descrito antes`

![](http://lengmarjorge.webcindario.com/imagenes/servidores.jpg)

> El servidor que aloja la página WEB www.albacete.es, que muestra una foto de Albacete tiene la siguiente configuración: 

![](http://lengmarjorge.webcindario.com/imagenes/albacete1.jpg)

La página web se vería desde un ordenador de la red 2 por ejemplo así:


![](http://lengmarjorge.webcindario.com/imagenes/albacete2.jpg)

> El servidor que aloja la página WEB www.wagner.es, que muestra una foto de Wagner tiene la siguiente configuración: 

![](http://lengmarjorge.webcindario.com/imagenes/wagner1.jpg)

La página web se vería desde un ordenador de la subred 3 de la red 1, que es la que tiene acceso exterior, por ejemplo así:

![](http://lengmarjorge.webcindario.com/imagenes/wagner2.jpg)

> El servidor que aloja la página WEB www.dilar.com, que muestra una foto de Dilar tiene la siguiente configuración: 

![](http://lengmarjorge.webcindario.com/imagenes/dilar1.jpg)

La página web se vería desde un ordenador de la red 4 con dirección IP DCHP por ejemplo así:

![](http://lengmarjorge.webcindario.com/imagenes/dilar2.jpg)

> Por último el servidor DNS, para resolver las direcciones WEB anteriores tiene la siguiente configuración: 

![](http://lengmarjorge.webcindario.com/imagenes/servidordns.jpg)

Esta dirección DNS la he puesto en todos los ordenadores que van a solicitar estas páginas WEB y he configurado este servidor con las IP de cada servidor WEB de esta forma:

![](http://lengmarjorge.webcindario.com/imagenes/servidordns1.jpg)

Por último muestro la imagen del conjunto de toda la red

![](http://lengmarjorge.webcindario.com/imagenes/red.jpg)


----------

Trabajo de Jorge Ortega González, para la clase de Sistemas Informáticos de 1ª de DAM en el IES Francisco Ayala.

----------











