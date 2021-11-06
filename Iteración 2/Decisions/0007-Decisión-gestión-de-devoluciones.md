# Decisión gestión de devoluciones.   

* Estatus: Accepted.   


## Context and Problem Statement   

La aplicación necesita tener un servicio para que un cliente pida una devolución y gestionar la misma. 


## Decisions Drivers   

* RF-6: Módulo de devoluciones. 

* RF-6.1: Pedir una devolución. 

* RF-6.1.1: Añadir artículos a una devolución. 

* RF-6.1.2: Devolver pedido completo. 

* RF-6.2: Modificar estado de una devolución. 

 
## Considered Options   

* Almacenar lista de devoluciones: La clase devolución contará con un identificador único, la lista de productos a devolver junto con sus cantidades, el precio de la devolución, descripción de la devolución (la razón de la misma) y un estado (pedida, aceptada, rechazada o tramitada) que por defecto será pedida.  Esta devolución se gestionará a través de una interfaz que permita definir qué clase de artículos añadir, de manera que se mostrará un listado de los productos comprados por el usuario organizados por pedidos, así se podrán añadir artículos individuales o un pedido completo.  
Además, cada devolución realizada por un usuario será guardada en la base de datos correspondiente en un listado de devoluciones realizadas de cada usuario. Por otro lado, al tener ese listado, cada usuario podrá ver su lista de pedidos devueltos. Cuando se termine de tramitar la devolución se le enviará un mensaje al cliente de que su devolución ha sido realizada con éxito, en caso contrario, también se le mandará un mensaje informando de lo mismo. 

* No almacenar lista de devoluciones: La clase devolución contará con un identificador único, la lista de productos a devolver junto con sus cantidades, el precio de la devolución, descripción de la devolución (la razón de la misma) y un estado (pedida, aceptada, rechazada o tramitada) que por defecto será pedida.  Esta devolución se gestionará a través de una interfaz que permita definir qué clase de artículos añadir, de manera que se mostrará un listado de los productos comprados por el usuario organizados por pedidos, así se podrán añadir artículos individuales o un pedido completo. Cuando se termine de tramitar la devolución se le enviará un mensaje al cliente de que su devolución ha sido realizada con éxito, en caso contrario, también se le mandará un mensaje informando de lo mismo. 


## Decision Outcome   

Opción escogida: Opción 1 Almacenar lista de devoluciones, porque al guardar un listado se puede realizar funciones imprescindibles para el correcto funcionamiento de la aplicación, así como evitar problemas de colapsos. 


### Positive Consequences   

* Los usuarios contarán con el servicio de devoluciones. 

* El usuario podrá seleccionar qué productos quiere devolver con facilidad. 

 
### Negative Consequences 

* Al contar con este tipo de sistema puede dar pie a que algunos usuarios pidan una devolución cuando no la necesitan. 
  

## Pros and Cons of the Options   
### Opción 1. Almacenar lista de devoluciones. 

* Bueno, porque se podrá obtener fácilmente información sobre qué productos devuelven los usuarios.  

* Bueno, porque tendremos todas las devoluciones guardadas, y tendremos la posibilidad de poner de nuevos los productos en el stock. 

* Bueno, porque si los usuarios lo desean pueden consultar su lista de devoluciones. 

* Bueno, porque evita que haya colapso en la emisión de notificaciones de devolución. 

* Malo, porque se tiene que gestionar la lista de devoluciones en la base de datos y por tanto se pierde almacenamiento. 


### Opción 2. No almacenar lista de devoluciones. 

* Bueno, porque es fácilmente implementable al no guardar en la base de datos. 

* Malo, porque tendremos que utilizar un gran tiempo en la escritura de las devoluciones en las bases de datos. 

* Malo, porque el sistema solo podría aceptar una devolución al mismo tiempo, y podría colapsar el sistema al intentar mandar cientos a la vez. 

* Malo, porque los usuarios no podrán consultar el estado de sus devoluciones en cualquier momento. 