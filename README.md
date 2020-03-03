## Repositorio proyecto OWNCLOUD en alta disponibilidad  
## DOCKER + NGINX + OWNCLOUD + LDAP + MARIADB  

# Objetivos  
* Comprender el modelo de Cloud Computing  
* Conocer el despliegue de software como servicio en Cloud  
* Orquestar microservicios  
* Cononer herramientas básica de balanceado y distribución de carga  

# Aquitectura
La composición de microservicios será la siguiente:
* NGINX : trabajará como Proxy y Balanceador de carga para el microservicio que albergará OwnCloud.
* OwnCloud: contendrá el microservicio de almacenamiento en Cloud.  
* MySQL/MariaDB: microservicio que dotará a OwnCloud de acceso y gestión de los datos.
* LDAP: microservicio para conectar la auten!cación de OwnCloud para los usuarios y el acceso.  

La arquitectura debe permitir balancear la carga desde el servicio NGINX hasta los contenedores (al menos 2), de modo que el tráfico se encauce hacía los contenedores de OwnCLoud. Los demás microservicios sólo es necesario que tengan una única instancia.
