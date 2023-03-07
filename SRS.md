# Requerimientos de Especificación de Software

## Tabla de Contenidos

---

[Tabla de Contenidos](#tabla-de-contenidos)
1. [Introducción](#introducción)
    1. [Propósito](#propósito)
    2. [Convenciones del documento](#convenciones-del-documento)
    3. [Alcance del proyecto](#alcance-del-proyecto)
    4. [Referencias](#referencias)
7. [Descripción General](#descripción-general)
8. [Características del Sistema](#características-del-sistema)
9. [Requerimientos de Datos](#requerimientos-de-datos)
10. [Requerimientos Externos de la Interfaz](#requerimientos-externos-de-la-interfaz)
11. [Atributos de la Calidad](#atributos-de-la-calidad)
12. [Internacionalización y Requerimientos de Locación](#internacionalización-y-requerimientos-de-locación)
13. [Otros Requerimientos](#otros-requerimientos)
14. [Modelos de Análisis](#modelos-de-análisis)

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
| NDS      | ?                                                                                              |
| AWS      | Amazon Web Services                                                                            |
| GCP      | Google Cloud Platform                                                                          |
| CSV      | Valores Separados por Comas (del inglés Comma Separated Values)                                |
| OS       | Sistema Operativo (del inglés Operation System)                                                |
| VPC      | Nube Privada Virtual (del inglés Virtual Private Cloud)                                        |
| EC2      | Elastic Compute Cloud                                                                          |
| API      | Interfaz de Programación de Aplicaciones (del inglés Application Programming Interface)        |
| JS       | Java Script                                                                                    |
| SRS      | Requerimientos de Especificación de Software (del inglés Software Requirements Specifications) |

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

(1998) IEEE. Consultado el 6 de marzo, 2023, IEEE Std 830-1998 IEEE Recommended Practice for Software Requirements Specifications. IEEE Computer Society. https://www.cse.msu.edu/SRSExample-webapp



---

## Descripción General

---

## Características del Sistema
    
### 1.- Venta de Vehiculos

Como cliente, debo poder comprar un vehiculo utilizando el sitio web, pare ello debo poder realizar lo siguiente:
    
- Seleccionar el vehiculo que deseo adquirir 
- Introducir mis datos de pago. 
- Subir documentos requeridos para la compra del vehiculo ( comporbante de domicilio, credito, etc. ).
- Consultar el estado de mi pedido. 


 ### 2.- Busqueda de vehiculos por lenguaje natural 
    
Como usuario del sistema, debo poder buscar vehiculos utilizando natural; por ejemplo, el usuario ingresa el siguiente texto: "Busco un coche familiar para utilizar los fines de semana". Acto siguiente, el sistema debe arrojar resultados de busqueda que tengan congruencia con lo solicitado.
 
### 3.- Catalogo de vehiculos 
Como dueño de grupo automotriz, o gerente de una agencia, debo poder dar de alta y administrar el catalogo de vehiculos que se venderan a los clientes del sitio web. Esta administracion incluye:

 - Dar de alta un vehiculo, utilizando su nombre, modelo, año, imagen, motor, etc.
 - Editar vehiculos existentes, ya sea cambiar su nombre, imagen, precio, etc.
 - Eliminar vehiculos del catalogo. 
 - Subir multiples vehiculos al catalogo por medio de un documento tipo excel. 
 - Consulta del catalogo de vehiculos.
 
### 4.- Administracion de empleados 
Como dueño de grupo automotriz, o gerente de una agencia, debo poder administrar los usuarios de mi agencia o grupo automotriz, esto incluye:
 - Dar de alta un empleados, utilizando su nombre, rol, dirección, correo, etc.
 - Eliminar empleados del sistema. 
    
### 5.- Administracion de Dueños   
Como super administrador, debo ser capaz de llevar una administracion de dueño automotrizes, esto incluye:
- Conslultar dueños registrados en el sistema.
- Eliminar dueño registrados sistema. 
- Dar de alta nuevos dueños.
- Consultar documentos subidos por un dueño de grupo automotriz a fin de aceptar una solicitud de unirse al sistema.

    
    
Adicionalmente, como super administrador, debo ser capaz de dar de alta a otros super administradores
---

## Requerimientos de Datos

---

## Requerimientos Externos de la Interfaz

---

## Atributos de la Calidad

---

## Internacionalización y Requerimientos de Locación

---

## Otros Requerimientos

---

## Modelos de Análisis

---

