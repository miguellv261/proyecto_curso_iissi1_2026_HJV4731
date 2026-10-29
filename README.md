# IISSIFIT

## Miembros del grupo L7-DF-GRUPO_3

 - López Velasco, Miguel Ángel
 - Jerez Gavira, Alejandro
 - Alaya Sotillo, José

contraseña, email, tipo de usuario, ficha fisica dentro de socio, RN DE AFORO, RN CLASE EN SALA, RN MEMBRESIA, TRIGGER ENTRENADOR


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

## 2. Visión general del sistema

### 2.1. Requisitos generales

- **RG-01:** El sistema deberá gestionar a los socios.
- **RG-02:** El sistema deberá gestionar a los administradores.
- **RG-03:** El sistema deberá gestionar la membresía.
- **RG-04:** El sistema deberá gestionar a los entrenadores.
- **RG-05:** El sistema deberá gestionar las salas del gimnasio.
- **RG-06:** El sistema deberá gestionar las clases.
- **RG-07:** El sistema deberá gestionar las reservas de los socios.
- **RG-08:** El sistema deberá gestionar los pagos.
- **RG-09:** El sistema deberá controlar la asistencia de los socios.


### 2.2. Usuarios del sistema

#### Administrador

Es el usuario con mayor nivel de acceso. Sus funciones principales serán:

- Consultar la información de socios y entrenadores.
- Gestionar las membresías ofrecidas.
- Supervisar las clases y salas.
- Consultar reservas y pagos.
- Obtener información sobre ingresos y ocupación.
- Supervisar el funcionamiento general de IISSIFIT.


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


## 3. Catálogo de requisitos

### 3.1. Requisitos funcionales

#### R.F.01. Listado de socios

Como recepcionista  
quiero consultar el listado completo de socios  
para localizar rápidamente a cualquier socio registrado.

**Prueba de aceptación**

* Se muestran todos los socios registrados en el sistema.
* Para cada socio se muestran su identificador, nombre, apellidos y estado.
* Si no hay socios registrados, se muestra un listado vacío.

#### R.F.02. Creación de socios

Como recepcionista  
quiero registrar un nuevo socio  
para mantener actualizada la información del gimnasio.

**Prueba de aceptación**

* Se almacenan todos los datos del socio indicados en RI-01.
* El socio queda registrado con estado activo y con la fecha de alta del día.
* Si ya existe un socio con el mismo DNI, el sistema rechaza el registro.
* Si falta algún dato obligatorio, el sistema rechaza el registro.

#### R.F.03. Edición de socios

Como recepcionista  
quiero modificar los datos de un socio  
para mantener su información correcta y actualizada.

**Prueba de aceptación**

* Se actualizan los datos modificados del socio (RI-01) y se conservan los demás.
* No se puede asignar un DNI que ya pertenezca a otro socio.
* Se puede cambiar el estado del socio entre activo e inactivo.
* Si el socio no existe, el sistema informa de que no se ha encontrado.

#### R.F.04. Borrado de socios

Como administrador  
quiero eliminar un socio del sistema  
para depurar registros que ya no son necesarios.

**Prueba de aceptación**

* El socio eliminado deja de aparecer en el listado de socios.
* Si el socio tiene reservas o pagos asociados, el sistema impide el borrado.
* Si el socio no existe, el sistema informa de que no se ha encontrado.

#### R.F.05. Listado de fichas físicas

Como recepcionista  
quiero consultar el listado de fichas físicas  
para conocer la información física registrada de los socios.

**Prueba de aceptación**

* Se muestran todas las fichas físicas registradas, cada una junto al socio al que pertenece.
* Para cada ficha se muestran el peso, la altura, el objetivo deportivo y la fecha de última actualización (RI-02).
* Si no hay fichas registradas, se muestra un listado vacío.

#### R.F.06. Creación de fichas físicas

Como recepcionista  
quiero crear la ficha física de un socio  
para registrar su situación física y su objetivo deportivo.

