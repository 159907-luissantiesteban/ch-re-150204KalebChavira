# Software Requirement Specification (SRS) para Systema de Reservación de Hotel CU

Index

- [1.-Introduccion](#Introduccion)
- [2.-Overall Description](#Overall-Description)
- [3.-Specific Requirements](#Specific-Requirements)
- [3.2 .-Functional requirements](#Functional-requirements)
***

## Introduccion ##

1.1 Purpose:

Crear un sistema el cual tenga el unico proposito de reservar cuartos de hotel en Ciudad Universitaria.

Llevar el control exacto de las altas y bajas de huespedes de un hotel, para así, dar de manera eficaz el cargo a pagar por parte del cliente.

* Registrar las altas y bajas de huespedes.
* Manejar la disposicion de habitaciones.
* Calcular el monto a pagar.

1.2 Scope:

El alcance del systema va para aquellas personas los cuales quieran hacer un apartado de reservación en el hotel el cual esta ubicado en Ciudad Universitaria, a los recepcionistas que estan encargados de hacer la reservacion ya sea a traves de una entrevista por llamada de celular o telefono, o en tener la entrevista en la recepcion del hotel.

a)Los costos tendran variacion dependidendo del tipo de habitacion a reservar, metodos de pago los cuales podran ser a traves de transaccion bancarea siendo todo esto en precencial al acudir al lugar.

b)Al momento de hacer la reservacion el recepcionista en todo momento estara mostrando las cantidades y los costos al cliente para que este sepa los cargos de dinero que se le estan haciendo.

c)La autitificacion del cliente se efectual al momento posterior al pago final.

d)Los administradores del hotel tienen acceso a cada parte del front end del systema, los recepcionistas tendran accesos restringidos tales como solo dar altas del systema.

1.3 Glosary:

 Descripción de las habitaciones:
 * Individual: Ideal para quienes viajan solos. No tienes más espacio del que necesitas, y además el precio se adecúa a las necesidades de todos aquellos huéspedes que buscan tener un lugar tranquilo para descansar en sus viajes de placer o negocios.
 
* Doble de uso individual: Este tipo de habitaciones suelen ofrecerse cuando el hotel, a falta de poder ofertar una habitación con una cama pequeña, dispone al huésped una habitación diseñada para dos personas; obviamente, al ser de mayor tamaño, su precio se eleva.
 
* Habitación doble: Como su nombre lo indica, esta clase de habitaciones son para dos personas. Las camas varían, pueden ser matrimoniales o dos camas individuales independientes.
 
Con cama supletoria: Estas habitaciones son ideales para quienes viajan con algún menor de edad. Si bien existe un costo por la cama adicional, usualmente suele ser más barato que contratar una habitación triple. Dependiendo de la edad del niño se coloca la cama que mejor le acomode. Algunos hoteles incluso cuentan con cunas para bebés.
 
* Habitación triple: Simple: estas habitaciones cuentan con 3 camas, o 2 más una supletoria. Es perfecta para los viajes con tus amigos.
 
 * Junior Suites: Cuentan con habitación doble, baño y salón.
 
* Suites: Conocidas por ser las mejores y más lujosas habitaciones en cualquier hotel, cuentan con dos habitaciones dobles, 2 baños, salón y estancia. Por supuesto, su precio es el más elevado. Las suitse más completas y lujosas suelen recibir el nombre de Suite presidencial, y generalmente son reservadas para personajes distinguidos.
 
* Suite nupcial: Pensada para aquellas parejas recién casadas y que quieren disfrutar de una luna de miel con privacidad e intimidad, estas habitaciones en los lugares más exclusivos de los hoteles (generalmente acompañadas sólo por las suite presidencial). Además de una cama matrimonial amplia, generalmente cuentan con jacuzzi y una vista única.
  
1.4 Referencias:

Joaquin Chavira, Eduardo Hernandez. (2019). Reservacion Hotel CU. 27/03/20019, de GitHub Sitio web: https://github.com/alanponce/OOP-100-days-of-code/blob/master/OOP/Proyects/Res_Hab_Hotel/Presentaci%C3%B3n

1.5 Overview

El systema a desarrollar ayudara con la eficiencia y eficacia en la reservacion de cuartos en el hotel ubicado en Ciuadad Universitaria, teniendo en cuenta las altas de habitaciones, baja de habitaciones y cambios en la reservacion de estas mismas.

En este systema se tendra restricciones entre el recepcionista y el administrador.

El cliente tendra a su dispocision diferentes habitaciones en cual podra hacer registro de la que se encuentren disponibles y la que guste reservar.

***

## Overall-Description ##

El systema funcionara usando el CRUD (create, read, update and delete), de una base de datos apartir de un sistema usando diferentes interfaces con cada uno de estos propositos:

