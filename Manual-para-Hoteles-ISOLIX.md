##Manual de Usuario

Por Ingeniería del Software Libre S.L.

EneBoo i-SL Hoteles Enterprise

###Indice

1. Emtorno de EneBoo.........................................................................................1
1. Área Financiera................................................................................................2
1. Área de Facturación.........................................................................................2
1. Estadística............................................................................................2
1. Ficha Policial.......................................................................................2
1. Ocupación............................................................................................2
1. Entradas y Salidas................................................................................2
1. Planing de Reservas.............................................................................3
1. Facturación.....................................................................................................3
1. La factura y sus repercusiones.............................................................3
1. Circuito de compra-venta....................................................................4
1. Conceptos generales............................................................................4
1. Búsqueda de documentos....................................................................4
1. Nueva Factura......................................................................................4
1. Cliente......................................................................................5
1. Datos........................................................................................5
1. IVA...........................................................................................6
1. Observaciones..........................................................................6
1. Contabilidad.............................................................................6
1. Impresión de documentos....................................................................6
1. Circuito completo de venta..................................................................7
1. Entrada de un presupuesto...................................................................7
1. Aprobar presupuesto............................................................................7
1. Generar albarán / Generar Factura......................................................7
1. Facturar...........................................................................................7
1. Tipos de contrato.................................................................................8
1. Contratos.............................................................................................8
1. Servicios a Clientes.............................................................................8
1. Cambiar de Ejercicio...........................................................................8
1. Informes...........................................................................................................9
1. Almacén.........................................................................................................10
1. Introducción.......................................................................................10
1. Entradas y salidas...............................................................................10
1. Datos generales..................................................................................10
1. Artículos.............................................................................................10
1. General...................................................................................11
1. Venta.......................................................................................11
1. Compra...................................................................................12
1. Stocks.....................................................................................12
1. Agentes..................................................................................12
1. Contabilidad...........................................................................12
1. Familias y Subfamilias......................................................................12
1. Tarifas................................................................................................12
1. Almacenes.........................................................................................12
1. Regularización de Stocks..................................................................13
1. Transferencias de Stocks...............................................................................13
1. Control de horas de Operarios....................................................................................13
1. EneBoo i-SL Hoteles Enterprise
1. Principal..........................................................................................................14
1. Empresa.........................................................................................................14
1. Cambiar empresa...........................................................................................15
1. Clientes.....................................................................................................15-16
1. Proveedores...................................................................................................17
1. Ejercicios Fiscales.........................................................................................17
1. Series de Facturación.....................................................................................18
1. Impuestos.......................................................................................................18
1. Cuentas Bancarias.........................................................................................18
1. Bancos...........................................................................................................18
1. Descuentos....................................................................................................18
1. Formas de Pago.............................................................................................18
1. Tipos de Rappel.............................................................................................18
1. Agentes..........................................................................................................18
1. Liquidaciones a Agentes................................................................................18
1. Técnicos.........................................................................................................19
1. Usuarios.........................................................................................................19
1. Departamentos...............................................................................................19
1. Grupos de clientes.........................................................................................19
1. Divisas...........................................................................................................19
1. Paises / Comunidades / Provincias................................................................19
1. Agencias........................................................................................................19
1. Reservas y Ocupación...................................................................................19
1. Habitaciones de clientes................................................................................19
1. Habitaciones..................................................................................................19
1. Centros de coste.............................................................................................19
1. Tesorería.....................................................................................................20
1. Recibos a clientes..........................................................................................20
1. Pagos múltiples de clientes............................................................................21
1. Remesas.........................................................................................................21
1. Pagarés de Proveedor.....................................................................................21
1. Área de recursos humanos......................................................................................22
1. Principal.........................................................................................................22
1. Empleados.....................................................................................................22
1. Candidatos.....................................................................................................22
1. Puestos de trabajo..........................................................................................22
1. Tipos de Contrato..........................................................................................22
1. Nóminas.........................................................................................................22
1. Dietas.............................................................................................................22
1. Área de Dirección..............................................................................................23
1. Análisis..........................................................................................................23
1. Configuración................................................................................................23
1. Navegador................................................................................................23-24
1. Área de C.R.M...............................................................................................24
1. Informes.........................................................................................................24
1. Marketing......................................................................................................24
1. Área de Colaboración............................................................................................25
1. Gestión documental.......................................................................................25
1. Sistema......................................................................................................25
EneBoo i-SL Hoteles Enterprise

##1. Introducción

Este manual esta dirigido para que el usuario, que necesita conocer completamente su herramienta de
trabajo, pueda extraer el máximo rendimiento a su aplicación, lo que le permite ahorrar tiempo,
evitar problemas y controlar de modo eficaz su empresa.

Eneboo es un fork de AbanQ 2.4, una aplicación orientada al desarrollo rápido de aplicaciones
empresariales basadas fuertemente en base de datos bajo la liciencia GPLv2.

Fue creado para poder introducir correcciones al programa y darle un aspecto lo más colaborativo
posible al proyecto.

Entre otras novedades, ofrece un sistema de compilación algo más sencillo y no hace uso de
módulos firmados binarios.

