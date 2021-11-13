# Decisión distribución dar de alta usuario.   

* Estatus: Accepted.   


## Context and Problem Statement    

La aplicación necesita tener un servicio para que los usuarios se puedan dar de alta. 
 

## Decisions Drivers   

* RF-13: Módulo dar de alta usuario. 

* RF-13.1: Crear usuario. 

* RF-13.2: Comprobar usuario no existente. 
 

## Considered Options   

*  Crear usuario y guardar en base de datos: El usuario podrá registrarse en la aplicación rellenando sus datos (Nombre de usuario, contraseña, correo electrónico y teléfono móvil). Una vez realizado esto se comprobará si existe un usuario con el mismo nombre. Si no es el caso, entonces el registro se realizará correctamente y se guardará la información del nuevo usuario en la base de datos correspondiente. Si existe un usuario con el mismo nombre que el proporcionado por el usuario, entonces se rechazará el registro y se avisará al usuario. 
 

## Decision Outcome    

Opción escogida: Opción 1 Crear usuario y guardar en base de datos, porque se necesita contar con una funcionalidad que permita al usuario rellenar sus datos y guardar los mismos en la base de datos. 


### Positive Consequences   

* Los usuarios contarán con la funcionalidad descrita. 


## Pros and Cons of the Options   
### Opción 1. Crear usuario y guardar en base de datos. 

* Bueno, porque es un sistema simple de implementar. 

* Malo, porque por no tener un software específico puede producirse una duplicación de datos según cómo se guarde la información. 

 

 