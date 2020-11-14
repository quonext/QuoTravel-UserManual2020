########
Porfolio
########
En este área vamos a poder dar de alta y mantener la información de los servicios que va a vender la agencia así como las condiciones de disponibilidad, venta y compra para cada uno de ellos. QuoTravel permite la gestión de los siguientes tipos de producto (TODO: Podriamos quitar Rentacar y Train de la lista?) que luego vamos a tratar en profundidad:

  * Entancias en Hoteles.
  * Traslados. 
  * Excursiones.
  * Circuitos
  * Ticket.
  * Billetes de avión.
  * Seguros de viaje
  * Genéricos.

Datos comunes
=============
Los productos comparten una serie de informaciones que vamos a poder mantener en el área Común de QuoTravel.

Tarifas
-------
Las tarifas nos van a permitir la definición de distintos niveles de precios dentro de los contratos que creemos para los distintos servicios/productos. Cada tarifa se define de la siguiente información:

  :Nombre: Etiqueta interna de la tarifa.
  :Orden: TODO: ¿Orden de aplicación de la tarifa?

  :Nombre público: Nombre que mostraremos a la hora de enviar los tarifarios a los clientes. Permite la opción multi-idioma.
  :Términos y condiciones: Texto libre para incluir a la hora de imprimir el tarifario. Permite la opción multi-idioma.
  :Disponible online: Marcaremos este campo para indicar que esta tarifa se puede utilizar en la venta online.

Observaciones
-------------
Podemos definir observaciones que deben aparecer automáticamente al hacer una reserva TODO: Aparecen en los vouchers. Para cada código de observación podemos indicar una serie de filtros (que se utilizan para saber si esta observación debe aparecer o no). La información para definir cada observación es la siguiente:

  :Tipo producto: Indicaremos a cúal de los tipos de producto queremos asociar esta observación.
  :Texto: Detalle de la observación, permite la definición en varios idiomas.

  :País: Cuando queremos limitar su aparición a las reservas de un páis.
  :Destino: Cuando queremos limitar su aparición a las reservas de un destino.
  :Zona: Cuando queremos limitar su aparición a las reservas de un zona.

  :Periodo de fechas: Podremos indicar el periodo de fechas de venta al que vamos a aplicar esta observación. (TODO: ¿Es cierto que aplica sobre venta?)
  :Activo: Podremos activar o desactivar manualmente la observación.

Etiquetas
---------
Utilidad para crear códigos de etiquetas que se podrán utilizar luego en la definición los servicios y que serán de utilidad a la hora de facilitar las busquedas en la venta online o a traves de la APP para la venta móvil. Cada etiqueta consta de la siguiente información:

  :Nombre: Identificación interna.
  :Descripción: Texto libre que podremos generar en los idiomas necesarios.   
