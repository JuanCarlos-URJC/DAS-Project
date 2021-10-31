# Decisión de distribución de la arquitectura.   

Estatus: Accepted.  


## Context and Problem Statement  

La aplicación actual posee un estilo de tres capas (tiers) y se desea migrar a una arquitectura de microservicios más flexible y escalable.  

  
## Decisions Drivers  

* RF-1: Migración del sistema.  

* RF-5.2: Conectar con middleware de pago.  

* RF-7: Acceder a Base de Datos.  

* RF-10: Servicio de mensajería.  

  
## Considered Options  

* Arquitectura de tres capas (tiers) sin subdivisiones de la estructura antigua: Se mantiene la capa de cliente, mientras que la capa de la lógica de negocio se mantendrá igual, pero se le añadirá de manera externa los middlewares necesarios (middleware de mensajería, de seguridad y el de pagos), y la capa de almacenamiento se mantendrá igual, pero añadiendo de manera externa la base de datos de Mongo DB. Además, contará con microservicios.  

* Arquitectura de tres capas (tiers) con subdivisiones de la estructura antigua: Se mantiene la capa de cliente, mientras que la capa de la lógica de negocio se compondrá de los middlewares necesarios (middleware de mensajería, de seguridad y el de pagos) y dos módulos de la propia lógica que se divide entre la general y la del módulo de notificaciones, y la capa de almacenamiento se dividirá en almacenamiento SQL, no SQL y la base de datos de Mongo DB. Además, contará con microservicios.  
  

## Decision Outcome  

Opción escogida: Opción 2 Arquitectura de tres capas (tiers) con subdivisiones de la estructura antigua, porque mejora la interacción entre distintos servicios.  

 
### Positive Consequences  

* Aumenta la flexibilidad.  

* Aumenta la escalabilidad de la aplicación.  

 
### Negative Consequences  

* Complica la arquitectura.  

  
## Pros and Cons of the Options  
### Opción 1. Arquitectura de tres capas (tiers) sin subdivisiones de la estructura antigua:  

* Bueno, porque permite conservar mayormente la estructura antigua.  

* Malo, porque es difícil a nivel de programador el comprender la estructura de todo el código. 

* Malo, porque tanto la base de datos como la lógica del programa se encuentran centralizadas y todos los procesos pasan por los mismos lugares.  

* Malo, porque pueden producirse colapsos en el intercambio de información entre servicios al pasar todos por las mismas partes.  

 
### Opción 2. Arquitectura de tres capas (tiers) con subdivisiones de la estructura antigua:  

* Bueno, porque el sistema no se encuentra centralizado en la capa de la lógica de negocio ni en la de almacenamiento.  

* Bueno, porque es menos probable que se produzcan colapsos en el intercambio de información entre servicios al no pasar todos por las mismas partes.  

* Malo, porque hay que rehacer la estructura original.  

* Malo, porque aumenta la complejidad de la estructura.  