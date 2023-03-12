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
    1. [Descripción de pruebas](#descripción-de-pruebas)
    2. [Objetivos de pruebas](#objetivos-de-pruebas)
    3. [Suposiciones de las pruebas](#suposiciones-de-las-pruebas)
    4. [Objetos de pruebas](#objetos-de-prueba)
    5. [Alcance de las pruebas](#alcance-de-las-pruebas)
    6. [Niveles de pruebas](#niveles-de-pruebas)
    7. [Criterios de aceptación de pruebas](#criterios-de-aceptación-de-pruebas)
    8. [Entregables de pruebas](#entregables-de-pruebas)
    9. [Lista de hitos](#lista-de-hitos)
    10. [Estimación del esfuerzo de prueba](#estimación-del-esfuerzo-de-prueba)
    
    
---

## Objetivos: 
Las metas que se desean alcanzar en el desarrollo de las pruebas de software están relacionadas con cumplir todos los requerimientos funcionales que el socio formador nos proveyó y a grandes rasgos estas son nuestras metas:

* Autenticación funcional y segura
* Búsqueda de vehículos exacta y fidedigna
* Chat con servicio al cliente amigable 
* Visualización de vehículos flexible y accesible
* Performance confiable y preciso
* Pruebas de manejo rápidas y a domicilio
* Experiencia de compra de vehículos fiable, funcional, rápida y flexible

El objetivo principal de las pruebas es asegurar de que entreguemos un producto funcional, seguro, con capacidad escalable, adaptabilidad, económico y con una experiencia de usuario amigable, que pueda generar ingresos al socio formador y al mismo tiempo revolucione la compra de vehículos nuevos en toda la República Mexicana.


## Alcance:

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

## Requerimientos para pruebas: 
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

### Niveles de Pruebas



---
