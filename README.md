# IISSIFIT

## Miembros del grupo L7-DF-GRUPO_3

 - López Velasco, Miguel Ángel
 - Jerez Gavira, Alejandro
 - Alaya Sotillo, José


## 1. Introducción al problema

IISSIFIT es un gimnasio local que comenzó como un negocio familiar. Ofrece servicios de entrenamiento y actividades deportivas a las personas de la zona. Al principio tenía alrededor de 100 clientes. La información se gestionaba de forma manual con hojas de cálculo, papel y documentos impresos.

![Gimnasio Antes De Reforma](imagenes/gym_antes.png)

En la actualidad, IISSIFIT ofrece varios servicios. Los socios pueden acceder a las instalaciones. También hay clases, entrenamientos personalizados y planes de membresía. Los usuarios principales son los socios, los entrenadores, el personal de recepción y administración, y los propietarios del gimnasio.

El crecimiento del gimnasio ha hecho que la gestión manual sea más difícil. Hay errores al registrar a los socios y los pagos. La información se repite. Es difícil ver qué clases están disponibles. Actualizar las cuotas es complicado. Las tareas administrativas toman mucho tiempo. No hay una única fuente de información, lo que hace difícil hacer estadísticas o tomar decisiones.

![Formularios](imagenes/formularios.png)

Los dueños quieren seguir creciendo. Quieren llegar a unos 2.000 socios. Quieren añadir más salas, contratar más entrenadores y ofrecer más actividades. Este crecimiento significa manejar más información y más operaciones.

![Gimnasio Reformado](imagenes/gym_reformado.png)

![Evolución de socios](imagenes/prevision-socios.png)

Para resolver estos problemas, se quiere crear una base de datos. Esta base de datos ayudará a organizar la información sobre socios, entrenadores, clases, salas, reservas, asistencias, membresías y pagos. Permite consultar y actualizar los datos de forma fácil.

Con esta base de datos se busca reducir errores. Se busca hacer más rápido el trabajo administrativo. Se busca mejorar la organización. Se quiere tener información precisa y actualizada. Esto dará una estructura adecuada para el futuro del gimnasio.


## 2. Glosario de términos

- **Aforo:** número máximo de personas que pueden estar en una sala o clase al mismo tiempo. Indica cuántas reservas se pueden hacer.

- **Asistencia:** registro de que un socio realmente acudió a una clase, a un entrenamiento o a las instalaciones en una fecha y hora específicas. Se diferencia de la reserva, que es solo la intención de asistir.

- **Clase:** sesión de actividad física grupal que imparte un entrenador en una sala y en un horario determinado. Tiene un aforo limitado y los socios se apuntan mediante reserva.

- **Cuota:** dinero que paga el socio periódicamente (mensual, trimestral o anual) por su membresía. El precio varía según la tarifa que tenga contratada.

- **Entrenador:** persona del gimnasio que imparte clases y también diseña y supervisa las rutinas y entrenamientos personalizados de los socios.

- **Membresía:** acuerdo o plan que permite al socio usar los servicios del gimnasio durante un tiempo. Puede ser básica, completa, familiar, de estudiante, entre otras.

- **Pago:** acción mediante la cual un socio abona una cuota o un servicio. Se registra con la fecha, el importe, el método de pago y el estado (pagado, pendiente o devuelto).

- **Reserva:** petición de un socio para tener un lugar en una clase o sesión específica. Puede estar confirmada, en lista de espera, cancelada o terminada.

- **Rutina:** conjunto de ejercicios planificados, con su orden, series y repeticiones, que un entrenador asigna a un socio para alcanzar un objetivo concreto.

- **Sala:** espacio físico del gimnasio donde se realizan actividades como spinning, yoga o musculación. Tiene un límite de personas y horarios definidos.

- **Socio:** persona registrada en el gimnasio que tiene una membresía activa. Puede usar las instalaciones, reservar clases y solicitar entrenamientos personalizados.


## 3. Visión general del sistema

### 3.1. Requisitos generales

