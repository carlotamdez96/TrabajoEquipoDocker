# Ejercicio 5 - Imagen con DockerFile

> Carlota Menéndez Álvarez

[TOC]



**La finalización de este apartado es la creación de una imagen con un servidor web que sirva un sitio web.**

Especificaciones:

Basar la imagen en nginx o apache

Desplegar una plantilla, o un trabajo de clase, que tenga al menos, un index.html y una carpeta con estilos, imagenes, etc.

### Pasos Principales

1. Creación del directorio de trabajo

   ![image-20230203091019617](imagenes/image-20230203091019617.png)

2. Creación del contenido HTML con imagenes y estilos

   ![image-20230203092334303](imagenes/image-20230203092334303.png)

3. Crear el fichero **DockerFile**

   ![image-20230203092927096](imagenes/image-20230203092927096.png)

4. Cambio los permisos

   ![image-20230203093254290](imagenes/image-20230203093254290.png)

5. Cambio el propietario

   ![image-20230203093942259](imagenes/image-20230203093942259.png)

6. Creación del **contenedor a partir de la imagen**

   ![image-20230203094309262](imagenes/image-20230203094309262.png)

7. Hago que corra el contenedor creado

   ![image-20230203094431625](imagenes/image-20230203094431625.png)

8. Vista de la pagina en el navegador

   ![image-20230203094511851](imagenes/image-20230203094511851.png)

   ![image-20230203094534705](imagenes/image-20230203094534705.png)

   

   

   ## Subir la imagen a Dockerhub

   Primero deberemos iniciar sesión y crear un repositorio nuevo.

   ![image-20230203094951303](imagenes/image-20230203094951303.png)

   Después deberemos saber el id de la imagen para crear un tag

   ![image-20230203095137402](imagenes/image-20230203095137402.png)

   Con el siguiente comando crearemos el tag de la imagen:

   ```sh
   docker tag(2e44d46018d9) carlota96menendez/my-pagina1:latest
   ```

   ![image-20230203095438822](imagenes/image-20230203095438822.png)

   Ahora será necesario loguearse a DockerHub

   ![image-20230203095602425](imagenes/image-20230203095602425.png)

   Comando: `docker login`.

   ### Subir la imagen a DockerHub

   ````sh
   docker push carlota96menendez/my-pagina1
   ````

   ![image-20230203095809682](imagenes/image-20230203095809682.png)

   Comprobación de que se ha subido la imagen correctamente

   ![image-20230203095918858](imagenes/image-20230203095918858.png)





### Descarga de la imagen creada  por otro miembro del grupo

Desde la maquina de Saul:

![image-20230203100939232](imagenes/image-20230203100939232.png)

Comprobación del funcionamiento del contenedor:



![image-20230203101011817](imagenes/image-20230203101011817.png)

![image-20230203101030450](imagenes/image-20230203101030450.png)



​		



