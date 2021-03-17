########
Porfolio
########
En este área vamos a poder dar de alta y mantener la información de los servicios que va a vender la agencia así como las condiciones de disponibilidad, venta y compra para cada uno de ellos. QuoTravel permite la gestión de los siguientes tipos de producto que luego vamos a tratar en profundidad:

  * Estancias en Hoteles.
  * Traslados. 
  * Excursiones.
  * Circuitos
  * Tickets.
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
  :Orden: Para poderlas ordenar en la selección de tarifas.

  :Nombre público: Nombre que mostraremos a la hora de enviar los tarifarios a los clientes. Permite la opción multi-idioma.
  :Términos y condiciones: Texto libre para incluir a la hora de imprimir el tarifario. Permite la opción multi-idioma.
  :Disponible online: Marcaremos este campo para indicar que esta tarifa se puede utilizar en la venta online.

Observaciones
-------------
Podemos definir observaciones que deben aparecer automáticamente al hacer una reserva. Aparecen en la página web y en los vouchers que se imprimen para los clientes. Para cada código de observación podemos indicar una serie de filtros (que se utilizan para saber si esta observación debe aparecer o no). La información para definir cada observación es la siguiente:

  :Tipo producto: Indicaremos a cúal de los tipos de producto queremos asociar esta observación.
  :Texto: Detalle de la observación, permite la definición en varios idiomas.

  :País: Cuando queremos limitar su aparición a las reservas de un páis.
  :Destino: Cuando queremos limitar su aparición a las reservas de un destino.
  :Zona: Cuando queremos limitar su aparición a las reservas de un zona.

  :Periodo de fechas: Podremos indicar el periodo de fechas de servicio al que vamos a aplicar esta observación.
  :Activo: Podremos activar o desactivar manualmente la observación.

Gestión de Fichas de producto
-----------------------------
Con la definición de fichas de producto, QuoTravel permite enriquecer la información que almacenamos para cada producto y que podremos enviar a nuestros clientes y utilizar en la página web. La información que podemos mantener para cada hoja de producto es la siguiente:

  :Nombre: Será la etiqueta identificativa de la ficha.
  :Descripción: Tengo ampliado para describir el producto, como vemos trabaja en un editor de texto embebido en QuoTravel. Este texto lo podremos traducir a todos los idiomas manejados por QuoTravel.
  :Imagen principal: Podremos asignar una primera imagen para el producto que usualmente se usa para acompañar a la descripción.
  :Listado de imagenes: Lista de todas las imágenes que se quieran asociar al producto.
  :Multimedia: Lista de los archivos multimedia que se quieran asociar al producto.
  :Características: Listado de características que se asocian al producto.
  :Etiquetas: Lista de las etiquetas que se asocian al producto.

En las fichas de producto podremos asignar características que permitan la busqueda de producto de una manera más intuitiva en la WEB o en la APP de venta móvil. La definición de cada característica viene dada por la siguiente información:

  :Nombre: Etiqueta identificativa, se puede introducir en todos los idiomas manejados por QuoTravel.
  :Icono: Asignación de un icono a la característica.
  :Grupo: Incluir la característica en uno de los grupos mencionados en el punto anterior.

Las características se pueden agrupar. La definición de cada grupo se realiza asignando un nombre al grupo. Desde la ficha del grupo podremos ver todas las características que se han incluido en él, así como añadir o quitar características.

En la ficha podemos asignar etiquetas que serán de utilidad a la hora de facilitar las busquedas en la venta online o a traves de la APP para la venta móvil. Cada etiqueta consta de la siguiente información:

  :Nombre: Identificación interna.
  :Descripción: Texto libre que podremos generar en los idiomas necesarios.

Clausulas
---------
Dentro de los contratos vamos a poder incluir unas clausulas que se incluirán como texto en la impresión de los contratos. Estas clausulas se basan en grupos de clausulas, para definir un grupo simplemente debemos darle un nombre. Una vez creado el grupo vamos a poder definir los textos que se deben incluir, estos textos se podrán ordenar como deseemos que aparezcan en la impresión. 

Hotel
=====
En este área vamos a completar la definición de los productos de hotel que vamos a gestionar dentro de QuoTravel, con toda la codificación asociada así como la gestión de los precios de compra y venta. 

Tipos de Hoteles
----------------
Esta opción nos permite crear, opcionalmente, diferentes tipologias de hoteles, como puedan ser hoteles, albergues, aparthoteles, campings, etc... Los tipos se definen con la siguiente información:

  :Nombre: Identificación interna.
  :Nombre traducido: Utilizaremos este valor cuando queramos hacer visible esta información de cara al exterior, se podrá traducir a todos los idiomas gestionados en QuoTravel.

