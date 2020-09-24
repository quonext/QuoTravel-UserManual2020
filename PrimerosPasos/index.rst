###########################
Primeros pasos en QuoTravel
###########################
En esta sección vamos a aprender a dar los primeros pasos en QuoTravel. 

Acceso al sistema
=================

El sistema se suministra siempre con algunos usuarios ya creados. Además de algunos usuarios que son necesarios para el funcionamiento del sistema, se proporciona un usuario con privilegios de administrador, que es el que utilizaremos para acceder al sistema por primera vez y para crear otros usuarios:

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
  * Logo -> Si utilizamos la opción *BYTES* vamos a poder usar el botón UPLOAD para cargar el fichero del logo. Si usamos la opcion URL se podrá indicar la ruta donde está almacenado el logo. Tiene el mismo uso que el nombre de la empresa

.. attention:: Configuración correo eletrónico. 

Configurar los datos del servidor de correo que QuoTravel va a utilizar en los procesos de envío de correo:

.. note:: Configuración SMTP

  * Host SMTP
  * Puerto SMTP
  * Activación de la capa de transporte (TLS)
  * Activación de Secure Sockets Layer (SSL)

.. note:: Credenciales administrador

  * Usuario y contraseña -> Datos de usuario para que el sistema los utilice para enviar los correos
  * Remitente de los correos electrónicos (también se puede agregar una dirección para recibir copia)

.. note:: Configuración POP 3

  * Host POP 3
  * Usuario y contraseña
  * Email rebote -> cuenta de correo a la que hay que enviar los correos cuando haya problemas en el proceso de envío

.. attention:: Integraciones

Configurar las integraciones que permiten a QuoTravel interactuar con diferentes sistemas para el envio de SMS, realizar traducciones, Colas de trabajo y más...

.. note:: SMS

QuoTravel puede utilizar SMS para informar, por ejemplo, de las horas de recogida a los clientes de traslados. Esta opción requiere tener una cuenta en el servicio Clickatell.

Habilitar Clickatell
  Para indicar si queremos utilizar Clickatell para el envío de SMS

Clave Clickatell
  La clave a utilizar para acceder a la plataforma de Clickatell

.. note:: Telegram

QuoTravel puede utilizar Telegram como metodo para informar a los cientes. 

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

QuoTravel utiliza este servicio de mapas

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
  Dirección

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

Usuarios
--------
QuoTravel maneja diferentes tipos de usuario que dan distintos niveles de acceso a la aplicación. Cuando se da de alta un nuevo usuario QuoTravel envía un correo con la contraseña de acceso que el usuario debe cambiar en su primer acceso. Para cada usuario vamos a poder definir la siguiente información:

Login
  Código alfanumérico del usuario. Debe ser único. No se distinguen mayúsculas.
Nombre
  El nombre completo del usuario
Email
  Email del usuario. El usuario recibirá un email de bienvenida en esta dirección, con el password.
Estado
  Un usuario puede estar en uno de los siguientes estados:

  ===============  ==============================================================================================
  Activo           El usuario puede acceder al sistema
  Inactivo         Hemos desactivado el usuario y no puede acceder al sistema
  Bloqueado        Sucede tras haberse equivocado más de 10 veces al poner el password
  Caducado         Ha pasado la fecha de caducidad. El usuario ya no puede acceder al sistema
  ===============  ==============================================================================================

Fecha de caducidad
  Aquí podemos indicar una fecha para la desactivación automática de este usuario. Después de esa fecha, el usuario pasará al estado *Caducado* y no podrá seguir accediendo a QuoTravel.
Foto
  La foto del usuario
Comentarios
  Comentarios de uso interno

.. attention:: Enviar correos al usuario

  1. Enviar correo
  2. Enviar correo de bienvenida
  3. Recuperar contraseña
