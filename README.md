 # City Know Pro v2 - Videojuego en plataforma WEBGL 

 Este repositorio presenta el BUILD del videojuego CITY KNOW PRO 2 desarrollado en UNITY3D v2018.4.9 para WebGL. El proposito del repositorio es desplegar el videojuego en el microservidor I3LAP. A continuación se describe el proceso de despliegue.

## DESPLIEGUE
Dentro del repositorio se encuentra la siguiente estructura de carpetas:

-  	Build
-  	StreamingAssets
- 	TemplateData
- 	index.html

además de los archivos,

- 	README.md
- 	version.json

**Nota:** el archivo version.json será el encargado de gestionar las versiones de despliegue

### Paso 1: Desplegar el sistema de información de CITY KNOW PRO en el microservidor
Para descargar la información de este repositorio en el I3LAP, es necesario realizar la descarga y despliegue del sistema de información, que se encuentra en: **https://github.com/cityi3lap/CityKnowPro2_SI**

### Paso 2: Desplegar el Videojuego
Despues de tener desplegado el sistema de información, se importan los archivos de la siguiente forma:

-   Los archivos son importados en **/var/www/html/city/game/**

Es decir, que los archivos (index.html, Build/, version.json, etc) estan ligados a la carpeta creada en el sistema de información (city/). 

## ACTUALIZACIÓN
Para realizar los procesos de actualización, es necesario verificar el archivo:

-   version.json

El cual poseé la version del videojuego. Se debe verificar si el archivo version.json del I3LAP y el archivo de este repositorio son diferentes (es decir, si hay cambios en el repositorio). Al encontrar estos cambios, se deben actualizar los archivos en el I3LAP, Volviendo al paso de **DESPLIEGUE** y sobreescribiendo los archivos.

**Nota:** No hay inconveniente en **eliminar** los archivos de despliegue en el I3LAP primero, para despúes descargar y desplegar nuevamente. La información de usuario no es almacenada dentro de estos archivos.
