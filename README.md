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
8. [Techstack](#techstack)
9. [Architecture](#architecture)
10. [Software Tests](#software-tests)

---

## User Stories
| id | Historia de usuario                                                                                                                                   | Criterio de aceptación                                                                          | clasificación |
| -- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ------------- |
| 1  | Como cliente debo poder crear mi cuenta.                                                                                                              | Pantalla de crear cuenta que contiene campos de email, contraseña y especificas de el domicilio | M-Must Have   |
| 2  | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder cerrar sesión.                                             | Boton en el navigation bar para que se pueda cerrar sesión                                      | M-Must Have   |
| 3  | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder iniciar sesión.                                            | Forma que contiene 2 campos: email y contraseña                                                 | M-Must Have   |
| 4  | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder actualizar datos de mi cuenta como nombre, ubicación, etc. | Forma que permita al usuario cambiar datos personales como nombre y domicilio                   | S-Should Have |
| 5  | Como cliente, vendedor, gerente, super-admin, administrador de grupo automotriz debo poder restablecer mi contraseña                                  | Boton que permite restablcer contraseña en caso de que se me haya olvidado                      | M-Must Have   |

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


## Techstack

Frontend:
<p>
<a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="typescript" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://reactjs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> 
</p>

Backend:
<p>
<a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://expressjs.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" alt="express" width="40" height="40"/> </a> <a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> 
</p>

Auth:
<p>
<a href="https://firebase.google.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/> </a>
</p>
  