**Prueba de aceptación**

* Se almacenan el peso, la altura, el objetivo deportivo y las observaciones del socio (RI-02).
* Las fechas de creación y de última actualización se establecen con la fecha del día.
* Un socio no puede tener más de una ficha física.
* Si el socio no existe, el sistema rechaza la creación.

#### R.F.07. Edición de fichas físicas

Como recepcionista  
quiero modificar la ficha física de un socio  
para mantener actualizados sus datos físicos.

**Prueba de aceptación**

* Se actualizan los datos modificados de la ficha (RI-02) y se conservan los demás.
* La fecha de última actualización se establece con la fecha del día.
* La fecha de creación no se modifica.
* Si el socio no tiene ficha física, el sistema lo indica.

#### R.F.08. Borrado de fichas físicas

Como administrador  
quiero eliminar la ficha física de un socio  
para eliminar información que ya no es necesaria.

**Prueba de aceptación**

* La ficha eliminada deja de mostrarse en el listado de fichas físicas.
* El socio al que pertenecía la ficha no se elimina.
* Si la ficha no existe, el sistema informa de que no se ha encontrado.

#### R.F.09. Listado de membresías

Como recepcionista  
quiero consultar las membresías ofrecidas  
para informar a los clientes.

**Prueba de aceptación**

* Se muestran todas las membresías registradas.
* Para cada una se muestran nombre, precio, duración y estado de disponibilidad (RI-03).
* Si no hay membresías registradas, se muestra un listado vacío.

#### R.F.10. Creación de membresías

Como administrador  
quiero crear una nueva membresía  
para ampliar la oferta del gimnasio.

**Prueba de aceptación**

* Se almacenan el nombre, la descripción, el precio, la duración y los servicios incluidos (RI-03).
* La membresía se crea con estado disponible.
* El precio debe ser mayor o igual que cero y la duración mayor que cero.
* No se puede crear una membresía con el mismo nombre que otra existente.

#### R.F.11. Edición de membresías

Como administrador  
quiero modificar los datos de una membresía  
para actualizar sus condiciones, como el precio o los servicios incluidos.

**Prueba de aceptación**

* Se actualizan los datos modificados de la membresía (RI-03) y se conservan los demás.
* Se puede cambiar el estado de disponibilidad de la membresía.
* Los socios que ya tienen contratada la membresía mantienen su asociación.
* Si la membresía no existe, el sistema informa de que no se ha encontrado.

#### R.F.12. Borrado de membresías

Como administrador  
quiero eliminar una membresía  
para retirar planes que ya no se ofrecen.

**Prueba de aceptación**

* La membresía eliminada deja de aparecer en el listado de membresías.
* Si hay socios con la membresía contratada, el sistema impide el borrado.
* Si la membresía no existe, el sistema informa de que no se ha encontrado.

#### R.F.13. Listado de entrenadores

Como administrador  
quiero consultar el listado completo de entrenadores  
para conocer la plantilla del gimnasio.

**Prueba de aceptación**

* Se muestran todos los entrenadores registrados.
* Para cada uno se muestran nombre, apellidos, especialidad y estado laboral (RI-04).
* Si no hay entrenadores registrados, se muestra un listado vacío.

#### R.F.14. Creación de entrenadores

Como administrador  
quiero registrar un nuevo entrenador  
para incorporarlo a la plantilla del gimnasio.

**Prueba de aceptación**

* Se almacenan todos los datos del entrenador indicados en RI-04.
* Si ya existe un entrenador con el mismo DNI, el sistema rechaza el registro.
* Si falta algún dato obligatorio, el sistema rechaza el registro.

#### R.F.15. Edición de entrenadores

Como administrador  
quiero modificar los datos de un entrenador  
para mantener actualizada la plantilla.

**Prueba de aceptación**