Está ideado principalmente para trabajar sobre PostgreSQL como base de datos, y, aunque
permite otros controladores (como MySQL o SQLite), el único recomendado es PostgreSQL
Antes de empezar a trabajar con Eneboo debemos indicar el servidor al que queremos conectar para
ir guardando los datos de nuestra aplicación. Nos aparece la siguiente pantalla.

Debemos insertar la base de datos donde se irán guardando todos los cambios de nuestra aplicación,
el usuario, la contraseña y la dirección IP del servidor. Pinchamos en conectar y estaremos dentro de
la aplicación.

Para llegar a la finalidad de que el usuario consiga conocer a la perfección la aplicación, debe seguir
completamente éste manual.

EneBoo i-SL Hoteles Enterprise
###Entorno de EneBoo

Un aspecto importante para poder aprovechar todas las posibilidades que brinda esta aplicación, es el
conocimiento de su entorno de trabajo.

Cada vez que inicie la aplicación tendrá un aspecto similar al mostrado en la siguiente imagen.
En ella se puede visualizar la pantalla principal, conteniendo el menú de Eneboo en la ventana
vertical a la izquierda. También dispone de dos ventanas pequeñas en las que se encuentran el
Historial, en el que se reflejan los últimos apartados más utilizados. Y los Marcadores, en él se
pueden insertar los apartados que le resulten más importantes o los más utilizados.

Todas las opciones que se pueden realizar con la aplicación se encuentran accesibles desde la
ventana principal.

Se puede escoger la opción que se desee situando el puntero del ratón sobre dicha opción y
pulsando el botón izquierdo, de este modo se abre una lista con las correspondientes opciones.
También tenemos acceso al menú principal haciendo click con el botón derecho del ratón en la
pantalla principal.

Nota: En función de la aplicación que tenga, estos menús serán distintos.

EneBoo i-SL Hoteles Enterprise

###Configurar empresa
Uno de los pasos previos para iniciar el trabajo con Eneboo, será insertar la información referente a
su empresa, que se realiza en el siguiente apartado:

Área de Facturación → Principal → Empresa (doble click)

En esta pantalla, en la pestaña General, se introduce la información referente a su empresa, para ser
utilizada posteriormente en los listados o documentos.

Valores por defecto

En este apartado se asignan todos los valores que se quiere que aparezcan por defecto en
EneBoo.

La información indicada en este apartado es útil al entrar fichas de clientes, proveedores, o
cualquier otra tarea, ya que aparecen por defecto los datos dados de alta en este apartado.

###Configuración local
Aquí podemos insertar la dirección de correo para poder enviar documentación directamente desde
EneBoo.

EneBoo i-SL Hoteles Enterprise

El siguiente paso es, dar de alta los almacenes con los que trabajemos.

EneBoo permite gestionar el control del stock de sus artículos, con la posibilidad añadida de trabajar
con varios almacenes.

Para dar de alta un almacén:

Área de Facturación → Almacén → Almacenes (doble click)

Hacemos click en insertar registro rellenamos todos los datos y guardamos.
EneBoo i-SL Hoteles Enterprise

##Área Facturación
Dentro de este apartado iremos insertando todos los datos para una correcta gestión de nuestra
empresa.

Clientes

Aquí vamos a introducir todos los datos relacionados con los clientes de la empresa. Esta
información será la que se utilizará para todas las gestiones asociadas con ellos: entrada de albaranes,
facturas, tesorería, etc.

A continuación como ejemplo se verá el diseño de una ficha de un cliente.

Seleccionar el menú Área de Facturación → Principal → Clientes (doble click)

La parte superior muestra los botones disponibles que se detallan a continuación:

* Nuevo: Se utiliza para dar de alta fichas. Desde el teclado pulsando tecla A.
* Modificar: Se utiliza para modificar datos de una ficha. Desde el teclado pulsando tecla M.
* Eliminar: Se utiliza para eliminar la ficha ya existente. Desde el teclado pulsando tecla E.
* Ver: Se utiliza para abrir la ficha del cliente y ver los datos. Desde el teclado pulsar tecla I.
* Imprimir ficha: Se utiliza para imprimir la ficha del cliente.

EneBoo i-SL Hoteles Enterprise

A continuación se detalla paso a paso como se realiza la entrada de una ficha de un cliente:

Las casillas con asterisco (*) se deben de rellenar obligatoriamente.

El código de cliente se puede cambiar o de lo contrario utilizará el código que EneBoo asigna por
defecto.

A continuación, escribimos el nombre del cliente así como todos los datos facilitados por él.
(Nacionalidad, Fecha de nacimiento, Comunidad, Nacido en...)

General

Dentro de la pestaña General seguimos rellenando con datos que nos facilita el cliente como por
ejemplo tipo de identificación (NIF, pasaporte, Certificado de residencia...) y el número. Teléfonos,
fax, e-mail, web...

En Grupo de clientes ponemos, en su caso, si el cliente pertenece a un grupo, por ejemplo: Cliente
Habitual y si le aplicamos una tarifa especial.

En el botón Insertar, se nos abre una ventana para incluir la dirección del cliente.