- **RG-01:** El sistema deberá gestionar la información de los socios.
- **RG-02:** El sistema deberá gestionar las fichas físicas de los socios.
- **RG-03:** El sistema deberá gestionar los diferentes tipos de membresía.
- **RG-04:** El sistema deberá gestionar la información de los entrenadores.
- **RG-05:** El sistema deberá gestionar las salas del gimnasio.
- **RG-06:** El sistema deberá gestionar la programación de clases.
- **RG-07:** El sistema deberá gestionar las reservas de los socios.
- **RG-08:** El sistema deberá gestionar los pagos.
- **RG-09:** El sistema deberá controlar las plazas disponibles en cada clase.
- **RG-10:** El sistema deberá evitar conflictos entre horarios, entrenadores y salas.
- **RG-11:** El sistema deberá permitir obtener listados y realizar consultas.


### 3.2. Usuarios del sistema

#### Administrador

Es el usuario con mayor nivel de acceso. Sus funciones principales serán:

- Consultar la información de socios y entrenadores.
- Gestionar las membresías ofrecidas.
- Supervisar las clases y salas.
- Consultar reservas y pagos.
- Obtener información sobre ingresos y ocupación.
- Supervisar el funcionamiento general de IISSIFIT.

#### Recepcionista

Es el personal encargado de atender a los socios. Sus funciones principales serán:

- Registrar y consultar socios.
- Consultar las fichas físicas.
- Consultar las membresías disponibles.
- Consultar clases y plazas disponibles.
- Gestionar las reservas.
- Registrar los pagos de los socios.

#### Entrenador

Es el profesional encargado de impartir las clases. Sus funciones principales serán:

- Consultar sus datos personales y profesionales.
- Consultar las clases que tiene asignadas.
- Consultar las salas en las que se imparten sus clases.
- Consultar los socios inscritos en sus clases.

#### Socio

Es el cliente registrado en el gimnasio. Sus funciones principales serán:

- Consultar sus datos personales.
- Consultar su ficha física.
- Consultar su membresía.
- Consultar las clases disponibles.
- Consultar sus reservas.
- Consultar los pagos realizados.


## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Listado de socios

Como recepcionista  
quiero consultar el listado completo de socios  
para localizar rápidamente a cualquier socio registrado.

**Prueba de aceptación**

* Se muestran todos los socios registrados en el sistema.
* Para cada socio se muestran su identificador, nombre, apellidos y estado.
* Si no hay socios registrados, se muestra un listado vacío.

#### R.F.02. Consulta de un socio concreto

Como socio  
quiero consultar mis datos personales  
para comprobar que son correctos.

**Prueba de aceptación**

* Se muestran todos los datos del socio indicado (RI-01).
* Un socio solo puede consultar sus propios datos.
* Si el socio no existe, el sistema informa de que no se ha encontrado.

#### R.F.03. Consulta de socios activos e inactivos

Como administrador  
quiero consultar los socios activos e inactivos  
para conocer la situación del gimnasio.

**Prueba de aceptación**

* Se puede filtrar el listado por estado activo o inactivo.
* El número de socios mostrados coincide con el estado seleccionado.
* Ningún socio aparece en ambos listados a la vez.

#### R.F.04. Consulta de socios por membresía

Como administrador  
quiero consultar los socios según la membresía contratada  
para conocer qué socios tiene cada plan.

**Prueba de aceptación**

* Al seleccionar una membresía, se muestran únicamente los socios que la tienen contratada.
* Si ningún socio tiene esa membresía, se muestra un listado vacío.

#### R.F.05. Consulta de la ficha física de un socio

Como recepcionista  
quiero consultar la ficha física de un socio  
para conocer su información registrada.

**Prueba de aceptación**

* Se muestran el peso, la altura, el objetivo deportivo y las observaciones del socio (RI-02).
* Se muestran las fechas de creación y de última actualización.
* Si el socio no tiene ficha física, el sistema lo indica.

#### R.F.06. Consulta de fichas físicas actualizadas en un periodo

Como administrador  
quiero consultar las fichas actualizadas en un periodo  
para controlar su mantenimiento.

**Prueba de aceptación**

* Se muestran solo las fichas cuya fecha de última actualización está dentro del periodo indicado.
* Cada ficha se muestra junto al socio al que pertenece.
* Si el periodo no es válido (fecha de inicio posterior a la de fin), el sistema lo rechaza.

