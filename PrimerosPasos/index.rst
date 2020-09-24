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
===
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

Usuarios
--------
QuoTravel maneja diferentes tipos de usuario que dan distintos niveles de acceso a la aplicación. Para cada usuario vamos a poder definir la siguiente información:

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

.. attention:: Send em
