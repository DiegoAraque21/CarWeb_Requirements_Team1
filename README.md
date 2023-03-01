# CarWeb Equipo1

---
##### Creadores: [@Diego Araque](https://github.com/DiegoAraque21), [@Salomon Dabbah](https://github.com/SalomonDabs), [@Marco Torres](https://github.com/marcotorresx), [@Fernando Valdeon](https://github.com/lfvm), [@Uriel Aguilar](https://github.com/u-urieldev)

## Índice

---

1. [Índice](#index)
2. [Historias de Usuario](#historias-de-usuario)
3. [WBS](#wbs)
4. [Requerimientos](#requerimientos)
5. [Backlog](#backlog)
6. [Estimación de costos y esfuerzo](#esfuerzo-costos)
7. [Diagrama de Gantt](#diagrama-de-gantt)
8. [Arquitectura](#arquitectura)
9. [Techstack](#techstack)
10. [Pruebas de software](#software-tests)

---

## Historias de Usuario

| id | Historia de usuario                                                                                                                                                                                                                                                                        | Criterio de aceptación                                                                                                                                                                                                                                                                                                                        | clasificación |
|---:|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
|  1 | Como cliente debo poder crear mi cuenta. Para poder hacer pagos y comunicarme con las agencias.                                                                                                                                                                                            | Pantalla de crear cuenta que permite: <br /> - Ingresar email <br /> - Ingresar contraseña <br /> - Ingresar datos personales (dirección, codigo postal, etc)                                                                                                                                                                                                        | M-Must Have   |
|  2 | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder cerrar sesión. Para que nadie pueda usar mi usuario en caso de perder mi dispositivo.                                                                                                           | Boton en el navigation bar, al cual al darle click elimine toda la información de usuario guardada como estado en la aplicacón web.                                                                                                                                                                                                            | M-Must Have   |
|  3 | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder iniciar sesión. Para poder hacer pagos, comunicarme con agencias o simplemente para acceder a funcionalidades especificas. Este ultimo apartado solo aplico para usuarios que no sean clientes. | Pantalla que contiene: <br /> - Input de email <br /> - Input de Contraseña <br /> - Boton que al ser presionadote dara acceso al sistema pero estaras autenticado y tendras acceso a otras funciones.                                                                                                                                                                           | M-Must Have   |
|  4 | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder actualizar datos de mi cuenta como nombre, ubicación, etc. Para que en caso de que cambio de residencia, nombre, etc., no sea necesario crear una nueva cuenta.                                 | Pantalla para poder editar mis datos de usuario, que contiene:  <br /> - Input de nombre <br /> - Input de informacion personal <br /> - Input de cambiar contraseña <br /> - Botón que cambia los datos guardados en la abse de datos y se ve reflejado el cambio automaticamente en la interfaz.                                                                                                                                                                               | S-Should Have |
|  5 | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder restablecer mi contraseña. Para poder tener mejor control sobre la seguridad de mi cuenta.                                                                                                      | Boton que permite restablcer contraseña en caso de que se me haya olvidado: <br/> - Al presionarlo el usuario recibira un mail en el cual recibira instrucciones para restablecer la contraseña.                                                                                                                             | M-Must Have   |
|  6 | Como cliente podré iniciar sesión directamente con google. Para poder hacerlo de manera mucho mas fácil, sin necesidad de llenar toda una forma.                                                                                                                                           | Boton que se conecte con firebase auth y permite hacer el login directamente con google: <br /> - Aparecerá un pop-up de google que permitira iniciar sesion facilmente.                                                                                                                                                                                                                                                      | C-Could Have  |
|  7 | Como gerente debo poder crear cuentas de mis vendedores. Para poder dar de alta a todo mi equipo y funcionar en la plataforma de una manera muy similar a la que tendríamos en la agencia.                                                                                                 | Pantalla que cree usuarios con contraseñas random para nuevos vendedores, esta contendra: <br /> - Input de email del vendedor <br /> - Input de nombre completo del vendedor <br /> Botón que cree la cuenta con la contraseña random, y que se envia un correo al vendedor con su contraseña.                                                                                                                                   | M-Must Have   |
|  8 | Como cliente debo poder registrar un método de pago. Para poder hacer transacciones en la aplicación y comprar los vehículos.                                                                                                                                                              | Al seleccionar pagar en un coche, tendre la opción de elegir entre multiples modalidades de pago a traves de un simple click. Esto junto a stripe permitira a los usuarios seleccionar sus metodos de pagos y hacerlo todo dentro de la plataforma. <br /> - Al seleccionar metodo de pago sera capaz de ingresar mis datos personales.                                                                                          | M-Must Have   |
|  9 | Como cliente debo poder ver la cuenta bancaria de la agencia para hacer transferencias. Para que en el caso de decidir este metodo de pago, tenga acceso rápido a la cuenta de la agencia para hacer el pago lo antes posible.                                                             | En caso de elegir transferencia como metodo de pago, como cliente sere capaz de ver la cuenta de la agencia y hacer el movimientos de esta manera. <br /> - Se ve la información de la cuenta bancaria de manera intuitiva.                                                                                                                                                                                            | M-Must Have   |
| 10 | Como cliente debo poder ver su estado de cuenta. Para poder ver a detalle mis transacciones en la aplicación y dar seguimiento.                                                                                                                                                            | Pantalla que contiene datos sobre transacciones hechas en el pasado por ese usuario en la aplicación. Aparecerán tarjetas con información referente a cargos y vehiculos ordenados.                                                                                                                                                           | C-Could Have  |
| 11 | Como cliente debo poder buscar con lenguaje natural el vehículo que quiero. Para filtrar entre todos los coches disponibles en las agencias                                                                                                                                                | Debo de poder buscar un vehiculo con lenguaje común que usaria con amigos u otros ambientes reales.<br /> - API de reconocimiento de lenguaje natural                                                                                                                                                                                               | S-Should Have |
| 12 | Como cliente también quiero poder usar filtros convencionales. Para encontrar el vehículo que quiero.                                                                                                                                                                                      | Debo de tener la opción de usar botones que filtren el coche que yo quiera (#puertas, color, capacidad, etc).<br /> - Base de datos de los vehículos                                                                                                                                                                                                | M-Must Have   |
| 13 | Como cliente debo poder buscar el coche que quiero sin necesidad de registrarse en la plataforma. Para facilitar el trámite y que la búsqueda sea veloz.                                                                                                                                   | Iniciar sesión o crear una cuenta no es necesario para navegar en el sistema en caso de ser cliente.<br />  - La página de registro tiene que estar después de que seleccione la prueba de manejo                                                                                                                                                   | M-Must Have   |
| 14 | Como cliente quiero poder comparar los distintos precios y ofertas del mismo coche de diferentes agencias. Para encontrar el mejor precio a mi conveniencia.                                                                                                                               | Pantalla de comparación de precios y planes de financiamiento del mismo modelo de coche en diferentes agencias.<br /> - Bases de datos de los diferentes coches <br /> - Ofertas de las agencias <br /> - Diferenciadores                                                                                                                                       | C-Could Have  |
| 15 | Como cliente quiero poder comparar las características de los coches en los que esté interesado. Para comprar el coche que más se adapte a mis necesidades.                                                                                                                                | Pantalla de comparación estilo la de apple para comparar celulares, pero de coches y sus caracteristicas mas relevantes.<br /> - Bases de datos de los vehículos <br /> - Comparación de características claves                                                                                                                                           | S-Should Have |
| 16 | Como cliente debo poder contactar a alguien de servicio al cliente. Para consultar dudas y/o hacer comentarios.                                                                                                                                                                            | Boton flotante en cada pantalla del sistema para que el cliente pueda recibir ayuda personalizada.<br /> - API de Chatbot para enlazar al cliente con un asesor <br /> - API Chat                                                                                                                                                                         | M-Must Have   |
| 17 | Como vendedor debo poder asesorar a los clientes que tengan dudas. Para dar un buen servicio y tener más ventas de autos.                                                                                                                                                                  | Como vendedor una de mis obligaciones será atender a clientes con dudas sobre algún coche o en especifico de la agencia a la que pertenezco.<br /> - API Chatbot <br /> - API Chat                                                                                                                                                                        | M-Must Have   |
| 18 | Como vendedor debo tener acceso a dudas de clientes en el chat general y tener la oportunidad de asesorar a cualquiera. Para asegurarse de que todas las preguntas tengan respuestas.                                                                                                      | Cada vendedor tiene acceso a todos los chats que siguen en espera y tendre la oprtunidad de elegir cualquiera y empezar a darle seguimiento.<br /> - Foro de preguntas y respuestas                                                                                                                                                                 | C-Could Have  |
| 19 | Como administrador de agencia debo dar de alta los vehículos de la agencia. Para que mis clientes puedan ver los autos disponibles y comprarlos cuando deseen.                                                                                                                             | A traves de un archivo csv, la agencia sera capaz de subir su catalogo con un solo click.<br /> - Input tipo archivo                                                                                                                                                                                                                                | M-Must Have   |
| 20 | Como cliente quiero poder visualizar con detalle los vehículos disponibles. Para conocer todos los aspectos de los vehículos que me interesan.                                                                                                                                             | Cada vehiculo se verá en tarjetas generales, al presionarlas nos llevará a una pantalla individual del vehículo donde se observarán todos los datos y peculiaridades. Ademas de botones para comprar el coche y solicitar una prueba de manejo.<br /> - Bases de datos de los vehículos <br /> - Landing Page <br /> - Características principales de los autos | M-Must Have   |
| 21 | Como cliente quiero poder comparar las diferentes ofertas y precios de las agencias. Para saber que opción de compra me conviene mas.                                                                                                                                                      | Comparar caracteristicas del mismo modelo de diferentes agencias, especificamente costos y planes de financiamiento. <br /> - Bases de datos de vehiculos <br /> - Comparación de caracteristicas                                                                                                                                                                                                                          | C-Could Have  |
| 22 | Como gerente quiero poder ver estadísticas de los modelos o ventas de mi agencia. Para obtener datos sobre que y en donde vendo mas.                                                                                                                                                       | Pantalla para que la agencia tenga seguimiento sobre su catálogo con información de gran relevancia. Como coches mas vendidos, cantidad de dinero ingresada, etc. <br /> - Comparación de caracteristicas <br /> - Graficas                                                                                                                                                                             | S-Should Have |
| 23 | Como cliente debo tener diferentes métodos de pago (arrendamiento, mensualidades, de contado). Para poder escoger cual me conviene mas al momento de comprar.                                                                                                                              | Al seleccionar pagar en un coche, tendré la opción de elegir entre multiples modalidades de pago a traves de un simple click                                                                                                                                                                                                | S-Should Have |
| 24 | Como agencia debo ingresar datos a los cuales me van a llegar los fondos de cualquier compra. Para que los fondos lleguen a la cuenta deseada.                                                                                                                                             | Cuando la agencia es aceptada por el super-admin, será obligada a añadir información de su cuenta bancaria. Para que los pagos sean de cliente a agencia, con unico intermediario la API que usemos (ejemplo: Stripe)   <br /> - Encriptación                                                                                                                      | M-Must Have   |
| 25 | Como vendedor quiero saber cuantas ventas he realizado y el estado de cada una (cantidad pagada). Para saber el status de mis clientes.                                                                                                                                                    | Los vendedores serán capaces de ver todas sus ventas en una pantalla especilidad y el estado de dichas ventas. <br /> - Estados de cuenta                                                                                                                                                                                                                           | C-Could Have  |
| 26 | Como gerente quiero tener acceso a todos los procesos de ventas de mi agencia, y en qué estado se encuentran (culminado, en proceso, empezado, etc). Para tener un seguimiento y control de mis vendedores.                                                                                | Los gerentes tendrán acceso a todos los movimientos de su agencia y de sus vendedores. Con esta información detallada podran realizar sus conclusiones.     <br /> - Base de datos de vendedores                                                                                                                                                                                  | S-Should Have |
| 27 | Como cliente quiero poder saber el estado de mi pedido, si el auto está en preparación, en camino, etc. Para tener un seguimiento de mi compra y seguridad.                                                                                                                                | Despues de pagar el coches, como cliente podre ver en una pantalla el estado de mi pedido. Se dará un aproximado de cuando llegara a su casa. <br /> - Seguimiento de los coches                                                                                                                                                                                                | M-Must Have   |
| 28 | Como administrador de agencia puedo escoger qué documentos necesita el cliente para realizar la prueba de manejo. Para que se entren los documentos necesarios.                                                                                                                            | Los administradores de las agencias estan encargados de decir que tipos de documentos son obligatorios para poder solicitar una prueba de manejo. <br /> - Encriptacion         <br /> - Input tipo archivo                                                                                                                                                                                     | M-Must Have   |
| 29 | Como cliente debe de poder subir mis documentos para realizar la prueba de manejo (INE, licencia de conducir, etc). Para que se pueda acreditar mi identidad.                                                                                                                              | Al solicitar la prueba de manejo de un vehículo, tendré que ingresar datos requeridos por la agencia para lograr el registro                                                                                                                                                                                                                  | M-Must Have   |
| 30 | Como cliente puedo decidir no hacer una prueba de manejo. Para saltar directamente a la compra y agilizar el proceso.                                                                                                                                                                      | No es obligatorio hacer una prueba de manejo para comprar el vehículo.                                                                                                                                                                                                                                                                        | M-Must Have   |
| 31 | Como cliente quiero poder saber el estado de mi prueba de auto para conocer si el auto está en procesamiento o en camino                                                                                                                                                                   | - Al solicitar la prueba de manejo, como cliente debo tener acceso a información relevante para dar seguimiento. <br />- El cliente debe poder ver el estado actual y los estados pasados. <br /> - El cliente debe poder ver las fechas importantes para saber cuando el vehículo.                                                                           | S-Should Have |
| 32 | Como administrador de grupo automotriz quiero dar de alta nuevas agencias para poder incrementar mis operaciones.                                                                                                                                                                          | - Los administradores de ga tendran una pantalla para dar de alta a sus agencias. <br /> - Estas cuentas seran creadas con contraseñas aleatorias.                                                                                                                                                                                                       | M-Must Have   |
| 33 | Como administrador de grupo automotriz de agencia quiero dar de alta nuevos gerentes para que ellos puedan controlar las agencias.                                                                                                                                                         | - Los admins de grupos deberán tener un formulario donde puedan dar de alta nuevos gerentes seleccionando la agencia. <br /> - El nuevo gerente deberá ser creado por el adimin                                                                                                                                                                      | M-Must Have   |
| 34 | Como gerente quiero poder dar de alta a los vendedores para que puedan realizar las ventas y contactar clientes dentro de la aplicación.                                                                                                                                                   | - Los gerentes deberán tener un formulario donde puedan dar de alta vendedores de su agencia. <br /> - El nuevo vendedor deberá ser creado por el gerente                                                                                                                                                                                            | M-Must Have   |
| 35 | Como gerente de agencia y administrador de grupo automotriz quiero configurar mis planes de financiamiento para ofrecer mejores ofertas a los clientes.                                                                                                                                    | - Deberá existir una seccion o formulario donde los administradores o gerentes puedan crear nuevos planes de finianciamiento. <br /> - Los usuarios deberán poder seleccionar esos planes a la hora de comprar un auto.                                                                                                                               | S-Should Have |
| 36 | Como gerente de la agencia quiero dar de alta el catálogo de autos de mi agencia para que los clientes puedan verlos.                                                                                                                                                                      | - El catálogo debe poder subirse desde un excel. <br /> - El sistema debe permitir subir el archivo y procesar y guardar los datos.                                                                                                                                                                                                                  | M-Must Have   |
| 37 | Como Super Admin debo poder dar de alta los grupos automotrices para que comiencen operaciones dentro de la aplicación                                                                                                                                                                     | - Se deben verificar los documentos de un grupo automotriz. <br /> - Se creara su cuenta en el sistema con una contraseña aleatoria.                                                                                                                                                                                                                 | M-Must Have   |
| 38 | Como Super-Admin debo poder dar de alta otros super usuarios para que varias personas sean las que controlen la plataforma y den de alta grupos.                                                                                                                                           | - Los super admin deberán tener una seccion o formulario donde puedan crear nuevos super admins.                                                                                                                                                                                                                                               | M-Must Have   |
| 39 | Como Super Admin debo poder visualizar documentos que los grupos automotrices suban para poder verificar que las agencias son reales.                                                                                                                                                      | - Los super-admins veran las solicitudes de los grupos automotrices y de esta manera verificar si son reales o no. <br /> - Despúes de verificar los datos deberá poder validar o rechazar.                                                                                                                                                          | M-Must Have   |
| 40 | Como super administrador quiero poder ver gráficos y estadísticas para conocer el estado de las operaciones.                                                                                                                                                                               | - Deberá de haber una seccion de gráficos y reportes. <br /> - Deberán haber gráficos o reportes con la información más relevante.                                                                                                                                                                                                                   | S-Should Have |
| 41 | Como administrador de grupo automotriz debo de poder ver gráficas y estadísticas sobre mi grupo (ventas, performance, etc.). Para concer las operaciones de mi grupo  y tomar desiciones.                                                                                                  | Los administradores de grupos automotrices tendran acceso a información de todas sus agencias, para verificar que tan cotizadas son y en base a eso tomar deciciones. Lo veran todo a traves de un dashboard, que tendrá varias graficas que muestren información representativa.                                                             | S-Should Have |
| 42 | Como vendedor, gerente, super-admin, administrador de grupo automotriz debo de cambiar mi contraseña al iniciar sesión por primera vez. Para asegurar que solo yo sepa mi contraseña.                                                                                                      | Cambiar la contraseñas despues de hacer el primer login es obligatorio por temas de seguridad. <br /> - Al hacer el primer inicio de sesión, aparecera un pop-up que obligue al usuario a cambiar su contraseña. <br /> - Despues de cambiar la contraseña, sera redirigido a editar datos por si acaso quiere añadir dirección, codigo postal, etc.                                                                                                                                       | M-Must Have   |
| 43 | Como cliente debo poder ver información general sobre el vehículo a través de tarjetas. Para poder informarme sin necesidad de ver a detalle cada vehículo                                                                                                                                 | Tarjetas individuales para cada vehículo, para que el cliente vea información relevante pero no abrumadora. Se veran: <br /> - Imagenes <br /> - Precio inicial <br /> - Caracteristicas basicas (puertas, capacidad, color, etc).                                                                                                                                      | M-Must Have   |

---

## WBS
![WBS Car Web diagram](https://user-images.githubusercontent.com/84464594/221742836-b0d2ab46-0f25-4b00-a39f-7b51d3967f17.png)

---

## Requerimientos
**Autenticación**
- Creación de usuario con correo y contraseña.
- Cerrar mi sesión debe ser posible para cualquier usuario del sistema.
- Iniciar sesión con correo y contraseña para cualquier usuario.
- Cualquier usuario debe poder cambiar su informacion. (nombre, ubicación, etc)
- Restablecer contraseña a través de un formato específico, debe ser posible para cualquier usuario de la aplicación.
- Cambiar contraseña para los vendedores, gerentes, super-admins y administradores de grupos automotrices es completamente necesarios (debido a que al principio se generan las cuentas con contraseñas random).
- Iniciar sesión con un pop de google (Firebase auth).

**Administración de empleados**
- Ingresar email y nombre del vendedor para crear su cuenta.
- Se generará una contraseña automática, la cual se le enviará al empleado.

**Métodos de pago Cliente**
- Elegir método de pago, al reservar un coche.
- Ingresar los datos de mi método de pago.
- En caso de elegir una transferencia, la información de la cuenta bancaria de la agencia debe estar disponible.
- Observar compras hechas en la aplicación.

**Búsqueda (Lenguaje natural y filtros)**
- Buscar vehículos con lenguaje natural.
- Barra de búsqueda intuitiva y fácil de acceder.
- Filtrar de manera manual para encontrar coches de tu agrado.
- Filtros accesibles y entendibles.
- Iniciar sesión no es obligatorio para navegar en el sistema.
- Mostrar un feed inicial para usuario que no tiene cuenta.
- Comparar los mismos modelos de coches de diferentes agencias.
- Comparar coches totalmente diferentes.

**Servicio al Cliente**
- Tener un chat para la atención de cada cliente.
- Botón flotante en cada pantalla.
- Comunicación con los clientes por parte de los vendedores de la respectiva agencia a la cual se le están solicitando preguntas.
- Mensajes sin respuesta disponibles para todos los vendedores para que se les pueda dar seguimiento.
- Si después de cierto tiempo no son seleccionadas por un vendedor, serán asignadas automáticamente de manera random.

**Catálogo de Vehículos**
- Se deben dar de alta el catálogo de las agencia a través de un archivo csv.
- Definir muy bien qué campos debe tener el archivo csv.
- Demo de archivo csv para que las agencias sepan cómo tiene que estar formateado su archivo.
- Tarjeta del vehículo con imagen principal e información importante.
- Todas las tarjetas contienen la misma información.
- Los vehículos disponibles tienen que aparecer con detalles en la plataforma.
- Botón para solicitar pruebas de manejo.
- Botón para pagar el vehículo.
- La plataforma tiene que tener un sistema de comparación de precios entre agencias.
- Debido a que el coche es igual, lo que se verá en estas comparaciones son diferencias de precios y planes de financiamiento.
- Generar gráficas para analizar las ventas de cada agencia 

**Venta de Vehículos**
- Pagar los vehículos con diferentes planes de compra.
- Decidir con botones intuitivos que metodo quiero utilizar.
- Requerir datos bancarios a las agencias para transferir fondos de vehículos.
- Estados de cuenta de clientes y etapa de pago en la que se encuentra. (Respectivo vendedor tendrá acceso)
- Visualización de procesos de venta por agencia, así como su estado actual.
- Proyección del estado del pedido para los clientes.

**Pruebas de Manejo**
- Capacidad de seleccionar los documentos necesarios para la prueba de manejo, para cada agencia.
- Capacidad para cargar documentos de los clientes a la plataforma.
- Capacidad de los clientes para rechazar la prueba de manejo
- Proyección del estado de la prueba de manejo

**Administración de Agencias**
- Dar de alta nuevas agencias en la plataforma con contraseñas random.
- Dar de alta gerentes con contraseñas random.
- Dar de alta a los vendedores con contraseñas random.
- Configuración de planes de financiamiento por parte del gerente de agencia
- Dar de alta catálogos de autos de las agencias mediante un archivo csv.

**Administración Super Admin**
- Dar de alta grupos automotrices con contraseñas random.
- Dar de alta a otros super usuarios con contraseñas random.
- Verificación de documentos de grupos automotrices.

**Reportes**
- Análisis de gráficos y estadísticas para el super-admin, para ver información básica de cada agencia.
- Análisis de gráficas y estadísticas por parte del administrador del grupo automotriz, sobre todas sus agencias.

---

## Diagrama de Gantt
|                  Task Name                  | Start  (Date) | End  (Date) | Duration (Days) |
|:-------------------------------------------:|:-------------:|:-----------:|:---------------:|
| Requerimientos                              |   2/13/2023   |   3/6/2023  |        21       |
| Historias de Usuario                        |   2/20/2023   |   3/6/2023  |        14       |
| Arquitectura                                |   2/27/2023   |   3/6/2023  |        7        |
| Diagramas UML                               |   2/27/2023   |  3/13/2023  |        14       |
| Diseño de UI/UX                             |    3/6/2023   |  3/27/2023  |        21       |
| Selección de servicios y nubes              |    3/6/2023   |  3/20/2023  |        14       |
| Configuración de la DB                      |    4/3/2023   |  4/10/2023  |        7        |
| Setup de backend en AWS                     |    4/3/2023   |  4/10/2023  |        7        |
| Setup del Frontend                          |    4/3/2023   |  4/10/2023  |        7        |
| Diseño API Gateway y AWS Lambda             |    4/3/2023   |  4/17/2023  |        14       |
| Diseño de endpoints                         |    4/6/2023   |  4/13/2023  |        7        |
| Desarrollo de endpoints                     |   4/10/2023   |  5/22/2023  |        42       |
| Conexión con el backend                     |   4/10/2023   |  4/17/2023  |        7        |
| Desarrollo del Frontend                     |   4/10/2023   |  5/22/2023  |        42       |
| Autenticación y autorización                |   4/10/2023   |  4/24/2023  |        14       |
| Roles en la nube                            |   4/10/2023   |  4/17/2023  |        7        |
| Creación de usuarios y roles                |   4/24/2023   |   5/8/2023  |        14       |
| Encriptar documentos                        |    5/1/2023   |  5/15/2023  |        14       |
| Pruebas de Backend                          |   5/22/2023   |   6/5/2023  |        14       |
| Pruebas de Frontend                         |   5/22/2023   |   6/5/2023  |        14       |
| Plan de lanzamiento                         |   5/22/2023   |  5/29/2023  |        7        |
| Pruebas Unitarias                           |   5/29/2023   |   6/9/2023  |        11       |
| Pruebas de Aceptación de Usuario            |   5/29/2023   |   6/5/2023  |        7        |
| Pruebas Integrales                          |    6/5/2023   |  6/15/2023  |        10       |
| Coordinar fecha de lanzamiento              |    6/5/2023   |  6/12/2023  |        7        |
| Pruebas No Funcionales (Rendimiento, Carga) |    6/5/2023   |  6/19/2023  |        14       |
| Lanzamiento                                 |   6/12/2023   |  6/19/2023  |        7        |

![Screenshot 2023-02-28 at 17 49 31](https://user-images.githubusercontent.com/70352787/222009582-73430987-8160-4ce9-9e00-b8cff78416be.jpg)

---

## Estimación de costos y esfuerzo
##### Costos
|                            |     |            |
|----------------------------|-----|------------|
| Esfuerzo total en MD       |     | 185        |
| Esfuerzo total en MD       |     | 185        |
| Salomon                    | 23% | 43         |
| Fernado                    | 17% | 31         |
| Diego                      | 22% | 40         |
| Uriel                      | 21% | 39         |
| Marco                      | 17% | 32         |
|                            |     |            |
| Costo Operacional Salomon  |     | ($2,000)   |
| Costo Operacional Fernando |     | ($2,100)   |
| Costo Operacional Diego    |     | ($1,510)   |
| Costo Operacional Uriel    |     | ($2,100)   |
| Costo Operacional Marco    |     | ($1,800)   |
|                            |     |            |
| Revenue ($)                |     | $750,000   |
|                            |     |            |
|                            |     |            |
| Total internal cost ($)    |     | ($351,000) |
|                            |     | $399,000   |
| Margin (%)                 |     | 53%        |

##### Esfuerzo

|                      | Topic                 | Nosotros | Cliente | Salomon | Fernando | Diego | Uriel | Marco |  Total |
|----------------------|-----------------------|:--------:|:-------:|:-------:|:--------:|:-----:|:-----:|:-----:|:------:|
| Project management   | Project Management    |     C    |    O    |  18 MD  |   5 MD   |  5 MD |  4 MD |  5 MD |  37 MD |
| Project Definition   | Scoping               |     O    |    S    |   2 MD  |   2 MD   |  2 MD |  2 MD |  3 MD |  11 MD |
|                      | Design                |     O    |    C    |  10 MD  |   5 MD   |  5 MD |  6 MD |  5 MD |  31 MD |
| Development          | DataBase              |     O    |    S    |   2 MD  |   10 MD  |  6 MD |  2 MD |  2 MD |  22 MD |
|                      | Backend               |     O    |    S    |   4 MD  |   10 MD  |  6 MD |  5 MD |  8 MD |  23 MD |
|                      | FrontEnd              |     O    |    S    |   2 MD  |   5 MD   |  6 MD |  8 MD |  4 MD |  20 MD |
|                      | Security              |     O    |    S    |   1 MD  |   1 MD   |  3 MD |  3 MD |  1 MD |  9 MD  |
|                      | Cloud                 |     O    |    S    |   2 MD  |   5 MD   |  4 MD |  5 MD |  2 MD |  18 MD |
| Validation           | Testing               |     O    |    C    |   1 MD  |   2 MD   |  2 MD |  3 MD |  1 MD |  9 MD  |
| Deployment & Closure | Production Deployment |     S    |    O    |   0 MD  |   1 MD   |  0 MD |  1 MD |  0 MD |  2 MD  |
|                      | Testing Deployment    |     C    |    O    |   1 MD  |   0 MD   |  1 MD |  0 MD |  1 MD |  3 MD  |
| Sub-total            |                       |          |         |  43 MD  |   31 MD  | 40 MD | 39 MD | 32 MD | 185 MD |

---

## Arquitectura

![Arquitectura CarWeb drawio](https://user-images.githubusercontent.com/57450093/221737889-ba914df5-3208-4078-bdfb-a1a3ff140ef8.png)

---

## Techstack

##### Frontend:

Se utilizará Typescript como lenguaje en el frontend en vez de Javascript. Ocupan la misma sintaxis pero es un lenguaje estricto en donde se tienen que definir los tipos de datos y permitira que tengamos menos errores. Además se puede usar perfectamente con react, que es una de las librerías de frontend mas utilizadas actualmente y que todos en el salón hemos utilizado. TailWind se usara para simplificar el css.

<p>
<a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="typescript" width="40" height="40"/> </a>
<a href="https://reactjs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> <a href="https://tailwindcss.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" alt="tailwind" width="40" height="40"/> </a>
</p>

##### Backend:

Para el backend proponemos una solución basada en la nube de AWS. En donde utilizaremos API gateway y AWS Lambda para tener un backend escalable, serverless y seguro. Esto implicaria crear funciones con AWS Lambda (las funciones de lambda pueden crearse en diferentes lenguajes, como equipo pensamos que la mejore opción seria usar python debido a que todos conocemos el lenguaje y es muy fácil de utilizar), a las cuales podremos acceder a traves de rutas creadas en API Gateway. Toda la infraestructa se encontrara en una VPC (Virtual Private Cloud), este lograra que no todo el mundo pueda acceder directamente a la API.

<p>
<a href="https://www.python.org/" target="_blank" rel="noreferrer"><img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg" title="Python" alt="Python" width="40" height="40"/></a>
<a href="https://aws.amazon.com/es/api-gateway/" target="_blank" rel="noreferrer"> <img src="https://cloudfront.romexsoft.com/wp-content/uploads/2020/09/Amazon-API-Gateway.svg" alt="api-gateway" width="40" height="40"/> </a> <a href="https://aws.amazon.com/es/lambda/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Amazon_Lambda_architecture_logo.svg/1200px-Amazon_Lambda_architecture_logo.svg.png" alt="aws-lambda" width="40" height="40"/> </a> <a href="https://aws.amazon.com/es/vpc/" target="_blank" rel="noreferrer"> <img src="https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/core-aws-services/connect-resources-with-aws-networking/images/aa91e6b1882061229f9220f4160052dc_65-b-47835-0-f-72-4801-975-a-5-f-9-d-419-e-012-c.png" alt="vpc-aws" width="40" height="40"/> </a>
</p>

##### Base de Datos y Almacenamiento:

PostgreSQL es el lenguaje de bases de datos que decidimos utilizar para este proyecto. Elegimos SQL debido a que nos permite hacer queries complejas y especificamente PostgreSQL debido a que tiene mejores tipos de datos que otras bases de datos SQL. Utilizaremos el servicio RDS (Relational Database Service) para hostear nuestra base de datos en la nube de AWS. Ademas de esto para guardar documentos de los clientes decidimos usar el servicio S3 de AWS; que nos permite guardar documentos, imagenes, etc.

<p>
<a href="https://www.postgresql.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="40" height="40"/> </a><a href="https://aws.amazon.com/es/rds/" target="_blank" rel="noreferrer"><img src="https://www.logicata.com/wp-content/uploads/2020/08/Amazon-RDS@4x.png" alt="RDS" width="40" height="40"/></a> <a href="https://aws.amazon.com/es/s3/" target="_blank" rel="noreferrer"> <img src="https://res.cloudinary.com/practicaldev/image/fetch/s--bZ7myZIR--/c_imagga_scale,f_auto,fl_progressive,h_1080,q_auto,w_1080/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ip7ork2m951siwgpkety.png" alt="s3" width="40" height="40"/> </a>
</p>

##### Despliegue y Autenticación:

Consideramos que implementar un servicio de Autenticación desde 0 no es una prioridad y podria ser bastante tardado. Por lo que decidimos usar el servicio de firebase auth que nos ofrece google. Esto nos permitira autenticar a nuestros usuarios de una manera muy sencilla y podremos incorporar increibles funcionalidades como iniciar sesión con google, facebook, etc. El hosting es muy fácil de implementar en firebase y consideramos que es la mejor opción porque ya lo hemos utilizado.

<p>
<a href="https://firebase.google.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/> </a>
</p>

##### ChatBot:

Crear un chatbot puede ser considerado como un proyecto a parte de lo que se busca con esta materia. Por eso como equipo buscamos incorporar dialogflow, un servicio de google cloud que nos permite usar un chatbot sin necesidad de progrqmarlo a su totalidad.

<p>
<a href="https://cloud.google.com/dialogflow?hl=es-419" target="_blank" rel="noreferrer"> <img src="https://planetachatbot.com/wp-content/uploads/2021/05/DIALOGFLOW.png" alt="Dialogflow" height="40"/> </a>
</p>

##### Procesamiento de lenguaje natural:

El socioformador busca que se puedan realizar busquedas a traves de lenguaje natural. Para procesarlo utilizaremos GCP Natural Language. De esta manera podremos destruturar el texto solicitado por los clientes y generar resultados que se asemejen a la busqueda.

<p>
<a href="https://cloud.google.com/natural-language?utm_source=google&utm_medium=cpc&utm_campaign=latam-MX-all-es-dr-SKWS-all-all-trial-e-dr-1605194-LUAC0014891&utm_content=text-ad-none-any-DEV_c-CRE_548115622250-ADGP_Hybrid%20%7C%20SKWS%20-%20EXA%20%7C%20Txt%20~%20AI%20&%20ML_Natural-Language-KWID_43700066578948460-kwd-477477959998&utm_term=KW_cloud%20natural%20language-ST_Cloud%20Natural%20Language&gclsrc=ds&gclid=CPfy37mct_0CFa6OxQIdMzYNew&hl=es-419" target="_blank" rel="noreferrer"> <img src="https://diamond-thumbnails.s3.us-west-2.amazonaws.com/thinkbigcms/Product/logo/d1e012b2-0f81-4d87-987d-362aca757ac2.png?hash=298750e8bc20834066726c67edf1516a" alt="Cloud Natural Language GCP" height="40"/> </a>
</p>

##### Pagos:

Para los pagos tenemos pensado incorporar un third-party como lo es Stripe. Este nos permitirá incorporar diferentes metodos de pago en nuestra aplicación de una forma muy sencilla.

<p>
<a href="https://stripe.com/mx?utm_campaign=paid_brand-MX_es_Search_Brand_Stripe-7351764142&utm_medium=cpc&utm_source=google&ad_content=618458268464&utm_term=stripe&utm_matchtype=e&utm_adposition=&utm_device=c" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/b/ba/Stripe_Logo%2C_revised_2016.svg" alt="stripe" height="40"/> </a>
</p>
