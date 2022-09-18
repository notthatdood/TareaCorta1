# **Documentación de la tarea 1**

## **Instalación**

**Para Windows**  
Antes de ejecutar cualquier comando se debe tener instalado en el equipo:
* Helm
* Docker desktop con kubernetes habilitado
* Minikube
* Powershell

Se debe clonar el repo de github: https://github.com/notthatdood/TareaCorta1.
Luego se abre powershell y se hace un change directory a donde se haya colocado este repo.

#### Instalar las herramientas de monitoreo y bases de datos
En la configuración de este helm chart solo están habilitadas prometheus y grafana, thanos está deshabilitada para su instalación. Solo se debe configurar el values.yaml de la carpeta monitoring para habilitarlo. Más adelante ejemplifica.  

1.Desde línea de comandos en Windows se debe ejecutar:
```sh
./createEverything.ps1
```
## **Configuración de grafana**

Luego de tener instaladas las bases que vamos a utilizar y las herramientas que van a monitorear esa base de datos. Podemos ingresar a grafana.  

1.Nos vamos a la línea de comandos y ejecutamos lo siguiente:
```sh
 kubectl port-forward svc/monitoring-grafana 8080:3000
```  
  
2.Entramos al navegador e ingresamos a grafana utilizando la dirección:  

http://127.0.0.1:8080

3.Escribimos las credenciales, por defecto será el usuario "admin" y la contraseña será "tarea1", esta contraseña está configurada en el values.yaml del helm chart "monitoring".

![N|Solid](https://i.pinimg.com/564x/59/67/f5/5967f5e69af4fd8c478b30827091462a.jpg)  

4.Nos vamos a la parte de configuración y Data sources  

![N|Solid](https://i.pinimg.com/originals/68/c9/f3/68c9f3724b86c67ea6858e56d9ebf2d2.jpg)  

5.Añadimos el data souces y seguidamente prometheus 

![N|Solid](https://i.pinimg.com/originals/ed/bb/a7/edbba713ff4d5a96e3bf25258d59cb68.jpg)  

![N|Solid](https://i.pinimg.com/originals/04/bc/e6/04bce615e432a85d4e588fe5bf958ebc.jpg)  

5.Indicamos el url de prometheus el cual será: http://monitoring-kube-prometheus-prometheus:9090  y guardamos los cambios. Debe aparecer un mensaje en donde indique que el Data source está funcionando.

![N|Solid](https://i.pinimg.com/originals/81/aa/d7/81aad70ee0eaf0518108d06a3712dbf6.jpg)  
![N|Solid](https://i.pinimg.com/originals/ee/5a/ef/ee5aefb88578c083f766c07441381145.jpg)  

**Añadiendo los dashboard de las bases de datos** 

**MariaDB**  
  
**MongoDB**  
  
**Elasticsearch**  
  
**PostgreSQL**  
  
**Grafana**

## **Configuración de las herramientas**  

**MariaDB**  
  
**MongoDB**  
  
**Elasticsearch**  
  
**PostgreSQL**  
  
**Grafana**  
  
## **Conclusiones**  
  
## **Recomendaciones**