En Observaciones podemos indicar cualquier dato a tener en cuenta.

Si marcamos la casilla De baja, tenemos que indicar la fecha y este cliente no lo podemos utilizar
para generar cualquier documento como albaranes, facturas...

EneBoo i-SL Hoteles Enterprise

Comercial

Será donde se indiquen sus condiciones comerciales, formas de pago, moneda, serie de facturación,
IVA, etc...

Con estos datos y los días de pago, Eneboo calcula la fecha de los vencimientos.

También podemos insertar el agente que lleva su ficha.

Direcciones

En este apartado se pueden indicar si el cliente dispone de varias direcciones, como por ejemplo,
dirección de facturación, dirección fiscal...

Cuentas Bancarias

En caso de que el cliente pueda tener varias domiciliaciones bancarias para la tramitación de los
recibos, serán indicadas en esta sección

Agenda

En este apartado se indica las personas de contacto. Y en la parte superior derecha aparecen dos
“clips” el de color azul es para asociar a un contacto y el rojo para eliminar asociación.

Descuentos

Será donde se indique si a este cliente se le aplica algún descuento a parte.

Documentos

En este apartado podemos visualizar todos los documentos generados a este cliente, como pueden ser
Ofertas, Pedidos, Albaranes, Facturas, Recibos, Gestión documental.

Contabilidad

Se informará en esta sección de los datos fiscales y las cuentas contables para su posterior trabajo en
contabilidad

Hotel

En este apartado podemos llevar el control de las entradas y salidas de nuestro cliente en el hotel.

Agencia: este apartado es para especificar la agencia por la cual el cliente hizo la reserva. Desde
aquí se pueden dar de alta más agencias.

Entrada y Salida: Aquí apuntaremos el día que entra y sale del hotel.

Habitaciones

Aquí tenemos el histórico de habitaciones ocupadas por el cliente.

Entradas/Reservas

En este apartado indicaremos si se trata de una entrada o de lo contrario si es una reserva
especificando fecha de entrada y salida.

Para finalizar y guardar todos los datos en la parte inferior-derecha hacemos “click” en el símbolo
verde.

Proveedores

En este apartado se introducen todos los datos de los proveedores, que más adelante se utilizan para
todas las gestiones asociadas con ellos, como entrada de albaranes, facturas, cartera, etc.

Artículos

En este apartado aparece la relación de artículos que hemos dado de alta. Al igual que en cualquier
ventana podemos crear un artículo nuevo, modificar, borrar, ver, duplicar...

EneBoo i-SL Hoteles Enterprise

EneBoo tiene varias opciones para tratar el tema de precios. Por un lado, tiene en la ficha del artículo
un precio de venta y otro de compra, pero esto a la mayoría de las empresas se les queda corto.

Por ello hemos introducido la utilización de las tarifas, que le permitirá asignar tantos precios como
sea necesario.

Al pinchar sobre artículo nuevo nos aparece la siguiente pantalla.

En el cuadro de Referencia indicamos la referencia o código del artículo y a continuación la
descripción.

Después tenemos varias pestañas General, Venta, Compra, Stocks, Agentes, Contabilidad.

General

Aquí indicamos la Familia a la que pertenece, en el caso de que pertenezca a alguna. La
clasificación de los artículos en familias puede resultar muy útil en el momento de realizar listados
de artículos de cualquier tipo o en la confección de tarifas.

Si el artículo no forma parte del stock, como por ejemplo las Habitaciones de un Hotel, marcamos la
casilla de Sin stock. De esta manera cada vez que hagamos un Albarán, no descontará stock de este
artículo.

También podemos indicar si este artículo Se compra o Se vende. Podemos marcar las dos opciones.

La opción que no marquemos, la pestaña quedará en blanco.

El siguiente apartado es Nivel TPV. En el caso de trabajar con un TPV, indicaremos en qué nivel se
encuentra éste artículo, para buscar y seleccionar este artículo en el TPV. Podemos añadir una
imagen a partir de un archivo.

EneBoo i-SL Hoteles Enterprise

En el apartado código de barras se puede insertar siempre que trabajemos con un lector de código
de barras.

Y en el apartado Observaciones indicar cualquier anotación sobre este artículo.

Venta

En este apartado indicaremos el precio de venta del artículo, pero solamente se puede introducir uno.

En caso de necesitar varios precios de venta, por ejemplo tarifas de distribuidor, de grandes
almacenes, clientes finales, etc. utilizaremos las tarifas.

Si tenemos tarifas creadas al pinchar en Generar precios, nos aparecerán los distintos precios según
las tarifas creadas.

Compra

En esta pestaña vamos a indicar los proveedores que suministran este artículo y el precio de coste de
cada uno de ellos.

También especificaremos el tipo de IVA de compra de este artículo.

Stocks

Aquí indicaremos el stock mínimo y máximo. También podemos marcar Permitir ventas sin stock,
para que, en el caso de que no tengamos stock podamos hacer un Albarán o Factura de lo contrario si
no lo marcamos cuando vayamos a hacer un Albarán o Factura nos saltará un mensaje que no se
puede insertar ese artículo por no tener stock.

