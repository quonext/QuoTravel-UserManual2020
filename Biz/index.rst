##############
Business rules
##############
En esta sección vamos a aprender a configurar todos los actores que intervienen en las transacciones dentro de QuoTravel así como algunos conceptos comunes como son los mercados, las lineas de producto, etc...

Mercados
========
Las reservas deben ir siempre asociadas a un mercado, por tanto es obligatorio crear al menos un código de mercado. El mercado será uno de los criterios que aplicará QuoTravel a la hora de buscar el precio que tiene que aplicar a la reserva, además de ser un concepto que puede servirnos para el estudio estadístico de la información. Los mercados se crean en *Biz -> Mercados*. La información a mantener para cada mercado es únicamente el nombre.

Grupos de agencias
==================
QuoTravel maneja el concepto de grupos de agencia para permitir al cliente dar condiciones comunes de Mark up a un conjunto de agencias. Este es un concepto voluntario que puede o no utilizarse y puede ponerse en marcha en cualquier momento. Los grupos de agencia se crean en *Biz -> Grupos de agencias*. La información para cada grupo es la siguiente:

  :Nombre: Etiqueta que representa al grupo dentro de QuoTravel.
  :Markup: Código de markup que aplicaremos a todas las agencias que asociemos al grupo, siempre que la propia agencia no tenga un markup propio.

Agencias
========
Las agencias dentro de QuoTravel representan a los clientes a los que se facturarán las reservas que vayamos asociando a ellas. Toda reserva debe tener una agencia relacionada. Si vamos a la opcion *Biz -> Agencias* vamos a ver un listado de las agencias creadas hasta el momento, su estado y posición, esto incluye el importe de sus reservas, el importe ya facturado y el saldo pendiente de cada una de ellas. Desde ls lista podremos abrir la ficha de una agencia para actualizar su información, consultar todos sus datos u obtner un PDF con todas las tarifas de esa agencia. La información a mantener para cada agencia es la siguiente:

General
-------
Datos generales de la agencia.

  :Nombre: Etiqueta que representa a la agencia en QuoTravel.
  :Estado: Nos indica si la agencia está activa. Podemos desactivar una agencia para dejar de utilizarla a nivel operativo pero conservar su referencia para los datos históricos. Existe un estado "Crédito excedido" que indica que la agencia ha superado alguno de sus límites de crédito y por tanto no puede hacer reservas.
  :Grupo: Enlace con los grupos de agencias mencionados anteriormente.
  :Mercado: Enlace con el mercado. De esta manera al indicar la agencia en la reserva también heredará el mercado, aunque será posible personalizar el mercado en cada reserva.
  :Idioma: Idioma por defecto de los clientes de esa agencia, se pondrá en las reservas de la agencia, aunque será posible personalizar el idioma en cada reserva.

Contacto
--------
Datos de contacto general con la agencia. 

  :Dirección completa: Texto en el que vamos a poder indicar la dirección postal completa de la agencia.
  :Teléfono: Número de contacto principal con la agencia
  :Email: Correo electrónico principal de la agencia

Operaciones
-----------
Datos que afectarán a la operativa diaria con las reservas de la agencia.

  :Marca: Indicaremos con cual de nuestras marcas trabaja este código de agencia.
  :Reglas de cancelación: Indicar cual es la regla general de cancelación con la que va a trabajar esta agencia.
  :Documentación requerida: //TODO: ¿Cual es el uso de este campo? 
  :Crédito permitido: Aquellas agencias que no tengan esta marca deberán prepagar todas sus reservas antes de la fecha de servicio y en caso contrario serán canceladas.
  :Permite venta directa: Marcas aquellas agencias a cuyos clientes podremos vender servicios que se pagan al contado en el destino, como las excursiones.
  :Requiere informe paro de ventas: //TODO: ¿Cual es el uso de este campo?