* Se actualizan los datos modificados del entrenador (RI-04) y se conservan los demás.
* No se puede asignar un DNI que ya pertenezca a otro entrenador.
* Se puede cambiar el estado laboral del entrenador.
* Si el entrenador no existe, el sistema informa de que no se ha encontrado.

#### R.F.16. Borrado de entrenadores

Como administrador  
quiero eliminar un entrenador del sistema  
para depurar registros de personal que ya no es necesario.

**Prueba de aceptación**

* El entrenador eliminado deja de aparecer en el listado de entrenadores.
* Si el entrenador tiene clases asignadas, el sistema impide el borrado.
* Si el entrenador no existe, el sistema informa de que no se ha encontrado.

#### R.F.17. Listado de salas

Como administrador  
quiero consultar el listado completo de salas  
para conocer las instalaciones del gimnasio.

**Prueba de aceptación**

* Se muestran todas las salas registradas.
* Para cada una se muestran nombre, aforo máximo y estado de disponibilidad (RI-05).
* Si no hay salas registradas, se muestra un listado vacío.

#### R.F.18. Creación de salas

Como administrador  
quiero crear una nueva sala  
para ampliar las instalaciones del gimnasio.

**Prueba de aceptación**

* Se almacenan el nombre, la ubicación, el aforo máximo, el tipo de actividad y la disponibilidad (RI-05).
* El aforo máximo debe ser mayor que cero.
* No se puede crear una sala con el mismo nombre que otra existente.

#### R.F.19. Edición de salas

Como administrador  
quiero modificar los datos de una sala  
para mantener actualizada la información de las instalaciones.

**Prueba de aceptación**

* Se actualizan los datos modificados de la sala (RI-05) y se conservan los demás.
* No se puede reducir el aforo por debajo del máximo de participantes de una clase asignada a la sala.
* Se debe aplicar la regla de negocio R.N.02.
* Si la sala no existe, el sistema informa de que no se ha encontrado.

#### R.F.20. Borrado de salas

Como administrador  
quiero eliminar una sala  
para retirar espacios que ya no se utilizan.

**Prueba de aceptación**

* La sala eliminada deja de aparecer en el listado de salas.
* Si la sala tiene clases asignadas, el sistema impide el borrado.
* Si la sala no existe, el sistema informa de que no se ha encontrado.

#### R.F.21. Listado de clases

Como socio  
quiero consultar las clases programadas  
para decidir cuáles reservar.

**Prueba de aceptación**

* Se muestran las clases con su nombre, fecha, hora, entrenador y sala (RI-06).
* No se muestran las clases canceladas.
* Si no hay clases programadas, se muestra un listado vacío.

#### R.F.22. Creación de clases

Como administrador  
quiero programar una nueva clase  
para organizar la oferta de actividades del gimnasio.

**Prueba de aceptación**

* Se almacenan todos los datos de la clase indicados en RI-06, incluyendo el entrenador responsable y la sala asignada.
* El número máximo de participantes no puede superar el aforo de la sala asignada.
* El entrenador y la sala no pueden tener otra clase cuyo horario coincida con la nueva.
* Se deben aplicar las reglas de negocio R.N.02 y R.N.04.

#### R.F.23. Edición de clases

Como administrador  
quiero modificar los datos de una clase  
para adaptar la programación a los cambios necesarios.

**Prueba de aceptación**

* Se actualizan los datos modificados de la clase (RI-06) y se conservan los demás.
* Si se cambia el horario, el entrenador o la sala, no puede haber coincidencia con otra clase.
* El número máximo de participantes no puede ser inferior al número de reservas activas ni superior al aforo de la sala.
* Se deben aplicar las reglas de negocio R.N.02 y R.N.04.
* Si la clase no existe, el sistema informa de que no se ha encontrado.

#### R.F.24. Borrado de clases

Como administrador  
quiero eliminar una clase  
para retirar de la programación las clases que no se van a impartir.

**Prueba de aceptación**