Agentes

Este apartado se utiliza en el caso de existir un agente, y asignarle sus comisiones por la venta de
este artículo.

Contabilidad

En este apartado podemos especificar la Subcuenta de compras y el IRPF de Compras.

Facturación

La factura y sus repercusiones

El documento principal de la aplicación, y que tiene efectos contables, es la Factura. El entrar en
gestión un pedido, albarán, un traspaso, estos no afectan a contabilidad.

A continuación se detallan las repercusiones contables que realiza la aplicación cuando el usuario
introduce una factura, ya sea desde el módulo de gestión o desde contabilidad.

EneBoo i-SL Hoteles Enterprise

Factura

_____________________|__________________________
| | | |
Asientos Registo IVA Tesorería Modelos hacienda
_______|________
| |
Balances Libros
| |
Sumas & Saldos
Situación
Pérdidas y Ganancias
Mayor
Diario

Tal como se muestra en el gráfico, al entrar una factura, automáticamente se registra:

* En el libro de IVA (tanto el repercutido, como el soportado, como el intracomunitario, etc)
* En Tesorería
* En los modelos de Hacienda
* En los apuntes contables

Cuando se realiza un cobro o un pago en tesorería, también se realiza el apunte correspondiente.

Circuito de compra-venta

En este capítulo se muestra el proceso de la venta o compra, desde la recepción de un pedido o de
una oferta hasta su facturación.

Se verá cómo realizar la entrada de presupuesto, generar el pedido, servir la mercancía y facturarlo.

Nota: En los ejemplos que se exponen a continuación se tratan documentos de venta,
teniendo en cuenta que se realiza de la misma forma para los documentos de compra.

EneBoo, da total libertad para generar documentos a partir de otros documentos. Por ejemplo:
* Pasar una oferta a un pedido, a un albarán o a una factura.
* Introducir un pedido (sin oferta) y pasar a un albarán o a una factura.
* Introducir un albarán (sin oferta ni pedido) y facturarlo.
* Introducir una factura (sin ningún otro documento previo).

Conceptos generales

Todos los documentos (ofertas, pedidos, albaranes y facturas) se realizan de la misma forma,
variando su contenido y significado. Para conocer la edición de cualquiera de estos documentos se
expone como ejemplo la búsqueda y entrada de una factura de venta, por tratarse de uno de los más
completos.

EneBoo i-SL Hoteles Enterprise

Búsqueda de un documento.

Para acceder al documento seleccionar en el menú :
Área de Facturación → Facturación → Facturas a Clientes (doble click)

Lo primero que se muestra al entrar en facturas es la pantalla de la selección.
En la parte superior aparecen las herramientas, nuevo, modificar, borrar, ver, duplicar e imprimir.
Más abajo está la barra de búsqueda donde podemos elegir cómo buscar el documento, por ejemplo,
por nombre de cliente, código, fecha...

Nueva Factura

Para hacer una factura nueva pulsamos insertar registro y se abre esta ventana.

EneBoo i-SL Hoteles Enterprise

En la parte superior indica a qué ejercicio pertenece, la serie de facturación y el número de la factura,
el cual EneBoo lo asigna automáticamente.

El documento se compone de los siguientes apartados: Cliente, Datos, IVA, Observaciones,
Contabilidad y están representados en la pantalla por unas pestañas, a las que puede acceder
pulsando sobre ellas con el ratón.

Cliente

Seleccionamos aquel cliente al que se desea realizar la factura. Al introducir el cliente, EneBoo
automáticamente asigna los valores que ya hemos introducido en la ficha del cliente. En este
momento, puede cambiar cualquier información, si se desea.

Datos

Aquí tenemos la fecha del documento (por defecto será la del día de entrada del mismo), también la
podemos modificar. También podemos indicar si le corresponde algún agente, si tiene recargo
financiero, el almacén a los que pertenecen los artículos, la forma de pago y la moneda.

IVA

Marcamos el tipo de IVA a aplicar al cliente.

Observaciones

En esta pestaña puedes indicar si la factura es Rectificativa o cualquier información a resaltar sobre
esta factura en el cuadro de diálogo.

Contabilidad

En este apartado nos indica toda la información contable que se crea automáticamente de esta
factura.

Más abajo está el apartado Líneas, donde entrarán los conceptos de servicios o artículos que se
compran o venden, en función del documento a entrar. También tenemos las opciones de modificar o
borrar líneas.

Hacemos clic en línea nueva y se nos abre el siguiente cuadro.

EneBoo i-SL Hoteles Enterprise

En Referencia, indicamos la referencia del artículo, si no la sabemos, pinchamos en la lupa y nos
aparece la relación de todos los artículos, buscamos el artículo que queremos y lo incluimos.
En la casilla de IVA indicamos el IVA correspondiente. Al igual que en la casilla de Recargo de
Equivalencia e IRPF, en su caso.

Macamos la cantidad servida, el precio de la unidad, indicamos si hay algún descuento, y en el caso
de que tuviera Agente asignado, marcamos la comisión de éste.

Introducimos tantas líneas como queramos, para guardar y finalizar pinchamos en el símbolo verde.
Impresión de documentos.

