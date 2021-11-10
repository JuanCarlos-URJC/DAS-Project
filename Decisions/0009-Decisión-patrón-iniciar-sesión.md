# Decisión patrón iniciar sesión.   

* Estatus: Proposed.   

  
## Context and Problem Statement   

La aplicación necesita tener un servicio para que un cliente pueda iniciar su sesión y gestionar la misma. 

 
## Decisions Drivers   

* RF-14: Módulo iniciar sesión. 

* RF-14.1: Iniciar sesión. 

* RF-14.2: Comprobar usuario existente. 

* RF-14.3: Cargar datos del usuario 

   
## Considered Options   

*  Patrón Access Token: Se usará el patrón Access Token para autentificar la identidad del usuario, de manera que el usuario proporciona su información (Nombre y contraseña) en la opción “Iniciar sesión”, a continuación, la aplicación manda una solicitud a la base de datos para comprobar que existe un usuario con esos datos en concreto. Si no encuentra un usuario así se rechaza el inicio de sesión y se avisa al usuario. Si se encuentra un usuario que cumple esas características entonces se trae la información del usuario a la capa de lógica del programa en la clase “Perfil” (que tiene todos los atributos de la clase Usuario) junto con el Access token y se procede a iniciar la aplicación con la información de dicha clase validando la operación con el Access Token generado. 

  
## Decision Outcome   

Opción escogida: Opción 1 Patrón Access Token, porque así se facilita el tratamiento de datos y obtención de datos pertenecientes al cliente en el futuro desde la capa de Lógica de negocio. 

 
### Positive Consequences   

* Los usuarios contarán con el servicio de inicio de sesión. 

  
## Pros and Cons of the Options   
### Opción 1. Patrón Access Token. 

* Bueno, porque es un sistema simple de implementar. 

* Bueno, porque facilita consultar la información del usuario que está usando la aplicación durante el tiempo que el usuario mantenga la sesión activa. 

* Bueno, porque validando el inicio de sesión con el Access Token se previene que se inicie sesión si la información no es correcta. 

* Malo, porque podemos llegar a crear una falla en el sistema, al tener que contar con un método de seguridad el cual puede llegar a fallar. 