#### R.F.07. Consulta de socios por objetivo deportivo

Como administrador  
quiero consultar los socios según su objetivo deportivo  
para conocer qué buscan los socios del gimnasio.

**Prueba de aceptación**

* Al indicar un objetivo, se muestran los socios cuya ficha física tiene ese objetivo.
* Los socios sin ficha física no aparecen en el resultado.

#### R.F.08. Consulta de peso, altura y fecha de actualización

Como socio  
quiero consultar el peso, la altura y la fecha de actualización de mi ficha  
para comprobar mis datos físicos.

**Prueba de aceptación**

* Se muestran el peso, la altura y la fecha de última actualización de la ficha del socio.
* Un socio solo puede consultar su propia ficha.

#### R.F.09. Listado de membresías disponibles

Como recepcionista  
quiero consultar las membresías disponibles  
para informar a los clientes.

**Prueba de aceptación**

* Se muestran únicamente las membresías cuyo estado es disponible.
* Para cada una se muestran nombre, precio y duración.

#### R.F.10. Consulta de una membresía concreta

Como socio  
quiero consultar los datos de mi membresía  
para conocer sus condiciones.

**Prueba de aceptación**

* Se muestran el nombre, la descripción, el precio, la duración y los servicios incluidos (RI-03).
* Si la membresía no existe, el sistema informa de que no se ha encontrado.

#### R.F.11. Consulta de socios por membresía

Como administrador  
quiero consultar los socios asociados a cada membresía  
para conocer quién tiene contratado cada plan.

**Prueba de aceptación**

* Para cada membresía se muestran los socios que la tienen contratada.
* Las membresías sin socios aparecen con una lista vacía.

#### R.F.12. Número de socios por tipo de membresía

Como administrador  
quiero consultar el número de socios de cada membresía  
para conocer su popularidad.

**Prueba de aceptación**

* Se muestra, para cada membresía, el número de socios que la tienen contratada.
* La suma de los totales coincide con el número de socios con membresía.

#### R.F.13. Listado de entrenadores

Como administrador  
quiero consultar el listado completo de entrenadores  
para conocer la plantilla del gimnasio.

**Prueba de aceptación**

* Se muestran todos los entrenadores registrados.
* Para cada uno se muestran nombre, apellidos, especialidad y estado laboral.

#### R.F.14. Consulta de un entrenador concreto

Como entrenador  
quiero consultar mis datos personales y profesionales  
para comprobar que son correctos.

**Prueba de aceptación**

* Se muestran todos los datos del entrenador (RI-04).
* Un entrenador solo puede consultar sus propios datos.

#### R.F.15. Consulta de entrenadores por especialidad

Como recepcionista  
quiero consultar los entrenadores según su especialidad  
para informar a los socios.

**Prueba de aceptación**

* Al indicar una especialidad, se muestran solo los entrenadores que la tienen.
* Si ningún entrenador tiene esa especialidad, se muestra un listado vacío.

#### R.F.16. Consulta de clases impartidas por un entrenador

Como entrenador  
quiero consultar mis clases asignadas  
para organizar mi horario.

**Prueba de aceptación**

* Se muestran las clases asignadas al entrenador con su fecha, hora y sala.
* No se muestran clases de otros entrenadores.
* Se debe aplicar la regla de negocio R.N.04.

#### R.F.17. Listado de salas

Como administrador  
quiero consultar el listado completo de salas  
para conocer las instalaciones del gimnasio.

**Prueba de aceptación**

* Se muestran todas las salas registradas.
* Para cada una se muestran nombre, aforo máximo y estado de disponibilidad.

#### R.F.18. Consulta de una sala concreta

Como recepcionista  
quiero consultar los datos de una sala  
para informar a los socios.

**Prueba de aceptación**

* Se muestran el nombre, la ubicación, el aforo, el tipo de actividad y la disponibilidad (RI-05).
* Si la sala no existe, el sistema informa de que no se ha encontrado.

#### R.F.19. Consulta de clases asignadas a una sala

Como entrenador  
quiero consultar la sala asignada a cada clase  
para saber dónde se imparte.

**Prueba de aceptación**