Seleccion de productos 
----------------------
Condiciones para el producto que podremos utilizar en las reservas de esta agencia. 

  :Permite on request: Lo marcaremos si esta agencia quiere disponibilidad aunque sea on request.
  :Permite PVP: Lo marcaremos si esta agencia respeta los PVP que le pasemos. Si no está marcada esta opción no le proporcionaremos precios que estén marcados como PVP obligatorio.
  :Terceros permitidos: Lo marcaremos si esta agencia quiere producto de terceros (producto que obtengamos a traves de una integración xml).

Revenue
-------
Condiciones que afectarán al precio de venta que daremos a la agencia.

  :Markup: Aquí asignamos el margen que se debe utilizar con este cliente. El margen se aplica sobre los precios de compra, cuando no existe un contrato de venta que fije el precio. Un ejemplo típico es el del producto que obtenemos a través de una integración con un tercero, donde solo tenemos el precio de compra.
  :Fee: Condiciones de tasas que aplicaremos a las reservas de este cliente. //TODO: ¿Que ocurre si a una agencia hay que facturarle el Handling fee y el Rep. Service?

Facturación
-----------
Datos que afectan a las facturas que vamos a generar en base a las reservas de la agencia.

  :Divisa: Código de la divisa a utilizar en la facturación. En caso de que sea necesario, QuoTravel realizará la conversión entre la divisa del precio de venta y la divisa de facturación.
  :Agente financiero: Relación con los agentes financieros que comentaremos dentro del modulo de finanzas y que nos servirá para obtener los datos de impuestos a utilizar.
  :Exportable a app facturación: //TODO: ¿Que significa esto? ¿Enlace con BC?
  :ID en app facturación: Código de enlace entre QuoTravel y la aplicación de facturación.
  :Facturar shuttle por separada: Permite indicar al sistema que al facturar los traslados genere una factura separada para los clientes de shuttle. 

Líneas de producto
==================
Esta codificación nos a va permitir separar los productos que vendemos y compramos para varias utilidades dentro de QuoTravel:
  1. Asignación a los contratos, de esta manera podemos simplificar el contenido de los mismos.
  2. Asignación a los markups, de esta manera se reducen las condiciones
  3. Agrupación estadística de nuestros productos para su posterior estudio.

La definición de una línea de producto se hace en *Biz -> Lineas de producto*; unicamente hay que rellenar una etiqueta identificativa. Tenemos la posibilidad de inactivar una linea de producto temporalmente. 

Markups
=======
Los márgenes nos sirven para indicar que reglas debemos aplicar para el cálculo de un precio de venta, cuando lo que tenemos es solo un contrato de compra.  Si existe un contrato de venta válido para nuestro cliente ese es el que manda pero, si solo tenemos un contrato de compra, todavía podemos obtener el precio de venta aplicando un margen, si es que existe alguno aplicable para nuestro cliente. Los markups se definen en *Biz -> Markups* y la información que podemos rellenar es la siguiente:

  :Nombre: Esta será la etiqueta identificativa.
  :Activo: Un código de markup se podrá desactivar temporalmente.
  :Retail: //TODO: ¿Cual es el uso de este campo? 

En la ficha del markup podremos ver y definir que entidades utilizan cada códigos:

  Grupos de agencias, Se pueden asociar varios grupos de agencia
  Agencias, Se pueden asociar varias agencias

En las lineas del markup podemos detallar el modo de aplicación y el importe del mismo:

  :Línea de producto: Enlace con productos, a traves de su línea de productos.
  :Porcentaje: Importe porcentual del markup.
  :Markup mínimo: Importe monetario del mínimo que queremos aplicar, en caso de que la aplicación del porcentaje sobre el precio de compra no llegue a este mínimo, este será el importe que vamos a facturar al cliente.
  :Markup máximo: En caso de que queramos limitar el importe a facturar al cliente. 
  :Activo: Cada línea del markup se puede activar o desactivar individualmente.

 La lógica de aplicación de margenes es:

  * Si no existe un contrato de venta entonces intentamos conseguir el precio de venta aplicando un margen sobre el precio de compra
  * Las reglas de margen están indicadas en la agencia o, si no, en el grupo de agencias
  * Buscamos una línea de margen activa para el producto que estamos vendiendo
  * Si existe esa línea aplicamos margen
  * Si no existe esa línea no podemos vender ese producto

