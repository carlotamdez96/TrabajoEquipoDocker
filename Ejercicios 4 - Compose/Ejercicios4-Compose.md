
# Ejercicio 4 - Docker Compose
## Desplegar la aplicación cmatrix utilizando docker-compose.

Lo primero de todo, instalamos Docker Compose:

```
apt install docker-compose
```

![](Imagenes/1.png)



![](Imagenes/2.png)

Con un contenedor que hemos creado de prueba lo tratamos de subir a docker hub para trabajar con el en el compose

```
docker commit ubumatrix saulom/ubumatrix:version1
```

![](Imagenes/3.png)

```
docker login

docker push saulom/ubumatrix:lastest

```

![](Imagenes/4.png)

Con esto intentamos hacer un docker-compose.yml: (con fallidos resultados)

![](Imagenes/11.png)

Tratamos de redactar un Dockerfile, pero como cmatrix requiere unos cuantos parametros de configuración la instalación falla

![](Imagenes/5.png)

Para ver como hubiera sido una instalación correcta creamos un contenedor

```
docker run -d -it --name ubugreenrain ubuntu

docker exec -it ubugreenrain bash

apt-update

apt-get install cmatrix
```

![](Imagenes/6.png)

Con esto el efecto cmatrix normal funcionaria, pero nosotros queremos además conseguir el efecto "greenrain"

Para ello debemos instalar unas dependencias

```
apt-get install git build-essential libncurses5-dev

```

![](Imagenes/7.png)

Clonamos el github de greenrain

```
git clone https://github.com/aguegu/greenrain
```

![](Imagenes/8.png)

Movemos los archivos a /usr/local/bin

```
mv /Descargas/greenrain/greenrain /usr/local/bin/
```

![](Imagenes/9.png)

Para ejecutarlo simplemente ejecutaremos
```
greenrain
```

y para salir "q"
![](Imagenes/10.png)