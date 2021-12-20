# Configuración de rutas dinámicas de enrutamiento utilizando OSPFv2 
author: Jesús
summary: Práctica 2
id: Práctica 2
categories: codelab,markdown
environments: Web
status: Published
feedback link: https://github.com/JesusJimenezSantana/HARDENING/issues

## Configurar las redes en los routers
Duration: 00:10:00

### Configuración 

Primero entraremos en el modo de configuración y luego escribimos: router ospf 1(ID:debe ser el mismo en todos los routers).
Y luego vamos añadiendo las redes conectadas directamente al router y su WILDCARD (máscara inversa de red), y un area de efecto la cuál estableceremos como 0 si no es OSPF multiárea:


![routerOspf](routerOspf.png)


## Configurar las interfaces pasivas
Duration: 00:10:00

### Configuración

Configuraremos en cada router unas interfaces pasivas, éstas no mandarán los paquetes OSPF por lo que reduciremos el tráfico de red.
Para esto entraremos en la configuración global del router y desde ahí a la configuración de OSPF donde introduciremos las interfaces que queramos configurar como pasivas:

![interfacespasivas](interfacespasivas.png)


## Configurar encriptación md5 
Duration: 00:10:00

### Configuración

Primero habilitaremos los mensajes encriptados en cada router, para ello iremos a la configuración de OSPF.
Luego tendremos que encriptar los mensajes para cada interfaz, para esto vamos a cada interfaz y le estableceremos una contraseña encriptada por md5 (DEBE SER LA MISMA ENTRE VECINOS): 

![ospfmd5](ospfmd5.png)

