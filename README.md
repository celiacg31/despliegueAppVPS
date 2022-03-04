# Tarea FTP - despliegue de aplicación en VPS

Despliegue de aplicación Full Stack en VPS

>Trabajo realizado por Jennifer Diez, Eresma Ibañez y Celia Corrales

## Reparto de tareas
Las tarea ha sido realizada por los tres miembros de forma simultánea en cuanto al despliegue de la aplicación. En cuanto al resto del trabajo:  
  -El repositorio Git así como la tabla de planificación han sido realizados por Celia.  
  -La recopilación de comandos ha sido recogida por Jennifer, siguiendo los videotutoriales aportados para la tarea.  
  -La composición final de la documentación de la tarea ha sido realizada por Eresma.  
  
## Planificación)
![](https://github.com/celiacg31/despliegueAppVPS/blob/275d054ae5299cad1459101b92ec8a5c00e11501/captura1.PNG)

## URL

1. Url del repositorio Github



2. Url del video explicativo de la tarea

https://www.loom.com/share/dab4b1bf71044efb91755f93c119d938

## Pasos



### Parte Frontend con angular

Instalamos un servidor apache

Desde el visual studio code modificamos los archivos que vamos a subir, eliminamos la carpeta de dist para volver a generarla con ng build --prod, una vez generado, me conecto en filezilla me sitúo en /var/www/html , selecciono todos los archivos del dist y los subo.

Le damos permisos para poder verlo en el navegador con sudo chmod -R 755 /var/www/html 


![](https://github.com/celiacg31/despliegueAppVPS/blob/c155e5379f0c8b159e9606d4f1d988cc602302d8/Im%C3%A1genes/03.PNG)

![](https://github.com/celiacg31/despliegueAppVPS/blob/e5be48e9cce8b9aa7d5baa51545928a8b836ea82/Im%C3%A1genes/04.PNG)

Configuramos el servidor apache para que soporte SSL, habilitamos el modo ssl, reiniciamos

Creamos una copia de seguridad de los archivos y editamos los archivos 000-default.conf y apache2.conf, los habilitamos y reiniciamos.

![](https://github.com/celiacg31/despliegueAppVPS/blob/c155e5379f0c8b159e9606d4f1d988cc602302d8/Im%C3%A1genes/02.PNG)

![](https://github.com/celiacg31/despliegueAppVPS/blob/e5be48e9cce8b9aa7d5baa51545928a8b836ea82/Im%C3%A1genes/05.PNG)

Configuro el spring para que sea un modo seguro creando un certificado

![](https://github.com/celiacg31/despliegueAppVPS/blob/d7b9a4fce4c4f59c042f3f3f429fbc2230ac7caa/Im%C3%A1genes/07.png)

![](https://github.com/celiacg31/despliegueAppVPS/blob/e5be48e9cce8b9aa7d5baa51545928a8b836ea82/Im%C3%A1genes/06.PNG)

![](https://github.com/celiacg31/despliegueAppVPS/blob/d7b9a4fce4c4f59c042f3f3f429fbc2230ac7caa/Im%C3%A1genes/08.png)

![](https://github.com/celiacg31/despliegueAppVPS/blob/d7b9a4fce4c4f59c042f3f3f429fbc2230ac7caa/Im%C3%A1genes/09.png)

![](https://github.com/celiacg31/despliegueAppVPS/blob/d7b9a4fce4c4f59c042f3f3f429fbc2230ac7caa/Im%C3%A1genes/10.png)

![](https://github.com/celiacg31/despliegueAppVPS/blob/d7b9a4fce4c4f59c042f3f3f429fbc2230ac7caa/Im%C3%A1genes/11.png)

![](https://github.com/celiacg31/despliegueAppVPS/blob/d7b9a4fce4c4f59c042f3f3f429fbc2230ac7caa/Im%C3%A1genes/12.png)

![](https://github.com/celiacg31/despliegueAppVPS/blob/d7b9a4fce4c4f59c042f3f3f429fbc2230ac7caa/Im%C3%A1genes/13.png)






