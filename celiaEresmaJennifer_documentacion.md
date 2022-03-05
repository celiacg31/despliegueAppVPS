---
title: Tarea FTP - Despliegue de aplicación en VPS
author: Celia Corrales, Eresma Ibáñez, Jennifer Díez
---

## Tarea FTP - Despliegue de aplicación en VPS

*:pushpin: Celia Corrales, Eresma Ibáñez y Jennifer Díez - Despliegue de Aplicaciones Web - Curso 2021/2022*



​	A continuación se detallan los pasos más relevantes en el despliegue de nuestra aplicación web. Ésta se ha desplegado en la nube privada del aula, concretamente en el servidor `172.16.21.140`.

​	Las instalaciones y configuraciones iniciales las realizaremos mediante PuTTY, un cliente SSH que nos permite conectarnos al servidor desde nuestro equipo. En primer lugar instalamos **MySQL** para trabajar con la base de datos de nuestra aplicación, la cual se llama `test_virtual`.

![01](celiaEresmaJennifer_documentacion.assets/01-16464085740621.png)

​	El siguiente paso es instalar **Java** y la herramienta de software **Maven**.

![02](celiaEresmaJennifer_documentacion.assets/02.png)

​	Instalamos además el servidor **vsFTPd**, uno de los servidores FTP más potentes y completos para Linux.

![03](celiaEresmaJennifer_documentacion.assets/03.png)

​	En este punto del proceso, pasamos a utilizar FileZilla, uno de los clientes FTP más populares que nos permite conectarnos al servidor al igual que lo hace PuTTY, pero en este caso mediante un entorno gráfico donde podemos ver los directorios, archivos, etc. Mediante FileZilla creamos la estructura de carpetas separando la parte del backend con la del frontend de nuestra aplicación.

![04](celiaEresmaJennifer_documentacion.assets/04.png)

​	Si probamos a lanzar nuestra aplicación (sin el apartado del frontend configurado todavía), comprobamos que **Spring** funciona sin problemas y que en el navegador podemos acceder al servidor.

![06](celiaEresmaJennifer_documentacion.assets/06.png)

![07](celiaEresmaJennifer_documentacion.assets/07.png)

El siguiente paso es instalar el servidor **Apache** para el despliegue de nuestra aplicación. Lo configuramos para que soporte SSL, habilitamos el modo ssl, reiniciamos. Creamos una copia de seguridad de los archivos y editamos los archivos *000-default.conf* y *apache2.conf*, los habilitamos y reiniciamos.

![002](celiaEresmaJennifer_documentacion.assets/002.PNG)

Tenemos que configurar spring para que sea un modo seguro creando un certificado.

![005](celiaEresmaJennifer_documentacion.assets/005.PNG)



![ ](celiaEresmaJennifer_documentacion.assets/006.PNG)

Se comprueba que se ha creado en la ruta correcta. Editamos el archivo properties para añadir la configuración SSL. Y Instalamos maven, comprobamos que funcione.

![007](celiaEresmaJennifer_documentacion.assets/007.png)

![008](celiaEresmaJennifer_documentacion.assets/008.png)



Subimos los archivos con el filezilla a la ruta */var/www/html*.

![009](celiaEresmaJennifer_documentacion.assets/009.png)



Comprobamos que funciona

![010](celiaEresmaJennifer_documentacion.assets/010.png)

Añadimos un usuario

![011](celiaEresmaJennifer_documentacion.assets/011.png)

![012](celiaEresmaJennifer_documentacion.assets/012.png)



![013](celiaEresmaJennifer_documentacion.assets/013.png)