* La clase eliminada deja de aparecer en el listado de clases.
* Si la clase tiene reservas activas, el sistema impide el borrado.
* Si la clase no existe, el sistema informa de que no se ha encontrado.

#### R.F.25. Listado de reservas

Como recepcionista  
quiero consultar las reservas de los socios  
para ayudarles con sus gestiones.

**Prueba de aceptación**

* Se muestran las reservas con el socio, la clase, la fecha de realización y el estado (RI-07).
* Se puede filtrar el listado por socio y por estado activa o cancelada.
* Un socio que consulta sus reservas solo ve las suyas.
* Si no hay reservas, se muestra un listado vacío.

#### R.F.26. Creación de reservas

Como socio  
quiero reservar una clase  
para asegurar mi plaza en la actividad.

**Prueba de aceptación**

* La reserva se crea con estado activa y con la fecha y hora de realización actuales.
* El socio debe estar activo, tener una membresía vigente y la clase debe tener plazas disponibles.
* El socio no puede tener otra reserva activa en una clase cuyo horario coincida.
* Se deben aplicar las reglas de negocio R.N.01, R.N.02 y R.N.03.

#### R.F.27. Edición de reservas

Como socio  
quiero cancelar o cambiar una reserva  
para organizar mis actividades.

**Prueba de aceptación**

* Se puede cambiar el estado de una reserva de activa a cancelada.
* Las reservas canceladas dejan de contar como plazas ocupadas de la clase.
* Si se cambia la clase reservada, se aplican las mismas comprobaciones que en la creación.
* Se deben aplicar las reglas de negocio R.N.01, R.N.02 y R.N.03.
* Un socio solo puede modificar sus propias reservas.

#### R.F.28. Borrado de reservas

Como administrador  
quiero eliminar una reserva  
para corregir registros erróneos.

**Prueba de aceptación**

* La reserva eliminada deja de aparecer en el listado de reservas.
* Si la reserva tiene una asistencia registrada, el sistema impide el borrado.
* Si la reserva no existe, el sistema informa de que no se ha encontrado.

#### R.F.29. Listado de pagos

Como recepcionista  
quiero consultar los pagos realizados  
para mantener actualizada la situación de los socios.

**Prueba de aceptación**

* Se muestran los pagos con el socio, la fecha, el importe, el método y el concepto (RI-08).
* Se puede filtrar el listado por socio y por periodo.
* Un socio que consulta sus pagos solo ve los suyos.
* Si el periodo indicado no es válido (fecha de inicio posterior a la de fin), el sistema lo rechaza.

#### R.F.30. Creación de pagos

Como recepcionista  
quiero registrar un pago de un socio  
para mantener actualizada su situación económica.

**Prueba de aceptación**

* Se almacenan el socio, la membresía relacionada, la fecha, el importe, el método de pago, el concepto y el estado (RI-08).
* El importe debe ser mayor que cero.
* El método de pago debe ser efectivo, tarjeta o transferencia.
* Si el socio no existe, el sistema rechaza el registro.

#### R.F.31. Edición de pagos

Como recepcionista  
quiero modificar los datos de un pago  
para corregir errores en el registro.

**Prueba de aceptación**

* Se actualizan los datos modificados del pago (RI-08) y se conservan los demás.
* El importe modificado debe seguir siendo mayor que cero.
* Se puede cambiar el estado del pago.
* Si el pago no existe, el sistema informa de que no se ha encontrado.

#### R.F.32. Borrado de pagos

Como administrador  
quiero eliminar un pago  
para depurar registros duplicados o erróneos.

**Prueba de aceptación**

* El pago eliminado deja de aparecer en el listado de pagos.
* Los ingresos mensuales se recalculan sin tener en cuenta el pago eliminado.
* Si el pago no existe, el sistema informa de que no se ha encontrado.

#### R.F.33. Listado de asistencias

Como entrenador  
quiero consultar las asistencias de los socios a mis clases  
para conocer quiénes han acudido.

**Prueba de aceptación**

