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
- Gestionar la información de los administradores.
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

#### R.F.05. Listado de administradores

Como administrador  
quiero consultar el listado completo de administradores  
para conocer quién gestiona el sistema.

**Prueba de aceptación**

* Se muestran todos los administradores registrados.
* Para cada uno se muestran su identificador, nombre y apellidos (RI-02).
* Solo un administrador puede consultar este listado.

#### R.F.06. Creación de administradores

Como administrador  
quiero registrar un nuevo administrador  
para que pueda gestionar el sistema.

**Prueba de aceptación**

* Se almacenan todos los datos del administrador indicados en RI-02.
* El administrador queda registrado con la fecha de alta del día.
* Si ya existe un administrador con el mismo DNI, el sistema rechaza el registro.
* Si falta algún dato obligatorio, el sistema rechaza el registro.

#### R.F.07. Edición de administradores

Como administrador  
quiero modificar los datos de un administrador  
para mantener su información correcta y actualizada.

**Prueba de aceptación**

* Se actualizan los datos modificados del administrador (RI-02) y se conservan los demás.
* No se puede asignar un DNI que ya pertenezca a otro administrador.
* Si el administrador no existe, el sistema informa de que no se ha encontrado.

#### R.F.08. Borrado de administradores

Como administrador  
quiero eliminar un administrador del sistema  
para retirar el acceso a quien ya no gestiona el gimnasio.

**Prueba de aceptación**

* El administrador eliminado deja de aparecer en el listado de administradores.
* No se puede eliminar al único administrador del sistema.
* Si el administrador no existe, el sistema informa de que no se ha encontrado.

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

#### R.F.37. Asignación o renovación de la membresía de un socio

Como recepcionista  
quiero asignar o renovar la membresía de un socio  
para que pueda reservar clases mientras su membresía esté vigente.

**Prueba de aceptación**

* Se asocia al socio la membresía indicada (RI-01) con la fecha de contratación o renovación del día.
* Solo se pueden asignar membresías cuyo estado es disponible (RI-03).
* Al renovar, la vigencia se calcula a partir de la duración de la membresía (RI-03).
* Cuando termina la vigencia, la membresía deja de estar vigente y el socio no puede reservar clases.
* Si el socio o la membresía no existen, el sistema informa de que no se han encontrado.
* Se debe aplicar la regla de negocio R.N.01.

#### R.F.38. Consulta de plazas disponibles de una clase

Como socio  
quiero consultar las plazas disponibles de cada clase  
para decidir cuál reservar antes de que se complete.

**Prueba de aceptación**

* Para cada clase se muestra el número de plazas libres, calculado como el máximo de participantes menos las reservas activas.
* Una clase completa muestra cero plazas disponibles.
* Las reservas canceladas no cuentan como plazas ocupadas.
* No se muestran las clases canceladas.
* Se debe aplicar la regla de negocio R.N.02.

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
- Fecha de inicio de la membresía contratada.

##### RI-02. Información de los administradores

De cada administrador se almacenará:

- Identificador único.
- DNI.
- Nombre.
- Apellidos.
- Teléfono.
- Correo electrónico.
- Fecha de alta.

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


### 3.2. Mapa de historias de usuario (opcional) de forma grafica

Cada fila es un requisito general (RG) y cada columna una operación. En cada celda se indica el requisito funcional, el rol que realiza la historia y la acción.

| Requisito general | Listado | Creación | Edición | Borrado | Otras historias |
|:------------------|:--------|:---------|:--------|:--------|:----------------|
| **RG-01. Socios** | **R.F.01** · Recepcionista<br>Consultar socios | **R.F.02** · Recepcionista<br>Registrar socio | **R.F.03** · Recepcionista<br>Modificar socio | **R.F.04** · Administrador<br>Eliminar socio | |
| **RG-02. Administradores** | **R.F.05** · Administrador<br>Consultar administradores | **R.F.06** · Administrador<br>Registrar administrador | **R.F.07** · Administrador<br>Modificar administrador | **R.F.08** · Administrador<br>Eliminar administrador | |
| **RG-03. Membresías** | **R.F.09** · Recepcionista<br>Consultar membresías | **R.F.10** · Administrador<br>Crear membresía | **R.F.11** · Administrador<br>Modificar membresía | **R.F.12** · Administrador<br>Eliminar membresía | **R.F.37** · Recepcionista<br>Asignar o renovar la membresía de un socio |
| **RG-04. Entrenadores** | **R.F.13** · Administrador<br>Consultar entrenadores | **R.F.14** · Administrador<br>Registrar entrenador | **R.F.15** · Administrador<br>Modificar entrenador | **R.F.16** · Administrador<br>Eliminar entrenador | |
| **RG-05. Salas** | **R.F.17** · Administrador<br>Consultar salas | **R.F.18** · Administrador<br>Crear sala | **R.F.19** · Administrador<br>Modificar sala | **R.F.20** · Administrador<br>Eliminar sala | |
| **RG-06. Clases** | **R.F.21** · Socio<br>Consultar clases | **R.F.22** · Administrador<br>Programar clase | **R.F.23** · Administrador<br>Modificar clase | **R.F.24** · Administrador<br>Eliminar clase | **R.F.38** · Socio<br>Consultar plazas disponibles de una clase |
| **RG-07. Reservas** | **R.F.25** · Recepcionista<br>Consultar reservas | **R.F.26** · Socio<br>Reservar clase | **R.F.27** · Socio<br>Cancelar o cambiar reserva | **R.F.28** · Administrador<br>Eliminar reserva | |
| **RG-08. Pagos** | **R.F.29** · Recepcionista<br>Consultar pagos | **R.F.30** · Recepcionista<br>Registrar pago | **R.F.31** · Recepcionista<br>Corregir pago | **R.F.32** · Administrador<br>Eliminar pago | |
| **RG-09. Asistencias** | **R.F.33** · Entrenador<br>Consultar asistencias | **R.F.34** · Recepcionista<br>Registrar asistencia | **R.F.35** · Recepcionista<br>Corregir asistencia | **R.F.36** · Administrador<br>Eliminar asistencia | |

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


