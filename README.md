# CarWeb_Requirements_Team1

---
##### Creators: [@Diego Araque](https://github.com/DiegoAraque21), [@Salomon Dabbah](https://github.com/SalomonDabs), [@Marco Torres](https://github.com/marcotorresx), [@Fernando Valdeon](https://github.com/lfvm), [@Uriel Aguilar](https://github.com/u-urieldev)

## Index

---

1. [Index](#index)
2. [User Stories](#user-stories)
3. [Requirements](#requirements)
4. [Backlog](#backlog)
5. [Effort and Cost Estimations](#effort-costs)
6. [WBS](#wbs)
7. [Gant](#gant)
8. [Architecture](#architecture)
9. [Software Tests](#software-tests)
10. [Techstack](#techstack)

---

## User Stories
| id | Historia de usuario                                                                                                                                   | Criterio de aceptación                                                                                                                                                                                                                          | clasificación |
| -- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| 1  | Como cliente debo poder crear mi cuenta.                                                                                                              | Pantalla de crear cuenta que contiene campos de email, contraseña y especificas de el domicilio                                                                                                                                                 | M-Must Have   |
| 2  | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder cerrar sesión.                                             | Boton en el navigation bar para que se pueda cerrar sesión                                                                                                                                                                                      | M-Must Have   |
| 3  | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder iniciar sesión.                                            | Forma que contiene 2 campos: email y contraseña                                                                                                                                                                                                 | M-Must Have   |
| 4  | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder actualizar datos de mi cuenta como nombre, ubicación, etc. | Forma que permita al usuario cambiar datos personales como nombre y domicilio                                                                                                                                                                   | S-Should Have |
| 5  | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder restablecer mi contraseña                                  | Boton que permite restablcer contraseña en caso de que se me haya olvidado                                                                                                                                                                      | M-Must Have   |
| 6  | Como cliente podre iniciar sesión directamente con google.                                                                                            | Boton que se conecte con firebase auth y permite hacer el login directamente con google                                                                                                                                                         | C-Could Have  |
| 7  | Como gerente debo poder crear cuentas de mis vendedores                                                                                               | Pantalla que cree usuarios con contraseñas random para nuevos vendedores                                                                                                                                                                        | M-Must Have   |
| 8  | Como cliente debo poder registrar un método de pago.                                                                                                  | Al seleccionar pagar en un coche, tendre la opción de elegir entre multiples modalidades de pago a traves de un simple click                                                                                                                    | M-Must Have   |
| 9  | Como cliente debo poder ver la cuenta bancaria de la agencia para hacer transferencias.                                                               | En caso de elegir transferencia como metodo de pago, como cliente sere capaz de ver la cuenta de la agencia y hacer el movimientos de esta manera                                                                                               | M-Must Have   |
| 10 | Como cliente debo poder ver su estado de cuenta.                                                                                                      | Pantalla que contiene datos sobre transacciones hechas en el pasado por ese usuario en la aplicación                                                                                                                                            | C-Could Have  |
| 11 | Como cliente debo poder buscar con lenguaje natural el vehículo que quiero.                                                                           | Debo de poder buscar un vehiculo con lenguaje comun que usaria con amigos u otros ambientes reales                                                                                                                                              | S-Should Have |
| 12 | Como cliente también quiero poder usar filtros convencionales.                                                                                        | Debo de tener la opción de usar botones que filtren el coche que yo quiera (#puertas, color, capacidad, etc)                                                                                                                                    | M-Must Have   |
| 13 | Como cliente debo poder buscar el coche que quiero sin necesidad de registrarse en la plataforma.                                                     | Iniciar sesión o crear una cuenta no es necesario para navegar en el sistema en caso de ser cliente.                                                                                                                                            | M-Must Have   |
| 14 | Como cliente quiero poder comparar los distintos precios y ofertas de los del mismo coche de diferentes agencias.                                     | Pantalla de comparación de precios y planes de financiamiento del mismo modelo de coche en diferentes agencias                                                                                                                                  | C-Could Have  |
| 15 | Como cliente quiero poder comparar las características de los coches en los que esté interesado.                                                      | Pantalla de comparación estilo la de apple para comparar celulares, pero de coches y sus caracteristicas mas relevantes.                                                                                                                        | S-Should Have |
| 16 | Como cliente debo poder contactar a alguien de servicio al cliente para consultar dudas.                                                              | Boton flotante en cada pantalla del sistema para que el cliente pueda recibir ayuda personalizada                                                                                                                                               | M-Must Have   |
| 17 | Como vendedor debo poder asesorar a los clientes que tengan dudas.                                                                                    | Cmo vendedor una de mis obligaciones sera atender a clientes con dudas sobre algun coche o en especifico de la agencia a la que pertenezco.                                                                                                     | M-Must Have   |
| 18 | Como vendedor debo tener acceso a dudas de clientes en el chat general y tener la oportunidad de asesorar a cualquiera.                               | Cada vendedor tienen acceso a todos los chats que siguen en espera y tendre la oprtunidad de elegir cualquiera y empezar a darle seguimiento                                                                                                    | C-Could Have  |
| 19 | Como administrador de agencia debo dar de alta los vehículos de la agencia.                                                                           | A traves de un archivo csv, la agencia sera capaz de subir su catalogo con un solo click                                                                                                                                                        | M-Must Have   |
| 20 | Como cliente quiero poder visualizar con detalle los vehículos disponibles.                                                                           | Cada vehiculo se vera en tarjetas generales, al presionarlas nos llevara a una pantalla individual del vehiculo donde se observaran todos los datos y peculiaridades. Ademas de botones para comprar el coche y solicitar una prueba de manejo. | M-Must Have   |
| 21 | Como cliente quiero poder comparar las diferentes ofertas y precios de las agencias.                                                                  | Comparar caracteristicas del mismo modelo de diferentes agencias, especificamente costos y planes de financiamiento.                                                                                                                            | C-Could Have  |
| 22 | Como gerente quiero poder ver estadísticas de los modelos o ventas de mi agencia.                                                                     | Pantalla para que la agencia tenga seguimiento sobre su catalogo con información de gran relevancia. Cmo coches mas vendidos, cantidad de dinero ingresada, etc.                                                                                | S-Should Have |
| 23 | Como cliente debo tener diferentes métodos de pago (arrendamiento, mensualidades, de contado)                                                         | Al seleccionar pagar en un coche, tendre la opción de elegir entre multiples modalidades de pago a traves de un simple click                                                                                                                    | S-Should Have |
| 24 | Como agencia debo ingresar datos a los cuales me van a llegar los fondos de cualquier compra.                                                         | Cuando la agencia es aceptada por el super-admin, sera obligada a añadir información de su cuenta bancaria. Para que los pagos sean de cliente a agencia, con unico intermediario la api que usemos (ejemplo: Stripe)                           | M-Must Have   |
| 25 | Como vendedor quiero saber cuantas ventas he realizado y el estado de cada una (cantidad pagada).                                                     | Los vendedores serán capaces de ver todas sus ventas en una pantalla especilidad y el estado de dichas ventas.                                                                                                                                  | C-Could Have  |
| 26 | Como gerente quiero tener acceso a todos los procesos de ventas de mi agencia, y en qué estado se encuentran (culminado, en proceso, empezado, etc).  | Los gerentes tendrán acceso a todos los movimientos de su agencia y de sus vendedores. Con esta información detallada podran realizar sus conclusiones.                                                                                         | S-Should Have |
| 27 | Como cliente quiero poder saber el estado de mi pedido, si el auto está en preparación, en camino, etc.                                               | Despues de pagar el coches, como cliente podre ver en una pantalla el estado de mi pedido. Se dara un aproximado de cuando llegara a su casa.                                                                                                   | M-Must Have   |
| 28 | Como administrador de agencia puedo escoger qué documentos necesita el cliente para realizar la prueba de manejo.                                     | Los administradores de las agencias estan encargados de decir que tipos de documentos son obligatorios para poder solicitar una prueba de manejo.                                                                                               | M-Must Have   |
| 29 | Como cliente debe de poder subir mis documentos para realizar la prueba de manejo (INE, licencia de conducir, etc)                                    | Al solicitar la prueba de manejo de un vehículo, tendre que ingresar datos requeridos por la agencia para lograr el registro                                                                                                                    | M-Must Have   |
| 30 | Como cliente puedo decidir no hacer una prueba de manejo.                                                                                             | No es obligatorio hacer una prueba de manejo para comprar el vehículo.                                                                                                                                                                          | M-Must Have   |
| 31 | Como cliente quiero poder saber el estado de mi prueba, si el auto está en preparación, en camino, etc.                                               | Al solicitar la prueba de manejo, como cliente debo tener acceso a información relevante para dar seguimiento. Especificamente fechas importantes para saber cuando el vehículo llegará a mi casa.                                              | S-Should Have |
| 32 | Como administrador de grupo automotriz quiero dar de alta nuevas agencias.                                                                            | Los administradores de ga tendran una pantalla para dar de alta a sus agencias, estas cuentas seran creadas con contraseñas random.                                                                                                             | M-Must Have   |
| 33 | Como administrador de grupo automotriz de agencia quiero dar de alta nuevos gerentes.                                                                 | Se crearan cuentas para los gerentes con contraseñas random.                                                                                                                                                                                    | M-Must Have   |
| 34 | Como gerente quiero poder dar de alta a los vendedores.                                                                                               | Se crearan cuentas para los vendedores de cada agencia con contraseñas random.                                                                                                                                                                  | M-Must Have   |
| 35 | Como gerente de agencia y administrador de grupo automotriz quiero configurar mis planes de financiamiento.                                           | Los planes de financiamiento son individuales para cada agencia, por lo que tanto los gerentes como los administrador de grupo automotriz podran agregar o eliminar sus planes.                                                                 | S-Should Have |
| 36 | Como gerente de la agencia quiero dar de alta el catálogo de autos de mi agencia.                                                                     | Dar de alta catalogos en una pantalla especial a traves de un archivo csv proporcionado por la agencia.                                                                                                                                         | M-Must Have   |
| 37 | Como Super Admin debo poder dar de alta los grupos automotrices                                                                                       | Al verificar los documentos de un grupo automotriz, se creara su cuenta en el sistema con una contraseña random.                                                                                                                                | M-Must Have   |
| 38 | Como Super Admin debo poder dar de alta otros super usuarios y administradores de grupos automotrices                                                 | Existiran muchos superusuarios en el sistema, todos tendran la posibilidad de crear nuevos usuarios con ese rol. De igual manera seran creados con contraseñas random.                                                                          | M-Must Have   |
| 39 | Como Super Admin debo poder visualizar documentos que los grupos automotrices suban para poder verificar que las agencias son reales.                 | Los super-admins veran las solicitudes de los grupos automotrices y de esta manera verificar si son reales o no.                                                                                                                                | M-Must Have   |
| 40 | Como super administrador quiero poder ver gráficos y estadísticas.                                                                                    | Los super-admins veran información basica sobre el negocio, para saber que tanto estan vendiendo sus agencias y mas información de valor con la que puedan mejorar su plan.                                                                     | S-Should Have |
| 41 | Como administrador de grupo automotriz debo de poder ver gráficas y estadísticas sobre mi grupo (ventas, performance, etc.)                           | Los administradores de grupos automotrices tendran acceso a información de todas sus agencias, para verificar que tan cotizadas son y en base a eso tomar deciciones.                                                                           | S-Should Have |
| 42 | Como vendedor, gerente, super-admin, administrador de grupo automotriz debo de cambiar mi contraseña al iniciar sesión por primera vez.               | Cambar la contraseñas despues de hacer el primer login es obligatorio por temas de seguridad.                                                                                                                                                   | M-Must Have   |
| 43 | Como cliente debo poder ver información general sobre el vehículo a través de tarjetas.                                                               | Tarjetas individuales para cada vehículo, para que el cliente vea información relevante pero no abrumadora.                                                                                                                                     | M-Must Have   |
---

## WBS
![WBS Car Web diagram](https://user-images.githubusercontent.com/78172208/221714997-2ac3fbf4-0dc9-4165-9f81-fdcac4d0d5c5.png)

---

## Requirements
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

## Architecture

![Arquitectura CarWeb drawio](https://user-images.githubusercontent.com/57450093/221737889-ba914df5-3208-4078-bdfb-a1a3ff140ef8.png)

---

## Techstack

Frontend:
<p>
<a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="typescript" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://reactjs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> 
</p>

Backend:
<p>
<a href="https://aws.amazon.com/es/api-gateway/" target="_blank" rel="noreferrer"> <img src="https://cloudfront.romexsoft.com/wp-content/uploads/2020/09/Amazon-API-Gateway.svg" alt="typescript" width="40" height="40"/> </a> <a href="https://aws.amazon.com/es/lambda/" target="_blank" rel="noreferrer"> <img src="https://miro.medium.com/v2/resize:fit:612/format:webp/0*pJZ8UMsoPEv1pjmI.png" alt="typescript" width="40" height="40"/> </a> <a href="https://aws.amazon.com/es/vpc/" target="_blank" rel="noreferrer"> <img src="https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/core-aws-services/connect-resources-with-aws-networking/images/aa91e6b1882061229f9220f4160052dc_65-b-47835-0-f-72-4801-975-a-5-f-9-d-419-e-012-c.png" alt="typescript" width="40" height="40"/> </a>
</p>

Storage:
<p>
<a href="https://www.postgresql.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="40" height="40"/> </a> <a href="[https://aws.amazon.com/es/vpc/](https://aws.amazon.com/es/s3/?nc=sn&loc=0)" target="_blank" rel="noreferrer"> <img src="https://aprenderbigdata.com/wp-content/uploads/amazon-s3-logo-300x225.png.webp" alt="typescript" width="40" height="40"/> </a>
</p>

Hosting and Auth:
<p>
<a href="https://firebase.google.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/> </a>
</p>

ChatBot:
<p>
<a href="https://cloud.google.com/dialogflow?hl=es-419" target="_blank" rel="noreferrer"> <img src="https://planetachatbot.com/wp-content/uploads/2021/05/DIALOGFLOW.png" height="40"/> </a>
</p>

Text Recognition:
<p>
<a href="https://cloud.google.com/natural-language?utm_source=google&utm_medium=cpc&utm_campaign=latam-MX-all-es-dr-SKWS-all-all-trial-e-dr-1605194-LUAC0014891&utm_content=text-ad-none-any-DEV_c-CRE_548115622250-ADGP_Hybrid%20%7C%20SKWS%20-%20EXA%20%7C%20Txt%20~%20AI%20&%20ML_Natural-Language-KWID_43700066578948460-kwd-477477959998&utm_term=KW_cloud%20natural%20language-ST_Cloud%20Natural%20Language&gclsrc=ds&gclid=CPfy37mct_0CFa6OxQIdMzYNew&hl=es-419" target="_blank" rel="noreferrer"> <img src="https://logos-world.net/wp-content/uploads/2021/02/Google-Cloud-Emblem.png" height="40"/> </a>
</p>

Payment:
<p>
<a href="https://stripe.com/mx?utm_campaign=paid_brand-MX_es_Search_Brand_Stripe-7351764142&utm_medium=cpc&utm_source=google&ad_content=618458268464&utm_term=stripe&utm_matchtype=e&utm_adposition=&utm_device=c" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/b/ba/Stripe_Logo%2C_revised_2016.svg" height="40"/> </a>
</p>