La impresión de documentos permite imprimirlos en hojas en blanco y adaptarse al formato
establecido por EneBoo, o también diseñar su propio formato y adaptarlo a su tipo de formulario.
En la ventana principal de Facturas de clientes, dispone del botón Imprimir, con el que puede
imprimir el documento que tiene en pantalla directamente.

Circuito completo de venta

A continuación se verá un ejemplo del circuito de venta más completo:
En primer lugar, llega la Oferta de un cliente. Una vez aceptada se hace el Pedido. Cuando se le
entrega el material realiza el Albarán y por último se genera la Factura.

Entrada de un presupuesto

El presupuesto es el documento el cual una vez que el cliente lo acepte, se pueda importar desde un
pedido, desde un albarán o desde una factura, sin necesidad de volver a introducir de nuevo la
información.

Para introducir un presupuesto hay que situarse en el menú Área de Facturación → Facturación →
Presupuestos y seguir los pasos que se detallan en el apartado anterior, ya que la entrada de
documentos es prácticamente igual en todos los casos.

Aprobar presupuesto

Una vez el cliente ha aceptado la oferta se puede generar un pedido, aunque puede pasar
directamente a un albarán o a una factura.

Para ello EneBoo permite en la edición del documento Importar las líneas del presupuesto, con lo
que se “ahorra” tener que introducir de nuevo las líneas.

Este proceso se realiza en Área de Facturación → Facturación → Presupuestos. Pulsamos el
botón que se encuentra arriba a la derecha Aprobar. Automáticamente el Presupuesto pasa a
Pedido. Este pedido puede ser modificado, incluyendo más líneas o con más datos del cliente.

Generar albarán / Generar factura

En el momento en que se envía el género al cliente, normalmente se genera el Albarán y para ello el

EneBoo i-SL Hoteles Enterprise

proceso denominado es igual que el caso anterior.

Dentro de Pedidos de Clientes, en la parte superior derecha, hay dos botones Generar Albarán o
Generar Factura. Puede hacer una factura directamente sin la necesidad de hacer un albarán, pero
en este caso generaremos un Albarán. Al pulsar este botón automáticamente se crea el albarán, el
cual podemos añadir o quitar las líneas que deseemos.

Facturar

Una vez introducidos los documentos (oferta, pedido o albarán), se puede generar la factura,
importando la información de cualquiera de estos documentos, incluso crear una factura con líneas
de los distintos documentos.

Nota: Al realizar el documento factura ya se generan los apuntes contables, por lo que no
habrá que entrar manualmente ningún apunte de facturas.

Este proceso lo hacemos de la siguiente manera.

Área de Facturación → Facturación → Albaranes de clientes

En la parte superior derecha hay un botón que indica Generar Factura, pinchamos y
automáticamente se genera la Factura. Al igual que los documentos anteriores las facturas también
pueden ser modificadas, incluyendo alguna línea más, etc...

Si observamos en la parte superior derecha también existe el botón Asociar. Este apartado sirve para
asociar el Pedido del que viene.

Almacén
Introducción

Eneboo permite gestionar de forma automática el control de sotck de sus artículos en tiempo real,
con la posibilidad añadida de trabajar con varios almacenes.

Para llevar esta gestión se realiza la entrada y la salida de artículos, mediante unos documentos que
aumentan o disminuyen el stock.

Entradas y Salidas

Para poder sacar el máximo partido a EneBoo hay que conocer perfectamente cómo reacciona cada
documento sobre el stock.

A continuación se detalla el efecto que producen las líneas de cada documento sobre el stock.
Documento Efecto sobre el stock Documento Efecto sobre el stock
Ofertas de venta No afecta stock Ofertas de compra. No afecta a stock
Pedidos de venta No afecta stock Pedidos de compra No afecta a stock
Albaranes de venta Disminuye stock Albaranes de compra Aumenta stock
Facturas de venta Disminuye stock Facturas de compra Aumenta stock

EneBoo i-SL Hoteles Enterprise

Los movimientos que se realizan al facturar los albaranes no implican ningún efecto sobre el stock,
ya que la actualización de éste se produce en el momento de la entrada/salida del albarán. La
factura, en este caso, denota la obligación en el pago de una mercancía ya entregada, pero no afectará
nuevamente al stock.

El stock de un almacén no puede modificarse en la ficha del artículo, sino que debe producirse un
movimiento en cualquiera de los documentos especificados. Por ejemplo, en el caso de que sea
necesario, porque el stock no cuadra con el stock real, se realiza una regularización.

Datos generales

Dentro de Almacén tenemos este apartado que sirve para indicar los datos por defecto que se
utilizarán en el programa, en este caso el IVA.

Familias y Subfamilias
En la Ficha de Artículos hay un campo que hace referencia a esta tabla, pudiendo asignar a cada
artículo la familia o subfamilia a la que pertenece.

Como ya hemos comentado anteriormente, la clasificación de los artículos en familias o subfamilias
puede resultar muy útil en el momento de realizar listados de artículos de cualquier tipo o en la
confección de tarifas.

