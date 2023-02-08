# Ejercicio 2 Almacenamiento - Portainer

> Carlota Menéndez Álvarez

[TOC]



## Instalación Portainer

Inicialmente deberé instalar en mi maquina virtual el docker compose:

```sh
sudo apt install docker-compose
```

Una vez realizado este paso deberemos crear el directorio donde se alojará y editar este fichero.

![image-20230208101254249](imagenes/image-20230208101254249.png)

El fichero contendrá lo siguiente:

![image-20230208101405548](imagenes/image-20230208101405548.png)

**Ponemos en marcha el contenedor usando Docker Compose**

```sh
docker-compose up -p
```

![image-20230208101518935](imagenes/image-20230208101518935.png)

En el navegador accedemos al servicio Portainer que tenemos en ejecucion en Docker:

![image-20230208101652023](imagenes/image-20230208101652023.png)

![image-20230208101815046](imagenes/image-20230208101815046.png)



**Operaciones sobre contenedores**

Situación actual de mi máquina

![image-20230208103134996](imagenes/image-20230208103134996.png)



- Muestro los contenedores que tengo

![image-20230208102342258](imagenes/image-20230208102342258.png)

Borro un contenedor:

![image-20230208102743765](imagenes/image-20230208102743765.png)



- Muestro las redes que tengo

![image-20230208102502548](imagenes/image-20230208102502548.png)

Operación de borrado de una red:

![image-20230208102601741](imagenes/image-20230208102601741.png)

Muestro los contenedores que tienen una red concreta:

![image-20230208103337249](imagenes/image-20230208103337249.png)





- Muestro los volumenes

  ![image-20230208102935959](../../../AppData/Roaming/Typora/typora-user-images/image-20230208102935959.png)

  Creo un volumen nuevo:

  ![image-20230208103036998](imagenes/image-20230208103036998.png)

  Muestro los volumenes que tiene un contenedor concreto, el de portainer en este caso:

  ![image-20230208103426949](imagenes/image-20230208103426949.png)