Categorias
----------
Utilizaremos esta opción para crear las categorias de establecimientos que queramos manejar dentro de QuoTravel. Cada categoria se define con la siguiente información:

  :Codigo: Etiqueta interna.
  :Nombre: Descripción de la categoria, se podrá traducir a todos los idiomas gestionados en QuoTravel.
  :LLaves: Valor relacionado con la clasificación de los apartamentos
  :Estrellas: Valor relacionado con la clasificación de los hoteles

Regímenes alimenticios
----------------------
Hay que crear la codificación interna de los regímenes que vamos a utilizar dentro de los contratos y las reservas. Para definir un régimen hay que introducir la siguiente información:

  :Código: Etiqueta identificativa.
  :Nombre: Descripción del régimen, se podrá traducir a todos los idiomas gestionados por QuoTravel. 

Tipos de habitación
-------------------
En este punto vamos a crear la codificación interna de los diferentes tipos de habitación que vamos a manejar en QuoTravel. Para definir un tipo de habitación hay que introducir la siguiente información:

  :Código: Etiqueta identificativa.
  :Nombre: Descripción del tipo de habitación, se podrá traducir a todos los idiomas gestionados por QuoTravel.

Extras hotel
------------
Esta opción se utiliza para mantener los extras que vamos a poder utilizar en los contratos de hotel para definir un cargo o un descuento que se aplicará en la reserva. Para definir un extra hay que introducir la siguiente información:

  :Código: Etiqueta identificativa.
  :Nombre: Descripción del extra, se podrá traducir a todos los idiomas gestionados por QuoTravel.

Hoteles
-------
Al entrar en la lista de hoteles vamos a poder buscar por nombre o filtrar por la oficina de venta, el proveedor, o la zona para localizar el hotel que estamos buscando. La información que vamos a mantener de cada establecimiento hotelero es la siguiente:

  :Nombre: Nombre para mostrar internamente.
  :Activo: Nos permite desactivar un establecimiento para que dejar de utilizarlo temporalmente.
  :Oficina: Código de oficina a la que vamos a relacionar este producto/hotel.
  :Dirección: Datos de contacto.
  :Punto de recogida: Enlazamos el hotel con un punto de recogida que será el utilizado en las reservas de traslado.

  :Proporcionado por: Podemos enlazar la ficha de hotel con una ficha de proveedor.
  :Linea de producto: Definir a que linea de producto pertenece el hotel, como hemos visto en el apartado de Negocio estas lineas de producto permiten la aplicación de margenes y la clasificación estadística de nuestros productos.
  :Zona: Ubicar el hotel dentro de una de las zonas, a traves de la zona estaremos también ubicando el hotel en un destino.

  :Tipo de hotel: Clasificación interna.
  :Categoría: Indicamos la clasificación del establecimiento.
  :Cadena hotelera: Datos informativo que nos permitirá filtrar los establecimientos de una cadena a la hora de buscar.

  :URL Google: Enlace a google maps.
  :Latitud: Coordenada del mapa.
  :Longitud: Coordenada del mapa, una vez rellenados estos datos podemos usar la opcion Show in google maps para ver la ubicación del establecimiento en ese servicio.

  :Edad mínima niños: Es la edad a partir de la cual aplicaremos el precio de niño a una persona.
  :Edad mínima jovenes: Es la edad a partir de la cual aplicaremos el precio de junior a una persona.
  :Edad mínima adultos: Es la edad a partir de la cual aplicaremos el precio de adulto a una persona.
  :Invertir orden por edad: Utilizamos este campo cuando queremos decirle al sistema que ordene los niños de menor a mayor para la aplicación de suplementos. 

  :Hoja de producto: Enlace con la hoja de producto que vamos a usar para este establecimiento. Las hojas de producto permiten añadir imagenes, videos, etiquetas y características a un producto. Desde la ficha del establecimiento podemos hacer una previsualización de la hoja producto.
  :PDF: Podemos adjuntar un PDF a la ficha de producto, se puede hacer mediante una imagen o una URL a una carpeta compartida.

  :Habitaciones: Definición de las habitaciones con las que trabaja el establecimiento.
  :Regímenes: Definición de los regímenes alimenticios con las que trabaja el establecimiento. Dentro del hotel un régimen podrá tener una descripción propia y un orden para la impresión de los contratos.
  :Cupos: Creación de los distintos cupos que vamos a poder usar en el establecimiento.

En la lista de los hoteles tenemos una opción para crear un punto de recogida para cada establecimiento automatizando esta tarea necesaria para trabajar con los traslados. 

