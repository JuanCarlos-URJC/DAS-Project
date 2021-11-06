# Decisión método de búsqueda de artículos.    
  
* Estatus: Accepted.    


## Context and Problem Statement    

La aplicación debe permitir a los usuarios buscar artículos, mostrando una lista de artículos relacionados con la búsqueda, para después poder seleccionarlos y añadirlos al carrito de la compra. 

  
## Decisions Drivers    

*  RF-2.1.1: Buscar artículo. 

  
## Considered Options    

* Situado en una clase a parte dentro del módulo de compras:  Se creará una clase que se encargue de acceder a la base de datos y obtener todos los artículos relacionados con la búsqueda, priorizando aquellos que coincidan con las preferencias del usuario.  

  
## Decision Outcome    

Opción escogida: Opción 1 Situado en una clase a parte dentro del módulo de compras, porque es preferible realizar la conexión entre base de datos y el listado a través de una clase aparte. 

  
### Positive Consequences    

* Mejora la organización del sistema.  


## Pros and Cons of the Options    
### Opción 1. Situado en una clase a parte dentro del módulo de compras. 

* Bueno, porque diferencia la búsqueda y obtención de la información del resto del programa. 

* Bueno, porque organiza en función de las preferencias del usuario. 


## Links 

 *  Refined by [ADR-0005] (0005-Decisión-organización-de-preferencias.md) 