Comisiones
==========
Las comisiones se aplican tanto a clientes como proveedores, y pueden convertirse en un descuento o en una comisión real con su iva correspondiente. En ambos casos se genera una línea de cargo que facturaremos, utilizaremos para validar la factura del proveedor, o se aplicará como un descuento en la factura. En el caso de las reservas que son pago directo en el hotel será el único servicio que vamos a facturar, con lo que será la única línea de cargo existente en la reserva. Las comisiones se van liquidando con cada reserva o pedido de compra. Las comisiones se definen en *Biz -> Comisiones* y la información que podemos mantener es la siguiente:

  :Nombre: Esta será la etiqueta identificativa.
  :Activa: Un código de comisiones se puede desactivar temporalmente.

En la ficha de la comisión vamos a poder ver y definir que entidades se asocian a cada código:

  Grupos de agencias, Se pueden asociar varios grupos de agencia
  Agencias, Se pueden asociar varias agencias

//TODO: Teniendo en cuenta que las comisiones se asocian a los contratos, ¿Que necesidad hay de esta lista de agencias?

En las lineas de la comisión vamos a poder detallar el modo de aplicación y el importe de la misma:

  :Líneas de producto: Enlace con productos, a traves de su línea de productos.
  :Porcentaje: Importe porcentual de la comisión
  :Descuento: Indicamos cuando queremos que la comisión se aplique como un descuento en la factura
  :Activo: Cada línea de comisión se puede activar o desactivar individualmente.

Fees
====
Para cada cliente podemos definir un conjunto de Fees (entre ellos el más habitual es el Handling Fee) que se aplicarán a las reservas para generar lineas de cargo que se incluiran en las facturas. Para mantener un Fee tenemos que ir a *Biz -> Fees* donde veremos que la información se estructura en forma de cabecera y lineas de detalle de la siguiente manera:

*Cabecera*
  :Nombre: Será la etiqueta identificativa
  :Concepto facturación: Enlace con la tabla que define el comportamiento a nivel de impuestos.

*Lineas*
  :Nombre: Es el enlace entre la cabecera y las lineas
  :Inicio: Fecha inicial de vigencia de la aplicación
  :Final: Fecha final de vigencia de la aplicación

  :Por noche: Indica si el precio de este Fee se va a aplicar a cada noche de la estancia.
  :IVA Incluido: Cuando se marque indica que el precio del Fee ya lleva los impuestos incluidos.
  :Porcentaje: El porcentaje del Fee que se aplicará sobre el importe del coste de la reserva. //TODO: Confirmar con Miguel

  :Min. Pax Grupo: Definición del mínimo de personas que tiene que tener una reserva para ser considerada de grupo. //TODO: Comentar si este total es por Expediente o reserva
  :Min. Habs. Grupo: Definición del mínimo de habitaciones que tiene que tener una reserva para ser considerada de grupo.

  :Precio adulto reserva individual: Precio por adulto que aplicaremos en las reservas individuales.
  :Precio niño reserva individual: Precio por niño que aplicaremos en las reservas individuales.
  :Precio habitación reserva individual: Precio por habitación que aplicaremos en las reservas individuales.
  :Precio reserva reserva individual: Precio por total por reserva que aplicaremos en las reservas individuales.

  :Precio adulto reserva grupo: Precio por adulto que aplicaremos en las reservas de grupo.
  :Precio niño reserva grupo: Precio por niño que aplicaremos en las reservas de grupo.
  :Precio habitación reserva grupo: Precio por habitación que aplicaremos en las reservas de grupo.
  :Precio reserva reserva grupos: Precio por total por reserva que aplicaremos en las reservas de grupo.

  :Para hoteles propios: Si está marcado aplicaremos el fee a las reservas donde el contrato de compra no esté marcado como facturación directa. Esto es, hoteles que gestionemos nosotros e integraciones con terceros.
  :Para hoteles directos: Si está marcado aplicaremos el fee a las reservas donde el contrato de compra sí esté marcado como facturación directa. Esto es, contratos que solo tenemos en el sistema para controlar los cupos y los cierres de venta.
  :Para traslados: Si está marcado quiere decir que aplicaremos este fee a las reservas de solo traslado. //TODO: Confirmar con Miguel.
  :Para cualquier expendiente: Cuando queremos que este fee se aplique a cualquier expendiente, sin importar los productos que haya en él.

