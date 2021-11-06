# Decisión patrón de pedidos.   

* Estatus: Accepted.   

 
## Context and Problem Statement   

La aplicación necesita poder crear y modificar pedidos a partir del carrito de la compra, en los que se marque el estado en el que está (pendiente de pago, pagado, enviado o entregado), para después guardarlos en la base de datos del usuario.  


## Decisions Drivers   

* RF-2.2. Crear pedido.    

* RF-2.2.1. Modificar estado de un pedido.    


## Considered Options   

* Patrón observer para pedido: Se utilizará el patrón observer para avisar al objeto de carrito de que debe vaciarse una vez se ha realizado la copia completa de los artículos del carrito al pedido. 

* Hacer uso de la función resetCarrito(): El traspaso de información entre el carrito y el pedido se realizará de tal manera que en cuanto se copien todos los artículos del carrito al pedido, el primero vaciará su lista de productos haciendo uso de la función resetCarrito(). 


## Decision Outcome   

Opción escogida: Opción 2 Hacer uso de la función resetCarrito(), para asegurarnos de que al realizar un pedido se vacíe el carrito de la compra, evitando así la creación de varios pedidos de un mismo carrito. 


### Positive Consequences   

* Los usuarios contarán con el servicio descrito para poder realizar sus pedidos. 


## Pros and Cons of the Options   
### Opción 1. Patrón observer para pedido.    

* Bueno, porque gracias al patrón observer se consigue una manera estructurada de eliminar la información del carrito. 

* Malo, porque complica el desarrollo de la aplicación al incluir más clases. 


###Opción 2. Hacer uso de la función resetCarrito(). 

* Bueno, porque al no contar con el patrón observer la implementación de la aplicación será más sencilla. 
