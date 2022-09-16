# **Documentación de la tarea 1**

## **Instalación**

**Para Windows**  
Antes de ejecutar cualquier comando se debe tener instalado en el equipo:
* Helm chard
* Docker desktop
* Kubernetes  

Para ejecutar las bases de datos el el archivo "databases" se debe añadir la carpeta de su usuario de sistema.    

#### Instalar las bases de datos
1.Desde linea de comandos en Windows se debe ejecutar el comando para descargar todas las dependencias de las bases de datos:
```sh
helm install databases databases --dependency-update
```  
2.Para instalar las bases de datos se debe ejecutar el siguiente comando:  
```sh
helm install databases databases --dry-run
```  

#### Instalar las herramientas de monitoreo
En la configuración de este helm chard solo están habilitadas prometheus y grafana, thanos no está habilitada para su instalación. Solo se debe configurar el values.yml de la carpeta monitoring para habilitarlo. Más adelante ejemplifica.  

1.Desde linea de comandos en Windows se debe ejecutar el comando para descargar todas las dependencias de las herramientas de monitoreo:
```sh
helm install monitoring monitoring --dependency-update
```  
2.Para instalar las bases de datos se debe ejecutar el siguiente comando:  
```sh
helm install monitoring monitoring --dry-run
```  