* Para una sala se muestran las clases que tiene programadas.
* Las clases se muestran ordenadas por fecha y hora.
* Se debe aplicar la regla de negocio R.N.04.

#### R.F.20. Consulta de salas disponibles

Como recepcionista  
quiero consultar las salas disponibles en una fecha y franja horaria  
para conocer su ocupación.

**Prueba de aceptación**

* Se muestran únicamente las salas sin ninguna clase cuyo horario coincida con la franja indicada.
* Una sala con una clase que solape parcialmente la franja no aparece como disponible.
* Se debe aplicar la regla de negocio R.N.04.

#### R.F.21. Listado de clases programadas

Como socio  
quiero consultar las clases programadas  
para decidir cuáles reservar.

**Prueba de aceptación**

* Se muestran las clases con su nombre, fecha, hora, entrenador y sala.
* No se muestran las clases canceladas.

#### R.F.22. Consulta de clases por fecha

Como socio  
quiero consultar las clases programadas para una fecha concreta  
para organizar mi día.

**Prueba de aceptación**

* Solo se muestran las clases de la fecha indicada.
* Las clases aparecen ordenadas por hora de inicio.
* Si no hay clases ese día, se muestra un listado vacío.

#### R.F.23. Consulta de clases por nivel de dificultad

Como socio  
quiero consultar las clases según su nivel de dificultad  
para elegir las que se adaptan a mi condición física.

**Prueba de aceptación**

* Al indicar un nivel, se muestran solo las clases de ese nivel.
* Cada clase muestra su nombre, fecha y hora.

#### R.F.24. Consulta de plazas disponibles

Como recepcionista  
quiero consultar las plazas disponibles de cada clase  
para informar a los socios antes de reservar.

**Prueba de aceptación**

* Para cada clase se muestra el número de plazas libres, calculado como el máximo de participantes menos las reservas activas.
* Una clase completa muestra cero plazas disponibles.
* Las reservas canceladas no cuentan como plazas ocupadas.
* Se debe aplicar la regla de negocio R.N.02.

#### R.F.25. Consulta de reservas de un socio

Como recepcionista  
quiero consultar las reservas de un socio  
para ayudarle con sus gestiones.

**Prueba de aceptación**

* Se muestran todas las reservas del socio con la clase, la fecha y el estado.
* Un socio que consulta sus propias reservas solo ve las suyas.
* Se debe aplicar la regla de negocio R.N.01.

#### R.F.26. Consulta de socios inscritos en una clase

Como entrenador  
quiero consultar los socios inscritos en mis clases  
para conocer los asistentes.

**Prueba de aceptación**

* Se muestran únicamente los socios con una reserva activa en la clase indicada.
* El número de socios mostrados no supera el máximo de participantes de la clase.
* Se debe aplicar la regla de negocio R.N.02.

#### R.F.27. Consulta de reservas activas y canceladas

Como administrador  
quiero consultar las reservas activas y canceladas  
para supervisar la actividad del gimnasio.

**Prueba de aceptación**

* Se puede filtrar el listado por estado activa o cancelada.
* Cada reserva se muestra con el socio, la clase y la fecha de realización (RI-07).

#### R.F.28. Clases con mayor número de reservas

Como administrador  
quiero consultar las clases con más reservas  
para conocer las actividades más demandadas.

**Prueba de aceptación**

* Las clases se muestran ordenadas de mayor a menor número de reservas activas.
* Para cada clase se muestra su número de reservas.

#### R.F.29. Consulta de pagos de un socio

Como socio  
quiero consultar mis pagos  
para comprobar los importes abonados.

**Prueba de aceptación**

* Se muestran todos los pagos del socio con fecha, importe, método y concepto (RI-08).
* Un socio solo puede consultar sus propios pagos.
* Se debe aplicar la regla de negocio R.N.05.

#### R.F.30. Consulta de pagos en un periodo

Como recepcionista  
quiero consultar los pagos realizados en un periodo  
para mantener actualizada la situación de los socios.

**Prueba de aceptación**

* Se muestran solo los pagos con fecha dentro del periodo indicado.
* Si el periodo no es válido, el sistema lo rechaza.
* Se debe aplicar la regla de negocio R.N.05.