Create: Creando la reservación de las habitaciones deseadas y quitar la disponibildad a esas habitaciones.

Read: Revisando si habitaciones estan desocupadas para poder ser apartadas.

Update: Poder generar cambios de la reservacion, cambios de habitacion o cambio de cantidad de reservaciones.

Delete: Dar de baja la reservacion y dar disponibilidad a las habitaciones que serian ocupadas.

Este mismo systema estara conectado a un systema de pago, el cual sera involucrado con pago de efectivo, o tarjeta de credito o debito.

2.1 Product perspective:

El proyecto funcionara en dos partes:

La primera parte funcionara con la reservacion, a traves de interfaces el proyecto tiene que visualizar la disponibilidad de las habitaciones, mostrar los tipos de habitaciones, los costos, la cantidad de personas, las fechas de entradas, fechas de salidas, restricciones de habitaciones, y la verificaciones de que los datos esten correctos.

Poder modificar la reservaciones, tal como poder modificar fechas, cantidad de habitaciones, tipos de habitaciones, forma de pago, etc.

Eliminar reservaciones, poder eliminar la reservacion ya efectuada y liberar las habitaciones apartadas.

La segunda parte es la forma de pago, ya que sea a traves de efectivo, se hacen los cargos por la reservacion y se efectua los calculos de los pagos y el cambio en el cual sea necesario de usar, a traves del sistema de transaaccion bancarea aun queda no establecida.

2.2 Product functions

La forma de efectuar el sistema es validando quien es el que usara el sistema, ya que sea un recepcionista o un administrador, este requiera entrar a traves de una pantalla de LOg In siendo validada por la base de datos y en la tablas de empleados con un usuario y una contraseña.

Una vez ya adentro del sistema, se llevara a cabo una entrevista sobre la reservacion de los cuartos del hotel siendo esta en persona o a traves de una llamada por telefono o celular, verificando y llendando todos los campos obligatorios de la interfaz de apartados es la manera en que se efectua la reservacion, despues de ese proceso se lleva a cabo la verificacion de la informacion de la habitacion o habitaciones del hotel, una vez validado esta en la base de datos y el cliente estando de acuerdo con sus especificaciones se llevara a caputarar los datos del cliente para concluir la reservacion de las habitaciones, estos datos tambien se guardaran en la base de datos pero llenando los datos en las tablas de clientes.

Al concluir la reservacion se quedan almacenados los datos de esta misma, cuando el cliente recida al hotel se llevara el metodo de pago ya se en efectivo y moverlo, o a traves de transacciones bancareas.

2.3 User Characteristics:

En esta area de trabajo se manejaran e tipos de actores que el cual son los Customers y los End Users, estos son los clientes que participarian en la entrevista para saber cuales habitaciones van a querer. Las carateristicas que ellos deben de tener son:
* Tener conocimiento de que tipo de habitaciones va a querer recervar.
* Tener un metodo de pago y la capacidad de hacerlo.
* Identificarse con su informacion real y veridica.
* Ser mayor de edad.
* Contar con la informacion anticipada de las capacidaddes del hotel.

Recepcionista:
* Tener la capacidad de entrar al systema como recipcionista con un usuario y una contraseña.
* Tener conocimiento de como llenar los campos de la interfaz de altas del systema.
* Tener la capacidad de atender amablemente al cliente.
* Ser empleado del hotel y haber sido capacitado para el puesto.

Administrador:
* Tener la capacidad de entrar al systema como admistrador con un usuario y una contraseña.
* Tener conocimiento de como llenar los campos de la interfaz de altas, bajas y cambios del systema.
* Tener la capacidad de atender amablemente al cliente.
* Tener la capacidad de poder apoyar al recepcionista con los conflictos encontrados.
* Ser empleado del hotel y haber sido capacitado para el puesto.

2.4 Constraints:

* El proyecto esta restingido a que trabaja de manera distribuida pero de manera local, solo se piensa desarrollar en el area de trabajo conectado en un systema remoto, para poder efectuar la reservacion es necesario estar usando las computadoras que se tiene instalado el systema.
* No existe una manera de mostrar visualmente las habitaciones disponibles al usuario a menos que se encuentre en la entrevista precencial.
* El programa no se puede ejecutar a menos que tengas un usuario y una contraseña activo en la base de datos.
*

2.5 Assumptions and dependencies:

* Que el banco ayude y proporciones los artefactos para desarrollar o implementar el sistema del metodo de pago atraves de transferencias bancareas
* 

2.6 Apportioning of requirements:

Los requisitos de la forma de pago atraves de tranferencias bancareas seras desplasadas al la siguiente etapa de mejoramiento del sistema, si es que no se encuentra la forma ideal para este metodo de pago.

***

## Specific Requirements ##

3.1 External Requirements:
* Tener instalado en las comnputadoras de trabajo de MySQL(ultima version disponible)
* Desarrollar la conexion de a la base de datos
* Entradas a tablas clientes:

Nombre de la entrada | Tipo de dato | Descripcion
------------ | ------------- | -------------
ID_Cliente | int | identificador del cliente
Nombre del Cliente | String | el nombre del cliente
Apellido del Cliente | String | el apellido del cliente
Telefono | LongInt | numero de telefono del cliente

3.1.1 User Interfaces

Login:

![LogIn](https://github.com/alanponce/OOP-100-days-of-code/blob/master/OOP/Proyects/Res_Hab_Hotel/Dise%C3%B1o%20Interface%20Grafica/LogIn.PNG)

Altas de registro del hotel:

![AltasHotel](https://github.com/alanponce/OOP-100-days-of-code/blob/master/OOP/Proyects/Res_Hab_Hotel/Bocetos/AltasHotel.PNG) 

Bajas:

![BajasHotel](https://github.com/alanponce/OOP-100-days-of-code/blob/master/OOP/Proyects/Res_Hab_Hotel/Dise%C3%B1o%20Interface%20Grafica/Bajas.PNG)

3.1.2 Hardware Requirements

Esta aplicacion no requiere cosas adicionales a una computadora y una red, ya que la base de datos de esta misma esta conectada a todas las computadoras, la base de datos esta ubicada en cada una de ellas y es actulizada al momento.

3.1.3

Software interfaces

Estas solo seran elaboradas con cada proceso tales como:
* Entrar al system siendo un usuario o administrador.
* Dar de alta reservaciones.
* Hacer cambios en la reservaciones.
* Eliminar Reservaciones.
* Un menu donde escojamos el tipo de proceso o salir del systema

3.1.4 Communications interfaces
La comunicacion entre la interfaces se maneja atraves del CRUD en la base de datos, estas interfaces lo que hacen es revisar la informacion de la base de datos y hacer modificaciones, tal como dar altas, bajas y cambios.


## Functional requirements ##

Esta sección incluye los requerimientos que especifican todas las acciones fundamentales del sistema de software del proyecto de reservaciones de habitaciones del Hotel Foráneos CU. 

3.2.1 User class 1 – Recepcionista

3.2.1.1 Functional requirement 1.1

ID: FR1 
Feature: Login del recepcionista 
DESC: Dado que el id y contraseña del recepcionista 
            fueron registrados por los programadores en el sistema 
            el recepcionista deberia ser capaz de usar ambos datos para acceder al sistema 
RAT:   En orden para que el recepcionista entre al sistema 
DEP: None 
 
3.2.1.2 Functional requirement 1.2 
 
ID: FR2 
Feature: Captura de la peticion de reservacion 
DESC: Dado que el recepcionista  
           esta en ejercicio de su funcion laboral de hacer una reservacion 
           Y esta dentro del sistema, en la interface de para hacer reservaciones en especifico* 
           el deberia ser capaz de verificar~ y llenar los campos obligatorios de la interfaz de apartados 
RAT:   En orden para capturar la peticion del cliente 
DEP: FR1
*Hay una interface mas especifica para esta etapa? 
~Como puede verificar?
 
3.2.1.3 Functional requirement 1.3 
 
ID: FR3 
Feature: Validación de reservación con la base de datos 
DESC: Dado que a sido capturada la informacion de la peticion de reservacion 
            se debería poder  verificar comparándola con la(s) habitación(es) en la base de datos 
 
                      Escenario: Se valida una reservacion 
                      Cuando en la verificacion de la base de datos 
                      Se encuentra(n) habitacionI(es) con caracterizacion parecida a la peticion de la reservacion 
                      Se deberia ser capaz de validar la reservacion 
 
                      Escenario: No valida una reservacion 
                      Cuando en la verificacion de la base de datos 
                      No se encuentra(n) habitacionI(es) con caracterizacion parecida a la peticion de la reservacion 
                      No se deberia de validar la reservacion 
 
RAT:   En orden para validar la reservación con la base de datos  
DEP: FR2 
 
3.2.1.4 Functional requirement 1.4 
 
ID: FR4 
Feature: Registro de la reservacion 
DESC: Dado que la reservacion esta validada en la base de datos 
            se deberian poder capturar los datos del cliente 
            Para poder registrar la reservacion 
            La cual pasa a la base de datos 
            datos del cliente en particular que tambien se guardaran en la base de datos de clientes 
RAT:   Para registrar la reservación 
DEP: FR3 