Habitaciones hotel
------------------
Dentro del hotel podemos personalizar la información de los tipos de habitación genéricos que hemos creado. La información que podemos mantener es la siguiente:

  :Orden: Decidir el orden de aparición en la impresión.
  :Tipo: Seleccionar el tipo de habitación de entre los genéricos creados en este mismo menú.
  :Descripción: Texto libre que podemos traducir a todos los idiomas gestionados por QuoTravel.
  :Foto: Se puede asociar una imagen a cada tipo de habitación, se puede incluir como una URL a una ruta compartida o directamente como una imagen.

  :Bebes permitidos: Podemos configurar las habitaciones para no aceptar reservas con Bebes. 
  :Niños permitidos: Podemos configurar las habitaciones para no aceptar reservas con Niños. 
  :Bebes ocupan cama: Indicamos si en las habitaciones que permiten bebes vamos a tenerlos en cuenta en la ocupación.

  :Cupo propietario: Utilizaremos esta opción en casos como las individuales que descuentan del cupo de las dobles. Este ejemplo lo que se haria es indicar el código de la doble en este campo.

  :Capacidades máximas: QuoTravel permite la definición de varias combinaciones de tipos de persona a la hora de definir la capacidad máxima de cada tipo de habitación.
  :Mínimo paxes: En aquellos contratos con precio por persona esta cantidad se aplicará para calcular la reserva.
  :Mínimo adultos para descuento niños: Indicar la cantidad de adultos necesarios para poder aplicar un suplementos a los niños que haya en ese tipo de habitación.

Regímenes alimenticios hotel
----------------------------
Dentro del hotel podemos personalizar la información de los regímenes alimenticios genéricos que hemos creado. La información que podemos mantener es la siguiente:

  :Orden: Decidir el orden de aparición en la impresión.
  :Tipo: Seleccionar el tipo de régimen de entre los genéricos creados en este mismo menú.
  :Descripción: Texto libre que podemos traducir a todos los idiomas gestionados por QuoTravel.

Extras permitidos en hotel
--------------------------
Mediante esta opción vamos a definir los extras permitidos en cada hotel. La información que podemos mantener es la siguiente:

  :Tipo: Enlace con la tabla de códigos genéricos definidos en este menú.
  :Descripción: Texto libre que podemos traducir a todos los idiomas gestionados por QuoTravel.
  :Opcional: Cuando este campo no esté marcado le estamos diciendo al sistema que este extra se aplicará todas reservas de ese hotel.
  :Solo uso interno: Para marcar aquellos extras que no queremos que se puedan usar desde la web.

Paros de venta  
--------------
Con esta opción gestionaremos los paros de venta recibidos de los hoteles y que afectarán a la posibilidad de crear reservas en QuoTravel. Esta consulta permite la visualización de todos los paros de venta dados de alta en el sistema. Los criterios de definición de un paro de venta son:

  :Hotel: Todo paro de venta tiene que estar asociado a un hotel. Al seleccionar el hotel se nos muestra el calendario mostrando el mes actual y el siguiente permitiendo a partir de ahí que el usuario se mueva líbremente cambiando de periodo. 
  :Agencia: En aquellos casos que interese podremos hacer un paro de ventas que solamente afecta a una agencia.
  :habitación: Si dejamos este campo en blanco quiere decir que estamos afectando a todas las habitaciones del hotel.
  :Regimen: Cuando sea necesario podemos incluir el regimen como criterio a la hora de cerrar o reabrir ventas. 
  :Periodo fechas: Con las fechas desde y hasta definimos el periodo de aplicación, ambas fechas son obligatorias.
  :On Request: Con esta marca le decimos a QuoTravel que no estamos cerrando si no que las reservas creadas quedan en estado On Request.

Desde el calendario tenemos tres acciones disponibles:

  :Cerrar: Crear el registro de cierre de ventas. Si ponemos el cursor sobre uno día veremos como en la parte inferior se muestran todas las operaciones de paros de venta.
  :Abrir: Cuando se quieran reabrir las ventas de un periodo cerrado anteriomente.
  :Deshacer: Esta herramienta permite deshacer, dejando sin efecto, las operaciones de cierre o apertura hechas en el hotel.

Gestión de cupos
----------------
Esta opción nos proporciona un calendario donde poder ver y actualizar la información de los cupos de cada hotel, permitiendo la definición de varios cupos sobre cada hotel. Los criterios de definición de una actualización de cupo son:

  :Hotel:  Toda actualización de cupo tiene que estar asociado a un hotel. Al seleccionar el hotel se nos muestra el calendario mostrando el mes actual y el siguiente permitiendo a partir de ahí que el usuario se mueva líbremente cambiando de periodo. Para cada día podremos ver la cantidad de habitaciones así como las reservas On Request y las disponibles.
  :Cupo: Asociar la operación a un código de cupo.
  :Agencia: En aquellos casos que interese podremos hacer una actualización que solamente afecta a una agencia.
  :Habitación: En la gestión de cupos el código es obligatorio.
  :Periodo fechas: Con las fechas desde y hasta definimos el periodo de aplicación, ambas fechas son obligatorias.
  :Cantidad: Indicar cual es la cantidad que queremos dejar. 

