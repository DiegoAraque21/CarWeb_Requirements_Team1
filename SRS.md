# Requerimientos de Especificación de Software

## Tabla de Contenidos

Cambio

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
    1. [Modelo de Datos Lógicos](#modelo-de-datos-lógicos)
    2. [Diccionario de Datos](#diccionario-de-datos)
    3. [Reportes](#reportes)
    4. [Adquisición e Integridad de Datos](#adquisición-e-integridad-de-datos)
6. [Requerimientos Externos de la Interfaz](#requerimientos-externos-de-la-interfaz)
7. [Atributos de la Calidad](#atributos-de-la-calidad)
    1. [Usabilidad](#usabilidad)
    2. [Desempeño](#desempeño)
    3. [Seguridad y Privacidad](#seguridad-y-privacidad)
    4. [Otros Importantes](#otros-importantes)
8. [Internacionalización y Requerimientos de Locación](#internacionalización-y-requerimientos-de-locación)
9. [Otros Requerimientos](#otros-requerimientos)
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
  
Nuestra visión es desarrollar una plataforma digital en la que se puedan comprar autos nuevos sin la necesidad de acudir a una agencia. Planeamos implementar herramientas de AI (utilizando servicios de nube) a nuestra plataforma, para facilitar búsquedas, mejor atención al cliente y en general ofrecer la mejor experiencia posible. Nuestra misión es proporcionar un sistema fácil y eficiente para la compra de vehículos en toda la República Mexicana y poner al alcance de cualquier usuario pruebas de manejo a domicilio de los autos en los que esté interesado.


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
    
El producto se basa en una aplicación web que le permita a distintos grupos automotrices y sus agencias tener presencia en la web. Brindando mucha comodidad a los clientes finales, debido a que no se tienen que trasladar directamente a la agencia a comprar el coche. Lo podrán hacer todo desde la comodidad de sus casas incluyendo la solicitud de las pruebas de manejo (al ser solicitadas, la idea es que se envíe un coche listo para ser probado a la dirección del usuario que la solicitó). Hay productos que ofrecen cosas similares, como Kavak. Pero nos diferenciamos de ellos, debido a que solo las agencias serán capaces de vender sus vehículos, después de ser dados de alta por NDS. En otras palabras, yo como individuo no podré vender mi coche en la plataforma.

Como cliente seré capaz de comprar el coche que más se ajuste a mis necesidades, con la oportunidad de elegir el plan de financiamiento ofrecido por la agencia seleccionada. Este producto es completamente nuevo y busca crear una nueva forma de comprar vehículos en la República Mexicana.

### Clases de Usuario y Características
    
- Cliente:

Este usuario es el que navegará por la plataforma en busca de vehículos de su agrado. Con el fin de comprarlos de la manera que más le convenga, sin necesidad de ir presencialmente a una agencia. El cliente no necesita tener una cuenta para la navegación, pero sí será necesaria para tener acceso a la atención al cliente, solicitar pruebas de manejo y reservar algún vehículo.

Se busca incorporar una búsqueda, para que el usuario sea capaz de encontrar el coche que le guste de una manera fácil e intuitiva. Aunque de igual manera se le presentarán filtros, si esa es su preferencia de búsqueda. De esta manera tendremos una plataforma "user-friendly", en la cual el cliente no le costará trabajo entenderla. Como un extra se tratará de implementar búsqueda por lenguaje natural, esto se hará si el tiempo lo permite.

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
    
El software planteado correrá de distintas formas. El frontend estará hosteado en firebase, que es un servicio de google, que a través de muy pocos clics permite hostear la aplicación web fácilmente. Este correrá en la región us-central1 de google cloud. Todos los otros servicios que decidamos usar de la nube de google se encontrarán en esta región.

En la otra mano, el backend correrá en AWS. En la arquitectura planteada, nuestro backend será serverless. Todo estará en una VPC (Virtual Private Cloud), utilizaremos Máquinas Virtuales ofrecidas por el servicio EC2, para poder conectarnos a estos servicios. Estas máquinas virtuales estarían usando el sistema operativo Amazon Linux 2 kernel 5.10 (debido a que está en la free-tier de AWS). De igual manera el servicio RDS se utilizará para hostear la base de datos, API Gateway para crear los endpoints de nuestra API, AWS Lambda para crear las funciones que modifican y obtendrán datos de nuestra base de datos y por último S3 para guardar los archivos que suban los usuarios de la aplicación. Todos estos servicios y cualquier otro que se incluya en el futuro que pertenezca a AWS correrán en la región us-west-1.

Elegimos estas zonas debido a que se nos dijo que será utilizada en toda la región mexicana, y estos datacenters de cada nube, son los más cercanos a México.

Para los pagos es muy importante incorporar un third-party. Como en este caso lo sería Stripe, este permitirá añadir a un tercero muy usado en la industria que se encargue de este tema, sin tener que preocuparnos de temas de seguridad en el ámbito de pagos.

Por último se tiene que implementar un chatbot, por lo que decidimos usar dialogflow (un servicio de google cloud). Este servicio debe coexistir con la aplicación desarrollada, ya que le da mucho valor a la aplicación tener un servicio de atención al cliente que brinde atención personalizada a cada cliente.

Por último como tecnologías se utilizará React (versión 18.1), Nodejs (versión 18.15), python (versión 3.8), typescript (versión 4.9.5), tailwind css (versión 3.2) y PostgreSQL (versión 15.2).
    
### Restricciones de la implementación y el Diseño
    
- 10 semanas de desarrollo. Aunque es tiempo suficiente para abarcar gran cantidad del producto, no todas las áreas se podrán finalizar, por lo que se privilegiará lo que se ha definido como “Must”.
- 100 dólares por persona en AWS, que no se acumulan. El hecho de no poder juntar todos estos créditos, nos limita mucho el uso de la nube. Aunque sí se puede lograr, es necesario que ocupemos bien los créditos para evitar desastres. De igual manera por tener este límite, no podremos usar las mejores opciones de acuerdo a nuestro objetivo por motivos de precios.
- Debido a que todo el salón forma el equipo de desarrollo, tenemos que limitar los lenguajes, a los que ya hemos utilizado todos en semestres anteriores. En este caso estamos atados a utilizar React, nodejs y python.
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
    
   #### Prioridad alta
    
### Administración de Dueños   
Como super administrador, debo ser capaz de llevar una administración de dueño automotrizes, esto incluye:
- Consultar dueños registrados en el sistema.
- Eliminar dueño registrados sistema. 
- Dar de alta nuevos dueños.
- Consultar documentos subidos por un dueño de grupo automotriz a fin de aceptar una solicitud de unirse al sistema.
- Dar de alta a otros super administradores.
   
   #### Prioridad alta

    
 ### Autenticación
 Cualquier usuario del sistema podrá iniciar sesión, administrar datos de su cuenta, o eliminar su cuenta. Sin embargo, cada usuario tiene un flujo diferente de autenticación:
    
- Como cliente debo poderme registrar en la plataforma utilizando mi correo eléctronico, contraseña y datos personales.
- Como empleado, un gerente debera poder dar de alta mi cuenta. Se me proporcionará una contraseña temporal que podre actualizar al iniciar sesión con mi correo y contraseña.
- Como gerente, un dueño debera poder dar de alta mi cuenta. Se me proporcionará una contraseña temporal que podre actualizar al iniciar sesión con mi correo y contraseña.
- Como dueño, podre mandar una solicitud para unirme al sistema, para ello deberé poder subir los documentos necesarios. Cuando mi solicitud sea aprovada, podré acceder a mi cuenta utlizando mi correo y contraseña.
    
    
   #### Prioridad alta

    
 ### Reportes
 
 Cada usuario tendra accesso a diferentes tipos de reportes, dependiendo del tipo de cuenta del usuario (super admin, dueño, gerente).
    
- Como super administrador, debo ver reportes relacionados a las diferentes agencias registradas en el sistema, asi como reportes relacionados a las ganancias del sistema, dueños de grupos automotrizes, ventas, etc.
- Como dueño de grupo automotriz, debo ser capas de vizualisar reportes individuales de cada agencia que tengo registrada, esto incluye, ventas por vehiculo, por categoría, por empleado, ventas por mes. Ademas tambien podre consultar reportes relacionados a los empleados registrados en el sistema.
- Como gerente de agencia, puedo ver reportes relacionados a mis agencias, incluyendo ventas y rendimiento individual de cada empleado.
    
   #### Prioridad media

 ### Soporte
 
Como usuario debo poder obtener soporte por parte del sistema, dependiendo de la necesidad, podre hablar con un vendedor o gerente, o con un representante 
del sistema.
- En caso de encontrar un bug, podre reportarlo con un representante del sistema o pedir ayuda por medio de un chat dentro del sitio web.
- En caso de querer mas detalles sobre un vehículo, podré comunicarme con un vendedor o gerente por medio de un chat dentro del sitio web.
- En caso de tener problemas con una venta o prueba de manejo, debo poder comunicarme con un representante del sistema o gerente de agencia.

    #### Prioridad media

### Modelo de negocios 
Como dueño de sistema,se me cobrará una renta mensual por diferentes casos de uso.

- Se me cobrará un porcentaje por cada vehículo que se muestre en el sitio web 
- Se me cobrará una renta mensual por uso 
- Se me cobrará una renta mensual por emplado 
- Se me cobrara un porcentaje por cada venta realizada 
- Debo poder consultar mis pagos y cobros 
- Debo poder realizar pagos 

    #### Prioridad alta

---

## Requerimientos de Datos
    
Para este sistema se va a necesitar obtener, procesar y almacenar muchos datos tanto de las agencias como de los usuarios. En esta sección se describirán los distintos tipos de datos y sus agrupaciones.

Entradas de información del sistema:
1. Archivo CSV con el inventario de autos de una agencia. El archivo será leído y los datos se guardarán en la base de datos.
2. Formularios para crear cuentas de usuarios y clientes. Los datos capturados serán guardados en la base de datos.
3. Archivos de verificación de identidad de clientes y existencia de agencias y grupos. Estos archivos serán subidos y encriptados en un bucket de S3.

    
### Modelo de Datos Lógicos
    
Para comprender los datos y campos que serán usados a lo largo del proyecto, así como la relación entre ellos, se realizó un diagrama entidad-relación donde se representan las tablas esperadas para nuestra base de datos. Cada Tabla contiene campos con su tipo de dato. El diagrama se puede ver en la siguiente liga:
    
https://drive.google.com/file/d/171kF48YTRDYluUXe_cOdQKLoMWoi97nI/view?usp=sharing 

![Diagramas DB drawio](https://user-images.githubusercontent.com/90577455/223881345-36e173bb-405a-4b7e-80c0-293acfee8315.png)
    
### Diccionario de Datos

El siguiente diccionario de datos describe cada campo de nuestros modelos entidad-relación. Para una mejor visualización y manejo se realizó en google sheets. Se puede acceder a él por medio de la siguiente liga:
    
https://docs.google.com/spreadsheets/d/1dj_NSC68d_dddoCCb_ERvuY2XQfWQLtKqfIQMko_fYk/edit?usp=sharing 
    
    
### Reportes

Hay una gran cantidad de reportes que se pueden generar con los datos que se obtengan de la aplicación, pero los más esenciales son los reportes de ventas para las agencias y vendedores y los reportes de ingresos para los super administradores.
    
**Reportes de Ventas de Vendedores:**
El sistema puede analizar las ventas realizadas por cada vendedor en el tiempo, por lo tanto se pueden generar reportes sobre las ventas de un vendedor para que los gerentes de agencias puedan evaluar el desempeño del personal.

**Reporte de Ventas de Agencia:**
El sistema podrá generar reportes de ventas sobre el tiempo de una agencia en particular. Se podrá ver el crecimiento con respecto a los meses anteriores y total ingresado.

El siguiente es un ejemplo de reporte de ventas. El formato y diseño será diferente pero el contenido será similar:
    
<img width="479" alt="image" src="https://user-images.githubusercontent.com/90577455/223881597-b521767a-cf4f-4a5f-bb20-1b0bf12e6b47.png">

**Reportes de Ingresos de CarWeb:**
Los super administradores (personal de CarWeb) podrán ver reportes de ingresos de la plataforma. Estos reportes deberán desglosar la cantidad ingresada por el tipo de entrada. 
El siguiente es un ejemplo de reporte de ingresos. El formato y diseño será diferente pero el contenido será similar:

<img width="486" alt="image" src="https://user-images.githubusercontent.com/90577455/223881652-1a020b6d-b3ee-4977-80e1-ea90b72900f3.png">
    
    
### Adquisición e Integridad de Datos
    
Para este sistema se requiere mucho control y sensibilidad con los datos puesto que se estará subiendo y almacenando información delicada y privada tanto de usuarios, clientes y agencias.

**Encriptación de Documentos:**
El sistema requiere confirmar la identidad de clientes y agencias, por lo tanto se pedirá que ambos suban documentos con su información privada o personal como comprobantes de domicilio, INE, etc. Es crucial que estos documentos estén encriptados para asegurar la integridad y autenticidad de los datos e incluso si hay fugas de información sea seguro que nadie pueda leer los archivos.

**Autenticación de Usuarios y Clientes:**
Para asegurar una correcta autenticación de los usuarios y clientes usaremos los servicios de Firebase Auth los cuales nos proporcionarán tokens de autenticación, y con ellos podremos checar las sesiones tanto de los usuarios como clientes.

**VPC:**
Para tener completo control y seguridad de todos los servicios de la aplicación desplegamos todos los servicios en una VPC de AWS. Con esto conseguiremos que ningún agente externo pueda acceder a los servicios o modificar los permisos de los usuarios.
    
---

## Requerimientos Externos de la Interfaz

### Interfaces de Usuario.
**Pagina Principal (Cliente).** <br>
La interfaz de usuario comenzará con un feed en el que se mostrarán los autos que la aplicación elija bajo ciertos criterios (paid partnership, populares, etc.) a modo de tarjetas con las fotos de los automóviles y los títulos correspondientes. existirá una navbar a un costado de la página principal en donde el usuario podrá navegar a las distintas secciones de la página. En el top de esta página principal, el usuario encontrará una barra de búsqueda, en la cual podrá insertar las características del auto que busca en lenguaje natural.

Shortcuts. 
- Enter: Buscar un auto con lenguaje natural.

Gestos: 
- Scroll en Y: Mostrar más autos.

<br>**Iniciar sesión (Cliente).** <br>
El cliente podrá iniciar sesión en esta ventana que contará con dos inputs, uno para el e-mail y otro para la contraseña, contará con un botón de iniciar sesión y otro para crear cuenta, así mismo existirá un botón para hacer login con Google.

Botones.
- Iniciar sesión.
- Crear cuenta.

Alertas de error.
- Error al iniciar sesión.
- Error al crear cuenta.

<br>**Información de auto (Cliente).** <br>
Al dar click en una card del auto, se navegará hacia otra ventana la cual contendrá una navbar con un botón para regresar. En el top de esta se mostrarán imágenes del auto. Debajo se mostrará el título del carro con algunas de sus características, como el color, el modelo. Al hacer scroll podremos encontrar las versiones del mismo y características adicionales de este la cual serán especificados por la agencia. A un costado de la mencionada sección encontraremos una sección con los precios de contado y de financiamiento, debajo de este un botón para pagar.

Shortcuts.
- Delete: Volver a la página anterior.

Gestos:
- Scroll en Y: Mostrar más información.

Botones.
- Pagar.
- Regresar.

<br> **Realizar pago.** <br>
Al dar click para el botón de pagar, se mostrará un dialog con inputs de los datos de la tarjeta bancaria, utilizando la interfaz de Stripe. 

Shortcuts.
- Delete: Volver a la página anterior.

Gestos.
- Click fuera del modal: Volver a la página anterior.

<br> **Información de vendedores (Gerentes de agencia).** <br>
Los administradores de agencia tendrán un panel en el que podrán dar de alta vendedores, este contará de dos pestañas las cuales se cambiarán entre sí por medio de botones. En la pantalla registrar se pedirán datos de un nuevo vendedor y contará con un botón para registrar al empleado, este abrirá un modal en el que aparecerán los datos del vendedor registrado junto con una contraseña predefinida. En la pestaña administrar, el administrador podrá ver gráficas para cada uno de los vendedores y así mismo información relevante para cada uno de sus productos anunciados.

Shortcuts.
- Delete: Volver a la página anterior.

Botones.
- Botón pestaña registrar.
- Botón pestaña administrar.
- Botón registrar empleado.

<br> **Información de agencias (Marcas).** <br> 
Las marcas tendrán un panel en el que podrán dar de alta agencias, este contará de dos pestañas las cuales se cambiarán entre sí por medio de botones. En la pantalla registrar se pedirán datos de la nueva agencia y contará con un botón para registrar al gerente de la agencia, este abrirá un modal en el que aparecerán los datos de la agencia junto con una contraseña predefinida para el gerente. En la pestaña administrar, el administrador podrá ver gráficas para cada una de las agencias y gerentes.

Shortcuts.
- Delete: Volver a la página anterior.

Botones.
- Botón pestaña registrar.
- Botón pestaña administrar.
- Botón registrar agencia.

<br> **Aprobación (Marcas).** <br>
En esta ventana, las marcas serán capaces de subir los documentos solicitados para la aplicación, en esta se podrá visualizar tales archivos así como ver el estatus de la solicitud.

Botones.
- Subir archivos.

Alertas de error.
- Tipo de archivo no permitido.

<br> **Solicitud de nuevas marcas (Super administradores).** <br>
Los super administradores tendrán un panel en donde podrán ver las marcas que han mandado solicitudes para registrarse en la aplicación. En esta podrán encontrar los archivos correspondientes que cada marca ha subido y podrán visualizar dichos archivos, en la parte inferior se encontrará un botón para aceptar a la marca.  

Botones.
- Botón pestaña aceptar marca

<br> **Seguimiento de compra (Vendedores).** <br>
En esta ventana los vendedores podrán ver los status de sus diferentes clientes, podrán administrar las ventas, los pagos o las pruebas de manejo, en esta sección, también podrán revisar los documentos subidos por el cliente y autorizar pruebas de manejo. El vendedor tendrá múltiples pestañas para sus distintos clientes con información relevante sobre ellos en cada una.

Botones.
- Autorizar prueba de manejo.
- Autorizar compra.

<br> **Subir catálogo (Gerentes).** <br>
En esta ventana se le permitirá a los gerentes de agencia subir un archivo csv a manera de drag and drop, una vez subido, se mostrará una vista previa de todas las cards de los carros que se subieron, dando click en estas se llevara a la misma ventana de información del vehículo que la que el cliente posee y finalmente tendrá un botón para confirmar su catálogo.

Botones.
- Autorizar catalogo.

Alertas de error.
- Tipo de archivo no permitido.

### Interfaces de Software
<br> **Auth.** <br>
El cliente utilizara Firebase para registrar una nueva cuenta y para iniciar sesión, para ambos procesos el input será un e-mail y una contraseña, el sistema utilizará la librería firebase-auth para iniciar sesión o crear cuenta respectivamente con método de la librería, la cual le devolverá al sistema un objeto tipo JSON en el que encontraremos si la respuesta fue exitosa o no.
- Input: Correo electrónico y contraseña.
- Output: Login/creación de cuenta o mensaje de error.


<br> **Pagos:** < br>
El cliente pagará ingresando los datos en la aplicación, el sistema utilizará Stripe para realizar los pagos de automóviles, utiliza la interfaz de usuario proporcionada por la misma y así mismo su API para realizar el cobro, a esta se le enviaran los datos bancarios y regresará un objeto tipo JSON con la información del cobro.
- Input: Datos bancarios.
- Output: Pago exitoso o mensaje de error.

<br> **Servicios en la nube:** <br>
El sistema utilizará API gateway como servicio de AWS para la comunicación, entre el cliente y los servicios en la nube, enviando peticiones HTTP  (Get, Post, Put, Delete, etc.) hacia el servicio AWS lambda.
- Input: Peticion HTTP.
- Output: Response tipó JSON. 

<br> **Bases de datos.** <br>
Se utiliza PostgreSQL como servicio de AWS para la base de datos. Las funciones de AWS lambda, enviaran request a la base de datos y estas regresaran un response tipo JSON.
- Input: Acción para la base de datos.
- Output: Response tipó JSON. 

Se utilizará S3 bucket para almacenar archivos, igualmente como servicio en la nube, las mismas funciones lambda serán las encargadas de comunicarse con este servicio.
- Input: Acción para S3.
- Output: Response tipó JSON. 

<br> **Frontend.** <br>
Para la estilización del frontend utilizaremos el framework para css Tailwind, esto para tener mayor rapidez y código limpio al momento del desarrollo del frontend.

### Interfaces de Hardware
El sistema no contará con interfaces de hardware.
    
### Interfaces de Comunicación
**Navegador web:** <br>
- Soporte para navegación segura en línea.
- Compatibilidad con los protocolos web estándar, como HTTP y HTTPS.
- Admite la visualización de archivos pdf.
- Admite la descarga de archivos desde la web.

<br> **Protocolos de red:** <br>
- Admite la integración con tecnologías de red existentes, como Wi-Fi y 3G/4G/5G.

<br> **Formularios electrónicos:** <br>
- Admite la creación y el envío de formularios.
- Admite la validación de datos del formulario y la verificación de errores.
- Los campos están sanitizados para prevenir ataques de inyección.

<br> **Formatos de mensaje pertinentes:** <br>
- Los formatos de comunicación entre API’s serán tipo JSON.

<br> **Encriptación o seguridad de la comunicación:** <br>
- Se deberá proteger la información de los clientes asi como de los usuarios.
- Las contraseñas se guardan cifradas en la base de datos.
- Se podrán usar tecnologías de cifrado, como TLS, SSL y SSH, para proteger la comunicación.

---

## Atributos de la Calidad
    
### Usabilidad
    
Primero que todo, lo que más sobresale en la usabilidad es la habilidad que le daremos a los usuarios de buscar el vehículo que desee a través de lenguaje natural. Esto quiere decir que con un prompt y un click, el cliente recibirá una respuesta del sistema acorde con lo solicitado. Debido a que esto puede resultar ser muy complicado, añadiremos filtros convencionales.

Además, el cliente no necesitará tener una cuenta para navegar por la plataforma. Crear una cuenta será necesario solo para cuando se soliciten pruebas de manejo o reserva de vehículos.

Por parte de las agencias, tendrán la facilidad de subir su catálogo a través de un archivo csv. Esto hará que el proceso de dar de alta todos sus vehículos sea más rápido. 

El acceso a la atención del cliente será sumamente fácil. Ya que en cada interfaz de la plataforma, existirá un botón flotante, que indica claramente que activa un chat. De esta manera el usuario nunca pensará que está solo y siempre se le ofrecerá ayuda.

Al usuario se le permitirá comparar los vehículos de su elección y de igual manera los planes de financiamiento que ofrecen distintas agencias para el mismo vehículo. De esta manera el cliente tendrá la información necesaria, para tomar la decisión que se ajuste más a sus necesidades.
    
La plataforma será responsive, por lo que el usuario final podrá ver toda la información desde una computadora, tableta o teléfono celular.
    
Por último la plataforma debe de ser consistente. Todas las pantallas usarán la misma paleta de colores, font, etc.
    
### Desempeño
    
El desempeño de nuestra aplicación depende de muchos factores. Primero que todo, al ser serverless, escalará automáticamente y evitaremos muchos problemas de cuello de botella. De igual manera, debido a que no podremos maximizar los servicios debido a límite de créditos no buscamos lo más rápido si no algo que se encuentre en un rango que ofrezca buen desempeño. Por último si el usuario no tiene conexión a internet la plataforma no funcionará y si la conexión es muy mala el desempeño se verá afectado, debido a que se tardará más en conseguir los datos.

Una restricción muy importante de desempeño que tenemos es que ninguna función lambda tarde más de 15 minutos, debido a que es el máximo que puede tomar para ejecutarse según la documentación de AWS.

### Seguridad y Privacidad

El sistema guardará toda la información sensible del usuario: contraseñas, documentos, etc. cifradas en la base de datos.

Después de cierto tiempo de inactividad, la sesión del usuario será cerrada.

Toda la comunicación entre el frontend y el backend será hecha mediante HTTPS. Lo que significa que estará cifrada.
Los documentos guardados en S3 estarán cifrados.

En términos de pagos, se creará un webhook para stripe. Este solo se puede acceder cuando se ha hecho un pago a través del third-party. De esta manera solo se podrá acceder a esto si se hace el pago.

Toda la API, base de datos y el storage se encontrarán en una VPC. Esta VPC tendrá una regla de seguridad que solo le permitirá a los servicios que se encuentran dentro de ella conectarse. De esta manera el último punto de acceso será API Gateway y máquinas virtuales que creemos en la misma VPC.

Los roles seguirán la regla del mínimo privilegio. Esto quiere decir que no se les enseñara más de lo que tienen que ver. Los super-admins solo ven información sobre la app, pero nada específico de los grupos automotrices. Los grupos automotrices van a poder ver toda la información de sus agencias y empleados. Los dueños de las agencias solo tendrán acceso a toda la información de su agencia. Los gerentes tendrán permisos de editar, crear y visualizar el catálogo, además de visualizar el desempeño de sus empleados. Por último los vendedores solo podrán visualizar el catálogo y darle seguimiento a sus clientes asignados, además podrán aceptar pruebas de manejo y reservas de vehículos.
    
### Otros Importantes

En términos de disponibilidad, debido a que está enfocado a la república mexicana. Buscaremos bajar la carga de los servidores en horas de flujo bajo.

Algo que también es de suma importancia, es el hecho de que la plataforma funcionará perfectamente en google chrome, mozilla firefox, microsoft edge y safari.

El sistema será completamente escalable gracias a las tecnologías de la nube de AWS que escogimos en nuestra arquitectura. API Gateway y AWS Lambda.
       
---

## Internacionalización y Requerimientos de Locación
    
Actualmente nuestra plataforma será utilizada exclusivamente en la República Mexicana, por lo que no es necesario hacer cambios específicos para otros países o ubicaciones. En caso de que la plataforma crezca y se decida la expansión del negocio podemos hacer planes para dicho desarrollo.

---

## Otros Requerimientos
    
En nuestras pláticas con el socio formador se nos informó que NDS va a encargarse de forma integral del aspecto legal, regulatorio y financiero. Para observar o analizar los requerimientos principales puedes acceder a [esta sección del documento](#características-del-sistema) antes presentada.
    
---

