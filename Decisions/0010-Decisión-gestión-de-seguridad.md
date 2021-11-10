# Decisión gestión de seguridad.   

* Estatus: Proposed.   


## Context and Problem Statement   

La aplicación necesitará ser segura y por tanto se deben tener en cuenta las siguientes medidas de seguridad.  


## Decisions Drivers   

* RF-12: Módulo de seguridad.   

* RF-12.1: Encriptar comunicaciones. 

* RF-12.2: Seguridad de contraseñas. 

* RF-12.2.1: “Salting” de contraseñas. 

* RF-12.2.2: Encriptar contraseñas. 

 
## Considered Options   

* AESCrypt y “Salting” por delante: Las comunicaciones se encriptarán mediante el protocolo HTTPS, mientras que para aumentar la seguridad de las contraseñas se procederá a hacer “Salting” y encriptación de las mismas. Este proceso consiste en crear un salting que no es más que un string aleatorio (hash), a continuación, se concatena la contraseña del usuario por detrás del salting, después se procede a crear un hash de esa unión y finalmente se guarda en la base de datos en una columna y en otra al lado se incluye el salting directamente. AESCrypt se usará para encriptar los datos personales de los clientes, esto se consigue gracias a que AESCrypt utiliza el algoritmo de cifrado AES y los códigos de 128 y 256 bits. 

* AxCrypt y “Salting” por delante: Las comunicaciones se encriptarán mediante el protocolo HTTPS, mientras que para aumentar la seguridad de las contraseñas se procederá a hacer “Salting” y encriptación de las mismas. Este proceso consiste en crear un salting que no es más que un string aleatorio (hash), a continuación, se concatena la contraseña del usuario por detrás del salting, después se procede a crear un hash de esa unión y finalmente se guarda en la base de datos en una columna y en otra al lado se incluye el salting directamente. AxCrypt se usará para encriptar los datos personales de los clientes, esto se consigue gracias a que AxCrypt utiliza el algoritmo de cifrado AES y los códigos de 128 y 256 bits. 

* BitLocker y “Salting” por delante: Las comunicaciones se encriptarán mediante el protocolo HTTPS, mientras que para aumentar la seguridad de las contraseñas se procederá a hacer “Salting” y encriptación de las mismas. Este proceso consiste en crear un salting que no es más que un string aleatorio (hash), a continuación, se concatena la contraseña del usuario por detrás del salting, después se procede a crear un hash de esa unión y finalmente se guarda en la base de datos en una columna y en otra al lado se incluye el salting directamente. BitLocker se utilizará para encriptar los datos personales de los clientes, esta herramienta aparece en las versiones de Windows 8 y 10. 

* 7-Zip y “Salting” por delante: Las comunicaciones se encriptarán mediante el protocolo HTTPS, mientras que para aumentar la seguridad de las contraseñas se procederá a hacer “Salting” y encriptación de las mismas. Este proceso consiste en crear un salting que no es más que un string aleatorio (hash), a continuación, se concatena la contraseña del usuario por detrás del salting, después se procede a crear un hash de esa unión y finalmente se guarda en la base de datos en una columna y en otra al lado se incluye el salting directamente. 7-Zip se utilizará para encriptar los datos personales de los clientes, esta herramienta de código abierto permite comprimir archivos y protegerlos con claves. 
  

## Decision Outcome   

Opción escogida: Opción 1 AESCrypt  y “Salting” por delante, porque es una manera sencilla se conseguir que la aplicación tenga una seguridad decente. 


### Positive Consequences   

* Los usuarios contarán con una aplicación en la que sus contraseñas serán seguras. 


### Negative Consequences 

* Aun usando estos métodos de seguridad la aplicación no se encuentra absolutamente protegida. 


## Pros and Cons of the Options   
### Opción 1. AESCrypt y “Salting” por delante. 

* Bueno, porque incluye un método sencillo para encriptar contraseñas. 

* Bueno, porque, aunque alguien consiguiera robar una contraseña y tuviera acceso a la tabla de contraseñas entonces no podría robar las cuentas de todos los usuarios que tengan contraseñas iguales (como por ejemplo fechas de nacimiento). 

* Bueno, porque AESCrypt  encripta de manera eficaz los datos. 

* Bueno, porque AESCrypt se adapta a distintos sistemas como Windows, Linux o Mac OS. 

* Bueno, porque AESCrypt sirve tanto para nivel personal como comercial. 

* Bueno, porque AESCrypt sirve para programadores web que utilizan Java. 

* Malo, porque AESCrypt restringe a un lenguaje de programación. 

 

### Opción 2. AxCrypt y “Salting” por delante. 

* Bueno, porque incluye un método sencillo para encriptar contraseñas. 

* Bueno, porque, aunque alguien consiguiera robar una contraseña y tuviera acceso a la tabla de contraseñas entonces no podría robar las cuentas de todos los usuarios que tengan contraseñas iguales (como por ejemplo fechas de nacimiento). 

* Bueno, porque AxCrypt funciona para Windows, Mac OS, Dropbox y Google Drive. 

* Bueno, porque AxCrypt simplifica el proceso de encriptación al solo tener que seleccionar una opción de cifrar. 

 

### Opción 3. BitLocker y “Salting” por delante. 

* Bueno, porque incluye un método sencillo para encriptar contraseñas. 

* Bueno, porque, aunque alguien consiguiera robar una contraseña y tuviera acceso a la tabla de contraseñas entonces no podría robar las cuentas de todos los usuarios que tengan contraseñas iguales (como por ejemplo fechas de nacimiento). 

* Bueno, porque BitLocker encripta los datos sin riesgo a perderlos. 

* Bueno, porque BitLocker sirve para encriptar discos duros completos sin tener que hacerlo en carpetas o archivos individuales. 

* Malo, porque BitLocker es usado generalmente para Windows 8 y 10. 

 

### Opción 4. 7-Zip y “Salting” por delante. 

* Bueno, porque incluye un método sencillo para encriptar contraseñas. 

* Bueno, porque, aunque alguien consiguiera robar una contraseña y tuviera acceso a la tabla de contraseñas entonces no podría robar las cuentas de todos los usuarios que tengan contraseñas iguales (como por ejemplo fechas de nacimiento). 

* Bueno, porque 7-Zip tiene la opción de encriptar los archivos usando AES-256. 

* Bueno, porque 7-Zip tiene la opción de comprimir archivos. 

* Bueno, porque en 7-Zip puede decidirse una clave para descomprimir los archivos. 

* Bueno, porque 7-Zip es gratis. 

* Malo, porque 7-Zip es código abierto y por tanto lo vuelve más vulnerable como sistema de seguridad. 

 