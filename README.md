# DockerLinuxSqlServer

Para la implementación de SQL Server es necesario descargar la imagen desde docker hub:
 docker pull mcr.microsoft.com/mssql/server:2022-latest
![image](https://user-images.githubusercontent.com/98118966/178618405-c1557275-bab0-4783-bd13-c956b9642e5f.png)




Este comando extrae la imagen del contendor más actual de sql server. 

Se procede a ejecutar la imagen del contenedor Linux en docker, para ello se ejecuta el comando:

docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=StrongPassword21$" -p 1433:1433 --name sql1 --hostname sql1 -d  mcr.microsoft.com/mssql/server:2022-latest

![image](https://user-images.githubusercontent.com/98118966/178618416-46035ff2-2a7b-4aef-ae8b-c98a3067c93f.png)


Una ves que realizamos ese proceso, se ejecuta el comando docker ps -a, el cual permite la visualización de todos los contenedores, para ello es necesario verificar la columna STATUS, si esta presenta un estado UP, significa que SqlServer se esta ejecutando.
![image](https://user-images.githubusercontent.com/98118966/178618427-e7423906-1b80-4bca-b54c-407f8b2c6820.png)
![image](https://user-images.githubusercontent.com/98118966/178618431-135ccaa5-4b68-41a3-8c9d-fdf95cae5b5c.png)

Luego de ello, ejecutamos el comando a continuación para levantar el bash interactiva dentro del contendor.

docker exec -it sql1 "bash"

![image](https://user-images.githubusercontent.com/98118966/178618439-5ddb5f5f-3ea1-4a1a-8677-1993680c72e7.png)


Con estos pasos se ha completado exitosamente el levantamiento del contenedor 
