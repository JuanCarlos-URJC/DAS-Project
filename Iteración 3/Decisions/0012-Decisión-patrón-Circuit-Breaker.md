# Decisión patrón Circuit Breaker. 

* Estatus: Accepted.   

  
## Context and Problem Statement   

La aplicación necesitará un sistema que impida la sobrecarga de peticiones al microservicio de pago.  

 
## Decisions Drivers   

* RF-9: Limitar Intentos Compra. 

 
## Considered Options   

* Patrón Circuit Breaker: Se usará el patrón Circuit Breaker para limitar a 5 el número de intentos de conectar al usuario al módulo de pago. Un intento fallido se produce cuando se considera que hay una sobrecarga. Esta se produce cuando muchos usuarios se intentan conectar al módulo de pago o cuando los middlewares de pago se encuentren saturados. Cuando se pasa el límite de intentos se procede a bloquear durante 10 minutos el botón de pagar al usuario para dar tiempo al sistema de dejar de estar sobrecargado. 

  
## Decision Outcome   

Opción escogida: Opción 1 Patrón Circuit Breaker porque es una manera eficaz de evitar la sobrecarga de microservicios. 

 
### Positive Consequences   

* La aplicación contará con una manera de evitar la sobrecarga de microservicios. 

  
### Negative Consequences 

* Se asume que se van a producir sobrecargas en los microservicios. 


## Pros and Cons of the Options   
### Opción 1. Patrón Circuit Breaker. 

* Bueno, porque evita que haya mayores problemas cuando se produce una sobrecarga. 

* Bueno, porque se da tiempo para que el sistema procese las solicitudes que tiene y deje de estar sobrecargado. 

* Malo, porque el tiempo de espera puede molestar a algunos usuarios. 


## Links 

*  Refined by [ADR-0002] (0000- Decisión-de-distribución-de-la-arquitectura.md) 

 