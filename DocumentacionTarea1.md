# **Documentación de la tarea 1**

## **Instalación**

**Para Windows**  
Antes de ejecutar cualquier comando se debe tener instalado en el equipo:
* Helm chard
* Docker desktop
* Kubernetes  

Para ejecutar las bases de datos el archivo "databases" y se debe añadir la carpeta de su usuario de sistema, igualmente con la carpeta "monitoring"  


#### Instalar las herramientas de monitoreo
En la configuración de este helm chard solo están habilitadas prometheus y grafana, thanos está deshabilitada para su instalación. Solo se debe configurar el values.yml de la carpeta monitoring para habilitarlo. Más adelante ejemplifica.  

1.Desde línea de comandos en Windows se debe ejecutar:
```sh
helm install monitoring monitoring --dependency-build
```  
2.Luego descargar todas las dependencias de las herramientas a utilizar
```sh
helm install monitoring monitoring --dependency-update
```  
2.Para instalar las herramientas de monitoreo se debe ejecutar el siguiente comando:  
```sh
helm install monitoring monitoring --dry-run
```  

#### Instalar las bases de datos
1.Desde línea de comandos en Windows se debe ejecutar:
```sh
helm install databases databases --dependency-build
```  
2.Descargar todas las dependencias  
```sh
helm install databases databases --dependency-update
```  
4.Para instalar las bases de datos se debe ejecutar el siguiente comando:  
```sh
helm install databases databases --dry-run
```  
## **Configuración de grafana**

Luego de tener instaladas las bases que vamos a utilizar y las herramientas que van a monitorear esa base de datos. Podemos ingresar a grafana.  

1.Nos vamos a la línea de comandos y ejecutamos lo siguiente:
```sh
 kubectl port-forward svc/monitoring-grafana 8080:3000
```  
  
2.Entramos al navegador e ingresamos a grafana utilizando la dirección:  

http://127.0.0.1:8080

3.Escribimos las credenciales, por defecto será el usuario "admin" y la contraseña será "tarea1", esta contraseña está configurada en el values.yml del helm "monitoring".

![N|Solid](https://i.pinimg.com/564x/59/67/f5/5967f5e69af4fd8c478b30827091462a.jpg)