Con la acción Set vamos a aplicar la cantidad de habitaciones en el hotel, habitación y periodo especificado.

Adicionalmente disponemos de una consulta de consumo de cupos donde el usuario puede ver aquellos hoteles que tengan una determinada cantidad de habitaciones libres, en un periodo de fechas, lo que es una herramienta util a la hora de responder a una petición de reserva.

Contratos hotel
---------------
En QuoTravel vamos a poder mantener la información de todos los contratos relacionados con los hoteles con lo que trabaja la agencia. Para poder vender un producto tenemos dos opciones :

  * Cargar un contrato de venta
  * Cargar un contrato de compra y definir un margen para la linea de producto de ese hotel.

  Esto es, podemos vender sin que exista contrato de compra o sin que exista contrato de venta. Realmente la venta es independiente de la compra, a no ser que en el contrato de venta explicitemos que, para ese contrato de venta, deben utilizarse exactamente uno o varios contratos de compra determinados.

Contratos compra hotel
**********************
En estos contratos vamos a mantener las condiciones en que compramos el producto, en cada uno de los contratos vamos a poder mantener la siguiente información, agrupada en distintas secciones:

  - General
      :Tarifa: Definiremos a que nivel de tarifa aplica este contrato.
      :Vendible con markup: Este contrato servirá de base a la venta mediante aplicando los margenes de las agencias o grupos de agencias.
      :Tipo de precio: Podemos trabajar con precios netos o con precios venta al público.
      :Fee x reserva: Precio que aplicaremos a cada reserva, adicional a los distintos precios definidos en el contrato.
      :Precios iva incluido: Para indicar que los precios que se introducen en el contrato ya llevan los impuestos incluidos. 
      :Divisa: Código de la divisa en que están introducidos los precios.
      :Concepto facturación: Enlace con la definición de los impuestos que aplicarán en este contrato.
      :Línea de productos: Indicaremos a que linea de productos aplica el contrato, de esta manera podemos comprar el mismo hotel a distintos precios en función de este concepto de QuoTravel.
      :Fechas de validez: Periodo de fechas cubierto por el contrato.
      :Fechas de venta: Periodo de ventas en el que aplicaremos este contrato.
      :Comentarios: Campos en los que podemos indicar unos textos libres con comentarios internos o algún termino especial del contrato.
      :Cupo: Definiremos de que cupo van a consumir las reservas de este contrato.
      :Cupo de seguridad: Definiremos cual es el cupo de seguridad que tendremos para las reservas de este contrato. Este cupo de seguridad se aplicará en caso de existir un paro de ventas. 
      :Porcentaje incremento: //TODO: Pendiente MPEREZ
      :PDF en ingles: Cuando queramos que la generación del PDF, con los datos del contrato, se haga en ingles.
      :Max. personas por reserva: Cantidad máxima de personas que aceptaremos en una reserva para poder aplicar este contrato.
      :Max. habitaciones por reserva: Cantidad máxima de habitaciones.
      :Permite precios ceo: //TODO: Pendiente MPEREZ

  - Relaciones, con los datos introducidos en esta sección vamos a limitar las reservas que pueden utilizar este contrato.
      :Oficina: Todo contrato debe estar relacionado con una de las oficinas de la compañia.
      :Proveedor: Empresa que nos va a facturar el coste de las reservas.
      :Agencias permitidas: Podemos relacionar el contrato con agencias, de manera individual, o mediante grupos de agencias. 
      :Mercados permitidos: Podemos relacionar el contrato con alguno de los mercados creados anteriormente.
      :Marcas: Podemos relacionar el contrato con alguna de nuestras marcas.
      :Agencias prohibidas: En aquellos casos en que sea más sencillo, podemos utilizar una lista de agencias o grupos de agencias prohibidas en lugar de las permitidas.
      :Mercados prohibidos: De igual manera lo podemos hacer con los mercados de origen.

  - Firma, almacenamiento informativo de los datos relativos a la firma del contrato. Estos datos se pueden obtener mediante la integración con Docusign.
      :Firmado en: Lugar de la firma.
      :Proveedor firmado por: Representante del proveedor.
      :Representante empresa: Representante de la agencia.
      :Fecha firma: Momento de la firma.
      :ID Docusign: Identificación recibida de la plataforma Docusign.
      :Enviado: Fecha de envío. 
      :Firmado: Fecha de la firma
      :Firmado por: Identificación de la persona que firmó el contrato.

  - Comisiones
      :Condiciones de comisión: Relación con la tabla de comisiones en caso de que existan. 