Como vemos un Fee se podrá definir como un precio fijo o como un porcentaje sobre el importe de la reserva, ambas condiciones son excluyentes. Para facilitar la creación de las lineas tenemos la acción *Copiar previo* que permite traer los datos del registro anterior al registro que estamos creando.

Límites de crédito
==================
Para controlar el riesgo que queremos asumir con cada cliente podemos utilizar los límites de crédito, estos límites de crédito de mantienen en *Biz -> Límites de crédito* y su información es la siguiente:

  :Nombre: Es la etiqueta identificativa.
  :Tipo: Podemos definir límites sobre las reservas (serán las reservas no facturadas) o sobre la facturación (serán las facturas no pagadas).

  :Divisa: Indica la divisa del importe que vamos a poner como límite
  :Limite: Importe del límite

  :Umbral de aviso: Importe a partir del que queremos recibir un aviso
  :Email: Direcciones de correo que van a recibir el aviso, separadas por el simbolo ;
  :Status: Para ver si el límite está activado, desactivado, avisado o excedido //TODO: ¿Qué aplicación tienen los dos últimos valores si un límite se puede aplicar a varios clientes 

Proveedores
===========
En *Biz -> Proveedores* podremos mantener la información de los proveedores a los que enviamos las peticiones de servicio (reservas o servicios) y de los que vamos a recibir las facturas de compra que tendremos que validar contra nuestras previsiones. En la lista de proveedores el usuario podrá ver el importe en pedidos de compra, el importe en facturas recibidas y el importe pendiente de pago. Desde la ficha del proveedor vamos a poder generar un PDF con todos los precios de compra de un proveedor TODO: "Ahora mismo no hace nada, lo he probado en varios proveedores". Los datos a mantener para cada proveedor son los siguientes:

  :Nombre: Es la etiqueta identificativa.
  :Status: Para poder desactivar un proveedor sin necesidad de borrarlo, así dejaremos de poder trabajar con él, respetando los históricos.
  :Comentarios: Notas que queramos dejar dentro de QuoTravel.

  :Divisa: Código de la divisa que usaremos en la facturación del proveedor.
  :Agente financiero: Enlace con los agentes que se definen en el area de finanzas que tienen la información fiscal y de impuestos.

  :Dirección: Es la dirección postal completa del proveedor.
  :Teléfono: Número principal de contacto con el proveedor.
  :Email: Correo electrónico principal del proveedor.

Facturación
-----------

  :Exportable a la app de facturación: TODO: ¿Que significa esto? ¿Enlace con BC?
  :ID en app de facturación: Código del proveedor dentro de la app de facturación.

Datos adicionales
-----------------

  :Pagadero a en vouchers: Texto que aparecerá en los vouchers que se emitan para los servicios de este proveedor.
  :Porcentaje extra de markup: Será un porcentaje de margen adicional que se aplicará sobre los márgenes definidos. TODO: ¿se aplica a la hora de buscar el precio de venta, verdad?
  :Provee hotel:
  :Provee transfer:
  :Provee excursiones:
  :Provee ticket:
  :Provee genericos: TODO: ¿Que aplicación práctica tienen estos campos? 

Envío de pedidos
----------------

  :Método envío pedidos: Podemos escoger entre el envío por correo como un PDF adjunto, el envío mediante XML o el envío mediante el agente de QuoOn. TODO: ¿Explicación?
  :Valor incluido en pedido: Marcaremos este campo cuando queramos que la valoración del servicio vaya incluida en el envío.
  :Dirección de envío: Dirección a la que vamos a enviar los pedidos de compra.
  :Envío automático: Marcar este campo para que los pedidos de compra se envíen automáticamente al asignarlo al proveedor.
  :Confirmación automática: Si marcamos este campo el pedido se marca como confirmado al enviarlo, en caso contrario hay que marcar el pedido como confirmado, de manera manual.
  :Email certificado: Para que el envío del correo se haga utilizando SSL. TODO: Confirmar que sea cierto.

