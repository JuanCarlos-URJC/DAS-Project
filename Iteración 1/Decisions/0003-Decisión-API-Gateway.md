# Decisión API Gateway.  

* Estatus: Proposed.  
 

## Context and Problem Statement  

La aplicación debe contar con un Gateway que sirva para que los clientes puedan comunicarse con los distintos microservicios. 

   

## Decisions Drivers  

* RF-11: Comunicación a través de Gateway.   

* RF-11.1: Monitorizar estado microservicio.   

  
## Considered Options  

* Patrón API Gateway: Para que los clientes puedan comunicarse con los diferentes microservicios sin necesidad de conocer la interfaz de cada uno de ellos.  


## Decision Outcome  

Opción escogida: Opción 1 Patrón API Gateway, porque los clientes podrán comunicarse con los diferentes microservicios.  

 
### Positive Consequences  

* Los clientes podrán comunicarse con los diferentes microservicios.  

* Los clientes solo se comunicarán con los microservicios a través de una única interfaz. 


## Pros and Cons of the Options  
### Opción 1. Patrón API Gateway.   

* Bueno, porque facilita la comunicación de los clientes con los diferentes microservicios, al constituir una única vía de comunicación. 