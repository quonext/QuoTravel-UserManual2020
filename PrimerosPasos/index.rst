###########################
Primeros pasos en QuoTravel
###########################
En esta sección vamos a aprender a dar los primeros pasos en QuoTravel y configurar aquellas tablas que servirán de base al resto de módulos. 

Acceso al sistema
=================
QuoTravel se suministra siempre con algunos usuarios ya creados. Además de algunos usuarios que son necesarios para el funcionamiento del sistema, se proporciona un usuario con privilegios de administrador, que es el que utilizaremos para acceder al sistema por primera vez y para crear otros usuarios:

========  =========
Usuario   **admin**
Password  **1**
========  =========

Se recomienda cambiar la contraseña para garantizar la seguridad del entorno. 

Configuracion inicial
*********************
En la sección *Admin* vamos a encontrar una serie de configuraciones que se deben completar para comenzar a utilizar QuoTravel y que vamos a revisar a continuación.

Datos básicos empresa
---------------------
Dentro de *AppConfig* vamos a configurar una serie de datos como son:

  * Business Name -> Nombre de la empresa que se utilizará en nuestra intranet, en documentos y en algunos emails
  * Logo -> Si utilizamos la opción *BYTES* vamos a poder usar el botón UPLOAD para cargar el fichero del logo (se acepta cualquier formato de imagen: jpg, png, gif, webp ...). Si usamos la opcion URL se podrá indicar la ruta donde está almacenado el logo. Tiene el mismo uso que el nombre de la empresa

.. attention:: Configuración correo eletrónico. 

Configurar los datos del servidor de correo que QuoTravel va a utilizar en los procesos de envío de correo:

.. note:: Configuración SMTP. Utilizamos esta configuración para el envío de correos

  * Host SMTP
  * Puerto SMTP
  * Activación de la capa de transporte (TLS)
  * Activación de Secure Sockets Layer (SSL)

.. note:: Credenciales administrador

  * Usuario y contraseña -> Datos de usuario para que el sistema los utilice para enviar los correos
  * Remitente de los correos electrónicos (también se puede agregar una dirección para recibir copia)

.. note:: Configuración POP 3. Utilizamos está configuración para la lectura de correos

  * Host POP 3
  * Usuario y contraseña
  * Email rebote -> Cuando un proceso de importar reservas desde un correo electrónico por fallo de formato da error, esta es la direccion que recibe un aviso con el mail reenviado.

.. note:: Gmail required links

Son los enlaces a seguir para autorizar que podamos enviar correos utilizando los servidores de gmail.

.. attention:: Integraciones

Configurar las integraciones que permiten a QuoTravel interactuar con diferentes sistemas para el envio de SMS, realizar traducciones, Colas de trabajo y más...

.. note:: SMS

QuoTravel puede utilizar SMS para informar, por ejemplo, de las horas de recogida a los clientes de traslados. Esta opción requiere tener una cuenta en el servicio Clickatell.

Habilitar Clickatell
  Para indicar si queremos utilizar Clickatell para el envío de SMS

Clave Clickatell
  La clave a utilizar para acceder a la plataforma de Clickatell

.. note:: Telegram

QuoTravel puede utilizar Telegram como metodo para informar a los cientes. El bot debe existir previamente, aquí unicamente configuramos los datos de conexión al servicio.   

Habilitar Telegram
  Para indicar si queremos utilizar Telegram para el envío de información.

Token bot Telegram
  Token para autenticar en el bot de Telegram

.. note:: DEEPL

QuoTravel puede utilizar este servicio para proponer traducciones en a la hora de introducir textos en diferentes idiomas.

Habilitar DeepL
  Para indicar que este servicio está activo.

Clave autenticación DeepL
  Clave de acceso al servicio DeepL

.. note:: MapBox

QuoTravel utiliza este servicio de mapas en la ficha del hotel, tanto en la web como dentro de QuoTravel.

.. note:: Flight stats

QuoTravel permite usar este servicio para actualizar la información de los horarios de vuelo de manera automática. 

ID Flight stats
  Identificación en el servicio.

Clave API Flight
  Clave de acceso a la API de Flight stats.