Dentro de una familia puedes crear nuevos artículos.

Tarifas
Con EneBoo puede determinar un número ilimitado de tarifas de venta para cada uno de sus
artículos, calcularlas automáticamente y actualizarlas, de una forma rápida, cómoda y sencilla.
Nota: Las tarifas siempre tendrán preferencia sobre el precio de venta de la ficha del
artículo.

Almacenes

EneBoo nos permite trabajar con varios almacenes. Podemos asignar a cada artículo el almacén al
que pertenece.

Regularización de stocks

Las regularizaciones de almacén surgen con la necesidad de ajustar diferencias de stock detectadas
en el almacén para un artículo o una serie de ellos.

Al pinchar en Regularización de stocks aparecerá una lista de artículos a los que ya hemos
regularizado anteriormente y podemos modificar. De lo contrario pinchamos en nuevo, escogemos el
artículo a regularizar y vamos rellenando datos.

Insertamos la fecha y la hora, la cantidad nueva y en motivo hacemos una breve descripción para
identificar esta regularización.

EneBoo i-SL Hoteles Enterprise

Transferencias de stocks

En el caso de existir varios almacenes en este apartado podemos hacer traspasos de artículos de un
almacén a otro.

Control de horas de operarios

Este apartado nos permite dar de alta a los operarios en diferentes categorías y llevar un control de
las horas trabajadas. También podemos hacer el parte de trabajo de cada operario.

Principal

Desde este apartado podemos personalizar EneBoo e insertar todos los datos que usamos en
cualquier documento.

Cambiar Empresa

EneBoo nos permite gestionar tantas empresas como queramos.

EneBoo i-SL Hoteles Enterprise

Desde este apartado nos da la opción de cambiar a la empresa con la que queremos trabajar.
Ejercicios Fiscales

Desde aquí podemos sacar un informe de los movimientos de cada año. También podemos cerrar
ejercicios.

Series de Facturación

En el caso de que existan varias series de facturación, será en este apartado donde los demos de alta.
Impuestos

Aquí daremos de alta todos los tipos de IVA con los que trabajaremos.

Cuentas Bancarias

Este apartado es para dar de alta los números de cuenta de nuestra empresa.

Bancos

Este listado viene cargado por defecto con algunos bancos, pero si tenemos que dar de alta, también
podemos.

Descuentos

En este apartado podemos dar de alta todos los descuentos a aplicar a los clientes

Formas de Pago

Aquí se especifican todas aquellas modalidades con que se puede cobrar / pagar los efectos de la
tesorería. Por ejemplo, a 30 días, al contado, en 30-60 días, etc...

Tipos de Rappel

También podemos dar de alta tipos de rappel a aplicar a los clientes. Por ejemplo: Al alquilar más de
10 habitaciones, se aplicará un 10 % de descuento.

Agentes

Este apartado es para dar de alta todos los agentes comerciales de la empresa.

EneBoo i-SL Hoteles Enterprise

Liquidaciones a Agentes

Las comisiones se calculan automáticamente a partir de las tablas configuradas y dependiendo del
representante. Sólo se calculan a partir de las facturas a clientes.

Para que cuando entremos los documentos, la aplicación asigne la comisión automáticamente, hay
que configurar la tabla de comisiones y la del agente previamente.

Las comisiones son calculadas con la información del agente y con el porcentaje de las líneas de las
facturas.

Para la entrada de una tabla de comisiones habrá que seguir el siguiente orden:
* Dar de alta los Agentes de la empresa.
* Dar de alta las familias de clientes y artículos.
* Asignar cada cliente y producto a su familia correspondiente.

Al entrar una factura se asignará el representante de la ficha del cliente y, si existen tablas de
comisiones, en las líneas de las facturas se podrá ver que han sido asignados automáticamente.

Técnicos

En este apartado daremos de alta a los técnicos que realicen trabajos en nuestra empresa.

EneBoo i-SL Hoteles Enterprise

Usuarios

Aquí tenemos la lista de los usuarios con sus datos, de cada persona que trabaja con EneBoo.
Departamentos

En este apartado podemos dar de alta los distintos departamentos que existen en nuestra empresa.
Por ejemplo: Departamento de Dirección, Departamento de Administración...etc.

Grupos de clientes

Aquí podemos hacer grupos de clientes y aplicarles una tarifa específica, por ejemplo, Cliente
Habitual...

Divisas

Dentro de este apartado podemos dar de alta las distintas monedas con las que trabaja nuestra
empresa. EneBoo carga por defecto un listado de divisas.

Paises / Comunidades / Provincias

Al igual que en el apartado anterior, EneBoo carga por defecto una lista de Paises, Comunidades y
Provincias, pero si su empresa necesita dar de alta otro país, también puede hacerlo.

Agencias

Aquí podemos dar de alta las Agencias por las cuales nuestros clientes hacen las reservas.

Reservas y Ocupación

Este apartado sirve para llevar un control de la Ocupación de nuestro hotel, hostal o camping...Aquí
nos indica toda la información del cliente que ocupa una habitación, la planta, si es reserva o entrada,
etc...

Habitaciones de clientes

