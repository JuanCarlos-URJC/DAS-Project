# Decisión MongoDB almacenamiento localización microservicios. 

* Estatus: Accepted.   

  
## Context and Problem Statement   

La aplicación necesitará un lugar donde se concentre la localización de los microservicios.  

 
## Decisions Drivers   

* RF-8: Almacenar localización de microservicios. 


## Considered Options   

* MongoDB: Se guardarán las localizaciones de todos los microservicios en MongoDB. 

  
## Decision Outcome   

Opción escogida: Opción 1 MongoDB porque es una manera eficaz de mantener en un mismo lugar información referente a todos los microservicios. 


### Positive Consequences   

* La aplicación contará con una localización dónde se encuentra almacenado cada microservicio 

  
### Negative Consequences 

* Puede ser un riesgo de seguridad el mantener en un mismo lugar toda la información referente a la localización de los microservicios. 

 
## Pros and Cons of the Options   
### Opción 1. MongoDB. 

* Bueno, porque proporciona una manera sencilla de almacenar la información. 

 
## Links 

*  Refined by [ADR-0000] (0000- Decisión-de-distribución-de-la-arquitectura.md) 

 