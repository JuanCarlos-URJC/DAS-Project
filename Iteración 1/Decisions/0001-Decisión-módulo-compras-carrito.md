# Decisión módulo de compras carrito.  

* Estatus: Accepted.  


## Context and Problem Statement  

La aplicación debe de contar con un módulo que se encargue de gestionar las compras y pedidos que hagan los usuarios de la aplicación.  

 
## Decisions Drivers  

* RF-2: Módulo de compras y pedidos.  

* RF-2.1: Carrito de la compra.  

* RF-2.1.2: Añadir artículo al carrito.  

* RF-2.1.3: Modificar cantidad de artículos del carrito.  

* RF-2.1.4: Eliminar artículo del carrito.   

* RF-2.1.5: Vaciar carrito.  


## Considered Options  

* Patrón singleton para carrito: Para asegurarnos de que solo existe una instancia de carrito por cliente a la hora de crear el mismo se utilizará el patrón singleton.  


## Decision Outcome  

Opción escogida: Opción 1 Patrón singleton para carrito, porque es necesario asegurar que solo existirá un carrito para cada cliente que entre en la aplicación.  

  
### Positive Consequences  

* Los usuarios contarán con el servicio descrito para poder realizar sus pedidos.  


## Pros and Cons of the Options   

### Opción 1. Patrón singleton para carrito.   

* Bueno, porque impide que haya problemas en ejecución si existieran distintas instancias de carritos.  

 