Aquí podemos ver todas las habitaciones del hotel, hostal o camping...y ver si están ocupadas. Desde
aquí podemos efectuar la salida del cliente de la habitación que tiene ocupada, automáticamente la
habitación queda libre.

Habitaciones

Este apartado sirve para sacar un informe al servicio de limpieza, en el que se indica si esta ocupada
la habitación, si está desocupada, etc...

Centros de Coste

Un centro de coste es todo departamento que cuente con un responsable y con un presupuesto. Una
empresa puede estructurarse en aquellos centros de costes que considere conveniente.

Para entenderlo mejor, pondremos varios ejemplos en el siguiente esquema.

EneBoo i-SL Hoteles Enterprise

Tesorería

Aquí tenemos todos los efectos de clientes, proveedores, listados...etc. En el caso de los efectos a
clientes podemos consultar, recibir, cobrar, devolver, etc...al igual que en proveedores.

Datos generales

Si no marcamos Pago indirecto de remesas: Al incluir un recibo de cliente en una remesa, el
correspondiente asiento de pago se asigna directamente a la subcuenta de la cuenta bancaria indicada
en la remesa.

Si marcamos Pago indirecto de remesas: Al incluir un recibo de cliente en una remesa, el
correspondiente asiento de pago se asigna a la subcuenta de Efectos comerciales con gestión de
cobro (E.C.G.C.) asociada a la cuenta bancaria de la remesa. Cuando se recibe la confirmación del
banco el usuario inserta un registro de pago para la remesa completa, que lleva las partidas de
E.C.G.C a la subcuenta de la cuenta bancaria.

Recibos a clientes

Esta opción permite tener el control de todos los recibos de nuestros clientes pagados, pendientes,
devueltos... El funcionamiento para los proveedores es exactamente igual.
EneBoo i-SL Hoteles Enterprise

Pagos múltiples de clientes

Este apartado sirve para agrupar varios recibos pendientes de un cliente en un solo recibo. Al igual
que en proveedores.

Remesas

EneBoo nos permite generar remesas de cobro de varios recibos de clientes.
Para generar nuevas remesas accedemos y pulsamos el botón “nuevo”. Aparece una ventana en la
que tenemos que indicar la fecha de la remesa y la fecha del cargo. Especificamos el banco y
seguidamente añadimos los efectos.

A continuación podemos generar el fichero para ser enviado al banco. Se dispone de la noma 19 y la
norma 58, en la parte superior-derecha se encuentran las dos opciones.

Pagarés de Proveedor

Aquí podremos insertar los pagarés que nosotros le hagamos a nuestros proveedores.

EneBoo i-SL Hoteles Enterprise

Área Financiera

Este apartado contempla todos los datos contables relacionados con la empresa, (asientos o apuntes,
cuentas, subcuentas...)

La función de los asientos es la de registrar todas las operaciones realizadas en la empresa.

Posteriormente permiten la realización del libro Diario, del libro Mayor, de los Balances, de
liquidación del IVA, etc...

En este apartado se puede consultar, modificar o dar de alta nuevos asientos en el diario. También
podemos sacar informes de la contabilidad de nuestra empresa.

La contabilidad en EneBoo se ha diseñado para que el usuario, cuando introduzca la información,
aunque no tenga nociones de contabilidad, ésta se genere sola. Por ejemplo, no necesita conocer
cómo se realiza el apunte de una venta o de un cobro, ya que al entrar la factura de venta o al cobrar
un vencimiento, se generará de forma automática el asiento contable correspondiente.

Estadística

Con los datos que iremos introduciendo en esta aplicación, en este apartado podremos sacar
información muy importante de la actividad de nuestra empresa.

Estadística

En este apartado podemos recolectar y analizar toda la ocupación hotelera que ha obtenido nuestra
empresa en un intervalo de fechas.

Ficha Policial

Los establecimientos hoteleros están obligados a confeccionar un impreso con los datos de todos sus
huéspedes mayores de 16 años: nombre, apellidos, lugar y fecha de nacimiento, residencia habitual,
número de pasaporte y lugar de expedición en caso de ser extranjero, firma y rúbrica. El hotel debe
hacer llegar a la comisaría de policía que le corresponda todas las fichas de registro dentro de las 24
horas siguientes al hospedaje del viajero.

Ocupación

Este apartado nos servirá para consultar el tanto por cien de la ocupación en el rango de fechas
marcado por nosotros.

Entradas y Salidas

Desde aquí podremos sacar dos clases de informes. Las entradas de clientes y las salidas. De esta
manera podemos llevar un control de las fechas en las que entran y salen los clientes.

Planing de Reservas

Este apartado nos permite sacar un cuadrante de las habitaciones que están reservadas, ocupadas o
libres.

EneBoo i-SL Hoteles Enterprise

Tipos de contrato

Podemos tener con nuestros clientes varios tipos de contratos periódicos y poder facturarlos según el
periodo determinado.

Contratos

En este apartado podemos generar las facturas de los contratos con nuestros clientes. Podemos
realizar tantas facturas como queramos en un solo proceso, en lugar de tener que hacerlas una a una.

Servicios a Clientes