Representantes
==============
En *Biz -> Reps* vamos a poder mantener la información de los representantes de venta. En QuoTravel podemos definir representantes que son, básicamente, agentes que se llevan una comisión sobre una venta, pudiendo ser empleados o proveedores. Para cada representante definiremos una serie de datos:

  :Nombre: Es la etiqueta identificativa.
  :Status: Para poder desactivar un representante sin necesidad de borrarlo, así dejaremos de poder trabajar con él, respetando los históricos.
  :Agente financiero: Enlace con los agentes que se definen en el area de finanzas que tienen la información fiscal y de impuestos. TODO: ¿Como se distingue cuando el representante es un empleado de cuando no lo és?

  :Oficina: Todo representante debe estar asociado a una oficina de venta. Este dato permitirá obtener una estadistica de todos los representantes de cada oficina.
  :Supervisor: Lo vamos a utilizar en aquellos casos en que un representante trabaje bajo la supervisión de otro representante. TODO: Yo estos campos los quitaria
  :Porcentaje comision supervisor: Cuando el supervisor cobre una comisión sobre las ventas de los representantes bajo su supervisión.

  :Dirección: Es la dirección postal completa del representante.
  :Teléfono: Número de contacto con el representante.
  :Email: Correo electrónico para contactar con él.
  :Comentarios: Notas que queramos dejar dentro de QuoTravel. 

Talonarios de tickets
---------------------
Vista de los talonarios ya entregados al representante, para que podamos revisar su estado. También tenemos un campo para ver el talonario que se usará en los tickets que se hagan a traves de la APP de venta de excursiones. 
 
Liquidación de ventas
=====================
Desde la ficha de cada representante podremos lanzar el proceso de liquidación que se inicia mostrando una pantalla al usuario donde podrán seguir los pasos hasta crear y registrar la liquidación:

  1. Seleccionar las fechas que se van a incluir en el proceso y pulsar en *Aplicar filtros*, estos filtros afectan al numero de reservas, total de venta y comisión que sale en la pantalla.
  2. El usuario acceder a la lista de tickets que se van a liquidar para excluir algún ticket que por algún motivo se quiera excluir de la liquidación aunque este dentro del periodo de fechas.
  3. Se puede hacer una previsualización de la liquidación.
  4. Para las ventas hechas al contado directamente por el representante el usuario podrá marcar la opción Crear factura para cliente contado.
  5. Una vez de acuerdo con la liquidación pulsando en el botón Liquidar para seguir adelante
  6. Se tienen que introducir los pagos, para representar el dinero entregado por el representante, que servirán para liquidarse con la factura.
  7. Una vez completado el proceso se podrá generar un PDF con la liquidación.

Comisiones
==========
En *Biz -> Comisiones* vamos a poder definir las comisiones que se aplican a los representantes. A cada comisión que se le asigna una etiqueta y después abrir la ficha de la comisión para detallarla. El detalle de las comisiones se introduce de la siguiente manera:

  :Agente: Será el código de representante al que aplica
  :Linea de producto: Enlace con las lineas de producto que agrupan los productos simplificando la introducción de comisiones.
  :Fechas: Periodo de aplicación
  :Base: Para indicar cual es el importe base de cálculo de la comisión. Las opciones son Total o Margen. TODO: No veo una manera facil de aplicar la comisión por Margen y me falta una opción para indicar Total sin impuestos.
  :Porcentaje: Precio de la comisión
  :Supervisor: Lo vamos a utilizar en aquellos casos en que un representante trabaje bajo la supervisión de otro representante.
  :Comisión supervisor: Cuando el supervisor cobre una comisión sobre las ventas de los representantes bajo su supervisión.
  :Resultado: TODO: Comentar opciones
  :Impuestos incluidos: Permite indicar si a la comisión hay que aplicar

Centros de producción
=====================
TODO: Comentarlo