* Se muestran las asistencias de la clase indicada con el socio y la fecha y hora de registro.
* Solo se muestran asistencias de clases asignadas al entrenador.
* Si la clase no tiene asistencias registradas, se muestra un listado vacío.

#### R.F.34. Creación de asistencias

Como recepcionista  
quiero registrar la asistencia de un socio a una clase  
para controlar quién acude a las actividades.

**Prueba de aceptación**

* Solo se puede registrar la asistencia de un socio que tenga una reserva activa en la clase.
* No se puede registrar dos veces la asistencia del mismo socio a la misma clase.
* Si el socio no tiene reserva activa en la clase, el sistema rechaza el registro.
* Se debe aplicar la regla de negocio R.N.01.

#### R.F.35. Edición de asistencias

Como recepcionista  
quiero modificar el registro de una asistencia  
para corregir errores en el control de asistencia.

**Prueba de aceptación**

* Se actualizan los datos modificados de la asistencia y se conservan los demás.
* La asistencia debe seguir asociada a una reserva activa del socio en esa clase.
* Si la asistencia no existe, el sistema informa de que no se ha encontrado.

#### R.F.36. Borrado de asistencias

Como administrador  
quiero eliminar un registro de asistencia  
para corregir registros erróneos.

**Prueba de aceptación**

* La asistencia eliminada deja de aparecer en el listado de asistencias.
* La reserva asociada a la asistencia no se elimina.
* Si la asistencia no existe, el sistema informa de que no se ha encontrado.

#### 3.1.1. Requisitos de información

##### RI-01. Información de los socios

De cada socio se almacenará: en linea,,,,

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

#### 3.1.2. Reglas de negocio

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


### 3.2. Mapa de historias de usuario (opcional) de forma grafica******

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

### 3.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Rendimiento**
Como recepcionista
quiero que las consultas habituales muestren sus resultados en menos de tres segundos, incluso con varios usuarios conectados simultáneamente
para atender a los socios sin esperas y garantizar una experiencia fluida.

**R.N.F. 02. Seguridad**
Como administrador
quiero que el acceso a la información esté limitado según el tipo de usuario y protegido mediante mecanismos de autenticación segura
para que cada usuario solo consulte y modifique lo que le corresponde.

**R.N.F. 03. Privacidad**
Como socio
quiero que mis datos personales estén protegidos frente a accesos no autorizados mediante medidas de seguridad adecuadas
para garantizar la confidencialidad de mi información.

**R.N.F. 04. Usabilidad**
Como recepcionista
quiero una interfaz clara, sencilla e intuitiva, con menús y opciones comprensibles
para realizar mis tareas sin necesidad de una formación extensa.

**R.N.F. 05. Integridad**
Como administrador
quiero que el sistema impida la introducción de información duplicada, incompleta o contradictoria
para disponer de datos fiables y coherentes.

**R.N.F. 06. Escalabilidad**
Como administrador
quiero que el sistema pueda gestionar el crecimiento desde los 100 socios iniciales hasta aproximadamente 2.000
para poder expandir el gimnasio sin rediseñar la base de datos.

**R.N.F. 07. Compatibilidad**
Como administrador
quiero que la base de datos funcione correctamente en un servidor MariaDB
para poder desplegarla en la infraestructura prevista.

**R.N.F. 08. Mantenibilidad**
Como administrador
quiero poder añadir nuevas salas, clases, membresías y servicios sin realizar grandes modificaciones en la estructura del sistema
para ampliar la oferta del gimnasio de forma sencilla.

**R.N.F. 09. Copias de seguridad**
Como administrador
quiero que se realicen copias de seguridad periódicas de la base de datos y que sea posible restaurarlas
para recuperar la información ante un fallo o una incidencia.

**R.N.F. 10. Disponibilidad**
Como socio
quiero que el sistema esté disponible al menos el 99 % del tiempo durante el horario de apertura del gimnasio y permita el acceso desde distintos dispositivos
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


