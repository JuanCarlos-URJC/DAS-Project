# Decisión patrón de notificaciones.   

* Estatus: Proposed.   
 

## Context and Problem Statement   

La aplicación necesitará un módulo encargado de gestionar y mandar las notificaciones necesarias.  
 

## Decisions Drivers   

* RF-4: Módulo de notificaciones. 

* RF-4.1: Crear notificación. 

* RF-4.2: Enviar notificación. 

* RF-5.3: Notificar estado final de pago. 

 
## Considered Options   

* Patrón Observer: Se usará el patrón Observer para el tratamiento de las notificaciones, de tal manera que una notificación estará conformada por un identificador único, una imagen (opcional), título, contenido y fecha (con hora, minuto y segundo) de envío. El módulo de notificación recibirá una señal de que tiene que mandar una notificación y la mandará donde corresponda, ya sea un usuario u otro módulo. Para mandar estas notificaciones se mandarán mediante un service worker que se implementará con el protocolo HTTPS en un Javascript. 
  

## Decision Outcome   

Opción escogida: Opción 1 patrón Observer porque es la manera más eficaz de distribuir notificaciones y avisar distintos módulos de sucesos que ocurren en el programa. 


### Positive Consequences   

* Los usuarios contarán con un sistema de notificaciones para que la aplicación les informe de cualquier problema o simplemente para confirmar que los procedimientos funcionan correctamente. 

  
### Negative Consequences 

* Pueden generarse retardos si distintos módulos pretenden notificar algo al usuario a la vez. 


## Pros and Cons of the Options   
### Opción 1. Patrón Observer. 

* Bueno, porque gracias al patrón Observer se modulariza que una única parte del código se encargue de las notificaciones. 

* Bueno, porque el Service Worker permite ser ejecutado en segundo plano. 

* Bueno, porque el Service Worker puede ser usado de manera offline. 

* Bueno, porque el Service Worker permite notificaciones de tipo push. 

* Bueno, porque el Service Worker es soportado en los principales navegadores (Google Chrome, Mozilla, Firefox, Opera, Microsoft Edge). 

* Malo, porque los navegadores en los que son soportados el Service Worker va en función del sistema en el que estén instalados. 

 

 