#### R.F.31. Consulta de ingresos mensuales

Como administrador  
quiero consultar los ingresos mensuales  
para analizar la evolución del gimnasio.

**Prueba de aceptación**

* Se muestra, para cada mes, la suma de los importes de los pagos realizados.
* Los meses sin pagos muestran un total de cero.

#### R.F.32. Consulta de ingresos por método de pago

Como administrador  
quiero consultar los ingresos según el método de pago  
para conocer cómo pagan los socios.

**Prueba de aceptación**

* Se muestra el total de ingresos para efectivo, tarjeta y transferencia.
* La suma de los tres totales coincide con los ingresos totales.
* Se debe aplicar la regla de negocio R.N.05.

#### 4.1.1. Requisitos de información

##### RI-01. Información de los socios

De cada socio se almacenará:

- Identificador único.
- DNI.
- Nombre.
- Apellidos.
- Fecha de nacimiento.
- Teléfono.
- Correo electrónico.
- Dirección.
- Fecha de alta.
- Estado, que podrá ser activo o inactivo.
- Membresía contratada.

##### RI-02. Información de las fichas físicas

De cada ficha física se almacenará:

- Identificador único.
- Socio al que pertenece.
- Peso.
- Altura.
- Objetivo deportivo.
- Observaciones.
- Fecha de creación.
- Fecha de la última actualización.

##### RI-03. Información de las membresías

De cada membresía se almacenará:

- Identificador único.
- Nombre.
- Descripción.
- Precio.
- Duración.
- Servicios incluidos.
- Estado de disponibilidad.

##### RI-04. Información de los entrenadores

De cada entrenador se almacenará:

- Identificador único.
- DNI.
- Nombre.
- Apellidos.
- Teléfono.
- Correo electrónico.
- Especialidad.
- Fecha de contratación.
- Estado laboral.

##### RI-05. Información de las salas

De cada sala se almacenará:

- Identificador único.
- Nombre.
- Ubicación.
- Aforo máximo.
- Tipo de actividad permitida.
- Estado de disponibilidad.

##### RI-06. Información de las clases

De cada clase se almacenará:

- Identificador único.
- Nombre.
- Descripción.
- Fecha.
- Hora de inicio.
- Duración.
- Nivel de dificultad.
- Número máximo de participantes.
- Entrenador responsable.
- Sala asignada.
- Estado.

##### RI-07. Información de las reservas

De cada reserva se almacenará:

- Identificador único.
- Socio que realiza la reserva.
- Clase reservada.
- Fecha y hora de realización.
- Estado, que podrá ser activa o cancelada.

##### RI-08. Información de los pagos

De cada pago se almacenará:

- Identificador único.
- Socio que realiza el pago.
- Membresía relacionada.
- Fecha.
- Importe.
- Método de pago.
- Concepto.
- Estado.

#### 4.1.2. Reglas de negocio

##### RN-01. Validez de una reserva

Un socio solamente podrá reservar una clase si se encuentra activo, tiene una membresía vigente y quedan plazas disponibles.

**Entidades implicadas:**

- Socio.
- Membresía.
- Reserva.
- Clase.

##### RN-02. Control de aforo

El número máximo de participantes de una clase no podrá superar el aforo de la sala en la que se imparte. El número de reservas activas tampoco podrá superar el máximo establecido para la clase.

**Entidades implicadas:**

- Clase.
- Sala.
- Reserva.

##### RN-03. Coincidencia de clases reservadas

Un socio no podrá reservar dos clases cuyos horarios coincidan total o parcialmente.

**Entidades implicadas:**

- Socio.
- Reserva.
- Clase.

##### RN-04. Disponibilidad de entrenadores y salas

Un entrenador no podrá impartir dos clases simultáneamente. Una sala tampoco podrá utilizarse para dos clases cuyos horarios coincidan.

**Entidades implicadas:**

- Entrenador.
- Sala.
- Clase.

##### RN-05. Validez de un pago

Todo pago deberá estar asociado a un socio registrado y a una membresía. Su importe deberá ser superior a cero y el método de pago tendrá que ser efectivo, tarjeta o transferencia.

**Entidades implicadas:**

- Socio.
- Membresía.
- Pago.

