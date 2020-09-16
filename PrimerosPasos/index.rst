###
Primeros pasos en QuoTravel
###
En esta sección vamos a aprender a dar los primeros pasos en QuoTravel. 

Acceso al sistema
===

El sistema se suministra siempre con algunos usuarios ya creados. Además de algunos usuarios que son necesarios para el funcionamiento del sistema, se proporciona un usuario con privilegios de administrador, que es el que utilizaremos para acceder al sistema por primera vez y para crear otros usuarios:

========  =========
Usuario   **admin**
Password  **1**
========  =========

Se recomienda cambiar la contraseña para garantizar la seguridad del entorno. 

Configuracion inicial
===

.. attention:: Datos básicos empresa

En la sección *Admin* vamos a encontrar una serie de configuraciones que se deben completar para comenzar a utilizar QuoTravel. Dentro de *AppConfig* vamos a configurar una serie de datos como son:

  * Business Name -> Nombre de la empresa que se utilizará en 
  * Logo -> Si utilizamos la opción *BYTES* vamos a poder usar el botón UPLOAD para cargar el fichero del logo. Si usamos la opcion URL se podrá indicar la ruta donde está almacenado el logo.

.. attention:: Configuración correo eletrónico. Configurar los datos del servidor de correo que QuoTravel va a utilizar en los procesos de envío de correo:

.. note:: Configuración SMTP

  * Host SMTP
  * Puerto SMTP
  * Activación de la capa de transporte (TLS)
  * Activación de Secure Sockets Layer (SSL)
  * Usuario y contraseña
  * Dirección origen de los correos electrónicos (también se puede agregar una dirección para recibir copia)

.. note:: Configuración POP 3
  * Host POP 3
  * Usuario y contraseña
  * Rebound
