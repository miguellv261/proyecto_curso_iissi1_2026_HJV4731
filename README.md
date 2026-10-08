#IISSI FIT

## Miembros del grupo L7-DF-GRUPO_3

 López Velasco, Miguel Ángel
 Jerez Gavira, Alejandro
 Alaya Sotillo, José


## 1. Introducción al problema

IISSIFIT es un gimnasio de ámbito local que comenzó como un pequeño negocio familiar dedicado a ofrecer servicios de entrenamiento y actividades deportivas a los vecinos de la zona. En sus primeros años contaba con alrededor de 100 clientes, por lo que la gestión de la información se realizaba manualmente mediante hojas de cálculo, documentos impresos y anotaciones en papel.

Actualmente, IISSIFIT ofrece diferentes servicios, como acceso a las instalaciones, clases dirigidas, entrenamientos personalizados y planes de membresía. Los principales usuarios del sistema son los socios o clientes, los entrenadores, el personal de recepción y administración y los administradores o propietarios del gimnasio.

El crecimiento del negocio ha hecho que la gestión manual resulte cada vez menos eficiente. Entre los principales problemas se encuentran los errores en el registro de socios y pagos, la duplicidad de información, la dificultad para consultar la disponibilidad de clases, la actualización de cuotas y la pérdida de tiempo en tareas administrativas. Además, la falta de información centralizada dificulta la realización de estadísticas y la toma de decisiones.

Los propietarios esperan continuar con la expansión del gimnasio, aumentando el número de socios hasta aproximadamente 2.000, incorporando nuevas salas, contratando más entrenadores y ampliando la oferta de actividades. Este crecimiento supondría un aumento considerable de la cantidad de información y operaciones que deben gestionarse.

Para solucionar estos problemas, se plantea el diseño y desarrollo de una base de datos para la gestión de IISSIFIT. Esta base de datos permitirá centralizar y organizar la información relacionada con socios, entrenadores, clases, salas, reservas, asistencias, membresías y pagos, facilitando su consulta y actualización.

Con esta base de datos se espera reducir errores, agilizar las tareas administrativas, mejorar la organización y disponer de información actualizada y fiable, proporcionando una estructura adecuada para el crecimiento futuro del gimnasio.


## 2. Glosario de términos

- Términos específicos del dominio del problema, ordenados alfabéticamente. Se valorará la presencia de información multimedia.

## 3. Visión general del sistema

### 3.1. Requisitos generales

### 3.2. Usuarios del sistema

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Título requisito funcional

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### 4.1.1. Requisitos de información

##### R.I.01. Título requisito de información

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

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