### 4.2. Mapa de historias de usuario (opcional)

#### Gestión de socios

- Como recepcionista, quiero gestionar los datos de los socios para mantener la información actualizada.
- Como administrador, quiero consultar los socios activos e inactivos para conocer la situación del gimnasio.
- Como socio, quiero consultar mis datos para comprobar que son correctos.

#### Gestión de fichas físicas

- Como recepcionista, quiero consultar la ficha física de un socio para conocer su información registrada.
- Como socio, quiero consultar mi ficha física para comprobar mis datos y mi objetivo deportivo.
- Como administrador, quiero consultar las fichas actualizadas en un periodo para controlar su mantenimiento.

#### Gestión de membresías

- Como recepcionista, quiero consultar las membresías para informar a los clientes.
- Como socio, quiero consultar mi membresía para conocer sus condiciones.
- Como administrador, quiero consultar el número de socios de cada membresía para conocer su popularidad.

#### Gestión de entrenadores

- Como administrador, quiero gestionar los datos de los entrenadores para mantener actualizada la plantilla.
- Como recepcionista, quiero consultar las especialidades de los entrenadores para informar a los socios.
- Como entrenador, quiero consultar mis clases asignadas para organizar mi horario.

#### Gestión de salas

- Como administrador, quiero gestionar las salas para organizar las instalaciones.
- Como recepcionista, quiero consultar las salas disponibles para conocer su ocupación.
- Como entrenador, quiero consultar la sala asignada a cada clase.

#### Gestión de clases

- Como administrador, quiero gestionar las clases para organizar la programación.
- Como socio, quiero consultar las clases disponibles para decidir cuáles reservar.
- Como entrenador, quiero consultar las clases que tengo asignadas.

#### Gestión de reservas

- Como socio, quiero gestionar mis reservas para organizar mis actividades.
- Como recepcionista, quiero consultar las reservas de un socio para ayudarle.
- Como entrenador, quiero consultar los socios inscritos en sus clases.

#### Gestión de pagos

- Como recepcionista, quiero registrar los pagos para mantener actualizada la situación de los socios.
- Como socio, quiero consultar mis pagos para comprobar los importes abonados.
- Como administrador, quiero consultar los ingresos mensuales para analizar la evolución del gimnasio.

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Rendimiento**  
Como recepcionista  
quiero que las consultas habituales muestren sus resultados en menos de tres segundos  
para atender a los socios sin esperas.

**R.N.F. 02. Seguridad**  
Como administrador  
quiero que el acceso a la información esté limitado según el tipo de usuario  
para que cada usuario solo consulte y modifique lo que le corresponde.

**R.N.F. 03. Privacidad**  
Como socio  
quiero que mis datos personales estén protegidos frente a accesos no autorizados  
para garantizar mi privacidad.

**R.N.F. 04. Usabilidad**  
Como recepcionista  
quiero una interfaz clara, sencilla e intuitiva  
para realizar mis tareas sin necesidad de una formación extensa.

**R.N.F. 05. Integridad**  
Como administrador  
quiero que el sistema impida la introducción de información duplicada, incompleta o contradictoria  
para disponer de datos fiables.

**R.N.F. 06. Escalabilidad**  
Como administrador  
quiero que el sistema pueda gestionar el crecimiento desde los 100 socios iniciales hasta aproximadamente 2.000  
para poder expandir el gimnasio sin rediseñar la base de datos.

**R.N.F. 07. Compatibilidad**  
Como administrador  
quiero que la base de datos funcione correctamente en un servidor MariaDB  
para poder desplegarla en la infraestructura prevista.

**R.N.F. 08. Mantenimiento**  
Como administrador  
quiero poder añadir nuevas salas, clases, membresías y servicios  
para ampliar la oferta del gimnasio sin modificar la estructura del sistema.

**R.N.F. 09. Copias de seguridad**  
Como administrador  
quiero que se realicen copias de seguridad periódicas de la base de datos  
para poder recuperar la información ante un fallo.

**R.N.F. 10. Disponibilidad**  
Como socio  
quiero que el sistema esté disponible durante el horario de apertura del gimnasio  
para consultar mis datos y reservar clases cuando lo necesite.


-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


