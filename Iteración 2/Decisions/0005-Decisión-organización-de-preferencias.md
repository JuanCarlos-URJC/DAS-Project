# Decisión organización de preferencias.   

* Estatus: Accepted.   


## Context and Problem Statement   

La aplicación necesita un módulo encargado de guardar las preferencias seleccionadas por el usuario.  
   

## Decisions Drivers   

* RF-3. Módulo de preferencias.     

* RF-3.1. Modificar preferencias. 

* RF-3.2. Reestablecer preferencias.    

   
## Considered Options   
  
* Sistema híbrido con cookies: La aplicación cuenta con una clase propia que se encarga de ofrecer las elecciones de preferencia al usuario, así como poder editar las mismas y devolver el valor por defecto (que es ninguna selección). Las preferencias seleccionadas de esta manera se guardarán en la base de datos correspondiente. Además, para mejorar la experiencia del usuario se puede usar un sistema de política de cookies que informe de páginas de terceros que el usuario haya visitado anteriormente. Para crear fácilmente una política de cookies se puede usar Quantcast. 

* Sistema puro sin cookies: La aplicación cuenta con una clase propia que se encarga de ofrecer las elecciones de preferencia al usuario, así como poder editar las mismas y devolver el valor por defecto (que es ninguna selección). Las preferencias seleccionadas de esta manera se guardarán en la base de datos correspondiente.  

 
## Decision Outcome   

Opción escogida: Opción 1. Sistema híbrido con cookies, porque así el usuario dispondrá de una mejor experiencia de personalización y recomendaciones sin que tenga que perder el tiempo en seleccionar lo que quiere ver.  

 
### Positive Consequences   

* Los usuarios contarán con un sistema personalizado de preferencias. 
 

## Pros and Cons of the Options   
### Opción 1. Sistema híbrido con cookies.  

* Bueno, porque gracias al servicio de cookies se cuenta con más medios por los que ofrecer una experiencia inolvidable al cliente. 

* Bueno, porque gracias a la clase de preferencias del propio programa se consigue que el cliente pueda personalizar las recomendaciones que quiere ver. 

* Malo, porque por al usar una política de cookies, los clientes pueden sentir que se viola su privacidad. 

* Malo, porque complica el desarrollo de la aplicación al tener en cuenta diferentes fuentes de información acerca de las preferencias del cliente. 

 
### Opción 2. Sistema puro sin cookies. 

* Bueno, porque gracias a la clase de preferencias del propio programa se consigue que el cliente pueda personalizar las recomendaciones que quiere ver. 

* Malo, porque los usuarios que prescindan de esta función no podrán disfrutar de una experiencia personalizada en la aplicación y por tanto más satisfactoria. 

 

 