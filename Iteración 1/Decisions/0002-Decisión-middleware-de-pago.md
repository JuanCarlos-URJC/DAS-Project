# Decisión middleware de pago. 

* Estatus: Proposed. 

 

## Context and Problem Statement 

Deberá existir un módulo capaz de gestionar los pagos. 

 

## Decisions Drivers 

* RF-5: Módulo de pagos. 

* RF-5.1: Elegir método de pago. 

* RF-5.2: Conectar con el middleware de pago. 

 

## Considered Options 

* Stripe y Paypal: Entre las opciones dispuestas para el pago del pedido del usuario se encontrará PayPal y Stripe. Para que los usuarios paguen por PayPal deberán tener una cuenta asociada a esa aplicación, mientras que Stripe es una pasarela de pago que acepta pagos con tarjeta de crédito/débito en línea. 

* Square y Paypal: Entre las opciones dispuestas para el pago del pedido del usuario se encontrará PayPal y Square. Para que los usuarios paguen por PayPal deberán tener una cuenta asociada a esa aplicación, mientras que Square es un procesador  de pagos de extremo a extremo o un terminar virtual que acepta pagos con tarjeta de crédito/débito en linea. 

 

## Decision Outcome 

Opción escogida: Opción 2 Square y Paypal, porque ofrece mayor amplitud de servicios para la compra en línea y simplifica el trabajo al contar con las diferentes opciones de implementación.  

 

### Positive Consequences 

* Los usuarios contarán con un servicio de pago que se necesita para el correcto funcionamiento de la aplicación. 

* Los usuarios cuentan con distintas opciones para adaptarse a las necesidades de los mismos. 

 

### Negative Consequences 

* Los pagos pasan a través de servicios de terceros y se depende de la seguridad de los mismos para que los pagos sean seguros. 

 

## Pros and Cons of the Options 

### Opción 1. Stripe y Paypal. 

* Bueno, porque Stripe es sencillo de implementar y conectar a la aplicación. 

* Bueno, porque Stripe aporta un panel de control intuitivo para monitorizar los pagos realizados en la aplicación a través de Stripe. 

* Bueno, porque Stripe cuenta con los siguientes servicios de pago: tarjeta de crédito/débito/internacionales, ACG de débito directo y crédito, transferencias electrónicas y Bitcoin. 

* Bueno, porque Stripe incluye un ligero descuento del 0,8% en transacciones grandes (con un tope de 5$). 

* Malo, porque Stripe cobra un cargo de 15$ por contracargo no decidido a su favor. 

* Malo, porque Stripe no cuenta con algunos de los servicios de pago que Square ofrece. 

 

### Opción 2. Square y Paypal. 

* Bueno, porque Square es utilizable en cualquier plataforma compatible. 

* Bueno, porque Square  permite el pago de dos maneras diferentes (lectura de tarjeta de crédito mediante un dispositivo inteligente y la introducción manual de la información de la tarjeta). 

* Bueno, porque Square procesa todas principales tarjetas de crédito en línea: Visa, Mastercard, Descubre y American Express. 

* Bueno, porque Square acepta pagos de Apple Pay, Android Pay y eWallet. 

* Bueno, porque Square ofrece hardware de caja. 

* Bueno, porque Square todo lo necesario para aceptar pagos y gestionar la aplicación se encuentra en un sistema centralizado. 

* Bueno, porque Square permite la implementación por código sencilla o crear la opción de pago directamente en la web de Square o utilizar un plugin para ampliar el servicio de pagos (WooCommerce). 

* Bueno, porque Square no cobra contracargos. 

* Bueno, porque Square ofrece Protección contra devoluciones de hasta 250$ al mes en transacciones que califiquen.  

* Malo, porque Square no cuenta con algunos de los servicios de pago que Stripe ofrece. 