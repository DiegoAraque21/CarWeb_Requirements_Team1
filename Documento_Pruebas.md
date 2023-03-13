# Pruebas de software

## Tabla de Contenidos

---

[Tabla de Contenidos](#tabla-de-contenidos)
1. [Objetivos](#objetivos)
2. [Alcance](#alcance)
    1. [Etapa 1 Pruebas de autenticación y administración de usuarios
](#etapa-1-pruebas-de-autenticación-y-administración-de-usuarios)
    2. [Etapa 2 Pruebas de búsqueda y filtración de vehículos](#etapa-2-pruebas-de-búsqueda-y-filtración-de-vehículos)
    3. [Etapa 3 Pruebas de chat con el servicio al cliente](#etapa-3-pruebas-de-chat-con-el-servicio-al-cliente)
    4. [Etapa 4 Pruebas de visualización y catálogo de automóviles](#etapa-4-pruebas-de-visualización-y-catálogo-de-automóviles)
    5. [Etapa 5 Pruebas de performance y estadísticas de agencias](#etapa-5-pruebas-de-performance-y-estadísticas-de-agencias)
    6. [Etapa 6 Pruebas del proceso de agendar pruebas de manejo](#etapa-6-pruebas-del-proceso-de-agendar-pruebas-de-manejo)
    7. [Etapa 7 Pruebas de compra de vehículos](#etapa-7-pruebas-de-compra-de-vehículos)
     
3. [Requerimientos para pruebas](#requerimientos-para-pruebas)
5. [Estrategia de pruebas](#estrategia-de-pruebas)
    1. [Descripción de la Estrategia](#descripción-de-la-estrategia)
    2. [Registro de Resultados](#registro-de-resultados)
    3. [Asunciones](#asunciones)
    4. [Niveles de pruebas](#niveles-de-pruebas)
    5. [Criterios de aceptación de pruebas](#criterios-de-aceptación-de-pruebas)
    6. [Entregables de pruebas](#entregables-de-pruebas)
    7. [Lista de hitos](#lista-de-hitos)
    8. [Estimación del esfuerzo de prueba](#estimación-del-esfuerzo-de-prueba)
  

6. [Proceso de Manejo de Pruebas]


 
    
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

Asunciones y riesgos: 
En este periodo únicamente nos enfocaremos en realizar pruebas funcionales de caja negra para revisar los componentes principales de nuestra plataforma. En caso de que las pruebas de caja negra fallen tendremos que implementar pruebas de caja negra. En este momento no está dentro de nuestro alcance hacer pruebas no funcionales por falta de tiempo y presupuesto, pero si en el futuro el socio formador desea que realicemos este tipo de pruebas podemos tomarlo en cuenta para implementarlo en un nuevo plan con fechas de entrega y presupuestos más razonables. 

Las etapas de pruebas se distribuirán de la siguiente manera:
##### Etapa 1 Pruebas de autenticación y administración de usuarios
##### Etapa 2: Pruebas de búsqueda y filtración de vehículos
##### Etapa 3: Pruebas de chat con el servicio al cliente
##### Etapa 4: Pruebas de visualización y catálogo de automóviles
##### Etapa 5: Pruebas de performance y estadísticas de agencias
##### Etapa 6: Pruebas del proceso de agendar pruebas de manejo
##### Etapa 7: Pruebas de compra de vehículos

---

## Requerimientos para pruebas
A continuación podrán observar una lista de requerimientos detallados de prueba en donde se especificarán cada uno de los módulos que tienen que ser probados para asegurar que la plataforma funcione de forma adecuada:

* Pruebas de registro, login y autenticación de usuarios
* Pruebas de administración de empleados (para dar de alta vendedores, gerentes, dueños de agencia, etc.)
* Pruebas  de administración de agencias (para dar de alta super-admins, grupos automotrices, agencias individuales, etc.)
* Pruebas para dar de alta nuevas agencias
* Pruebas para asegurarnos de que la API de GCP está recibiendo el lenguaje natural y está guardando los valores importantes de los vehículos de forma pertinente
* Pruebas para asegurarnos de que los filtros convencionales estén funcionando de manera correcta
* Pruebas de contacto entre el servicio al cliente y el usuario
* Pruebas para visualizar las tarjetas de los vehículos registrados en la plataforma
* Pruebas para comparar las características y precios de los diferentes vehículos que la plataforma ofrece
* Pruebas para dar de alta el catálogo de los vehículos de cada agencia
* Pruebas relacionadas con las estadísticas de las ventas, contactos, performance e información general de las agencias
* Pruebas del estado del proceso en el que se encuentra una venta activa
* Pruebas de todo el proceso para agendar una prueba de manejo:
* Probar que se puedan subir y verificar los documentos personales
* Probar que el cliente se ponga en contacto con el vendedor de la agencia
* Probar la selección de ubicación por parte del cliente para acordar la entrega del automóvil 
* Probar la selección de fecha y horario asignado para realizar la prueba de manejo
* Pruebas de la compra de vehículos:
* Pruebas relacionadas a la configuración de planes de financiamiento por parte de las agencias
* Pruebas para seleccionar plan de financiamiento por parte del cliente
* Pruebas para elegir método de pago 
* Pruebas para visualizar la información de las cuentas bancarias de las agencias
* Pruebas para realizar pagos mensuales y de contado
* Pruebas de fiabilidad generales para asegurarnos de que estamos entregando una plataforma de calidad

---

## Estrategia de pruebas

Para asegurar el correcto funcionamiento del sistema, en comparación a lo necesitado y establecido por el cliente, se necesita tener una estrategia para la ejecución de pruebas. Nuestra propuesta de estrategia considera las necesidades y limitaciones que se tienen en el proyecto.

### Descripción de la Estrategia
**1. Pruebas Unitarias**

Las primeras pruebas a desarrollar serán las unitarias, dichas pruebas se harán en paralelo con el desarrollo del proyecto, ejecutando las cada que se desarrolle un nuevo componente o módulo con el fin de detectar errores en tempranas etapas y evitar costos en un futuro. 
El primer tipo de prueba unitaria que se deberá ejecutar al desarrollar un nuevo componente será la ‘caja negra’ de entrada y salida para todos los componentes y ‘caja negra’ de historias de usuario con funcionalidades críticas. Si la prueba es exitosa se continuará con los siguientes componentes. En caso de fallar, se ejecutará la prueba de ‘caja blanca’ de camino básico para detectar en qué parte exactamente está el error.

**2. Pruebas de Integración**

Las pruebas de integración se harán cuando se hayan hecho pruebas unitarias sobre todos los componentes de una parte del sistema. Se harán pruebas de integración ascendentes para conseguir identificar los errores con mayor facilidad.

**3. Pruebas de Aceptación**

Cada cierto número de sprints se hará una prueba de aceptación con el cliente en base a las historias de usuario, previamente definidas, para que acepte el funcionamiento y comportamiento de esa funcionalidad. En caso de aceptación se continuará con el desarrollo. En caso de falló se revisará la diferencia con lo establecido en los requerimientos y se decidirá si los cambios proceden o se ignoran.

**4. Pruebas Estáticas**

Las pruebas estáticas se realizan simultáneamente con las demás pruebas puesto que tanto este documento como los demás que describen el sistema deben de actualizarse y verificar que sigan siendo correctos mientras avanza el sistema.

**5. Pruebas No Funcionales**

Las pruebas no funcionales se realizarán en menor medida y solo las esenciales requeridas por el cliente por cuestiones de falta de tiempo y recursos. Las pruebas de carga y rendimiento se ejecutarán en las últimas semanas del proyecto.

### Registro de Resultados
Las pruebas y sus resultados serán registrados en una aplicación tercera. Las pruebas tendrán 4 estados distintos:
- Pendiente
- En proceso
- Completada
- Fallida


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

### Proceso de Manejo de Pruebas

### Criterios de aceptación de pruebas

##### - Pruebas Unitarias

##### - Pruebas de Integración

##### - Pruebas de aceptación de usuarios

### Entregables de Pruebas

---