En este apartado podemos anotar los servicios que ser le han realizado a nuestros clientes. Por
ejemplo: Guía Turístico, Lavandería, Actividades al aire libre... para después generar el Albarán y
seguidamente la Factura.

Cambiar de Ejercicio

Cuando estamos trabajando, siempre estamos trabajando sobre el ejercicio actual, ahora bien, si
queremos hacer cualquier consulta sobre ejercicios anteriores a continuación explicamos cómo
hacerlo.

Dentro de Facturación existe el apartado Cambiar de Ejercicio, aquí nos da la opción a cambiar de
año y consultar algún documento, como puede ser Presupuesto, Pedido, Albarán, Factura, etc...

EneBoo i-SL Hoteles Enterprise

Informes

Los informes sirven para sacar información especificada a partir de los datos introducidos en el
programa.

Podemos sacar un informe resumido o detallado, según la opción que elijamos, de cualquiera de los
datos, como por ejemplo, Facturas de un cliente en el mismo año.

Para ello abrimos el tipo de informe que queremos, en este caso Facturas de clientes, y pinchamos en
nuevo, rellenamos el cuadro con los filtros que queremos hacer, y guardamos. Después pinchamos en
la impresora y nos aparece el listado con los datos que hemos solicitado.

EneBoo i-SL Hoteles Enterprise

Área de recursos humanos

Principal

La administración de los Recursos Humanos, hace referencia al manejo, administración, gestión o
dirección del personal del negocio.

Y el área de Recursos Humanos, hace referencia al área, departamento o sección un negocio o
empresa, encargada de administrar los Recursos Humanos.

Como dueños del negocio, podemos nombrar un encargado o crear un área encargada de la
administración de los Recursos Humanos, sin embargo, existen funciones relacionadas a los
Recursos Humanos, que deben ser realizadas por nosotros y por todo trabajador que tenga personal a
su cargo, funciones tales como liderazgo, motivación o control.

Empleados

Desde este apartado podemos dar de alta todos los empleados que tenemos en nuestra empresa.
Dentro de la ficha de cada empleado podemos insertar los datos laborales, la formación...etc.

Candidatos

Aquí podemos introducir los curriculum que vayamos recibiendo para determinar el perfil de la
persona que necesitamos para cubrir el puesto que estamos ofreciendo.

EneBoo i-SL Hoteles Enterprise

Puestos de Trabajo

En este apartado iremos dando de alta todos los puesto de trabajo para que en la ficha del empleado
podamos asignarle el puesto de trabajo al que pertenece.

Tipos de Contrato

Al igual que en el apartado anterior daremos de alta Tipos de contrato para insertarlo en la ficha del
empleado. Por ejemplo: Temporal, Indefinido...

Nóminas

También podremos dar de alta las nóminas de los empleados y llevar un control de los meses que ha
cobrado, el importe...

Dietas

Daremos de alta las asignaciones que la empresa paga al trabajador cuando tiene que desplazarse o
viajar fuera del lugar donde se encuentra su centro de trabajo.

Estos desplazamientos producen una serie de gastos, como son los de transporte, comidas, y en caso
de tener que pasar fuera una o varias noches, gastos de alojamiento.

Área de Dirección

Análisis

Esta área lo denominamos “Business Intelligence”, se refiere al uso de datos en una empresa para
facilitar la toma de decisiones. Abarca la comprensión del funcionamiento actual de la empresa, bien
como la anticipación de acontecimientos futuros, con el objetivo de ofrecer conocimientos para
respaldar las decisiones empresariales.

Configuración

Desde aquí elegiremos la base de datos y los años a analizar.
Navegador

EneBoo i-SL Hoteles Enterprise

En este apartado podremos ir eligiendo los datos a analizar. Por ejemplo: Ventas por trimestre
En el eje X podemos poner por trimestre y en el eje Y artículos. Automáticamente nos aparecerá una
tabla con los datos solicitados.

Tenemos la opción de ver los resultados en diferentes gráficos.

EneBoo i-SL Hoteles Enterprise

Área de C.R.M.

El CRM (Customer Relationship Management) se refiere a la administración de todas las
interacciones que pueden tener un negocio y sus clientes.

Permite darle seguimiento a las actividades de los clientes, mejorar la efectividad de ventas,
proporcionar un mejor servicio al cliente y crear relaciones rentables con los clientes.

Infomes

En este apartado podremos sacar cualquier tipo de informe relacionado con el área del CRM.
Podremos sacar, previsiones de venta, Incidencias,...

Marketing

El marketing analiza la gestión comercial de las organizaciones, con el objetivo de retener y fidelizar
a los clientes a través de la satisfacción de sus necesidades.

Desde aquí podemos llevar un control de llamadas a clientes para dar información de nuevas
campañas.

Área de Colaboración

Gestión documental

La gestión documental permite rastrear y almacenar documentos electrónicos o imágenes de
documentos en papel y añadirlos a la ficha de cliente. Como por ejemplo: Contratos, copia del DNI,
etc...

Sistema

Desde aquí podemos administrar el control de acceso y los permisos a los usuarios.

EneBoo i-SL Hoteles Enterprise