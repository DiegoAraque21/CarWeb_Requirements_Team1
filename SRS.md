# Requerimientos de Especificación de Software

## Tabla de Contenidos

---

[Tabla de Contenidos](#tabla-de-contenidos)
1. [Introducción](#introducción)
    1. [Propósito](#propósito)
    2. [Convenciones del documento](#convenciones-del-documento)
    3. [Alcance del proyecto](#alcance-del-proyecto)
    4. [Referencias](#referencias)
2. [Descripción General](#descripción-general)
    1. [Perspectiva del Producto](#perspectiva-del-producto)
    2. [Clases de Usuario y Características](#clases-de-usuario-y-características)
    3. [Ambiente Operacional](#ambiente-operacional)
    4. [Restricciones de la implementación y el diseño](#restricciones-de-la-implementación-y-el-diseño)
    5. [Suposiciones y Dependencias](#suposiciones-y-dependencias)
3. [Características del Sistema](#características-del-sistema)
    1. [Venta de Vehículos](#venta-de-vehículos)
    2. [Pruebas de manejo](#pruebas-de-manejo)
    3. [Búsqueda de vehículos por lenguaje natural](#búsqueda-de-vehículos-por-lenguaje-natural)
    4. [Catálogo de vehículos](#catálogo-de-vehículos)
    5. [Administración de empleados](#administración-de-empleados)
    6. [Administración de dueños](#administración-de-dueños)
    7. [Autenticación](#autenticación)
    8. [Reportes](#reportes)
    9. [Soporte](#soporte)
    10. [Modelo de negocios](#modelo-de-negocios)
4. [Requerimientos de Datos](#requerimientos-de-datos)
5. [Requerimientos Externos de la Interfaz](#requerimientos-externos-de-la-interfaz)
6. [Atributos de la Calidad](#atributos-de-la-calidad)
7. [Internacionalización y Requerimientos de Locación](#internacionalización-y-requerimientos-de-locación)
8. [Otros Requerimientos](#otros-requerimientos)
9. [Modelos de Análisis](#modelos-de-análisis)

---

## Introducción

En este documento presentaremos la planeación de software de nuestra plataforma de compra de vehículos en línea, abordaremos temas relacionados con descripciones, requerimientos, pruebas, implementación y desarrollo de software. Estos temas estarán divididos en el índice en el que el usuario podrá seleccionar diferentes temas y acceder a ellos individualmente con un solo click. Para acceder a la tabla de contenidos [haz click aquí](#tabla-de-contenidos).

### Propósito

El propósito de este documento es presentar una descripción detallada de nuestro producto para que PMs, testers, analistas, product owners, desarrolladores y arquitectos de software y todo el equipo de NDS pueda analizar nuestra planeación del proyecto y encontrar áreas de oportunidad o mejora en el sistema antes de pasar a la etapa del desarrollo de la plataforma. De esta manera aclaramos nuestra visión y podemos alinearnos a los propósitos específicos de NDS.

### Convenciones del documento

Nuestro documento contiene las siguientes convenciones tipográficas:

- Acrónimos:

| Acrónimo | Significado                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| DB       | Base de datos (del inglés Data Base)                                                           |
| AI       | Inteligencia Artificial (del inglés Artificial Intelligence)                                   |
| PM       | Gerente del Proyecto (del inglés Project Manager)                                              |
| NDS      | Nearshore Delivery Systems, Socio Formador                                                     |
| AWS      | Amazon Web Services                                                                            |
| GCP      | Google Cloud Platform                                                                          |
| CSV      | Valores Separados por Comas (del inglés Comma Separated Values)                                |
| OS       | Sistema Operativo (del inglés Operation System)                                                |
| VPC      | Nube Privada Virtual (del inglés Virtual Private Cloud)                                        |
| EC2      | Elastic Compute Cloud                                                                          |
| API      | Interfaz de Programación de Aplicaciones (del inglés Application Programming Interface)        |
| JS       | Java Script                                                                                    |
| SRS      | Requerimientos de Especificación de Software (del inglés Software Requirements Specifications) |
| TS       | TypeScript                                                                                     |

- Convenciones de sintaxis:

| Convención         | Significado                      |
|--------------------|----------------------------------|
|*Itálicas*          | Texto sacado de fuentes externas |
|**Negritas**        | Títulos,  subtítulos             |
|<ins>Subrayado<ins/>| Roles, clasificaciones           |

  
### Alcance del proyecto
  
Nuestra visión es desarrollar una plataforma virtual en la que se puedan comprar autos nuevos sin la necesidad de acudir a una agencia. Planeamos implementar herramientas de inteligencia artificial (utilizando servicios de nube) a nuestra plataforma, para facilitar búsquedas, mejor atención al cliente y en general ofrecer la mejor experiencia posible. Nuestra misión es facilitar y agilizar el trámite de la compra de vehículos en toda la República Mexicana y poner al alcance de cualquier usuario pruebas de manejo a domicilio de los autos en los que esté interesado.


### Referencias
  
(2022). Consultado el 6 de marzo, 2023, NDS Cognitive Labs página web: https://ndscognitivelabs.com/ 

(1998) IEEE. Consultado el 6 de marzo, 2023, IEEE Std 830-1998 IEEE Recommended Practice for Software Requirements Specifications. IEEE Computer Society. 
https://www.cse.msu.edu/SRSExample-webapp

(2023) Documentación de AWS EC2, Consultado el 7 de marzo, 2023, Amazon.com página web: https://docs.aws.amazon.com/ec2/?icmpid=docs_homepage_compute 

(2023) Documentación de Google Cloud, Consultado el 7 de marzo, 2023, Google Cloud página web: https://cloud.google.com/docs?hl=es-419 

(2023) Documentación de Stripe, Consultado el 7 de marzo, 2023, Stripe.com página web: https://stripe.com/docs 

(2020) JavaScript With Syntax For Types.  Consultado el 7 de marzo, 2023, typescriptlang página web: https://www.typescriptlang.org/ 

(2021)  Consultado el 7 de marzo, 2023, Reactjs.org página web: https://reactjs.org/  

(2023) Amazon API Gateway | API Management | Amazon Web Services   Consultado el 7 de marzo, 2023, Amazon Web Services, Inc. página web: https://aws.amazon.com/es/api-gateway/ 

‌(2023) Welcome to Python.org.  Consultado el 7 de marzo, 2023, Python.org página web: https://www.python.org/ 

(2023) AWS | Lambda - Gestión de recursos informáticos.  Consultado el 7 de marzo, 2023, Amazon Web Services, Inc. página web: https://aws.amazon.com/es/lambda/ 

(2023) AWS | Red virtual privada en la nube (VPC).  Consultado el 7 de marzo, 2023, Amazon Web Services, Inc. página web: https://aws.amazon.com/es/vpc/

(2023) Group, D. PostgreSQL.  Consultado el 7 de marzo, 2023, PostgreSQL página web: https://www.postgresql.org/ 

(2023) AWS | Servicio de bases de datos relacionales (RDS).  Consultado el 7 de marzo, 2023, Amazon Web Services, Inc. página web: https://aws.amazon.com/es/rds/

(2023) AWS | Almacenamiento de datos seguro en la nube (S3).  Consultado el 7 de marzo, 2023, Amazon Web Services, Inc. página web: https://aws.amazon.com/es/s3/

(2022) Firebase.  Consultado el 7 de marzo, 2023, Firebase página web: https://firebase.google.com/?hl=es-419 

(2023) Documentación de Dialogflow ES.  Consultado el 7 de marzo, 2023, Google Cloud página web: https://cloud.google.com/dialogflow/es/docs?hl=es-419 

---

## Descripción General
    
### Perspectiva del Producto
    
El producto se basa en una aplicación que le permita a distintos grupos automotrices y sus agencias tener presencia en la web. Brindando mucha comodidad a los clientes finales, debido a que no se tienen que trasladar directamente a la agencia a comprar el coche. Lo podrán hacer todo desde la comodidad de sus casas incluyendo la solicitud de las pruebas de manejo (al ser solicitadas, la idea es que se envia un coche listo para ser probado a la dirección del usuario que la solícito). Hay productos que ofrecen cosas similares, como Kavak. Pero nos diferenciamos de ellos, debido a que solo las agencias serán capaces de vender sus vehículos, después de ser dados de alta por NDS. En otras palabras, yo como individuo no podre vender mi coche en la plataforma.

Como cliente seré capaz de comprar el coche que más se ajuste a mis necesidades, con la oportunidad de elegir el plan de financiamiento ofrecido por la agencia seleccionada. Este producto es completamente nuevo y busca crear una nueva forma de comprar vehículos en la República Mexicana.

    
### Clases de Usuario y Características
    
- Cliente:

Este usuario es el que navegará por la plataforma en busca de vehículos de su agrado. Con el fin de comprarlos de la manera que más le convenga, sin necesidad de ir presencialmente a una agencia. El cliente no necesita tener una cuenta para la navegación, pero sí será necesaria para tener acceso a la atención al cliente, solicitar pruebas de manejo y reservar algún vehículo.

Se busca incorporar una búsqueda de lenguaje natural, para que el usuario sea capaz de encontrar el coche que le guste de una manera fácil e intuitiva. Aunque de igual manera se le presentarán filtros, si esa es su preferencia de búsqueda. De esta manera tendremos una plataforma "user-friendly", en la cual el cliente no le costará trabajo entenderla.


- Vendedor:

El vendedor es el usuario que tendrá contacto directo con los clientes. Estará encargado de aceptar pruebas de manejo, darle seguimiento a los clientes que soliciten soporte y aprobar reservas. Como vendedor, podrás ver todos los coches del catálogo de mi agencia, pero no seré capaz de editar ninguna información.

- Gerente:

El gerente estará encargado de darle seguimiento a todos los vendedores de sus agencias y también en darlos de alta. Tendrán acceso a información de valor, que les permitirá acceder al desempeño de sus vendedores. De igual manera será el encargado de dar de alta el catálogo y darle seguimiento en el futuro (podre cambiar los vehículos del catálogo como gerente).

- Administrador de agencia:

El dueño de la agencia tendrá información sobre todos sus subordinados (gerentes, vendedores) y además sobre el desempeño de su agencia y catálogo. De igual manera, es el que da de alta a todos sus gerentes. El administrador de agencia también tiene la capacidad de modificar el catálogo y darle seguimiento. Y podrán desactivar las cuentas de todos sus subordinados (gerentes y vendedores).

- Administrador de grupo automotriz:

Un grupo automotriz puede tener muchas agencias bajo su control. Como administrador, seré capaz de dar de alta a todas las agencias y ver el desempeño de cada una en la plataforma. Tomando en cuenta que es el usuario con más privilegios podrá observar información d valor de todas las agencias que se encuentran bajo su mando.

- Super Administrador:

El superadministrador está encargado de dar de alta a todos los grupos automotrices. Revisaran la validez de los documentos enviados, y en caso de ser válidos los darán de alta. Los super-administradores serán empleados de NDS. Y de igual manera tendrán información sobre la aplicación, pero nada específico sobre los otros usuarios.
    
### Ambiente Operacional
    

![Arquitectura CarWeb drawio](https://user-images.githubusercontent.com/57450093/221737889-ba914df5-3208-4078-bdfb-a1a3ff140ef8.png)
Figura 1. Arquitectura Propuesta
    
El software planteado correrá de distintas formas. El frontend estará hosteado en firebase, que es un servicio de google que lo permite fácilmente. Este correrá en la región us-central1 de google cloud. Todos los otros servicios que decidamos usar de la nube de google se encontrarán en esta región.

En la otra mano, el backend correrá en AWS. En la arquitectura planteada, nuestro backend será serverless. Todo estará en una VPC (Virtual Private Cloud), utilizaremos Máquinas Virtuales ofrecidas por el servicio EC2, para poder conectarnos a estos servicios. Estas máquinas virtuales estarían usando el sistema operativo Amazon Linux 2 kernel 5.10 (since it 's included in the free tier). De igual manera el servicio RDS se utilizará para hostear la base de datos, API Gateway para crear los endpoints de nuestra API, AWS Lambda para crear las funciones que modifican y obtendrán datos de nuestra base de datos y por último S3 para guardar los archivos que suban los usuarios de la aplicación. Todos estos servicios y cualquier otro que se incluya en el futuro que pertenezca a AWS correrán en la región us-west-1.

Elegimos estas zonas debido a que se nos dijo que será utilizada en toda la región mexicana, y estos datacenters de cada nube, son los más cercanos a México.

Para los pagos es muy importante incorporar un third-party. Como en este caso lo sería Stripe, este permitirá añadir a un tercero muy usado en la industria que se encargue de este tema, sin tener que preocuparnos de temas de seguridad en el ámbito de pagos.

Por último se tiene que implementar un chatbot, por lo que decidimos usar dialogflow (un servicio de google cloud). Este servicio debe coexistir con la aplicación desarrollada, ya que le da mucho valor a la aplicación tener un servicio de atención al cliente que brinde atención personalizada a cada cliente.

Por último como tecnologías se utilizará React (versión 18.1), Nodejs (versión 18.15), python (versión 3.8), typescript (versión 4.9.5), tailwind css (versión 3.2) y PostgreSQL (versión 15.2).
    
### Restricciones de la implementación y el Diseño
    
- 10 semanas de desarrollo. Aunque es tiempo suficiente para abarcar gran cantidad del producto, no todas las áreas se podrán finalizar.
- 100 dólares por persona en AWS, que no se acumulan. El hecho de no poder juntar todos estos créditos, nos limita mucho el uso de la nube. Aunque sí se puede lograr, es necesario que ocupemos bien los créditos para evitar desastres. De igual manera por tener este límite, no podremos usar las mejores opciones de acuerdo a nuestro objetivo por motivos de precios.
- Debido a que todo el salón forma el equipo, tenemos que limitar los lenguajes, a los que ya hemos utilizado todos en semestres anteriores. En este caso estamos atados a utilizar React, nodejs y python.
- Todos somos estudiantes de ingeniería de software, por lo que nuestras habilidades de diseño no son las mejores. Se buscará generar las interfaces más intuitivas en base a nuestras habilidades.
- En términos de pruebas asumimos que solo se harán pruebas unitarias, tanto de caja negra como de caja blanca. Las no funcionales no serán realizadas por temas de tiempo y el hecho de requerir software externo.

    
### Suposiciones y Dependencias
    
- Se utilizará Stripe como third-party de pagos. Asumimos que servirá aun y cuando se incorporen los planes de financiamiento de cada agencia.
- Suponemos que el modelo de negocios será un pago mensual, dependiendo de la cantidad de agencias que tiene el grupo automotriz y de la cantidad de vehículos que incluye cada catálogo.
- Suponemos que será suficiente implementar nuestra solución en la nube con los 100 créditos ofrecidos por el tec.
- Al querer que las empresas suban su catálogo en un archivo CSV, esperamos que las agencias tengan imágenes de sus vehículos en alguna nube o en el internet.
- Suponemos que la nube de AWS, tiene algún servicio que permite cifrar todos los archivos que suben los clientes a la aplicación.
- Dependemos de reuniones semanales con el socio formador, para implementar de buena forma una metodología ágil. En la cual recibimos feedback de NDS y lo tomamos en cuenta para el desarrollo.


---

## Características del Sistema
    
### Venta de Vehículos

Como cliente, debo poder comprar un vehículo utilizando el sitio web, pare ello debo poder realizar lo siguiente:
    
- Seleccionar el vehículo que deseo adquirir 
- Introducir mis datos de pago. 
- Subir documentos requeridos para la compra del vehículo ( comporbante de domicilio, credito, etc. ).
- Consultar el estado de mi pedido. 

    #### Prioridad alta
### Pruebas de manejo
Como cliente, debo poder pedir pruebas de manejo, para lograrlo debo poder realizar las siguientes acciones:
- Seleccionar la agencia del vehiculo que quiero probar. 
- Seleccionar un vehiculo dentro de la agencia.
- Enviar una solicitud de prueba de manejo.
- Consultar mis solicitudes.
- Contactar a un empleado en caso de necesitar ayuda.

    #### Prioridad alta

 ### Búsqueda de vehículos por lenguaje natural 
    
Como usuario del sistema, debo poder buscar vehículos utilizando natural; por ejemplo, el usuario ingresa el siguiente texto: "Busco un coche familiar para utilizar los fines de semana". Acto siguiente, el sistema debe arrojar resultados de busqueda que tengan congruencia con lo solicitado.
     
   #### Prioridad alta

### Catálogo de vehículos 
Como dueño de grupo automotriz, o gerente de una agencia, debo poder dar de alta y administrar el catálogo de vehículos que se venderán a los clientes del sitio web. Esta administración incluye:

 - Dar de alta un vehículo, utilizando su nombre, modelo, año, imagen, motor, etc.
 - Editar vehículos existentes, ya sea cambiar su nombre, imagen, precio, etc.
 - Eliminar vehículos del cátalogo. 
 - Subir multiples vehiculos al catálogo por medio de un documento tipo excel. 
 - Consulta del catálogo de vehículos.
    
    #### Prioridad alta

 
### Administración de empleados 
Como dueño de grupo automotriz, o gerente de una agencia, debo poder administrar los usuarios de mi agencia o grupo automotriz, esto incluye:
 - Dar de alta un empleados, utilizando su nombre, rol, dirección, correo, etc.
 - Eliminar empleados del sistema. 
    
   #### prioridad alta
    
### Administración de Dueños   
Como super administrador, debo ser capaz de llevar una administración de dueño automotrizes, esto incluye:
- Conslultar dueños registrados en el sistema.
- Eliminar dueño registrados sistema. 
- Dar de alta nuevos dueños.
- Consultar documentos subidos por un dueño de grupo automotriz a fin de aceptar una solicitud de unirse al sistema.
- Dar de alta a otros super administradores.
   
   #### prioridad alta

    
 ### Autenticación
 Cualquier usuario del sistema podrá iniciar sesión, administrar datos de su cuenta, o eliminar su cuenta. Sin embargo, cada usuario tiene un flujo diferente de autenticación:
    
- Como cliente debo poderme registrar en la plataforma utilizando mi correo eléctronico, contraseña y datos personales.
- Como empleado, un gerente debera poder dar de alta mi cuenta. Se me proporcionará una contraseña temporal que podre actualizar al iniciar sesión con mi correo y contraseña.
- Como gerente, un dueño debera poder dar de alta mi cuenta. Se me proporcionará una contraseña temporal que podre actualizar al iniciar sesión con mi correo y contraseña.
- Como dueño, podre mandar una solicitud para unirme al sistema, para ello deberé poder subir los documentos necesarios. Cuando mi solicitud sea aprovada, podré acceder a mi cuenta utlizando mi correo y contraseña.
    
    
   #### prioridad alta

    
 ### Reportes
 
 Cada usuario tendra accesso a diferentes tipos de reportes, dependiendo del tipo de cuenta del usuario (super admin, dueño, gerente).
    
- Como super administrador, debo ver reportes relacionados a las diferentes agencias registradas en el sistema, asi como reportes relacionados a las ganancias del sistema, dueños de grupos automotrizes, ventas, etc.
- Como dueño de grupo automotriz, debo ser capas de vizualisar reportes individuales de cada agencia que tengo registrada, esto incluye, ventas por vehiculo, por categoría, por empleado, ventas por mes. Ademas tambien podre consultar reportes relacionados a los empleados registrados en el sistema.
- Como gerente de agencia, puedo ver reportes relacionados a mis agencias, incluyendo ventas y rendimiento individual de cada empleado.
    
   #### prioridad media

 ### Soporte
 
Como usuario debo poder obtener soporte por parte del sistema, dependiendo de la necesidad, podre hablar con un vendedor o gerente, o con un representante 
del sistema.
- En caso de encontrar un bug, podre reportarlo con un representante del sistema o pedir ayuda por medio de un chat dentro del sitio web.
- En caso de querer mas detalles sobre un vehículo, podré comunicarme con un vendedor o gerente por medio de un chat dentro del sitio web.
- En caso de tener problemas con una venta o prueba de manejo, debo poder comunicarme con un representante del sistema o gerente de agencia.
  #### prioridad media

### Modelo de negocios 
Como dueño de sistema,se me cobrará una renta mensual por diferentes casos de uso.

- Se me cobrará un porcentaje por cada vehículo que se muestre en el sitio web 
- Se me cobrará una renta mensual por uso 
- Se me cobrará una renta mensual por emplado 
- Se me cobrara un porcentaje por cada venta realizada 
- Debo poder consultar mis pagos y cobros 
- Debo poder realizar pagos 

 #### prioridad alta

---

## Requerimientos de Datos

---

## Requerimientos Externos de la Interfaz

---

## Atributos de la Calidad

---

## Internacionalización y Requerimientos de Locación
    
Actualmente nuestra plataforma será utilizada exclusivamente en la República Mexicana, por lo que no es necesario hacer cambios específicos para otros países o ubicaciones. En caso de que la plataforma crezca y se decida la expansión del negocio podemos hacer planes para dicho desarrollo.

---

## Otros Requerimientos
    
En nuestras pláticas con el socio formador se nos informó que NDS va a encargarse de forma integral del aspecto legal, regulatorio y financiero. Para observar o analizar los requerimientos principales puedes acceder a [esta sección del documento](#características-del-sistema) antes presentada.
    
---

## Modelos de Análisis

---