.. note:: DOCUSIGN

QuoTravel puede utilizar este servicio para el envio de los contratos a los clientes y proveedores de una manera segura.

Clave integración
  Clave de acceso al servicio.

URI redirección 
  Campor proporcionado por DOCUSIGN como parte de los datos de conexión.

Clave privada
  Clave de firma dentro del servicio

.. note:: Message Queue

QuoTravel utiliza las colas de trabajo para la automatización de algunos procesos que se explicarán más adelante.

Host Message Queue
  Dirección del servidor

Usuario Message Queue
  Usuario del servicio

Contraseña Message Queue 
  Contraseña de acceso al servicio

.. attention:: CMS
Aquí indicaremos la información necesaria para poder trabajar con el gestor de contenidos que después podremos aprovechar en la web. 

Directorio configuración Nginx
  Aquí indicamos el path del firectorio donde deben crearse los ficheros de configuración de Nginx

Comando para recargar Nginx
  Aquí indicamos el comando que debe ejecutarse cada vez que actualizamos la configuración de Nginx

.. attention:: Plantillas

QuoTravel utiliza plantillas para todos los documentos e emails que se generan desde la plataforma.

De esta forma podemos personalizarlos.

Normalmente utilizamos XSL-FO para generar pdfs y Freemarker para generar el html que metemos en los emails.

Xsl-fo para listados
  Se utilia para generar los pdf a partir de los listados

Xsl-fo para contrato de hotel
  Se utiliza para generar el pdf para revisar / firmar el contrato de hotel

Xsl-fopara contrato de traslado
  Se utiliza para generar el pdf para revisar / firmar el contrato de traslado

Xsl-fo para el voucher
  Se utiliza para generar el voucher en formato pdf

Xsl-fo para factura emitida
  Se utiliza para generar el pdf de una factura

Xsl-fo para el mundo
  Se utiliza para generar un pdf con todo nuestro producto

Xsl-fo para objeto
  Se utiliza para generar un pdf para cualquier objeto del sistema, con vistas a imprimirlo.

Xsl-fo para listas de traslado
  Se utiliza para generar un pdf con una lista de traslados

Xsl-fo para pedidos de compra
  Se utiliza para generar un pdf para un pedido de compra

Freemarker para pedido de compra
  Se utiliza para generar el email para una pedido de compra

Freemarker para SMS horario recogida
  Se utiliza para generar el SMS que enviamos a los clientes para informar la hora de recogida de los traslados

Freemarker para email horario recogida
  Se utiliza para generar el email que enviamos a los hoteles para informar la hora de recogida de los traslados

Freemarker para SMS horario recogida en español
  Se utiliza para generar el SMS que enviamos a los hoteles para informar la hora de recogida de los traslados cuanod el móvil es español (prefijo 34).

.. attention:: Conceptos facturación

QuoTravel permite configurar una serie de cnceptos de facturación que actuarán como valores por defecto en caso de que un producto no tenga configurado ese campo. Estos conceptos se utilizarán en la facturacion para determinar los impuestos que aplican en cada caso.

.. attention:: Divisa local

QuoTravel utilizará esta divisa como divisa común a la hora de realizar comparaciones entre ingresos y costes que pueden definirse en distintas divisas dentro de los contratos.

.. attention:: Facturación

Marca de agua facturas
  El funcionamiento para rellenar este campo es el mismo que en el caso del logo, explicado en esta misma sección del manual. Esta marca de agua se utilizará en la impresión de las facturas.

Agente venta directa
  En este campo vamos a poder especificar el agente contable que utilizará QuoTravel para las facturas hechas como venta directa (usualmente llamado cliente contado).

.. attention:: Traslados

QuoTravel permite definir las plantillas para las listas de pasajeros, diferenciando por el tipo de servicio (Shuttle, Privado, Ejecutivo y Compartido).

.. attention:: Contabilidad

Correo notificaciones contabilidad
  Dirección de correo para enviar notificaciones al departamento de facturación/contabilidad

Margen cuadre facturas
  Este campo permite indicar

Margen aceptación factura
  Mediante este campo podemos indicar cual es el margen de diferencia a la hora de aceptar una factura de compra que nos llegue a traves de la integración con Voxel.

