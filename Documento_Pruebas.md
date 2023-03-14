# Pruebas de software

## Tabla de Contenidos

---

[Tabla de Contenidos](#tabla-de-contenidos)
1. [Objetivos](#objetivos)
2. [Alcance](#alcance)
3. [Requerimientos para pruebas](#requerimientos-para-pruebas)
    1. [Etapa 1 Pruebas de autenticación y administración de usuarios](#etapa-1-pruebas-de-autenticación-y-administración-de-usuarios)
    2. [Etapa 2 Pruebas de búsqueda y filtración de vehículos](#etapa-2-pruebas-de-búsqueda-y-filtración-de-vehículos)
    3. [Etapa 3 Pruebas de chat con el servicio al cliente](#etapa-3-pruebas-de-chat-con-el-servicio-al-cliente)
    4. [Etapa 4 Pruebas de visualización y catálogo de automóviles](#etapa-4-pruebas-de-visualización-y-catálogo-de-automóviles)
    5. [Etapa 5 Pruebas de performance y estadísticas de agencias](#etapa-5-pruebas-de-performance-y-estadísticas-de-agencias)
    6. [Etapa 6 Pruebas del proceso de agendar pruebas de manejo](#etapa-6-pruebas-del-proceso-de-agendar-pruebas-de-manejo)
    7. [Etapa 7 Pruebas de compra de vehículos](#etapa-7-pruebas-de-compra-de-vehículos)
     
5. [Estrategia de pruebas](#estrategia-de-pruebas)
    1. [Descripción de la Estrategia](#descripción-de-la-estrategia)
    2. [Registro de Resultados](#registro-de-resultados)
    3. [Asunciones](#asunciones)
    4. [Niveles de pruebas](#niveles-de-pruebas)
    5. [Criterios de aceptación de pruebas](#criterios-de-aceptación-de-pruebas)
    6. [Entregables de pruebas](#entregables-de-pruebas)
    7. [Lista de hitos](#lista-de-hitos)
    8. [Estimación del esfuerzo de prueba](#estimación-del-esfuerzo-de-prueba)
  

6. [Proceso de Manejo de Pruebas](#Proceso-de-Manejo-de-Pruebas)


 
    
---

## Objetivos
Las metas que se desean alcanzar en el desarrollo de las pruebas de software están relacionadas con cumplir todos los requerimientos funcionales que el socio formador nos proveyó y a grandes rasgos estas son nuestras metas:

* Autenticación funcional y segura
* Búsqueda de vehículos exacta y fidedigna
* Chat con servicio al cliente amigable 
* Visualización de vehículos flexible y accesible
* Performance confiable y preciso
* Pruebas de manejo rápidas y a domicilio
* Experiencia de compra de vehículos fiable, funcional, rápida y flexible

El objetivo principal de las pruebas es asegurar de que entreguemos un producto funcional, seguro, con capacidad escalable, adaptabilidad, económico y con una experiencia de usuario amigable, que pueda generar ingresos al socio formador y al mismo tiempo revolucione la compra de vehículos nuevos en toda la República Mexicana.


## Alcance

**Stakeholders (NDS):**
Ellos utilizarán este documento para analizar y determinar si estamos entregando la plataforma que ellos esperan y si cumple con los requerimientos acordados.

**Project Manager:**
El PM va a utilizar este documento para programar las pruebas estáticas en los sprints subsecuentes, así como validar los recorridos de las funcionalidades críticas.

**Miembros del equipo (desarrolladores):**
Nosotros utilizaremos este documento para programar, planear y desarrollar las pruebas dinámicas.



En este periodo únicamente nos enfocaremos en realizar pruebas funcionales de caja negra para revisar los componentes principales de nuestra plataforma. En caso de que las pruebas de caja negra fallen tendremos que implementar pruebas de caja blanca. En este momento no está dentro de nuestro alcance hacer pruebas no funcionales por falta de tiempo y presupuesto, pero si en el futuro el socio formador desea que realicemos este tipo de pruebas podemos tomarlo en cuenta para implementarlo en un nuevo plan con fechas de entrega y presupuestos más razonables. 

---

## Requerimientos para pruebas
A continuación podrán observar una lista de requerimientos detallados de prueba en donde se especificarán cada uno de los módulos que tienen que ser probados para asegurar que la plataforma funcione de forma adecuada:

### Etapa 1 Pruebas de autenticación y administración de usuarios
* Pruebas de registro, login y autenticación de usuarios
* Pruebas de administración de empleados (para dar de alta vendedores, gerentes, dueños de agencia, etc.)
* Pruebas  de administración de agencias (para dar de alta super-admins, grupos automotrices, agencias individuales, etc.)
* Pruebas para dar de alta nuevas agencias

### Etapa 2 Pruebas de búsqueda y filtración de vehículos
* Pruebas para asegurarnos de que la API de GCP está recibiendo el lenguaje natural y está guardando los valores importantes de los vehículos de forma pertinente
* Pruebas para asegurarnos de que los filtros convencionales estén funcionando de manera correcta

### Etapa 3: Pruebas de chat con el servicio al cliente
*  Pruebas de contacto entre el servicio al cliente y el usuario

### Etapa 4: Pruebas de visualización y catálogo de automóviles
* Pruebas para visualizar las tarjetas de los vehículos registrados en la plataforma
* Pruebas para comparar las características y precios de los diferentes vehículos que la plataforma ofrece
* Pruebas para dar de alta el catálogo de los vehículos de cada agencia

### Etapa 5: Pruebas de performance y estadísticas de agencias
* Pruebas relacionadas con las estadísticas de las ventas, contactos, performance e información general de las agencias
* Pruebas del estado del proceso en el que se encuentra una venta activa

### Etapa 6: Pruebas del proceso de agendar pruebas de manejo
* Probar que se puedan subir y verificar los documentos personales
* Probar que el cliente se ponga en contacto con el vendedor de la agencia
* Probar la selección de ubicación por parte del cliente para acordar la entrega del automóvil 
* Probar la selección de fecha y horario asignado para realizar la prueba de manejo

### Etapa 7: Pruebas de compra de vehículos y fiabilidad

* Pruebas relacionadas a la configuración de planes de financiamiento por parte de las agencias
* Pruebas para seleccionar plan de financiamiento por parte del cliente
* Pruebas para elegir método de pago 
* Pruebas para visualizar la información de las cuentas bancarias de las agencias
* Pruebas para realizar pagos mensuales y de contado
* Pruebas de fiabilidad generales para asegurarnos de que estamos entregando una plataforma de calidad

---

## Estrategia de pruebas

Para asegurar el correcto funcionamiento del sistema, en comparación a lo necesitado y establecido por el cliente, se necesita tener una estrategia para la ejecución de pruebas. Nuestra propuesta de estrategia considera las necesidades y limitaciones que se tienen en el proyecto.

En este proyecto solamente se probarán requerimientos funcionales puesto que los requerimiento no funcionales fueron establecidos muy generales y no hay la suficiente especificación para que sean probados.

### Descripción de la Estrategia

**1. Pruebas Informales**

Las primeras pruebas a realizar en cada componente elaborado deberán ser las pruebas informales, las cuales serán ejecutadas por los mismos desarrolladores al terminar sus componentes verificando que el componente funcione como se esperaba. Esto puede ahorrar mucho tiempo y recursos puesto que las siguientes no se harán pruebas más elaboradas si se detectan los errores en esta primera etapa.


**2. Pruebas Unitarias**

Las primeras pruebas a desarrollar serán las unitarias, dichas pruebas se harán en paralelo con el desarrollo del proyecto, ejecutando las cada que se desarrolle un nuevo componente o módulo con el fin de detectar errores en tempranas etapas y evitar costos en un futuro. 
El primer tipo de prueba unitaria que se deberá ejecutar al desarrollar un nuevo componente será la ‘caja negra’ de entrada y salida para todos los componentes y ‘caja negra’ de historias de usuario con funcionalidades críticas. Si la prueba es exitosa se continuará con los siguientes componentes. En caso de fallar, se ejecutará la prueba de ‘caja blanca’ de camino básico para detectar en qué parte exactamente está el error.

**3. Pruebas de Integración**

Las pruebas de integración se harán cuando se hayan hecho pruebas unitarias sobre todos los componentes de una parte del sistema. Se harán pruebas de integración ascendentes para conseguir identificar los errores con mayor facilidad.

**4. Pruebas de Aceptación**

Cada cierto número de sprints se hará una prueba de aceptación con el cliente en base a las historias de usuario, previamente definidas, para que acepte el funcionamiento y comportamiento de esa funcionalidad. En caso de aceptación se continuará con el desarrollo. En caso de falló se revisará la diferencia con lo establecido en los requerimientos y se decidirá si los cambios proceden o se ignoran.

**5. Pruebas Estáticas**

Las pruebas estáticas se realizan simultáneamente con las demás pruebas puesto que tanto este documento como los demás que describen el sistema deben de actualizarse y verificar que sigan siendo correctos mientras avanza el sistema.

**6. Pruebas No Funcionales**

Las pruebas no funcionales se realizarán en menor medida y solo las esenciales requeridas por el cliente por cuestiones de falta de tiempo y recursos. Las pruebas de carga y rendimiento se ejecutarán en las últimas semanas del proyecto si se tiene el tiempo suficiente. En las asunciones indicamos que realizar esta etapa es muy complicada y que probablemente no lo hagamos en estas 10 semanas.

### Registro de Resultados
Las pruebas y sus resultados serán registrados en una aplicación tercera. Las pruebas tendrán 4 estados distintos:
- Pendiente
- En proceso
- Completada
- Fallida

Las pruebas serán registradas usando un formato predefinido el cual se encuentra en la siguiente liga:
https://docs.google.com/document/d/1t2Xix2SGu7ehTf0pryhvRfB8F-wArDWJ7EIHMivqNzc/edit?usp=sharing


### Asunciones

- Tendremos el tiempo suficiente para probar unitariamente todos los componentes.
- Los tests serán hechos en el mismo ambiente de pruebas.
- El ambiente de pruebas es muy similar o igual al ambiente de producción.
- Las pruebas de caja blanca solo se realizan cuando las pruebas de caja negra fallen.
- Tanto el documento de pruebas como los demás documentos estarán actualizados con los cambios que se realicen a lo largo del proyecto.
- Las historias de usuario están bien definidas.
- Se llevará registro de todas las pruebas realizadas así como de sus resultados.
- Debido a limitaciones de tiempo solo se buscará hacer pruebas unitarias y de integración. Por lo que las pruebas de rendimiento, carga y estrés no se realizarán.

### Niveles de Pruebas

##### - Pruebas Unitarias

Propósito: Estas pruebas son realizadas para verificar la funcionalidad de los requerimientos funcionales ya definidos.

Alcance: Todos los requerimientos funcionales que terminan siendo implementados para generar el producto serán probados.

Probadores: Equipo de Pruebas

Método: Se harán pruebas de caja negra para cada requerimiento funcional del sistema. En caso de que las prubas fallen, el equipo de pruebs estará encargado de correr pruebas de caja blanca para identificar en donde yace el problema

Ritmo: Cada vez que logremos algun hito, se realizaran las pruebas para verificar que todo esta en orden.

##### - Pruebas de integración

Propósito: Aqui probaremos la interacción de nuestra plataforma con distintos servicios, como lo es la base de datos, comunicación entre frontend y backend, etc. 

Alcance: Se buscara probar todas las interacciones de multiples procesos de esta manera. Para así verificar que no estamos teniendo ningun problema en ese sentido.

Probadores: Equipo de Pruebas

Método: Se seguira el metodo "Top Down", el que busca que se hagan pruebas de integración en modulos de alto nivel primero y hasta el final hacer pruebas de bajo nivel.

Ritmo: Para realizar este tipo de pruebas necesitamos tener ya alguna parte del sistema avanzada. De igual manera definiremos hitos en relacion a pruebas de integración, que nos harán saber cuando es el momento indicado para probar.

##### - Pruebas de aceptación de usuario

Propósito: Le presentaremos la plataforma a el socio formador, ellos nos darán critica constructiva para ajustarnos aún más a sus necesidades.

Alcance: Cadda semana y de igual manera hasta el final del proceso de desarrollo el socio formador verá todas las funcionalidades que se han implementado hasta el momento y nos darán su opinión al respecto.

Probadores: Socio formador (NDS) con el equipo de pruebas

Método: Presentar el software de manera formal al socio formador para que nos den retroalimentación. 

Ritmo: Cada vez que se complete una funcionalidad de la plataforma, se le enseñara al socio formador.

---

### Proceso de Manejo de Pruebas

#### Participantes
Durante todo el proceso de desarrollo de pruebas del proyecto, participaran los siguientes roles:

- Tester: Encargado de realizar las pruebas informales, de caja negra y de caja blanca.
- Jefe de Testers: Encargado de repartir tareas a los testers, sera el que determine si las pruebaas realizadas fueron correctas y pasan los estandares de calidad. Esta persona sera encargada de aprobar o no las pruebas realizadas, y tambien de tomar decisicones durante el desarrollo de pruebas

#### Pruebas Informales 

Las pruebas informales se llevaran acabo durante el sprint, cada desarrollador debera de probar su codigo antes de enviar un pull rquest al repositorio. Esto con fin de agilizar el proceso de pruebas y reducir la cantidad de bugs a la hora de hacer las pruebas formales.

De igual manera, mientras se desarrolla, cada programador debe asegurarse que se estan llevando los lineamientos de calidad de software, como nombramiento de variables correctas, tener el codigo en ingles, separar codigo en funciones, etc. Lo cual ayudara a mejorar la legibilidad del codigo.

Por ultimo cada programador debera proponer al menos tres pruebas unitarias, ya sean casos de exito o de error. Mas adelante el encargado de pruebas del sprint aprobara las pruebas unitarias que se deberan de desarrollar el siguiente sprint.

#### Pruebas Formales 

Pruebas de caja Negra:

- Cada sprint, el jefe de pruebas debera revisar las propuestas enviadas previamente por los desarolladores. Despues de confirmar estas, el jefe debera asignar a cada desarrollador cierto numero de pruebas, de preferencia de algo que no hayan trabajado previamente, con fin de evitar sesgos.

- El tester debera programar las pruebas unitarias requeridas por el jefe, ya sean de backend, frontend o incluso pruebase de integración.

Pruebas de caja Blanca:

- En caso de encontrar un Bug, o que fallen las pruebas de caja negra, el tester debera de notificar al equipo.
- Una vez notifcado, el jefe de de testing, debera de decidir si es necesario llevar una prueba de caja blanca o si no es necesario para solucionar el problema.
- En caso de que sea necesario una prueba de caja blanca, el tester debera relizar un analisis profundo del modulo que se esta desarrollando, con fin de encontrar el problema. Una vez identificado el problema, el bug debera de ser resuelto por la misma persona que realizo la prueba de caja blanca.
- Cuando el tester termine la preuba de caja blanca, se realizaran de nuevo pruebas de caja negra. 
- El ciclo continua hasta que se hayan resuelto los problemas encontrados

---
