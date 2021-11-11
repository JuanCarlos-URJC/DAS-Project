# Decisión middleware de mensajería. 

* Estatus: Proposed.   
 

## Context and Problem Statement   

La aplicación necesitará un sistema de mensajería para que los usuarios puedan hablar entre sí en caso de tener alguna duda con algún pedido. 
 

## Decisions Drivers   

* RF-10: Servicio de mensajería. 
 

## Considered Options   

* RabbitMQ: Es una cola de mensajería desarrollada en lenguaje erlang que utiliza el protocolo AMQP que sirve como método para comunicación entre aplicaciones. Los usuarios usarán de manera indirecta este servicio gracias a una interfaz de mensajería de la aplicación.  
 

## Decision Outcome   

Opción escogida: Opción 1 RabbitMQ porque se basa en el protocolo AMQP solicitado y tiene capacidad para adaptarse a lo que la aplicación necesite. 
 

### Positive Consequences   

* Los usuarios contarán con un sistema de mensajería entre usuarios para resolver sus dudas.  

* Por contar con un middleware para este servicio se asegura que el sistema sea eficiente. 

* Al usar el protocolo AMQP no se limita la programación a Java como ocurre con JMS, AMQP solo define el formato de los datos intercambiados. 

* AMQP proporciona un modo de mensaje más rico que JMS. 
 

### Negative Consequences 

* El uso de un middleware puede simplificar o complicar el proceso de codificación. 


## Pros and Cons of the Options   
### Opción 1. RabbitMQ. 

* Bueno, porque ofrece 6 modos diferentes: simple, de trabajo, de publicación/suscripción de publicación y suscripción, de enrutamiento, de tema de temas y de llamada remota RPC (este último no es recomendado ya que no usa especialmente MQ). 

* Bueno, porque posee buena estabilidad. 

* Bueno, porque posee tres modelos para el intercambio de mensajes: intercambio directo e individual por topic, todos los consumidores conectados a la cola reciben el mensaje, cada consumidor recibe un mensaje enviado. 

* Bueno, porque tiene una interfaz moderna e intuitiva. 

* Bueno, porque tiene buena flexibilidad y plugins disponibles. 

 

 