.. attention:: Activar módulos web

  Los campos de esta pestaña van a permitir activar los tipos de producto que se van a poder vender mediante los iframes de QuoTravel.

.. attention:: Controles genéricos

Máximo de reservas
  QuoTravel permite establecer un máximo de reservas en un periodo de minutos definido por el usuario y se puede activar la opción para desactivar el hotel en caso de cumplirse las condidiciones. 

Markup negativo
  Podemos indicar al programa que desactive un producto si detectamos una venta online con markup negativo, para darnos tiempo a revisar los contratos y ver si se ha producido un error.

Usuarios
--------
QuoTravel maneja diferentes tipos de usuario que dan distintos niveles de acceso a la aplicación. Cuando se da de alta un nuevo usuario QuoTravel envía un correo con la contraseña de acceso que el usuario debe cambiar en su primer acceso. Para cada usuario vamos a poder definir la siguiente información:

:Login: Código alfanumérico del usuario. Debe ser único. No se distinguen mayúsculas.
:Nombre: El nombre completo del usuario
:Email: Email del usuario. El usuario recibirá un email de bienvenida en esta dirección, con el password.
:Estado: Un usuario puede estar en uno de los siguientes estados:

  ===============  ==============================================================================================
  Activo           El usuario puede acceder al sistema
  Inactivo         Hemos desactivado el usuario y no puede acceder al sistema
  Bloqueado        Sucede tras haberse equivocado más de 10 veces al poner el password
  Caducado         Ha pasado la fecha de caducidad. El usuario ya no puede acceder al sistema
  ===============  ==============================================================================================

Para proteger el sistema, si un usuario se equivoca de manera consecutiva 10 veces al intentar acceder al sistema, el usuario queda bloqueado. Esto es así para evitar que alguien averigue los passwords utilizando un proceso automático. Cuando esto sucede, el usuario pasa a estado *Bloqueado* y hay que desbloquearlo entrando en la ficha del usuario y cambiando su estado a *Activo*.

:Fecha de caducidad: Aquí podemos indicar una fecha para la desactivación automática de este usuario. Después de esa fecha, el usuario pasará al estado *Caducado* y no podrá seguir accediendo a QuoTravel.
:Foto: La foto del usuario, en estos momentos es un dato que se muestra solo en esta ficha
:Comentarios: Comentarios de uso interno
:Oauth: Este campo se pondrá a verdadero cuando la contraseña no resida en la base de datos de QuoTravel (AD, Google). 

.. attention:: Enviar correos al usuario

  1. Enviar correo. Esta acción nos permite comprobar que la dirección de correo es correcta
  2. Enviar correo de bienvenida. Esta acción nos permite enviar un enlace para facilitar la primera conexión del usuario, en esta conexión el usuario deberá cambiar la contraseña.
  3. Recuperar contraseña. Si un usuario ha olvidado el pasword puede recuperarlo utilizando la opción *Password olvidado* que le aparece cuando va a acceder a QuoTravel. El sistema le enviará entonces un email con una url para indicar un nuevo password. El link que recibe el usuario tiene fecha de caducidad.

Tipos de usuario
****************
Los diferentes tipos de usuario son:

  1. QuoTravel/Back. Son los usuarios que tendrán acceso a la configuración y operatividad de QuoTravel, en función de los permisos controlaremos el acceso a los distintos módulos.
  2. Aeropuerto. Son los usuarios que acceden al módulo especifico del aeropuerto. Siempre relacionados con un aeropuerto concreto para ver gestionar sus traslados.
  3. Agencia. Acceso para que las agencias puedan gestionar sus reservas directamente en QuoTravel.
  4. Proveedor. Acceso para que los proveedores puedan ver sus pedidos de compra directamente en QuoTravel
  5. Representantes. Son los usuarios que podrán utilizar la APP de venta de excursiones. Cada usuario estará asociado a un punto de venta, código de representante y banco (para la integración de los cobros de tarjeta)
  6. Tokens API. Para las integraciones B2B que se vayan a utilizar. El ID del token lo asigna automáticamente QuoTravel mediante la acción Create Token
  7. Web. Usuarios finales de la Web, son los usuarios que se dan de alta en la web del cliente y mediante esta opción podremos mantener la informacion del programa de puntos.

Organización de la empresa
==========================
QuoTravel permite adaptarse a la organización interna de la empresa, incluyendo varias empresas con distribución en varias oficinas, así como la gestión de diferentes marcas de comercialización. Dentro del menú Admin encontraremos el área Organización donde podremos mantener esta información. 

Creación de empresas
-------------------
Dentro del área de organización podremos crear las diferentes empresas que vayamos a mantener en la instancia de QuoTravel. Esto quiere decir que dentro de la misma base de datos pueden coexistir varias empresas diferentes, cada una con su contabilidad, pero compartiendo la base de datos de clientes, usuarios, etc. De esta manera una oficina puede gestionar servicios independientemente de si luego serán facturados por una u otra empresa. Naturalmente, si queremos mantener bases de datos estancas para cada una de nuestras empresas también es posible. Para cada empresa vamos a poder mantener la siguiente información:

:Nombre: Nombre que queremos que se muestre en los informes
:Logo: Imagen corporativa de la compañia
:Agente financiero: Relación con los agentes financieros que comentaremos más adelante y que nos servirá para obtener los datos de impuestos a utilizar.
:Serie facturación: Aquí indicaremos el código de série para las facturas emitidas por esta empresa
:Serie autofactura: Aquí indicaremos el código de série a utilizar cuando la empresa se autofacture un coste
:Registry data: Pendiente de confirmar que es el NIF 
:Datos de pago: Registro de los datos bancarios de la empresa

Creación de marcas
------------------
Las creación de marcas permite a la empresa comercializar un mismo producto con diferentes precios, campañas de marketing y sitios web. Siempre debe existir al menos una marca por instancia de QuoTravel. Tanto la carga de producto como las reservas necesitan estar asociadas a una oficina. La información a mantener para cada marca se divide en tres áreas:

Principal

:Nombre: Identificación de la marca
:Empresa: Toda marca debe estar relacionada con una de las empresas creadas anteriormente
:Markup para retail: Relación con los códigos de markup que definiremos más adelante y que nos permitirán obtener un precio de venta a partir del precio de compra sin necesidad de tener un contrato de venta dado de alta en QuoTravel.

Web

:Terminos y condiciones: Texto que aparecerá en la página web, se podrá traducir a los idiomas que se deseen, esta traducción se podrá aprovechar del servicio DEEPL en caso de que se haya configurado en AppConfig.
:Texto mailing no deseado: Texto que aparecerá en la página web. 

Pasarela de pago

:TPV: Aquí indicaremos código de pasarela de pago que se usará en la página web de venta al público de esta marca. En el área financiera podremos ver como se configuran las pasarelas de pago.

Creación de oficinas
--------------------
La creación de oficinas permite la distribución de áreas de responsabilidad de las reservas y servicios dentro de las áreas operacionales de QuoTravel. Tanto la carga de producto como las reservas necesitan estar asociadas a una oficina. La información a mantener para cada oficina se divide en las siguientes areas:

Identificación

:ID: Código de identificación de la oficina, servirá para enlazar en los productos y reservas
:Nombre: Descripción de la oficina
:Logo: Imagen asociada a la oficina 

Configuración

:Zona: Relación de la oficina con una de las zonas que definimos dentro del área mundo de Admin
:Empresa: Toda oficina tiene que estar relacionada con una empresa para conocer el origen de las facturas emitidas para reservas y servicios de esa oficina
:Serie reservas: Definición de la numeración de las reservas relacionada con la oficina

Contacto

:Email: Dirección de contacto de la oficina
:Telefono y fax: Datos de contacto
:Dirección: Dirección postal de la oficina
:Teléfono de confirmación de recogidas: Pendiente

Correo

:Host: La dirección del servidor de correo saliente. Normalmente este dato lo proporcionará el departamento de sistemas
:Puerto: El puerto del servidor de correo saliente. Normalmente este dato lo proporcionará el departamento de sistemas
:Usuario: El usuario a utilizar para conectarse al servidor de correo