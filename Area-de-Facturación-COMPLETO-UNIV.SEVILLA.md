* CREADO POR: [Universidad de Sevilla](http://www.us.es): Mariano Aguayo Camacho; Esther Chávez Miranda; Miguel Ángel Domingo Carrillo; Guillermo Molleda Jimena
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 13 de febrero de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Area-de-Facturaci%C3%B3n-COMPLETO-UNIV.SEVILLA)

----
#EN CONSTRUCCIÓN






##Sistemas de Información para las Finanzas y la Contabilidad

##                Curso 20  /20
***        yyy





###Tema 3. Sistemas ERP (Enterprise Resource Planning). Práctica Eneboo-FACTURACIÓN

###Parte I. El Sistema de Información empresarial y los Sistemas de Planificación de Recursos Empresariales (ERP). 

###Introducción.



En este apartado se analizarán los siguientes aspectos en relación con la aplicación Eneboo:

1. Arquitectura de Eneboo.
1. Explicación breve de los principales botones de la aplicación.

####Arquitectura de Eneboo:

* La aplicación ERP AbanQ se basa en la tecnología Cliente-Servidor, se trata realmente de un programa cliente de bases de datos que se instala en el ordenador del usuario. Podemos decir, por tanto, que AbanQ permite interpretar los datos pedidos al gestor de bases de datos instalado en el servidor, en nuestro caso PostgreSQL, utilizando el lenguaje SQL, para la posterior presentación al usuario de la información.

* En el siguiente gráfico se presenta un esquema del funcionamiento de AbanQ:


* Como se puede observar, la aplicación con el nombre flitte se ejecuta desde el cliente, de igual forma que con un navegador web y las páginas escritas en HTML, los datos son pedidos por la red utilizando el lenguaje SQL. Los módulos (metadatos) también son guardados como un dato más en la base de datos, de esa forma se evita tener que instalarlos en cada ordenador cliente, pues éstos cogen los módulos desde el mismo servidor. Así es muy fácil añadir nuevas funcionalidades al ERP y sean automáticamente utilizadas por todos los clientes.

* Por tanto, al iniciar AbanQ, éste descarga del servidor los módulos con sus instrucciones (los guarda y los renueva si existen nuevas versiones), y mediante la ejecución de estos módulos, el usuario va pidiendo y modificando los datos que necesite. En resumen, el programa AbanQ interpreta las instrucciones y datos llegados desde el servidor y presenta la información en el ordenador del usuario.

* La potencia de usar estándares como el lenguaje SQL, permite a esta aplicación funcionar con distintos gestores de bases de datos, así se podría conectar tanto a un servidor con PostgreSQL como con MySQL. En futuras versiones será compatible también con servidores Oracle SQL. Para más información sobre la tecnología que subyace en la base de AbanQ leer el documento sobre la Arquitectura Abierta de Aplicaciones Dinámicas (A3D) que se encuentra en http://abanq.org/documentacion/documento.php?ref=tutorial1.

*Explicación breve de los botones utilizados en el programa.*

* Aceptar los cambios e ir al primer registro (F5).
* Aceptar los cambios e ir al registro anterior (F6).
* Aceptar los cambios e ir al registro siguiente (F7).
* Aceptar los cambios e ir al último registro (F8).
* Aceptar los cambios y continuar con la edición de un nuevo registro (F9).
* Aceptar los cambios y cerrar formulario (F10).
* Cancelar los cambios y cerrar formulario (Esc).
* Insertar registro (A).
* Modificar registro (M).
* Eliminar registro (E).
* Ver registro (V).
* Copiar registro (C)
* Imprimir tabla (I)
* Seleccionar fecha (F2)

 Buscar valor en tabla relacionada

####Acceso y salida del programa

* Para entrar en el ERP ir a Inicio/programas/AbanQ. Se abrirán dos ventanas desde donde accederemos a la base de datos envoltosa con el botón Conectar. No usen en el nombre de la base de datos acentos, eñes, ni cualquier otro carácter extraño al idioma inglés, pues dará error.

* Recordamos que esta aplicación puede abrirse varias veces a la vez, y en cada una trabajar con una empresa diferente, simplemente eligiendo distintas bases de datos.


* Si la base de datos se ha creado con anterioridad (por ejemplo, para cargar los módulos) no aparecerá la ventana siguiente:


* Debido a la complejidad del sistema, AbanQ divide los subsistemas de la empresa en áreas y éstas, a su vez, en diversos módulos o funcionalidades. Las dos áreas con las que vamos a trabajar son Área de Facturación, desde la que se gestionan los aspectos relacionados con el aprovisionamiento y la gestión de ventas, y el Área Financiera desde la que se gestiona la contabilidad.



* Las restantes áreas o subsistemas de la empresa no los veremos ni utilizaremos en este manual.

###Personalización de la aplicación para la empresa Envoltosa

Veremos aquí cómo introducir los datos básicos de la empresa y los referentes a su fiscalidad.

#####Datos básicos de la empresa

La operativa normal de funcionamiento de este tipo de aplicaciones consiste en introducir en el sistema los datos básicos de la empresa. Para ello, accedemos al módulo Área de Facturación/Principal/Empresa donde crearemos la empresa Envoltosa. Al utilizar el programa por primera vez, cuando pulsamos en Área de Facturación/Principal se crea una empresa por defecto. Sustituiremos sus datos por los de EnvoltoSA.

* Carpeta: Datos generales.
* Código: 0. El código debe ser único para cada empresa.
* Nombre: ENVOLTOSA
* CIF/NIF: A-41147852
* Administrador: RAFAEL MUÑOZ OLIVE.
* Domicilio: SAN FRANCISCO, 4
* Población: SEVILLA
* Provincia: SEVILLA
* C. Postal: 41018
* Teléfono: 954100001
* Fax: 954100002
* E-mail: envol@micorreo.es
* Web: http://www.envoltosa.com



* Posteriormente, desde la opción Principal/Empresa, podemos modificar las características generales (pestaña General) y los valores por defecto (pestaña Valores por defecto) de la configuración básica de la empresa Envoltosa.

* Desde la segunda pestaña: Valores por defecto, activaremos la casilla de Contabilidad integrada y dejaremos desactivada la de Aplicar recargo de equivalencia. Recordemos que en este ERP, a diferencia de los programas independientes de un mismo proveedor, la contabilidad no está enlazada sino integrada. Además, activaremos la casilla Controlar stocks desde pedidos de clientes. 



* En esta misma pestaña de Valores por defecto vamos a introducir también el almacén de la empresa, al que denominaremos Almacén Calpe, con código AC, que al no estar creado pasaremos a darlo de alta con sus datos correspondientes: Una dirección postal y los datos de contacto. 
Para ello pulsaremos sobre el botón con una lupa a la derecha de la etiqueta “Almacén”. Esto mostrará la ventana “Almacenes” en la que podremos crear el nuevo almacén. 


* Para insertarlo pulsamos el botón  que nos permite acceder a la ventana e incluir información detallada sobre nuestro almacén.

* Daremos aquí de alta al único almacén que tiene la empresa, situado en Sevilla, polígono industrial Calpe, c/ A, nº 12.
* Cód. almacén: AC (AD si ya existiera AC)
* Nombre: Almacén Calpe.
* Dirección: Polígono industrial Calpe, nº 12.
* Población: Sevilla	Código postal: 41004
* Provincia: Sevilla	País: ES 
* Teléfono: 954 25 98 76. 
* Inventario valorado: Coste medio


* El Código Almacén permitirá identificar a éste en el resto del programa. Como puede observarse, el campo País aparece en forma de botón lo que nos está indicando que existe una tabla maestra asociada a este campo. Cuando ocurre esto debemos pulsar el botón e incluir y/o seleccionar la información en la tabla maestra correspondiente. En caso contrario, la información será incompleta y no se podrá utilizar de la misma forma. Por ejemplo, puede observarse que si se edita el campo país incluyendo la leyenda “ES” a su derecha no aparecerá la bandera de España y, sin embargo, si pulsamos el botón País y seleccionamos el país con código ES, sí que aparecerá.


* A la hora de valorar nuestro inventario podremos optar por una de las tres opciones siguientes:
Coste medio, Porcentaje del PVP o Coste del proveedor.
El programa indicará siempre este almacén en los documentos que se vayan añadiendo, de forma que no se tenga que teclear el código del almacén salvo que se vaya a utilizar otro.
Tras introducir los datos pulsaremos el botón aceptar [].


* Y pulsando en la ventana Almacenes en el botón  como aparece activado el registro correspondiente al Almacén Calpe, se incluirá el registro en el campo Almacén de la ventana Empresa.



* Para terminar la ejecución del programa es posible pulsar sobre el botón marcado con una X [ ] para cada ventana de los módulos abiertos, situado en la parte derecha de la barra de títulos, y finalmente en el botón Salir () de la ventana principal del programa. Si hiciéramos directamente esto último, sin cerrar cada una de las ventanas de módulos, la próxima vez que se inicie el programa seguirá todo abierto, es decir, como estaba al Salir del programa.
Para saber el nombre y la función de los botones, basta con mantener inmóvil el puntero del ratón sobre el botón deseado, durante unos segundos, para que aparezca un pequeño texto con su descripción.

#####Menú Fiscalidad
Área de Facturación>Principal/Fiscalidad

######Contenido de Fiscalidad:
* 1. Ejercicios fiscales
* 2. Series de facturación
* 3. Impuestos

Antes de comenzar a trabajar con nuestra empresa, es necesario configurar una serie de parámetros generales. Esto se consigue mediante las opciones del menú Fiscalidad, las cuales se analizarán a continuación.

* La primera opción del menú es la de Ejercicios fiscales. Por defecto, aparece creado el ejercicio correspondiente al ejercicio actual. 


* Pulsando el botón Modificar () en la ventana Ejercicios fiscales podemos ver sus datos.


* El campo Dígitos de subcuenta afecta a todas las subcuentas, que pasarán a codificarse por el valor indicado en este campo. El número de dígitos es un campo de cumplimentación obligatoria e indica la longitud de los códigos de las subcuentas en la empresa en cuestión. El valor deberá estar comprendido entre 5 y 15. Esta decisión es importante, ya que repercutirá en la manera en que se podrá obtener información relevante para el proceso de toma de decisiones. La decisión deberá basarse en las necesidades informativas y estadísticas que requiera la empresa en cuestión. Debe tenerse en cuenta que el programa asigna los cuatro primeros dígitos de cada subcuenta siguiendo el cuadro de cuentas establecido en el PGC.

*ATENCIÓN*: Una vez seleccionado el número de dígitos con el que trabajará su empresa, ya no podrá variar este parámetro, pues una vez creada esta opción se bloquea. Asimismo, influirá en la empresa con la que se trabajará en el próximo ejercicio, pues al tener la opción de generar el asiento de apertura del siguiente ejercicio a partir del cierre del ejercicio en curso, tampoco podrá variarse el número de dígitos de la contabilidad del año próximo.

* Ejemplo: Imaginemos que la empresa desea identificar a los clientes por provincias y que, en cada una de ellas, se estima que, como máximo, se atenderán a 99 clientes. Para poder atender este requerimiento, la codificación adecuada de las subcuentas será:







* Los cuatro primeros dígitos identificarán la cuenta de clientes del PGC (4300); los dos siguientes, la provincia: 28 (Madrid), 41 (Sevilla), 14 (Córdoba), etc. Los dos últimos, identifican al cliente: 1, 2, …99.
	43004106: cliente número 6 de Sevilla
	43001425: cliente 25 de Córdoba.

* Normalmente, el sistema de codificación de las cuentas de clientes y/o proveedores, o las de gastos e ingresos, serán los principales aspectos a considerar para determinar el número de Dígitos de subcuenta a utilizar, pero no olvidemos que ello afectará a todas las subcuentas.

* En el caso de que no se desee trabajar con 10 dígitos, que como hemos afirmado anteriormente es lo que AbanQ propone por defecto, debe editarse el campo Dígitos de subcuenta (véase imagen anterior) incluyendo el valor deseado. También puede realizarse desde el módulo Principal del Área Financiera, en el menú Ejercicio, seleccionando Cambiar actual y pulsando el botón Cambiar.

* Por otro lado, si editamos la pestaña Series, dentro de la ventana de Editar Ejercicio fiscal, podremos ver y modificar la numeración inicial de las facturas que se generarán en el programa (ver apartado Secuencias de documentos).



* Por tanto, en la imagen anterior podrá observarse el número que se le asignará a la siguiente factura emitida a clientes (nfacturacli) que aparecerá en la columna Valor sin bloqueo (irán incluyéndose automáticamente conforme se vayan creando los documentos). 

* Después de haber aceptado las ventanas anteriores (es decir, aceptamos y guardamos cambios en la ventana Editar Secuencias de Ejercicios y la de Ejercicios Fiscales), nos aparecerá el siguiente mensaje:



* Una vez Aceptado el mensaje seguiremos las indicaciones del programa y pulsaremos el botón Cuadro de cuentas que aparece en la esquina superior izquierda de la ventana Ejercicios Fiscales. 


* Hecho ésto aparecerá el siguiente mensaje que también aceptaremos:



* De esta forma se generará un plan de cuentas por defecto, según el PGC a la empresa Envoltosa, con una longitud por defecto de 10 dígitos para las subcuentas contables. 


* Una vez generado el Plan de Cuentas nos aparecerá un mensaje de confirmación.


* En caso de que esta operación ya se hubiese realizado con anterioridad, aparecerá el siguiente mensaje:



* La segunda opción de Fiscalidad es Series de facturación. Desde esta opción se definen las diferentes series con las que se trabajará en las facturas emitidas a los clientes y sus cuentas de ventas asociadas. 

* Si pulsamos en el botón  (Modificar registro) podemos ver el detalle de información relativa a la serie A de facturación creada por defecto por el programa. Como puede verse en la siguiente pantalla, la serie A está definida para facturas con IVA y no sujetas a IRPF.

* Podrían crearse otras series, como por ejemplo una específica para las facturas rectificativas (relacionada con la devolución de mercancías y/o modificación de facturas) con la descripción “Rectificación de la factura nº”, pero por ahora, aceptamos la serie A que viene por defecto.

* Como puede observarse el campo Cuenta de ventas aparece en blanco. Para incluirla, pulsamos el botón  que nos dará acceso a la tabla maestra de Cuentas.

* En el campo Buscar indicaremos la cuenta 700 (de ventas) y, 

una vez localizada la seleccionaremos y cerraremos el formulario.
* El resultado aparece en la siguiente imagen.


* Igualmente, podríamos crear tantas series de facturación como se consideren necesarias aplicándoles, si procede, la retención o activar-desactivar la opción Sin IVA. 



* Antes de volver al menú Fiscalidad, debemos continuar con la configuración de los modelos tributarios de EnvoltoSA. Para eso, podemos buscar en la ventana del Área de Facturación el menú Módulos y, dentro de éste, señalar Área Financiera>G:Modelos, o bien, minimizar o cerrar la ventana del Área de Facturación y en la ventana AbanQ, hay que acudir al Área Financiera y al Módulo Modelos. Al entrar en él, AbanQ pide de forma automática que se configuren los modelos tributarios.



* En esta pantalla no hay que rellenar nada, por lo que pasamos a la pestaña Modelo 347, en la cuál hay que especificar la cuenta que se va a utilizar en las operaciones bancarias con la Hacienda Pública. 



* Para ello, hacemos clic en Cod. Cuenta efectivo y accedemos a la tabla Cuentas Bancarias. En esta opción, a la que también podemos acceder desde el Área de Facturación en el menú Tablas Generales /Cuentas bancarias, añadiremos los datos de las cuentas bancarias con las que trabaja normalmente nuestra empresa, y que también se utilizará para la realización de pagos a nuestros proveedores, se recogerán las remesas de los recibos de nuestros clientes, entre otros datos. 


* Se dará de alta, pulsando el botón Insertar Registro, la cuenta bancaria de EnvoltoSA con el código que el programa ofrece por defecto (000001 ó 000002 si ya existiera la anterior) y la descripción C/C Banco Zaragozano, además de los siguientes datos identificativos. 



* En el caso de que aún no hayamos dado de alta la sucursal que solemos utilizar de nuestra entidad bancaria en la opción Bancos, podremos hacerlo en esta ventana desde el botón  en el campo Oficina Nº. Al añadir alguna oficina los datos que se preguntan son las habituales, pudiendo incluirse también el nombre de una persona de contacto y algunos comentarios, lo que será útil para mantener un contacto personalizado. Obviamente, el dar de alta aquí a distintas sucursales sólo será útil si éstas se van a emplear más adelante más de una vez, ya que, en otro caso, no habrá ahorro de trabajo. 


* Una vez incluidos los datos de la Sucursal Aceptamos los cambios y vamos cerrando el formulario hasta llegar a la ventana de Insertar Sucursales donde continuamos incluyendo la información del campo Cuenta (0000102147).

* Posteriormente, en el apartado de Contabilidad debemos indicar las subcuentas contables que utilizará el programa para generar automáticamente los asientos en los que se realicen pagos o cobros por esta entidad pues, como puede recordarse, al crear la empresa enlazamos la facturación con la contabilidad. Así, por ejemplo, si realizamos un pago de una factura a proveedores indicando como Cuenta Bancaria de pago la 001, siempre que hayamos definido correctamente con antelación las subcuentas contables asociadas, el programa registrará automáticamente el asiento contable de pago.
* Para incluir el dato Subcuenta (referido a la subcuenta contable que asignaremos a nuestro banco) deberemos pulsar el botón  y, dado que es una cuenta específica de banco, pulsaremos en Insertar Registro porque no aparecerá dada de alta1. 


* Una vez incluida la subcuenta de banco aceptamos los cambios y seleccionamos el registro para incorporarlo en el formulario de Insertar Cuentas Bancarias.
Para insertar la subcuenta de Efectos comerciales en gestión de cobro, volvemos a pulsar sobre el botón  que nos trasladará hasta la ventana de Subcuentas. En este caso buscaremos la subcuenta (es suficiente con incluir los primeros cuatro dígitos en el cuadro de edición del apartado Buscar, esto es, 4312) y después la seleccionaremos para que se incluya en el formulario de Cuentas Bancarias. 


* Una vez incluida toda la información correspondiente para insertar nuestra cuenta bancaria el formulario quedaría de la siguiente forma:


* Código: 000001 (0 000002)	Descripción: C/C BANCO ZARAGOZANO 
* Entidad bancaria: 0103 (Banco Zaragozano)
* Oficina nº: 0182 (ó 0183 si ya existiera) (Nombre: Nervión. Dirección: Avda. Buhaira, 2, 41018 – Sevilla – País: ES .
* Contacto: Contacto: Julián Amores Soto, teléfono 954 214 541, fax: 954 214 542)
* Entidad 0103 – Oficina 0182 – Dígitos de Control 74 – Cuenta: 0000102147
(CCC: 0103/0182/74/0000102147)

* En el apartado subcuentas introduciremos: en el campo Subcuenta contable: 572.1 del Banco Zaragozano. Cómo aún no se ha creado habrá que darla de alta (crear la 572.2 si ya existiera la 572.1). Una forma de hacerlo es pulsando sobre el botón  que se encuentra en la sección Contabilidad. Una vez en la ventana de Subcuentas se pulsa sobre Insertar registro y se introducen los datos (cuenta 572, código 572.1, descripción Banco Zaragozano). En el campo Efectos comerciales gestión de cobros el código 4312.0 que no es necesario crear (pueden buscar en las subcuentas, por descripción, el texto “%gestión de cobro” y aparecerá la 4312.0 para seleccionarla).

* Después hay que completar los porcentajes de las casillas del modelo incorporando los nuevos tipos del IVA (General del 21%, Reducido del 10%). El formulario quedará como se presenta en la siguiente imagen. 




* Una vez completada la configuración de los Datos fiscales continuamos con la configuración del menú Fiscalidad del Área de Facturación.

####La tercera opción de Fiscalidad es Impuestos.

Por defecto, el programa ya tiene configurado tres códigos de IVA, uno para el IVA general del 18%, otro para el reducido del 8% y un tercero para el superreducido del 4%. (Se debe a que estamos trabajando con una versión del año 2012, pues la del 2013 dio problemas al instalarla).

* Por regla general, en los programas de facturación no se trabaja con los porcentajes de IVA directamente en las facturas; es decir, éste no se indica expresamente como un número, sino que se establecen una serie de tipos de IVA generales, cada uno con su porcentaje y recargo de equivalencia correspondiente, que son los que se aplicarán en las facturas. A cada artículo le corresponde un tipo de IVA determinado, que se le asigna cuando se da de alta a dicho artículo. Esto se hace porque los diferentes tipos de IVA son los establecidos legalmente en función del tipo de bien o servicio que se trate, y éstos no se deben cambiar.

* En esta opción de Impuestos se especifican los distintos tipos de IVA que se van a utilizar en el programa. Para añadir o modificar un tipo de IVA, se nos piden los siguientes datos: Código, se refiere a una serie de caracteres alfanuméricos con el que se identificará a este tipo de I.V.A. en el resto del programa; Descripción; % I.V.A., el porcentaje utilizado en este tipo; y % Recargo, que se refiere al porcentaje de recargo de equivalencia que lleva asociado el tipo de IVA que estemos dando de alta. Aceptaremos todos estos datos por defecto.

*ATENCIÓN*: Si se cambia el porcentaje de un tipo de I.V.A., éste se modificará también en las facturas ya creadas. Para evitar los errores que puede ocasionar esta forma de operar, debemos utilizar la pestaña “Periodos” de forma que podamos registrar las modificaciones en los porcentajes de IVA (por ejemplo, cambio del 18% al 21%) asociados a un mismo tipo de IVA (por ejemplo, IVA General) como resultado de cambios normativos que serán de aplicación durante parte de un ejercicio económico (por ejemplo, subida de IVA en facturas a partir del 01/09/2012).
En este caso, los porcentajes del impuesto se indican en la pestaña

* Comenzamos, por tanto, a incluir los distintos tipos de IVA comenzando por el IVA General. Para ello, como puede recordarse, accedemos al Área de Facturación> Módulo Principal>menú Fiscalidad> Impuestos.


* Ya que para contabilizar las facturas recibidas por parte de nuestros proveedores Hacienda permite un tiempo máximo de 4 años, dejaremos los tres tipos que aparecen por defecto, con sus porcentajes correspondientes, aunque no le asignaremos en este momento subcuentas contables. Como puede observarse aparecen dados de alta los tres tipos de IVA: general, reducido y superreducido. 

* A continuación daremos de alta el código IVA21 e IVA10. Habrá que indicar los porcentajes de IVA y de recargo de equivalencia asociados.
* Código IVA
* Porcentaje IVA
* Porcentaje Recargo de Equivalencia
* IVA21
21
5.20
* IVA10
10
1.4

* A continuación insertaremos un período para indicar que ese IVA21 se utilizará desde el 01-01-2013 hasta el 31-12-2013  y que los porcentajes de IVA y de Recargo de Equivalencia son del 21 y del 5.4, respectivamente. Haremos lo mismo con el IVA10.

* Una vez aceptemos los cambios la ventana quedará tal y como se indica en la figura siguiente:



* Asimismo, habrá que definir las correspondientes subcuentas contables de IVA repercutido y soportado, que aún no están dadas de altas en el PGC. Para ello editaremos los dos códigos de IVA y daremos de alta obligatoriamente las correspondientes subcuentas contables en el plan de cuentas.

* Aunque no es obligatorio, suele contabilizarse cada cuota de IVA tanto repercutido como soportado en una cuenta específica para cada tipo y naturaleza del IVA. Ello es extremadamente útil a la hora de encontrar posibles descuadres entre los libros registros de IVA, los mayores de la contabilidad y las declaraciones automáticas facilitadas por los programas. En nuestra empresa, consideraremos tan sólo una diferenciación en base a los tipos impositivos, sin tener en cuenta las distintas naturalezas del IVA. En base a ello, distinguiremos las siguientes cuentas: 

* 472000010: para recoger las cuotas deducibles al 10%.
* 472000021: para recoger las cuotas deducibles al 21%.

* 47700010: para recoger las cuotas devengadas al 10%.
* 47700021: para recoger las cuotas devengadas al 21%.

* Vamos entonces a proceder a dar de alta los distintos tipos de IVA. En primer lugar lo haremos con las compras (pestaña Contabilidad (compras)) 472.21 (o 472.10) (notación abreviada de la subcuenta 4720000021 o 4720000010) asignándoles a cada una de ellas el Tipo de cuenta Especial IVASOP, el código de IVA correspondiente y el modelo 303 donde van a figurar.


* Pulsamos el botón Buscar en el apartado de IVA Soportado y, después, el botón Insertar Registro en la ventana de Subcuentas, incluyendo la información de la subcuenta 472.21 con la descripción  H.P. IVA SOPORTADO AL 21%:

* Al tratarse de una cuenta especial pulsamos el botón Buscar y usamos el código IVASOP.

* Una vez incluida la información en el apartado Subcuenta, hay que pulsar en la pestaña Otros datos > IVA para seleccionar el tipo de IVA.

* A continuación, accedemos a la pestaña Modelos para indicar las casillas de enlace con el modelo 303.





* Una vez hecho esto, aceptamos los cambios realizados hasta llegar a la ventana de Editar Impuestos en la que pulsaremos la pestaña Contabilidad (ventas):


* Cuenta: 472
* Código: 472.21
* Descripción: HP IVA SOPORTADO 21%
* Tipo Especial: IVASOP
* Otros Datos:
* I.V.A.: IVA21
* Modelos: 
* Casillas: [22]-[23]

* En segundo lugar lo haremos con las de ventas, las subcuentas 477.21 (ó 477.10) y Tipo de cuenta Especial IVAREP. En la ventana de edición del GEN (ó RED), seleccionen la pestaña Contabilidad (Ventas), pulsen la lupa de I.V.A. Repercutido (véase en Imagen anterior). Quedaría de la siguiente forma:






* Cuenta: 477
* Código: 477.21
* Descripción: HP IVA REPERCUTIDO 21%
* Tipo Especial: IVAREP
* Otros Datos:
* I.V.A.: IVA21
* Modelos: 
* Casillas [01]-[09]: IVA DEVENGADO- RÉGIMEN GENERAL

* En la misma ventana de Editar Impuestos, a continuación incluiremos las subcuentas H.P. deudor por IVA (470.0) e I.V.A. Repercutido Exento (477.0) –en la pestaña Contabilidad (compras)- y H.P. acreedor I.V.A (475.0) –en la pestaña Contabilidad (ventas). 
Es importante anotar que aunque estas subcuentas aparecen incluidas en la tabla Subcuentas es necesario que se asocien a cuentas especiales de IVA para que el programa opere correctamente. Si no se modifican las mismas para incluir las cuentas de tipo Especial cuando vayamos a grabar la información nos saldrá un mensaje indicándonos que lo hará el programa de forma automática.




* Procedemos por tanto a incorporar la información necesaria. Desde la pestaña Contabilidad (compras) en la ventana Editar impuestos pulsamos el botón de Buscar que aparece en el campo H.P. Deudor I.V.A. y aparecerá la ventana de Subcuentas donde buscaremos la subcuenta utilizando el código 47 :

* En la ventana de Subcuentas pulsamos en Modificar Registro y aparecerá:




*ATENCIÓN*: En el caso de que sólo se teclee en el campo correspondiente los dígitos de la subcuenta y no se hayan dado de alta en la contabilidad no se generará correctamente ningún asiento contable asociado a ellas.



###Área de Facturación.

Tablas generales
Área Facturación>Principal/Tablas Generales

* Contenido de Tablas Generales:
1. Cuentas bancarias
1. Bancos
1. Descuentos
1. Formas de pago
1. Tipos de Rappel
1. Agentes
1. Liquidaciones de agentes
1. Departamentos
1. Usuarios 
1. Grupos de clientes
1. Divisas
1. Países
1. Provincias

* Ya tenemos creada y seleccionada nuestra nueva empresa, pero antes de poder trabajar con ella es necesario añadir una serie de datos iniciales, sin los que no se podrá trabajar: formas de pago, cuentas bancarias, etc. Para ello se utiliza, entre otros, el menú TABLAS GENERALES y el menú PRINCIPAL del módulo Principal en el Área de Facturación. Comenzaremos dando de alta los datos que se solicitan en TABLAS GENERALES, ya que son necesarios para crear luego las fichas de clientes y demás.

#####Cuentas bancarias.

La primera opción de Tablas Generales es la de Cuentas bancarias, desde donde añadiremos los datos de las cuentas bancarias con las que trabaja normalmente nuestra empresa, tanto desde donde se harán los pagos a nuestros proveedores como donde se recogerán las remesas de los recibos de nuestros clientes. Esta opción ya la hemos estudiado con anterioridad al tratar la configuración de los modelos fiscales.


#####Bancos

La segunda opción de Tablas generales es Bancos, donde observaremos que el banco con el que trabaja la empresa, el Zaragozano ya está creado por defecto. En esta opción se podrán dar de alta además las sucursales de dichos bancos donde se recogen las cuentas con las que se trabajará en el programa, tanto las de Envoltosa como las de sus proveedores y clientes. Demos de alta a CajaSol con el número 2106.

Consultamos la sucursal incluida anterioremente de nuestra entidad el Banco Zaragozano:



#####Descuentos

La tercera opción de Tablas generales es Descuentos, se aplicará tanto para registrar los aplicables a clientes como para los que nos aplican los proveedores. Introduciremos los 2 tipos de descuentos: uno para los clientes mayoristas, con el código A (C si ya existiera) del 7% y otro para los clientes minoristas, con el código B (D si ya existiera) del 4%.



#####Formas de pago

La cuarta opción de Tablas generales es Formas de pago, desde donde introduciremos las 3 formas de pago que viene utilizando la empresa, tanto para el cobro a los clientes como para el pago a sus proveedores.

* Las formas de pago se utilizan en el programa para generar los recibos necesarios al registrarse una factura, tanto de proveedores como de clientes. Los recibos generados se gestionan en el módulo tesorería del área de facturación. En cada recibo se indica la cantidad y la fecha en que ha de pagarse y se entregan al cliente junto con la factura, para recordárselo. El hecho de entregar el recibo no significa que esté pagada la deuda, ésto sólo será así cuando el recibo sea pasado al estado de Pagado.


* Para insertar una nueva forma de pago es necesario pulsar el botón Insertar registro. La ventana de creación incluye la información común de los recibos a generar. Lo primero que se pide es un código, con diez caracteres como máximo, la opción generar recibos con el texto Emitido o Pagado (esta última opción sólo debe emplearse con pagos al contado), la descripción de la forma de pago, la cuenta bancaria y su descripción, la cual lleva enlazada la subcuenta contable en la que se contabilizarán los asientos para el pago o el cobro de la factura que utilice esta forma de pago, si se deja en blanco se utiliza la caja (57.0).


* También aparecen las siguientes opciones: Pago por domiciliación y Ajuste a meses completos. El primero de ellos debe activarse en caso de que se desee que al imprimir la factura aparezca la cuenta bancaria del cliente y el segundo si se desea que los recibos que se generen calculen su vencimiento por meses exactos cuando su periodicidad en días sea un múltiplo de 30, tanto en el primer recibo como en los posteriores. 
Supongamos el siguiente caso: una factura emitida el 26 de noviembre, se debe pagar en tres plazos; el primer recibo a los 20 días (se contarán a partir del día siguiente de la emisión del recibo) y los dos restantes a 30 y 60 días después de realizar el primer pago.

*Solución:* 

A) Si no se activase la casilla Ajuste a meses completos, el programa haría lo siguiente:

* Fecha emisión factura
* Primer pago
* Segundo pago
* Tercer pago
* 26 de noviembre
* 16 de diciembre (+20días)
* 15 de enero (+30d)
* 14 de febrero (+30d)

B) Si se activase la casilla Ajuste a meses completos, el programa haría lo siguiente:

* Fecha emisión factura
* Primer pago
* Segundo pago
* Tercer pago
* 26 de noviembre
* 16 de diciembre (+20días)
* 16 de enero (+1 mes)
* 16 de febrero (+1 mes)




* En el ejemplo para explicar la casilla de meses completos, los datos de la práctica serían:

Código: MC	Descripción: Un pago a los 20 días, y dos a los 30 y 60 días tras el primero. 


* Tras esto y después de pulsar sobre el botón Insertar registro de la sección Plazos viene un cuadro que nos permite seleccionar entre Porcentual, Número de plazos e Importe fijo.
* De esta forma, incluimos la información:
Tipo Número de plazos
Días aplazados: 20 	Número de plazos: 3 	Cadencia en días: 30



* Existen unos condicionantes para elegir una u otra forma de pago, pero no siempre son excluyentes, hay ocasiones en que es factible usar tanto el tipo Porcentual como el de Número de plazos. Estudiémoslo:

* Porcentual: Si queremos que se genere un número prefijado de recibos podemos elegir la opción Porcentual el programa nos permite indicar cuantos días se aplaza el vencimiento de cada recibo respecto a la fecha de factura, no respecto a la fecha de vencimiento del recibo anterior y qué porcentaje del importe total. El resto de campos aparecen desactivados.

* Pongamos un ejemplo para aclarar el funcionamiento del programa y evitar cometer un error a la hora de su uso. Supongamos que deseamos dar de alta una forma de pago (código: 50) consistente en dos pagos, el primero a los 30 días desde fecha de emisión de factura por el 50% de la deuda y el segundo pasados 20 días desde la fecha de vencimiento del primer recibo (Descripción: Vencimiento a los 30 y 50 días). 

* Lo correcto sería indicar dos pagos porcentuales. En Días aplazados del primer recibo 30 y % Aplazado 50 y 50 en días aplazados segundo recibo y % Aplazado 50.





* Lo incorrecto sería si indicáramos 30 en Días aplazados primer recibo y 20 en Días aplazados segundo recibo, el programa reordenaría los recibos, entendiendo que el primer pago se hace a los 20 días desde fecha de emisión de factura y el segundo a los 30 días desde fecha de emisión de factura, por lo tanto estaríamos definiendo una forma de pago distinta a la descrita anteriormente.



* Número de plazos: Si queremos obtener un número de recibos predeterminado, todos sus vencimientos separados con la misma distancia temporal (sin contar el primer vencimiento respecto de la fecha de factura) y todos por el mismo importe (mismo porcentaje del total); entonces podemos elegir la opción Número de plazos para crear todos los recibos por el importe resultante de dividir el importe total de la factura entre el número de plazos indicado en el campo correspondiente. En el campo Días aplazados se recoge el tiempo que transcurrirá desde la fecha de emisión de la factura hasta el vencimiento del primer recibo. En el campo Número de plazos indicaremos cuántos recibos se generarán hasta sumar el total de la factura. En el campo Cadencia en días se indicará el tiempo que debe transcurrir entre dos recibos consecutivos.


* El tipo Número de plazos casi siempre puede realizarse como tipo Porcentual, pero si queremos obtener 20 recibos con un 5% de importe cada uno, es más rápido y elegante hacerlo con Número de plazos que con tipo Porcentual.

* Existen otras razones para preferir el tipo por plazos al porcentual, así si en el ejemplo de los meses completos hubiéramos utilizado el tipo Porcentual, sería imposible ajustar los vencimientos a meses completos ya que el programa no detectaría ningún múltiplo de 30 en los días aplazados.

* Realicemos, entonces, otra práctica con los datos que figuran a continuación:

Código: MCP 	Descripción: Un pago a los 20 días, y dos a los 30 y 60 días tras el primero. 

* Eligiendo Tipo Porcentual
33.33% a los 20 días	33.33% a los 50 días (20+30d)	33.34% a los 80 días (20+60d)


* Si elegimos, al insertar los Plazos, el Tipo Número de plazos (insertar con el código MC2 e igual descripción que el anterior).
Días aplazado: 20 días, Número de plazos: 3 plazos, Cadencia: 30 días (aquí la casilla meses completos sí funcionaría).



* Importe fijo: En caso de que queramos definir el importe monetario exacto de cada recibo, activaremos la opción Importe fijo; el programa creará los recibos necesarios hasta que se complete el total de la factura, teniendo todos ellos la cantidad indicada en el campo Importe fijo. Para evitar que pueda suceder que el último recibo sea por una cantidad muy pequeña en el campo Importe mínimo podemos indicar la cantidad mínima que puede tener el último recibo, en caso de no llegar a este importe mínimo, se sumará dicha cantidad al recibo anterior, el cual se convertirá en el último de todos.


* Ejemplo: Si queremos dividir el pago en mensualidades de 100 euros, con un recibo mínimo de 20 euros, los campos tendrían los siguientes valores:

* Código: IF100; Descripción: Importe Fijo 100 euros/mes. Tipo: Importe fijo, Días aplazados: 30, Cadencia: 30, Importe fijo: 100, Importe mínimo 20.


* Si nos hacen una compra por un importe de 215 euros usando esta forma de pago, los recibos serían dos: uno de 100 euros a los 30 días y otro de 115 euros a los 60 días. Los 15 euros se han sumado al segundo recibo porque no llegaban a los 20 euros que se requerían para emitir un nuevo recibo.

* Ahora vamos a dar de alta una forma pago sencilla, que consiste en generar un único pago con vencimiento a los 30 días de la fecha de emisión de la factura. Esos 30 días no son naturales. Si ya existe el código 30, escriba 30B. (Truco: En el campo Cuenta pulsar F4 para que se autocomplete.)


* Otra posibilidad sería utilizar el tipo por Número de plazos, al ser un solo pago el campo cadencia no tiene uso, pudiéndose dejar en blanco o con cualquier número:



* 30 (ó 30B). VENCIMIENTO A 30 DÍAS. Debe elegirse la opción Generar recibos como emitidos. Cuenta bancaria Banco Zaragozano y activar Ajuste a meses completos. Es un pago único, por lo que podemos elegir Porcentual e introducir días aplazados: 30 y % aplazado: 100%. Al tener plazos del mismo importe (uno sólo) y misma distancia temporal entre plazos (al no haber más plazos es indiferente), también podría elegirse número de plazos: 1 y días aplazados 30, la cadencia no importa por la ausencia de recibos posteriores.

* 60 (ó 60B). VENCIMIENTO A 30 y 60 DÍAS. Debe elegirse la opción Generar recibos como emitidos. Cuenta bancaria Banco Zaragozano y activar Ajuste a meses completos. Al ser plazos del mismo importe y con la misma distancia temporal podemos elegir el tipo Número de plazos: Días aplazados: 30, número de plazos: 2 y cadencia o distancia temporal para sucesivos recibos: 30. Se podrían haber creado dos plazos de tipo Porcentual, pero sería menos elegante, pueden intentarlo para comprender mejor el funcionamiento.



* Modificar CONTADO. Debe elegirse la opción Generar recibos como pagados. DEJAR EN BLANCO el campo Cuenta bancaria. De esta forma el programa asignará la subcuenta de Caja, euros (57.0) por defecto a la hora de registrar el asiento contable. 


* FIJO60. En cada recibo se pagarán 60€ hasta que se abone el total de la deuda. Como descripción de la forma de pago anotaremos: IMPORTE FIJO DE 60€. Debe elegirse la opción Generar recibos como emitidos. Cuenta bancaria Banco Zaragozano. En caso de que el último recibo sea inferior a 10€, se desea que este importe se sume al del recibo anterior. El primer recibo se exigirá a partir de los 30 días de su emisión y los demás cada 30 días.

* Una vez realizada la práctica la ventana de Formas de pago quedaría de la siguiente forma:


#####Tipos de Rappel

La quinta opción de Tablas generales es Tipos de Rappel, desde donde introduciremos los rappels aplicados por la empresa a sus clientes. Los rappels son descuentos que se aplican a los clientes si llegan a un determinado volumen de ventas prefijado por el usuario, definidos con límite de unidades monetarias. Para definirlos es necesario introducir un código identificativo, un límite inferior y otro superior y un porcentaje de descuento. Es posible indicar, en “Intervalos”, un descuento distinto a volúmenes de compra diferentes. 

* El tipo de rappel aplicable a cada cliente se especificará en la tabla de clientes.

* Los importes de los rappels no aparecen en las facturas de los clientes. En su lugar, hay que obtener una Liquidación de rappels a clientes existiendo un módulo específico para realizar tal liquidación, módulo del que carecemos.

* Para los clientes mayoristas aplicaremos el código 1 y la descripción “Rappel Mayoristas”.
Limite inferior: 2.000. Límite superior: 6.000. Descuento: 1%.
Limite inferior: 6.000.01. Límite superior: 30.000. Descuento: 3%.
Limite inferior: 30.000.01. Límite superior: 99.999.999.999. Descuento: 5%.

* Para clientes minoristas aplicaremos el código 2 y la descripción “Rappel Minoristas”.
Limite inferior: 200. Límite superior: 600. Descuento: 0,5%.
Limite inferior: 600,01. Límite superior: 3.000. Descuento: 2%.
Limite inferior: 3.000,01. Límite superior: 99.999.999.999. Descuento: 4%.



#####Agentes comerciales

La sexta opción de Tablas generales es Agentes comerciales, desde donde introduciremos los datos del comercial de la empresa.

Los agentes comerciales son profesionales que facilitan las ventas a determinados clientes, motivo por el que se llevan una comisión por cada venta que hacen. Estas comisiones se van acumulando, para periódicamente pagarles con una liquidación. Al dar de alta a los clientes se les asigna, en caso de que lo tengan, un agente comercial. Por este motivo vamos a explicar ahora cómo añadir agentes comerciales, antes de pasar a los clientes.

La ventana de Agentes Comerciales contiene varias secciones. En la sección Agente se pide un código (si ya existe el 1 escriban 1B), el nombre, apellidos y el DNI. En la sección Condiciones se pide la comisión que cobra, el departamento al que se adscribe y el porcentaje de retención del IRPF que se le aplicará en sus liquidaciones. La sección Dirección para introducir su dirección personal y finalmente un campo Proveedor que explicaremos más abajo.

Agente:
Código 1 (ó 1B). DNI/CIF: 47887447-K
Apellidos: LÓPEZ RODRÍGUEZ
Nombre: MANUELA
Condiciones:
% Comisión: 5	% I.R.P.F.: 15
Departamento: 000001	Nombre: COMERCIAL
Dirección:
Dirección: C/ DUCADO, 21
Ciudad: SEVILLA	Código postal: 41006
Provincia: SEVILLA
País: ES
Proveedor: (crear uno nuevo), Cuenta contable: 4100.101
Serie: AG (dar también de alta en el ejercicio fiscal)



Todos los agentes recibirán un 5% en concepto de comisión por la venta de nuestros productos Y SE LES RETIENE UN 15%.

Es necesario dar de alta el Departamento comercial al que pertenece el agente (si ya existiese, créenlo de nuevo con el código 000002).



Al final tenemos el campo Proveedor, el cual sirve para asociar al agente con un número de subcuenta contable y facilitar otras funcionalidades necesarias (cuenta corriente donde pagarle, gestión documental, subcuenta bancaria, etc.)

El caso es que, a efectos de su gestión en AbanQ, un agente se gestiona como un proveedor (de servicios - acreedor), ya que nos presta el servicio de buscar o atender clientes; por ello el programa en lugar de duplicar todo lo relativo a proveedores para los agentes, pues nos hace crear una ficha de proveedor al agente aunque esto suponga la inserción de algunos datos por duplicado (nombre, DNI, domicilio), permitiendo asociar a los agentes todas las funcionalidades creadas para los proveedores (gestión documental, mayor de la subcuenta contable, etc.)

Hay que tener cuidado al dar de alta al agente como proveedor, pues el programa por defecto asocia en las fichas de proveedores una subcuenta contable 4000.X en lugar de la que le corresponde como cualquier prestatario de servicios (4100.X). Por ello, debemos modificar la subcuenta antes de que se cree en la contabilidad. 

Para hacer la práctica, en la ventana en la que estamos incluyendo el Agente Manuela (Editar Agentes Comerciales) en la esquina inferior izquierda aparece el campo Proveedor. Para insertar a Manuela en la tabla de Proveedores pulsamos sobre el botón Proveedor y después, en la ventana de Proveedores pulsamos en Insertar registro. Una vez aquí, lo primero que haremos es cambiar el número de subcuenta asignado al agente. Para ello accedemos a la pestaña Contabilidad.

Como puede observarse en la imagen, y como comentábamos anteriormente, en el campo Subcuenta de esta pestaña (Contabilidad) aparece la Subcuenta 400.1, cuando debería aparecer una cuenta del grupo 410. Para asignarle a Manuela su subcuenta, pulsamos la lupa, en este campo, y cuando accedamos a la tabla de Subcuentas pulsamos el botón Insertar registro.
Asignaremos a este agente a la cuenta 410 y la subcuenta 4100.101.

Esta subcuenta se utilizará para contabilizar automáticamente las liquidaciones del agente cada vez que registremos una factura por sus servicios. Una vez aceptados los cambios y cerrados los formularios la pestaña de Contabilidad quedaría como aparece en la siguiente imagen.


A continuación, pulsamos en la pestaña General para introducir un nuevo código para el agente (000101)2 el nombre, y NIF del Agente. IMPORTANTE, se debe incluir sólo la información especificada.


Luego pasamos al apartado Subcuentas por ejercicio (en la pestaña Contabilidad de la ventana Insertar Proveedores), en el cuál asignaremos la cuenta que acabamos de crear para los ejercicios fiscales dados de alta en el programa. Lo haremos pulsando el botón  que aparece en el apartado Subcuentas por ejercicio en esta pestaña.

Ahora ya podemos continuar con la información adicional que aparece en la carpeta General. Pulsamos, dentro del apartado Dirección principal, en el botón Insertar, para incluir la Dirección Fiscal del Agente (necesaria para la emisión de facturas). Como vemos, es necesario repetir estos datos al dar de alta al agente también como proveedor.


En la carpeta Comercial habrá que introducir los siguientes datos. Nótese que como los agentes están sometidos a una retención del 15%, para que ésta se realice de forma automática no podemos utilizar la serie A que creamos en su momento. Por esta razón, crearemos una nueva serie de facturas, denominada AG, AGENTES (RETENCIÓN). El campo Cuenta de ventas dejadlo en blanco porque sólo compramos sus servicios (cuenta 623 que en la contabilidad está asignada a LIQAGE - liquidación de agentes).




Aceptamos los cambios para cerrar la ventana de proveedores y también la de agentes que quedaría como se muestra a continuación.

Por último, hay que tener en cuenta que al crear una nueva serie, debemos asociarla al ejercicio en que vamos a usarla. Abrimos el menú Fiscalidad / Ejercicios fiscales, modificamos el registro correspondiente al Ejercicio 2013 y en la pestaña Series de la parte inferior añadan el registro: Código Serie AG.


La ventana de Ejercicios Fiscales quedaría como sigue:


Otros agentes para practicar dándolos de alta:

Cód. agente: 2
Apellidos: ORTEGA PÉREZ		Nombre: VIRGINIA
DNI/CIF: 36996336P
Dirección: PLAZA ALFARO, 14		Ciudad: VALENCIA
Provincia: VALENCIA	País: ES 	Cód. postal: 46004
Comisiones: 5%
Departamento: Comercial 
IRPF: 15%
Proveedor: (crear uno nuevo), Cuenta contable: 4100.102

Cód. agente: 3
Apellidos: REALES RUIZ		Nombre: ANGEL
DNI/CIF: 15995115H
Dirección: CALLE BASILICA, 23 	Ciudad: BARCELONA
Provincia: BARCELONA	País: ES 	Cód. postal: 08509
Comisiones: 5%
Departamento: Comercial
IRPF: 15%
Proveedor: (crear uno nuevo), Cuenta contable: 4100.103

Cód. agente: 4
Apellidos: LOPEZ PIÑAS		Nombre: JOSE
DNI/CIF: 35775335P
Dirección: AVDA URUGUAY, 4		Ciudad: MADRID
Provincia: MADRID		País: ES 	Cód. postal: 28013
Comisiones: 5%
Departamento: Comercial
IRPF: 15%
Proveedor: (crear uno nuevo), Cuenta contable: 4100.104

#####Departamentos

La octava opción de Tablas generales es Departamentos, que hace referencia a las distintas áreas a las que pertenecen los trabajadores de la empresa. En nuestro ejemplo, ya está dado de alta en la aplicación el Departamento Comercial, al que pertenecen los agentes comerciales.


#####Grupos de clientes

La décima opción de Tablas generales es Grupos de clientes, que permite agrupar los clientes de forma que sean tratados conjuntamente. Esto es útil cuando se trata de obtener informes y estadísticas, o cuando se quiere aplicar unas condiciones comerciales distintas a un grupo de clientes, como puede ser aplicarle una subida o una bajada en el precio base. En nuestro caso distinguiremos entre clientes que son a su vez empresas (MAYORISTAS) y particulares (MINORISTAS). Asimismo se darán de alta dos tarifas, si bien en un primer momento sólo se aplicará una reducción del 5% a los precios bases de los clientes mayoristas.

Añadiremos:
Código: 1 (ó 3 si ya existiera)
Nombre del grupo: Mayoristas.
Tarifa: 000001 (ó 000003 si ya existiera) Nombre: Clientes Mayoristas
Incremento porcentual: -5

Código: 2 (ó 4 si ya existiera)
Nombre del grupo: Minoristas.
Tarifa: 000002 (ó 000004 si ya existiera) Nombre Clientes Minoristas
Incremento lineal y porcentual: 0 (sin precio Especial)


Como puede observarse en la siguiente pantalla, dejaremos los campos Incremento Porcentual e Incremento Lineal a cero. Estas tarifas de ventas también se utilizan en el fichero maestro de artículos.


#####Divisas

La undécima opción de Tablas generales es Divisas, donde aceptamos los datos relativos al euro, los cuales ya vienen definidos por defecto en el programa.

Las dos últimas opciones son Países y Provincias, donde podemos consultar los datos relativos a nuestro país España, los cuales ya vienen por defecto.

###Menú principal
Área Facturación>Principal/Principal/Proveedores

* En este menú se encuentran los ficheros relativos a los proveedores y clientes. 

#####Proveedores.

Daremos de alta en este apartado la información relativa a los proveedores con los que se trabaja, ya que no es posible hacer compras a proveedores que no estén dados de alta. 

Cód. Proveedor: automático; Nombre: ABANÍCATE; NIF/DNI: 35704711T; Dirección fiscal: C/ PEZ Nº 3; Ciudad: Barcelona; Provincia: Barcelona; C. Postal: 08017; País: ES ; Persona de contacto: CAMPOS CUEVAS, SANDRA.
Carpeta Comercial.
Divisa: EUR; Forma de pago: 60, por el Banco Zaragozano;
Carpeta Cuentas bancarias.
Banco: BSANTANDER; Cuenta: 0049 0257 0000158987 (DC 68); Dirección: Diagonal, 87; C.P. 08008, Población: Barcelona; Provincia: 08; País: ES .
Al añadir un nuevo proveedor hemos de asignarle un código y un nombre.

* A continuación, la primera pestaña a cumplimentar sería Contabilidad si quisiéramos modificar el código de subcuenta asignado por defecto, en otro caso seguimos por la pestaña General donde, como su propio nombre indica se registra información genérica relativa al proveedor, entre la que incluimos el nombre de la empresa, NIF, dirección principal e información de contacto. Para añadir la dirección principal del proveedor pulsaremos el botón Insertar. 

* En la siguiente pestaña, Comercial, se incluirá la información relativa a la facturación realizada por el proveedor, entre la que se incluye la forma de pago habitual, la divisa con la que se trabaja, la serie de facturación y el IVA aplicable a los gastos de transportes en el caso de que sean portes debidos, es decir, por cuenta del comprador.


* En el campo Cuenta de pago se incluirá el código de nuestra cuenta bancaria a través de la que se realizarán los pagos al proveedor que estamos dando de alta (F4 para autocompletar). Por último, si el proveedor aplica algún tipo de descuento en sus compras se incluirá la información necesaria pulsando el botón Insertar registro en el apartado Descuentos aplicables.

* A continuación, la pestaña Cuentas Bancarias se utiliza para registrar la información de las cuentas bancarias del proveedor. No deben incluirse en este apartado, por tanto, las cuentas bancarias de la empresa a través de las que se realizan los pagos pues, como se ha mencionado anteriormente, éstas se darán de alta en la pestaña Comercial pulsando sobre Cuenta de pago.



* Cuando el proveedor disponga de más de una dirección se incluirá en la pestaña Direcciones. Como puede observarse en la ventana que aparece a continuación, la dirección principal (incluida anteriormente en la pestaña General) aparece, por defecto, en primera posición en el listado de direcciones.


* La quinta pestaña de esta ventana, Agenda de contactos, permite incluir información de las personas con las que tratamos directamente de la empresa.

* Las dos últimas pestañas, ofrecen información de interés incluida, normalmente, en otros módulos o apartados del programa relacionado con el proveedor. En Documentos, se pueden consultar y modificar Pedidos, Albaranes y Facturas emitidos por éste y en la pestaña Contabilidad se accede al mayor de la subcuenta del proveedor, una vez creado.






* Los datos para realizar prácticas son:

Carpeta General.
Cód. Proveedor: automático; Nombre: ALMAYOR, S.A.; NIF/DNI: A-28348129; Dirección: MOMBELTRAN, 5; Ciudad: Madrid; Provincia: Madrid; C. Postal: 28035; País: ES . Persona de contacto: BARBOSA GÓMEZ, SARA.
Carpeta Comercial.
Forma de pago: 30; Cuenta de pago: Banco Zaragozano.
Carpeta Cuentas bancarias.
Banco: Caja Madrid; Cuenta: 2038 1902 1472000001 (DC 07); Dirección: Huertas, 72; Población: Madrid; Provincia: Madrid; CP: 28003; País: ES .

* Carpeta General.
Cód. Proveedor: automático; Nombre: ALYBEBIDAS; NIF/DNI: B-089834504; Dirección: ROSSEND, 8; Ciudad y provincia: Barcelona; C. Postal: 08014; País: ES ; Persona de contacto: CARRERA ESTEPA, JOAQUIN MANUEL
Carpeta Comercial.
Forma de pago: 60; Cuenta de pago: Banco Zaragozano.
Carpeta Cuentas bancarias.
Banco: Banco Santander Central Hispano; Cuenta: 0049 0257 0014523698 (DC 66); Dirección: Diagonal, 87; C.P. 08008, Población: Barcelona; Provincia: 08; País: ES ..

* Carpeta General.
Cód. Proveedor: automático; Nombre: TODOENVASE; NIF/DNI: A-41680968; Dirección: PRENSA, 35; Ciudad: Sevilla; Provincia: Sevilla; C. Postal: 41007; País: ES ; Persona de contacto: AGUILAR VALERA, JUAN FRANCISCO.
Carpeta Comercial.
Forma de pago: 30; Cuenta de pago: Banco Zaragozano.
Carpeta Cuentas bancarias.
Banco: Banco ZARAGOZANO; Cuenta: 0103 0182 9994411220 (DC 70); Dirección: Av. Buhaira, 2; Población: Sevilla; Provincia: Sevilla; CP: 41018; País: ES . (Ya estaba dada de alta).

* Carpeta General.
Cód. Proveedor: automático; Nombre: BEBERYCOMER, SL; NIF/DNI: B-39283581; Dirección: c/ CAÑAMAS, 27; Ciudad: Valencia; Provincia: Valencia; C. Postal: 46011; País: ES ; Persona de contacto: ÁLVAREZ HERNÁNDEZ, GUADALUPE.
Carpeta Comercial.
Forma de pago: 60; Cuenta de pago: Banco Zaragozano.
Carpeta Cuentas bancarias.
Banco: Bankinter; Cuenta: 0128 2330 5555202020 (DC 81); Dirección: Los Naranjos, 75; Población: Valencia; Provincia: Valencia; CP: 46011; País: ES .

* Carpeta General.
Cód. Proveedor: automático; Nombre: EMBALAJES Y CIA; NIF/DNI: B28010945; Dirección: c/ GUZMAN, 11; Ciudad: Madrid; Provincia: Madrid; C. Postal: 28003; País: ES ; Persona de contacto: BALLESTEROS FERNÁNDEZ, SIMONA.
Carpeta Comercial.
Forma de pago: 30; Cuenta de pago: Banco Zaragozano.
Carpeta Cuentas bancarias.
Banco: Caja Madrid; Cuenta: 2038 1902 1155021021 (DC 06); Dirección: Huertas, 72; Población: Madrid; Provincia: Madrid; País: ES .

* Carpeta General.
Cód. Proveedor: automático; Nombre: DULCESDULCES; NIF/DNI: A-46916829; Dirección: c/ FRANCISCO, 27; Ciudad: Valencia; Provincia: Valencia; C. Postal: 46018; País: ES ; Persona de contacto: BALBUENA LUNA, M. ALEJANDRA.
Carpeta Comercial.
Forma de pago: CONT; Cuenta de pago: Banco Zaragozano.
Carpeta Cuentas bancarias.
Banco: Bankinter; Cuenta: 0128 2330 3321021022 (DC 85); Dirección: Los Naranjos, 75; Población: Valencia; Provincia: Valencia; País: ES .

#####Clientes.
Área Facturación>Principal/Principal/Clientes

* Daremos de alta en este apartado la información relativa a los clientes. No es necesario crear una ficha para cada cliente de la empresa, pues es posible crear una factura de venta y en la misma escribir el nombre, CIF y dirección sin incluir nada en el campo Código del cliente. Cuando se cree el asiento contable AbanQ volcará la información en la subcuenta de clientes varios 430.0.

* Pero para clientes habituales o que superen ciertos importes, debemos guardar información sobre sus datos y facturas por motivos fiscales (modelo 347 sobre operaciones con terceras personas). Al añadir un nuevo cliente hemos de asignarle un código y un nombre. La ficha del cliente contiene las siguientes carpetas: General, Comercial, Cuentas Bancarias, Direcciones, Agenda, Descuentos, Documentos y Contabilidad.

* Carpeta General.
Cód. cliente: automático; Nombre: Abenámar, S.A.; Nombre comercial: Abenámar; Grupo clientes: 2; NIF/DNI: A41547244; Dirección: CALLE CUNA, 51; Ciudad: SEVILLA; Provincia: Sevilla; País: ES ; C. Postal: 41005; Persona de contacto: JUAN MIGUEL ROJAS CENTELLA.
Carpeta Comercial.
Forma de pago: 30; Serie de facturas: A; Divisa (defecto): EUR; Tipo de rappel: 2; Agente Comercial: 1; Días de pago: 15, 30; Remesar en: 00001 (pulsad F4); Régimen de IVA: General; Riesgo máx. autorizado: 60.000; Nº copias factura: 1;
Carpeta Cuentas bancarias.
Banco: BSANTANDER; Cuenta: 0049 0268 5475475475 (DC 82); Dirección: C/ ARAÑA, 43; C.P. 41003; Población: SEVILLA; Provincia: SEVILLA; País: ES . Es la cuenta de domiciliación.
Carpeta Descuentos.
Aplicar descuento B (Clientes minoristas).

* La primera pestaña a cumplimentar es General donde, como su propio nombre indica se registra información genérica relativa al cliente, entre la que incluimos el nombre comercial de la empresa, CIF/NIF, grupo de clientes al que pertenece, dirección de facturación e información de contacto. Para añadir la dirección de facturación del cliente pulsaremos el botón Insertar. Es obligatorio incluir al menos una dirección del cliente para luego poder dar de alta cualquier documento relacionado con el mismo. 

* Una vez incluida una dirección del cliente en la pestaña General cualquier modificación de la misma se tendrá que realizar editando el registro correspondiente en la pestaña Direcciones.

* Si por cualquier motivo un cliente causara baja temporal y no deseamos seguir trabajando con él activaremos la opción De baja, indicando la fecha de inicio de esta baja. Si posteriormente quisiésemos volver a trabajar con él, tendríamos que desactivar esta opción.


* En la siguiente pestaña, Comercial, se incluirá la información relativa a la facturación, entre la que se incluye la Forma de pago habitual, la Serie de facturación, la divisa con la que se trabaja, el Tipo de rappel que se le aplicará, en su caso, y el Agente comercial que mediará las ventas con el cliente. Nuestra cuenta bancaria a través de la que realizaremos el cobro al cliente se incluirá en el apartado “Remesar en”. En relación con los impuestos habrá que especificar el tipo de IVA aplicable (general, exportaciones, U.E., exentos) y si es necesario incluir el Recargo de Equivalencia en factura, en cuyo caso se activará la opción Aplicar recargo de equivalencia. El programa también permite hacer una gestión de riesgo del cliente mediante el establecimiento de un límite máximo de facturación (Riesgo máximo autorizado). El volumen de las compras acumuladas por el cliente y no abonadas a la empresa son calculadas automáticamente por el programa incluyendo su importe en el apartado Riesgo alcanzado. En esta versión el programa sólo comprueba el citado riesgo al facturar al cliente.

* En la pestaña Direcciones se registrarán los distintos domicilios del cliente, pudiendo distinguir aquél al que se remitirán las facturas del que utilizaremos para enviar la mercancía. Para ello seleccionamos la dirección correspondiente y después pulsaremos los botones Dirección de facturación y Dirección de envío. Como puede observarse en la ventana que aparece a continuación, la dirección principal (incluida anteriormente en la pestaña General) aparece en primera posición en el listado de direcciones.

* En la siguiente carpeta, Cuentas Bancarias, se indica la cuenta corriente del cliente y se utiliza, normalmente, cuando los cobros están domiciliados. Para darla de alta pulsaremos el botón Insertar registro. En el caso de existir una única cuenta bancaria dada de alta será ésta la considerada a efectos de domiciliación pero, en el caso de existir varias, habrá que seleccionar una de ellas utilizando para ello el botón Cuenta de Domiciliación.



* Pulsen el botón para seleccionar la cuenta bancaria del cliente como cuenta de domiciliación:


* La quinta pestaña de esta ventana, Agenda de contactos, permite incluir información de las personas de la empresa con las que tratamos directamente.
La sexta pestaña, Descuentos, permite definir para cada cliente qué descuento se le aplicará por defecto, con independencia de que se le aplique finalmente algún descuento nuevo o no se le aplique ninguno porque las circunstancias así lo requieran.

* Las dos últimas pestañas, ofrecen información de interés incluida, normalmente, en otros módulos o apartados del programa relacionada con el proveedor. En Documentos, se pueden consultar y modificar Pedidos, Albaranes y Facturas emitidos por éste y en la pestaña Contabilidad se accede al mayor de la subcuenta del proveedor, una vez creado. 


* Los datos para realizar prácticas son:
Carpeta General.
Cód. cliente: automático; Nombre: REGALO, S.L.; Nombre comercial: REGALOS; Grupo clientes: 1; NIF/DNI: B41365256; Dirección: CRUZ DEL CAMPO, 12; Ciudad: SEVILLA; Provincia: SEVILLA; País: ES ; C. Postal: 41017; Persona de contacto: JOSÉ ANTONIO MARTÍNEZ DOMÍNGUEZ.
Carpeta Comercial.
Forma de pago: 60; Serie de facturas: A; Divisa (defecto): EUR; Tipo de rappel: 1; Cuenta remesas: 000001 (pulsad F4); Riesgo máx. autorizado: 30000; Nº copias factura: 1.
Carpeta Cuentas Bancarias.
Banco: ZARAGOZANO; Cuenta: 0103 0182 2542542542 (DC 71); Dirección: AVDA DE LA BUHAIRA, 2; Población: SEVILLA; Provincia: Sevilla; País: ES .
Carpeta Descuentos.
Tipo descuento: A.

* Carpeta General.
Cód. cliente: automático; Nombre: El Corte Francés, S.A.; Nombre comercial: EL CORTE INGLES; Grupo clientes: 1; NIF/DNI: A28258422; Dirección: MARÍA DE MOLINA, 43; Ciudad: MADRID; Provincia: MADRID; País: ES ; C. Postal: 28010; Persona de contacto: CRISTÓBAL PEREZ CRUZ.
Carpeta Comercial.
Forma de pago: 30; Serie de facturas: A; Divisa (defecto): EUR; Tipo de rappel: 1; Agente: 4; Cuenta remesas: 000001; Riesgo máx. autorizado: 120000.
Carpeta Cuentas Bancarias.
Banco: CAJAMADRID; Cuenta: 2038 1902 1591599511 (DC 02); Dirección: HUERTAS, 72; Población: MADRID; Provincia: MADRID; País: ES .
Carpeta Descuentos.
Tipo descuento: A;

* Carpeta General.
Cód. cliente: automático; Nombre: FALLERA, S.L.; Nombre comercial: FALLERA DE VALENCIA; Grupo clientes: 1; NIF/DNI: B46258471; Dirección: LOS NARANJOS, 654; Ciudad: VALENCIA; Provincia: Valencia; País: ES ; C. Postal: 46002; Persona de contacto: ANDRES ROSADO CRESPO.
Carpeta Comercial.
Forma de pago: CONT; Divisa (defecto): EUR; Serie de facturas: A; Tipo de rappel: 1; Cuenta remesas: 000001; Riesgo máx. autorizado: 30000.
Carpeta Cuentas Bancarias.
Banco: BANESTO; Cuenta: 0030 0125 3577533577 (DC 89); Dirección: LUGO, 45; Población: VALENCIA; Provincia: VALENCIA; CP: 46002; País: ES .
Carpeta Descuentos.
Tipo descuento: A.

* Carpeta General.
Cód. cliente: automático; Nombre: DOLORES ABRIL REINA.; Grupo clientes: 2; NIF/DNI: 24158741R; Dirección: BETIS, 87; Ciudad: SEVILLA; Provincia: Sevilla; País: ES ; C. Postal: 41001; Persona de contacto: DOLORES ABRIL REINA
Carpeta Comercial.
Forma de pago: CONT; Divisa (defecto): EUR; Serie de facturas: A; Tipo de rappel: 2; Cuenta remesas: 000001; Riesgo máx. autorizado: 60000.
Carpeta Cuentas Bancarias.
Banco: ZARAGOZANO; Cuenta: 0103 0182 1473691473 (DC 77); Dirección: AVDA DE LA BUHAIRA, 2; Población: SEVILLA; Provincia: SEVILLA; País: ES .
Carpeta Descuentos.
Tipo descuento: B.

###Artículos
Área Facturación>Almacén/Almacén/Artículos

Muestra un listado de todos los artículos existentes en nuestra empresa, disponibles o no, con su referencia, descripción, precio de venta y familia. Además es posible aquí ver o modificar todos los datos de un artículo concreto, o añadir otros nuevos. 

* Para añadir un nuevo artículo, tras pulsar el botón insertar registro, se introducirá la Referencia, un código alfanumérico que permitirá identificar el producto junto con la Descripción. 

* La ventana de datos del artículo se compone de varias carpetas: General, Venta, Compra, Stocks, Agentes y Contabilidad como puede observarse en la figura que aparece más adelante.

* Carpeta General.
Referencia: ABANICOL (ABANIC2 si ya existiera)	Descripción: ABANICO/ FOLGADO/LISO
Familia: C (Complementos) (Habrá que crearla, pues no existe)
Carpeta. Venta. 
Precio de venta: 7.5,	Tipo de IVA: IVA21	Pulsad el botón Generar precios
Carpeta. Compra.
Tipo de IVA: IVA21	Proveedor: 000002 (Abanícate)	Ref. prov.: AFL
Coste (divisa): 5.00
Carpeta Stocks
Stock mínimo: 50	Stock máximo: 150	
ALMACÉN: AC. Stock físico: 300 uds. (Añadir el físico en Stock por Almacén | Regularizaciones)
Carpeta Contabilidad:
Subcuenta de compras: 6.0
Subcuenta de IRPF: 4751.0
Subcuenta de ventas: 7.0 


* En la pestaña, General, el primer dato a incluir es la Familia, es decir, el grupo al que pertenece el artículo. Si no existiese dicha familia, se puede dar de alta en este momento, sin necesidad de ir al menú correspondiente. En nuestro ejemplo, crearemos la familia Complementos con el código C. En caso de utilizarse podemos anotar el código de barras del artículo, pudiendo optar por los formatos de codificación Code39, Code128, EAN, etc. e incluso insertar la imagen del producto. En el caso de que el usuario no tenga la necesidad de definir familias, si es una información que no se utiliza por parte de la gerencia para tomar sus decisiones, puede darse de alta un artículo sin indicarle familia. Dentro de las familias es posible definir Subfamilias, para agrupamiento de artículos de una misma familia.

* Por último, el programa permite elegir si el producto tiene stocks (los servicios no lo tienen), se compra (si lo fabricamos nosotros no se compra) o si se vende (si es una materia prima o componente que no se vende a terceros).

* En la segunda pestaña, Venta, es donde incluimos la información necesaria para la facturación, esto es, precio de venta del artículo, tipo de IVA aplicable (para más información sobre éste último ver el apartado dedicado a la Personalización de la empresa). Pulsando el botón Generar precios, el programa pone los precios de ventas correspondientes a las tarifas de ventas, que ya se dieron de alta. 

* En la tercera pestaña, Compra, incluiremos el precio de compra del artículo. Dado que éste puede ser suministrado por distintos proveedores, el programa nos permite especificar el coste del producto por cada uno de ellos. También se puede incluir la referencia que el proveedor asigna al artículo en cuestión lo que resulta de gran utilidad a la hora de solventar cualquier problema relacionado con la mercancía. Para añadir los precios por proveedor pulsaremos el botón Insertar registro. Cuando compremos los productos el programa ofrecerá información sobre el coste medio de las existencias.




* En la pestaña Stocks, incluimos los niveles de Stock mínimo y Stock máximo para el artículo que serán utilizados por el módulo de Producción del programa. En el apartado Stock por almacén se ES ecifican las existencias actuales en cada almacén. Activar la opción [V] Permitir ventas sin stock permitirá la venta de artículos de los que no se dispone de existencias físicas en el almacén. Debe tenerse cuidado con esta opción porque si no se activa, el programa no nos permitirá registrar ningún Pedido relacionado con el cliente, a no ser que dispongamos de la mercancía solicitada en cantidad suficiente para hacer frente a su posterior entrega.



* El campo stock físico se va actualizando en cada momento de forma automática por el programa y no se permite, por tanto, su modificación salvo los casos en que se realice una regularización de almacenes y del inventario porque se detecten diferencias con el volumen que facilita el programa. Para dar de alta el volumen con el que partimos en este momento, es necesario entrar en la opción Stocks por almacén y añadir un nuevo registro en esta opción. Dentro de ella, hay que especificar que en el almacén Calpe de la empresa hay un total de 300 unidades, para lo cual, hacemos clic en el botón Insertar y se introducen los datos que mostramos a continuación.



* La pantalla quedaría de la siguiente manera:


* y la carpeta Stocks de la ficha del artículo así:



* En la carpeta Contabilidad, hay que introducir los códigos de las subcuentas de compras (600.0), de IRPF para las compras (4751.0) y la subcuenta de ventas (7.0).



* Carpeta general
Referencia: BOMBAY (BOMBAY2 si ya existiera).
Descripción: Bombay Sapphire 47% 1.00ltr.
Familia: B (Bebidas)
Carpeta. Venta.
Precio de venta: 15.00	Tipo de IVA: IVA21
Carpeta. Compra.
Proveedor: AlyBebidas	Divisa: EUR	Coste (divisa): 9.00 (Comprobar nº proveedores, los agentes también lo son)
Carpeta Stocks
Stock mínimo: 50	Stock máximo: 150. ALMACÉN: AC, Stock físico: 300 uds.
Carpeta Contabilidad:
Subcuenta de compras: 6.0
Subcuenta de IRPF: 4751.0
Subcuenta de ventas: 7.0 

* Carpeta general
Referencia: Brandy.		
Descripción: Brandy 1866 (Estuche) 0.70 ltr
Familia: B (Bebidas)	
Carpeta. Venta.
Precio de venta: 30 	Tipo de IVA: IVA21
Carpeta. Compra.
Proveedor: BeberyComer		Divisa: EUR	Coste (divisa): 21.00
Carpeta Stocks
Stock mínimo: 50. Stock máximo: 150. ALMACÉN: AC, 300
Carpeta Contabilidad:
Subcuenta de compras: 6.0
Subcuenta de IRPF: 4751.0
Subcuenta de ventas: 7.0 


* Carpeta general
Referencia: Cardhu.		
Descripción: Cardhu 12 years ltr. Familia: B (Bebidas)
Carpeta Venta.
Precio de venta: 25	Tipo de IVA: IVA21
Carpeta. Compra.
Proveedor: AlyBebidas	. Divisa: EUR	Coste (divisa): 17.00	
Carpeta Stocks
Stock mínimo: 50	Stock máximo: 150. ALMACÉN: AC, 300
Carpeta Contabilidad:
Subcuenta de compras: 6.0
Subcuenta de IRPF: 4751.0
Subcuenta de ventas: 7.0 

* Carpeta general
Referencia: ARAMIS120.		
Descripción: Aramis Asl 120ml. Familia: P (Perfumería)
Carpeta. Venta.
Precio de venta: 25	Tipo de IVA: IVA21
Carpeta. Compra.
Proveedor: AlMayor.		Divisa: EUR	Coste (divisa): 17.00	
Carpeta Stocks
Stock mínimo: 50	Stock máximo: 150. ALMACÉN: AC, 300
Carpeta Contabilidad:
Subcuenta de compras: 6.0
Subcuenta de IRPF: 4751.0
Subcuenta de ventas: 7.0 

* Carpeta general
Referencia: CARLOS1.
Descripción: Carlos I 1.00 ltr. Familia: B (Bebidas)
Carpeta. Venta.
Precio de venta: 15	Tipo de IVA: IVA21
Carpeta Compra.
Proveedor: BeberyComer. 	Divisa: EUR	Coste (divisa): 14.00
Carpeta Stocks
Stock mínimo: 50	Stock máximo: 150. ALMACÉN: AC, 300.
Carpeta Contabilidad:
Subcuenta de compras: 6.0
Subcuenta de IRPF: 4751.0
Subcuenta de ventas: 7.0 

* Carpeta general
Referencia: CARTAS50C.	Descripción: FORNIER/ESP_GEMELA/50C/(275) Familia: J (Juguetería)
Carpeta Venta.
Precio de venta: 8.	Tipo de IVA: IVA21
Carpeta. Compra.
Proveedor: AlMayor.	 	Divisa: EUR	Coste (divisa): 2.00
Carpeta Stocks
Stock mínimo: 50. Stock máximo: 150. ALMACÉN: AC, 300
Carpeta Contabilidad:
Subcuenta de compras: 6.0
Subcuenta de IRPF: 4751.0
Subcuenta de ventas: 7.0 

#Gestión de compras

En este menú se encuentran las opciones relativas a las compras del programa. Estudiaremos las siguientes:
1. Pedidos a proveedores.
1. Albaranes de proveedores.
1. Facturas de proveedores.
1. Facturas rectificativas de proveedores.
1. Tesorería/Recibos de proveedores.

##Pedidos a proveedores 
Área de Facturación>Facturación/Compras

En esta ventana realizaremos la siguiente práctica:
1. Insertar registros. Tres pedidos nuevos.
1. Botón generar albarán. Crear un albarán desde un pedido.
1. Botón generar factura. Crear una factura desde un pedido.

En esta opción registraremos aquellos pedidos que se realicen a los proveedores. Estos documentos no suponen ninguna entrada de productos en el almacén, sino una información acerca de los artículos que estamos pendientes de recibir, para realizar un seguimiento de la mercancía. Por ello, puede ocurrir que la empresa no desee llevar este tipo de control, con lo cual podrá pasar directamente a trabajar con los albaranes.

*Comenzamos realizando la siguiente práctica:*

[1] Primer pedido. Con fecha 1 de octubre le hacemos un pedido a ABANICATE (COD. 000006) de 25 abanicos lisos (Ref: ABANICOL) que eventualmente se pagará al contado y no con la forma de pago de 60 días asignada a ese proveedor cuando se le dio de alta.

Para dar de alta a un nuevo pedido pulsaremos sobre el botón Insertar registro.

En primer lugar podremos cambiar la serie de facturación a la que pertenece dicho pedido (por defecto es la serie A). El resto de datos que conforma la cabecera del pedido se rellenan de forma automática por el programa.


En la pestaña Proveedor se incorporarán los datos del proveedor.


En relación con el estado del pedido (campo Servido), éste se rellena de forma automática por el programa y posee tres posibles valores, 
No. No existe ningún albarán (o factura) que lo respalde, es decir, no ha entrado la mercancía en nuestro almacén. Si hemos cometido algún error en ese pedido se puede modificar o eliminar sin mayor contratiempo.
Parcial. Una parte de los productos que componen este pedido ha llegado al almacén, a través de uno o más albaranes o facturas. Será imposible su modificación o eliminación sin antes haber eliminado o modificado el albarán o factura que se haya generado.
Sí. Toda la mercancía ha llegado al almacén, a través de uno o varios albaranes o facturas. Será imposible su modificación o eliminación sin antes haber eliminado o modificado el albarán o factura que se haya generado. 

En la pestaña Datos se completará la información adicional necesaria asociada a este pedido, como son: Almacén donde se recogerán los productos, forma de pago, divisa y tasa de conversión, en su caso, así como el recargo financiero.

En el caso de que solo hayamos dado de alta un almacén no será posible introducir en dicho campo algún valor. Por ello, si hay que registrar un pedido a un proveedor que se recoja en un almacén aún no dado de alta, habrá, en primer lugar que darlo de alta en el módulo Almacén, menú Almacén, opción Almacenes. A continuación ya podremos registrar el pedido al proveedor.


Una vez incluida la información relativa al proveedor, para la introducción de líneas del pedido pulsamos el botón  en el apartado Líneas, donde incluiremos la referencia del artículo (pulsar el botón Referencia, para acceder a la tabla de artículos), la cantidad a pedir, el precio si experimenta algún cambio respecto al definido en la ficha del artículo y los descuentos aplicables, en su caso. Para seleccionar el artículo podemos acotar la búsqueda activando la opción Mostrar sólo los artículos del proveedor.

Por último, indicar que en la ventana de Insertar/Editar Pedidos a Proveedores el botón (Documentos relacionados), permite acceder y consultar información relativa a los documentos generados a partir del pedido: Permite seguir la trazabilidad o ruta seguida por los documentos.
El pedido quedaría de la siguiente forma:


Al insertar los pedidos, el programa asigna automáticamente el número que aparece en la ventana Editar Secuencias de Ejercicios, que se encuentra dentro del Área de Facturación, en el módulo Principal y dentro de éste en el menú Principal/Fiscalidad/Ejercicios fiscales botón Modificar registro. Por último se accede a la pestaña Series y se elige Modificar registro.

* Como puede observarse en la ventana anterior, ya se ha creado, en relación con las compras, algún pedido: “Valor” de npedidoprov indica el número de pedido que se asignará al crear el siguiente pedido a proveedores, normalmente será una unidad mayor al último pedido creado (puede que sea superior si hemos eliminado alguno).

* Continuando con la operación de añadir un pedido de compras (recuérdese que estábamos trabajando en el Área de Facturación, módulo Facturación, menú Compras, Pedidos a proveedores) una vez pulsado el botón Insertar registro, habrá que rellenar información sobre el nuevo pedido: pestañas Proveedor, Datos y Observaciones.

* [2] Segundo pedido. Con fecha 03-octubre le hacemos un pedido a ABANICATE (COD. 000006) de 60 abanicos lisos (Ref: ABANICOL).


* [3] Tercer pedido. Con fecha 4 de octubre le hacemos un pedido a AlyBebidas (COD. 000008) de 40 botellas de licor (Ref: BOMBAY).

* Al finalizar el alta de estos últimos pedidos se podrán observar en la ventana de Pedidos:


* Si bien los pedidos no implicaban la entrada de mercancía en el almacén, tanto el albarán como la factura (en el caso de que no se trabaje con albaranes previos) sí implican tal entrada:

* A la hora de crear un albarán a partir de un pedido previo, podríamos realizarlo de dos formas diferentes:

1. Desde la ventana de Pedidos a través del botón Generar albarán nos permitirá crear de forma automática el albarán, a partir del pedido seleccionado. El albarán tendrá como fecha la del ordenador y por ello debemos editarlo para insertar la fecha correcta. Al respecto indicar que la modificación de la fecha no tendría lugar en la empresa real pues esta opción se ejecutaría el día que los artículos entren en almacén, por lo que coincidirá la fecha del albarán con la fecha del ordenador. En clase se modifica porque el caso debe servir para todos los grupos y en cada grupo se realiza en un día diferente.

1. Desde la ventana de Albaranes de Proveedores, a través del botón Asociar. Esta segunda opción se explicará más adelante, en la sección dedicada a los albaranes.

Botón Generar Albarán 

* [4] Con fecha 5 de octubre se recibe, a través de un albarán, la mercancía en almacén correspondiente al pedido 1 (de 1 de octubre). Para ello habrá que seleccionar el Pedido en cuestión y después pulsar el botón Generar Albarán. 
Para realizar esta operación, en primer lugar, IMPORTANTE, hemos de seleccionar en el listado de Pedidos aquél que hemos recibido (para ello pulsamos sobre el pedido en cuestión) y después pulsaremos sobre el botón Generar Albarán.

Una vez registrado el Albarán, observad cómo de forma automática ha cambiado el estado del Pedido, siendo ahora Servido, Sí y Editable No.


* Si lo abrimos y pulsamos el botón para ver la trazabilidad de documentos, veremos la relación del pedido con el albarán:


*Nota*: Recordamos que la numeración del documento es la conjunción de Ejercicio/Serie/Número (EEEESSNNNNNN). En la imagen coincide el número tanto para el pedido como para el albarán (000001) pero cada uno sigue su propia numeración.
Nos falta corregir la fecha del albarán (a 5 de octubre), ya que al crearlo tendrá como fecha la del ordenador, tal como podemos comprobar si consultamos los albaranes de compras (ir al Menú Compras/Albaranes). Esto motiva que tengamos que modificarla manualmente, acción que acometeremos pulsando el botón Modificar registro una vez seleccionado el último Albarán creado.

* También desde albaranes podemos consultar la trazabilidad entre documentos, el documento editado (el albarán en este caso) aparece en la primera fila y los documentos de donde procede o que deriven de él aparecen en las filas inferiores. El número de fila NO informa del orden de creación, ese orden lo da la posición de más a la izquierda hasta la derecha (desde presupuestos hasta pagos).

* Botón Generar Factura
Volvamos al menú Compras/Pedidos, seleccionen el pedido nº 2 (de 3 de octubre). El botón Generar Factura nos permitirá crear de forma automática la factura correspondiente al pedido seleccionado, creándose también de forma automática el albarán previo. Como ocurría al emplear el botón Generar Albarán habrá que prestar atención Especial a la fecha de la factura, que habrá de introducirse manualmente; sin embargo, la fecha del albarán no se podrá cambiar, ya que tiene una factura asociada. Si la forma de pago generara algún recibo como Pagado, para editar la factura habría primero que editar el recibo en el módulo de Tesorería – Recibos a proveedores, eliminando ese pago en la parte inferior de la ventana de edición, tras lo cual podremos cambiar la fecha de factura.

* [5] Con fecha 12 de octubre se recibe, a través de una factura, la mercancía en almacén correspondiente al pedido 2 (de 3 de octubre).
Se deberá utilizar, por tanto, el botón Generar Factura, una vez seleccionado el pedido en la ventana de pedidos de compras (menú Compras/Pedidos). 
La factura tendrá como fecha la del ordenador. Esto motiva que tengamos manualmente que modificarla, acción que acometeremos desde la ventana de Facturas de Proveedores (menú Compras/Facturas).


* Observad como el estado del pedido facturado ha cambiado (ahora aparecerá Servido, Sí y Editable No).
_____________________________________________________________________________________

##Albaranes de proveedores
Área de Facturación>Facturación/Compras

En esta ventana realizaremos la siguiente práctica:
Modificar registro. Modificar un albarán ya creado.
Botón Generar albarán desde la ventana de pedidos. Completar pedidos parcialmente recibidos.
Botón Asociar. Crear albarán a partir de un grupo de pedidos. Agrupar pedidos.

Este documento se registra cuando los artículos han entrado en el almacén. Dicho documento podrá efectuarse directamente o teniendo relación con un pedido anterior. Asimismo, un pedido puede generar más de un albarán.

Para dar de alta un nuevo albarán podemos pulsar sobre el botón Insertar registro (de la ventana Albaranes de proveedores), pero en vez de ello vamos a modificar el albarán creado a partir de un pedido. Abran el penúltimo albarán creado (el último no se podría modificar por estar ya facturado).

Vamos a ver cómo registrar varios albaranes a partir de un único pedido:

* [6] Primer albarán. Se comprueba que la mercancía registrada en el primer albarán (de 5 de octubre) no se corresponde con la que llega al almacén. Con fecha 05-10-08 se recibieron 7 abanicos de los 25 solicitados.

* AbanQ generó el albarán por toda la mercancía que figuraba en el pedido. En nuestro ejemplo lo hicimos desde la propia ventana de Pedidos, a través del botón Generar albarán. Una vez grabado el mismo, y ya desde la ventana de Albaranes procedemos a editar dicho albarán, modificando (utilizando el botón Modificar registro) la cantidad (7), tal y como se recoge en la siguiente figura.


* Como puede observarse en la ventana de pedidos de proveedor, el pedido de 1 de octubre aparece como Servido: Parcial (si ya estaba abierta habrá que refrescar la ventana con un clic de ratón).


* [7] Nuevo albarán. El 7 de octubre se recibe mediante albarán la mercancía que faltaba de ese pedido (de 1 de octubre y servido parcialmente).

AbanQ automáticamente crea el albarán por el total de la mercancía pendiente de entregar que figura en el pedido. En nuestro ejemplo lo haremos desde la propia ventana de Pedidos, a través del botón Generar albarán. 

* Una vez grabado el mismo, y ya desde la ventana de Albaranes procedemos a editar dicho albarán, modificando la fecha del mismo a 7 de octubre como fecha de entrada de la mercancía.

* Una vez grabado el albarán, el pedido vuelve a aparecer como totalmente recibido, estado de Servido: Sí.

Botón Asociar 

Permite agrupar los pedidos realizados con anterioridad a los proveedores entre unas fechas determinadas. Esta opción habrá que repetirla para cada uno de nuestros proveedores.

* Una vez que pulsamos el botón Asociar, aparece la ventana Agrupar Pedidos de Proveedores: Todos los campos de la mitad superior, a excepción de la fecha de albarán, establecen un filtro o condición sobre los pedidos que podrán pasar al nuevo albarán. En la parte inferior hay dos fechas entre las cuales (incluidas ellas) estarán los pedidos a agrupar.

* Si se deja en blanco algún campo, el filtro acoge todos sus posibles valores, por ello es importante rellenar al menos el código de proveedor, la forma de pago (el programa utilizará la forma de pago que aparezca en el primer pedido agrupado), la serie si se usan varias (en nuestro caso no es necesario porque todos los pedidos usan la serie A) y la divisa (en nuestro caso no importa porque siempre es el euro). Si se mezclan estos valores, el albarán será erróneo por no respetar los términos del pedido (misma forma de pago, misma serie de facturación y misma moneda de pago).

Nota: Si se deja en blanco el campo Almacén, el programa creará tantos albaranes como almacenes distintos aparezcan en los pedidos seleccionados. Es el único campo que no ocasiona combinaciones indebidas al dejarlo en blanco.

* Es necesario indicar el periodo o rango de fechas en el que buscar los pedidos (Pedidos desde/hasta). Una vez rellenos los campos que estimemos oportunos pulsaremos sobre el botón Actualizar, con lo cual aparecerán todos los pedidos que cumplan las condiciones anteriormente definidas. Si algún pedido de los que surjan no se desea tener en cuenta, lo seleccionamos primero y a continuación pulsamos sobre el botón Incluir/Quitar (o pulsamos un doble clic de ratón sobre el mismo).

* [8] Nuevo albarán. El 25 de octubre se recibe en el almacén la mercancía que se había solicitado al proveedor AlyBebidas, entre los días 1 y 24 de octubre, proceso que llevará a la generación del Albarán correspondiente.


* Una vez incluida la información en las secciones Proveedor y Datos albarán, habrá que pulsar el botón Actualizar y aparecerán los pedidos que cumplen las condiciones anteriormente expuestas. 

* Para completar el proceso habrá que pulsar el botón aceptar y así cerrar el formulario. La ventana de Albaranes de proveedores quedaría como se muestra en la siguiente imagen.



Botón Generar Factura 

* Provoca la generación automática de una factura a partir del albarán seleccionado. Como fecha de la misma aparecerá la que tenga el ordenador. Habrá que prestar atención Especial a la fecha de la factura, que habrá que modificar manualmente. Si la forma de pago generara algún recibo como Pagado, habría primero que editar el recibo en el módulo de Tesorería – Recibos a proveedores, eliminando ese pago en la parte inferior de la ventana de edición, tras lo cual podremos cambiar la fecha de factura.

##Facturas de proveedores
Área de Facturación>Facturación/Compras

* En esta ventana realizaremos la siguiente práctica:
Visualizar la primera factura.
Asociar varios albaranes para crear una factura.

* La factura es el documento que formaliza la compra al proveedor. En el caso de que se inserte directamente una factura, es decir, sin partir de un albarán previo, su registro supondrá la entrada de los artículos en el almacén. Existe la posibilidad de que una factura recoja la información de más de un albarán o pedido. La factura recibida por parte del proveedor deberá contener explícitamente los artículos adquiridos. En el caso de que en la misma se indique que dicha factura se corresponde con los artículos que figuran en el albarán o albaranes XX, habrá que guardar también dichos albaranes en previsión de una posible inspección de la Agencia tributaria.

* La numeración de estas facturas de proveedores es interna a la empresa, la factura legalmente exigible la crea el vendedor (proveedor) y cuando llegue el documento físico es aconsejable incluir dicho numero en el campo Número Proveedor, para, entre otros motivos: poder cotejar los datos con nuestra factura, aclarar cualquier incidencia con el proveedor, realizar una búsqueda más ágil y rápida, etc.

* Cuando se da de alta una factura de forma automática se genera el asiento contable que representa ese hecho contable de la compra. La creación de una factura implica la generación del asiento contable correspondiente en la contabilidad, ello se hará de forma automática (contabilidad integrada). Igualmente, según vayan pagándose los recibos generados, también se creará el asiento correspondiente a cada pago.

* Para poder hacer modificaciones en la factura, en el caso de que la misma lleve asociado algún pago al contado con generación de recibos pagados, habrá que eliminar primero el pago en el recibo del módulo de Tesorería – Recibos a proveedores. Ello eliminaría automáticamente el asiento contable del pago.

Botón Asociar. 

* Permite agrupar los albaranes realizados con anterioridad por los proveedores entre unas fechas determinadas. Es usual generar las facturas a final de mes incluyendo las entregas (albaranes) de mercancías acaecidos durante ese periodo, esta operación tendría que realizarse para cada proveedor. Se podría dejar el proveedor en blanco siempre que se hubiesen respetado los valores por defecto en todos los albaranes del mismo proveedor (misma serie de facturación, misma divisa y misma forma de pago), de otra forma se generarían combinaciones erróneas respecto a las condiciones establecidas en los documentos anteriores.

* Como ya comentamos al asociar pedidos para crear albaranes, en la ventana Agrupar Albaranes de Proveedores: Todos los campos de la mitad superior, a excepción de la fecha de factura, establecen un filtro o condición sobre los albaranes que podrán pasar a la nueva factura. En la parte inferior hay dos fechas entre las cuales (incluidas ellas) estarán los albaranes a agrupar (Albaranes desde/hasta).

* [9] Nueva factura. Con fecha 31 de octubre se facturan los albaranes comprendidos entre el 1 y el 31 de octubre del proveedor ABANÍCATE, los cuales tienen como forma de pago CONT (al contado).



* Una vez incluida la información en las secciones Proveedor y Datos factura, habrá que pulsar el botón Actualizar y aparecerán los albaranes que cumplen las condiciones anteriormente expuestas.

* Para completar el proceso habrá que pulsar el botón aceptar y así cerrar el formulario.

* Los albaranes incluidos quedarán marcados como no pendientes de facturas, y no se podrán modificar. La nueva factura, al ser la forma de pago al contado, 
Aparecerá como pagada, y no se podrá modificar salvo que se eliminen sus recibos en Área de Facturación | Tesorería | Tesorería |Recibos a proveedores.

###Facturas rectificativas de proveedores

* Podremos encontrarnos con los siguientes casos que obligan a realizar una factura rectificativa:

* Rectificación de una factura por incumplimiento de requisitos formales, errores de aplicación de precios, cantidades o descuentos, y modificaciones que afectan a la base imponible. 
Devoluciones de toda o parte de la mercancía o anulación de operaciones. 
Descuentos por alcanzar un volumen de compra (rappels). 

* En nuestro caso sólo analizaremos la segunda de las causas, es decir, la devolución de mercancías a nuestro proveedor.

* [10] Con fecha 2 de noviembre se procede a devolver a ABANICATE 4 ABANICOL procedentes de la factura nº 1, por encontrase los mismos estropeados.

* Para añadir un Abono pulsaremos el botón Insertar registro, indicando el proveedor y fecha en la pestaña Proveedor. A continuación, a diferencia de una factura normal iremos a la pestaña Observaciones, hay que activar el cuadro Rectificativa y pulsar sobre el icono, tras lo cual aparecerán las posibles facturas a rectificar. Éstas son aquéllas que están pendientes de pago, puesto que una factura con recibo abonado no se puede modificar (sin eliminar antes el pago en Tesorería).



* Seleccionamos la factura correcta, en nuestro caso la del 12 de octubre. Hecho esto, nos aparecerá la siguiente ventana, donde seleccionaremos la opción Copiar líneas de la factura con cantidad negativa.



* Si aparece un error indicando que la cuenta de Devoluciones de compras no está activada, será necesario indicar el número de esta cuenta Especial. 


* Cancelamos entonces la factura que estábamos añadiendo y procedemos a configurar, tal como nos indica el programa, la cuenta.
Para ello iremos a Área Financiera | Principal | Financiera | Configuración | Cuentas Especiales, y seleccionaremos la cuenta con el código DEVCOM; en ella indicaremos como Cuenta la 6080, y como subcuenta la 6080000000.


* Volvemos al Área de Facturación > Módulo Facturación > Compras > Facturas e indicamos la información necesaria para insertar la factura rectificativa (anotada anteriormente)



Modificamos los artículos que se vayan a devolver, sustituyendo el valor que aparece en el campo Cantidad por la cantidad correspondiente a la mercancía devuelta (en nuestro caso -4). No debe olvidarse que las cantidades deben figurar como negativas (recibir –N uds. es entregar +N uds. Sacándolas del almacén).



La tabla de facturas quedaría como se muestra a continuación.


Si editamos la factura rectificativa, en la pestaña Contabilidad pueden ver el asiento contable asociado (se usa la subcuenta contable 608.0 Devoluciones de Compras).





En el programa tendremos ahora una por la cantidad de artículos que se le compró, y otra, en negativo, correspondiente a la cantidad devuelta por nosotros. La factura rectificativa que acabamos de generar no sustituye a la que la originó sino que la complementa, de forma que la deuda real que mantenemos con el proveedor será la que resulte de restar al importe de la compra el importe de la devolución. Toda esta información puede consultarse accediendo al mayor del proveedor, tal como se muestra a continuación (Área Financiera>Menú Cuadro de cuentas > Subcuentas: buscar subcuenta 400.1, botón Editar Subcuenta, carpeta Libro mayor).



Además del efecto económico, el abono repercute en el inventario en almacén pues supondrá la salida de mercancía, al entrar una cantidad negativa en almacén en la práctica está saliendo esa cantidad.

##Tesorería/recibos de proveedores
Área de Facturación> Tesorería/Tesorería/Recibos a Proveedores

* En esta ventana realizaremos la siguiente práctica:
1. Pago de un recibo.
1. Devolución de un recibo.
1. Posponer parte del pago de un recibo.

A través de esta opción podremos ver cuándo y por qué importe se generarán los diferentes recibos a pagar a nuestros proveedores, lo que nos ayudará al control de la tesorería y de los vencimientos. 

* Accederemos a ella a través del módulo Tesorería, menú Tesorería, opción Recibos a Proveedores.


* El código de cada recibo es igual al código de la factura origen al que se suma un número de recibo. Así para la factura 20110A000001 (del ejercicio 0001 y serie 0A) existen dos recibos de de 182 y 181 euros, respectivamente, con vencimiento el día 12 de noviembre y 12 de diciembre (forma de pago 60), y para la factura rectificativa (si se hizo) las devoluciones son con forma de pago a 30 días (primer recibo por -12 euros) y 60 días (segundo por -12,20 euros).

* [11] Con fecha 12 de noviembre se procede a registrar el pago desde nuestro banco del primer recibo.

Añadan un Pago/Devolución en el primer recibo. Una vez aceptados los cambios su estado habrá pasado de Emitido a Pagado.


* [12] Con fecha 13 de noviembre se procede a devolver el recibo pagado por un defecto de forma.

Añadan de nuevo otro Pago/Devolución en el primer recibo. Verán que se pueden ir añadiendo cambios de estado Pagado/Devuelto/Pagado/Devuelto… indefinidamente. Si se quisiera modificar la factura origen de estos recibos, habría que eliminar todos los pagos y devoluciones registrados.


* [13] Con fecha 18 de noviembre se eliminan los pagos y devoluciones del primer recibo y se pagan sólo 100 euros, dejando el resto para negociar una nueva fecha de pago.

Abran el primer recibo, borren los pagos y devoluciones, modifiquen el importe a 100 euros. 

Al aceptar verán que se ha dividido el recibo en dos.



* Pagamos el primero de ellos con fecha de 18 de noviembre.


###Gestión de ventas

En este apartado vamos a estudiar todo el flujo de información y los documentos relativos a las ventas:

1. Pedidos de clientes
1. Albaranes a clientes
1. Facturas a clientes
1. Facturas rectificativas a clientes
1. Tesorería/Recibos de clientes
1. Tesorería/Remesas de clientes

####Pedidos de clientes
Área de Facturación> Facturación/Ventas

En esta ventana realizaremos la siguiente práctica:
1. Insertar registro. Creación de dos pedidos de clientes.
1. Insertar registro con anticipo. Creación de un pedido pidiendo parte del importe total.
1. Generar albarán a partir de un pedido.

En esta opción confeccionaremos aquellos pedidos que realicen los clientes. Estos documentos no suponen ninguna salida física de productos del almacén, sino una información acerca de los productos que estamos pendientes de servir, lo que nos permitirá hacer un seguimiento de los mismos. Por ello, puede ocurrir que la empresa no desee llevar este tipo de control, con lo cual podrá pasar directamente a trabajar con los albaranes y/o facturas. 

AbanQ, al contrario que muchos de los programas de facturación, permite actualizar el stock de los artículos cuando se genera un pedido (uso de la opción [V] Controlar stocks desde pedidos de cliente en el Área de Facturación> Principal – Menú Principal/Empresa – Pestaña Valores por defecto en conjunción con tener desactivada la opción [_] Permitir ventas sin stock en el Área de Facturación> Almacén – Menú Almacén/Artículos – Modificar – Pestaña Stocks). La razón es guiarse por el Principio de Prudencia para evitar cualquier posible Ruptura de Stock: Esto significa que es preferible perder ventas potenciales (cliente A pide todo nuestro stock, Cliente B no es atendido porque le decimos que no nos quedan mercancías, Cliente A se echa atrás y perdemos la venta), a dar la mala imagen de decir a un cliente que tenemos mercancías y luego no tenerlas (Cliente A pide todo nuestro stock, Cliente B pide 2 unidades, Cliente A llega y se lleva todo con el correspondiente albarán, finalmente Cliente B viene a por su pedido y vemos que no podemos atenderle). Al ser AbanQ un ERP, permite personalizar los módulos para dar otras posibilidades.

En el caso de que no haya suficiente stock en almacén para atender el pedido el programa, además de avisarlo, no nos dejará grabarlo hasta que no le indiquemos una cantidad que deje el stock como máximo en 0 unidades. La forma de ver la cantidad de stock que de ese artículo tenemos en almacén es bien fácil, en la misma ventana de añadir un artículo al pedido, pulsando en el botón con la lupa para elegir artículo, lo seleccionamos y pulsamos el botón para modificar registro, y dentro del artículo en cuestión abran la pestaña Stocks. La cantidad que figura en el campo Disponible será el límite que podamos pedir del mismo. Dicha cantidad se obtiene restando a la columna Cantidad el valor que aparece en la columna Reservada

_____________________________________________________________________________________
[14] Nuevo pedido. Con fecha 20 de octubre el cliente Abenámar S.A. (000001), nos hace un pedido de 25 abanicos lisos (ABANICOL). La fecha prevista de entrega es de dos días después.
_______________________________________________________________

Añadamos el nuevo pedido: Para dar de alta a un nuevo pedido pulsaremos sobre el botón Insertar registro. En la pestaña Cliente rellenaremos los datos relativos al cliente.


En la pestaña Datos, se incluirán los aspectos económicos del pedido, así como el almacén (siempre antes de indicar los artículos) del cual saldrá la mercancía. Es posible indicar la fecha prevista de salida del mismo, aunque este campo es meramente informativo.


* En la sección inferior introduciremos los artículos que conformen el pedido.


* Una vez grabado el mismo nos aparecerá la siguiente figura donde lo más destacable es que su estado es Servido No. Al igual que ocurría con los Pedidos a Proveedores un pedido puede presentar tres estados posibles: Servido No, Servido Parcial y Servido Sí.


* [15] Nuevo pedido. Con fecha 22 de octubre Abenámar nos hace un pedido de 15 abanicos lisos (ABANICOL) más. La fecha prevista de entrega es dentro de dos días.


* Anticipo de clientes. La introducción de un anticipo se realizará en la pestaña Anticipos, en la ventana de insertar Pedidos de clientes, pues los anticipos se gestionan siempre desde el formulario de pedidos, ya que, normalmente, el cliente solicita un presupuesto y la empresa le pide un anticipo para aceptarlo formalmente y generar un pedido en firme. Una vez generado el pedido lo normal es adjuntar en el mismo el anticipo para justificar dicho pedido. Con dicho anticipo se recoge la cantidad entregada por el cliente en el momento de confirmar el pedido. La cantidad que figure en el mismo dará lugar a un asiento en nuestra contabilidad que registra el cobro.

* [16] Nuevo pedido con anticipo. Con fecha 30 de octubre el cliente Abenámar S.A. (000001), nos hace un pedido de 25 abanicos lisos (ABANICOL). La fecha prevista de entrega es el 2 de noviembre. El cliente nos adelanta en este momento 100 €.


* En la pestaña Anticipos insertamos uno y en su pestaña Datos se introduce la fecha y el importe del mismo (o el %). 



* El programa nos permite indicar el anticipo como porcentaje sobre el total del pedido o como importe absoluto (si aceptamos el anticipo y lo abrimos de nuevo, se puede ver el porcentaje del importe marcado). También podemos ver el asiento creado por el cobro del anticipo en la pestaña Contabilidad.



* Otros botones de interés en la ventana principal de Pedidos de clientes:

Botón Generar Albarán

* Nos permitirá crear de forma automática el albarán, a partir de un pedido seleccionado. Debemos modificar (desde Ventas/Albaranes) “si fuese necesario” el día en que se generará el correspondiente albarán, pues por defecto se asume como fecha del mismo la que tenga el sistema.

* [17] Generar albarán. Con fecha 22 de octubre se sirve mediante albarán la mercancía procedente del pedido nº 1 (de 20 de octubre).


* Una vez generado el albarán observamos cómo cambia el estado del pedido pasando a Servido Sí y Editable No (círculo de prohibido). La columna Pedido indica si se han pedido a proveedores los artículos para casos en que se trabaja sin stocks (según hace el pedido el cliente, nosotros lo hacemos al proveedor, requiere de una funcionalidad extra no incluida en esta versión).


Botón Generar Factura

* Permite generar una factura a partir del pedido seleccionado. La fecha de la misma será la que tenga el sistema. Si en la misma figura como forma de pago al Contado, será imposible su modificación.


####Albaranes a clientes
Área de Facturación> Facturación/Ventas

En esta ventana realizaremos la siguiente práctica:

1. Crear albarán directamente.
1. Botón Asociar.
1. Generar factura desde un albarán A1 (F1)

* En esta sección confeccionaremos los albaranes a los clientes. Estos documentos suponen salida de productos del almacén. Dicho documento podrá generarse directamente o tomando como base la información existente en un pedido previo. Asimismo un pedido puede generar más de un albarán y varios pedidos se pueden agrupar en un único albarán.

* [18] Nuevo albarán. El 23 de octubre el cliente REGALO, S.L. compra en mostrador 10 botellas de BOMBAY, el cliente nos firma la entrega en el albarán correspondiente.

* Para dar de alta a un nuevo albarán pulsaremos sobre el botón Insertar registro, elegir el cliente, la fecha de compra como fecha de albarán y los artículos entregados.


* No es necesario que exista un pedido previo para crear un albarán.

* Otros botones de interés en la ventana principal de Albaranes a clientes:

Botón Asociar.

* Permite agrupar los pedidos realizados con anterioridad a los clientes entre unas fechas determinadas.

* En la sección superior de la ventana Agrupar pedidos a clientes se incluye el cliente del que vamos a agrupar los albaranes y el período de tiempo (pedidos desde/hasta). Tras pulsar sobre el botón Actualizar sabremos qué pedidos cumplen con las condiciones definidas y decidiremos cuáles de ellos se incluirán y cuáles no.
La sección Datos albarán actúa de filtro a la hora de que el programa seleccione unos u otros pedidos. Es obligatorio que aparezca una F.Pago, de manera que se elegirán aquellos pedidos que tengan la misma forma de pago. Si el campo Almacén se deja vacío el programa seleccionará todos los pedidos que teniendo la misma Forma de Pago elegida que coincidan en el período de tiempo incluido (Pedidos desde/hasta), es decir, el rango de fechas, estén en el almacén que estén. 

* [19] Nuevo albarán. El 24 de octubre se envía mediante albarán la mercancía procedente del pedido nº 2 (de 22 de octubre), realizado por el cliente Abenámar S.A. En el rango de fechas escriban 1 al 31 de octubre y desmarquen los pedidos que no queremos elegir.

* Para registrar el nuevo albarán utilizaremos el botón Asociar en la ventana de Albaranes a clientes (Menú Compras/Albaranes a clientes). Una vez seleccionado el cliente, pulsaremos el botón Dirección para elegir la dirección a la que se enviará la mercancía. Habrá que comprobar los datos que aparecen en los campos Forma de pago, Almacén y Agente, e incluir la información necesaria sobre la Fecha del albarán y rango de fechas (apartado Pedidos) para realizar el filtro de pedidos.



* Botón Generar Factura

Permite generar una factura a partir del albarán seleccionado. La fecha de la misma será la que tenga el sistema. Si en la misma figura como forma de pago al Contado o si se paga parte de la factura al contado, habrá que eliminar dicho pago para modificar la fecha de la factura (módulo de Tesorería – Tesorería/Recibos a clientes).

Una vez generada la factura el estado del albarán habrá cambiado a Pte.Factura: No (en rojo), siendo imposible su modificación.

* [20] Generar factura. Con fecha 23 de octubre se registra la factura procedente del albarán nº 1 (de 22 de octubre).

* Al generar la factura se crea el asiento contable automáticamente, el cual se modifica a la vez que la factura (miren la Fecha del asiento en la pestaña Contabilidad tras guardar el cambio y volver a abrir la factura).


####Facturas a clientes
Área de Facturación> Facturación/Ventas

* En esta ventana realizaremos la siguiente práctica:

1. Insertar registro.
1. Botón Asociar.

* Incluiremos los documentos que recogen los ingresos obtenidos tras las ventas a los clientes. En el caso de que se genere directamente una factura también supondrá la salida de los artículos del almacén. Existe la posibilidad de que una factura recoja la información de más de un albarán.

* Las facturas a clientes, a diferencia de pedidos y albaranes, sí son exigibles legalmente por lo que habrá que prestar una Especial atención a su numeración y a que no existan saltos o huecos en la misma.

* Para modificar una factura, en el caso de que la factura lleve asociado algún recibo ya pagado, habrá que eliminar primero el pago en el recibo dentro del módulo de Tesorería en Tesorería – Recibos a clientes, antes de poder hacer modificaciones en la factura, ello eliminaría también el asiento contable del pago.

* [21] Nueva factura. Con fecha 25 de octubre se realiza una nueva venta, esta vez con factura, a Regalo, S.L. de 15 BOMBAY y 10 abanicos lisos (ABANICOL).


* Otros botones de interés en la ventana principal de Facturas a clientes:

Botón Asociar

* Permite agrupar los albaranes realizados con anterioridad a los clientes entre unas fechas determinadas.

* [22] Siguiente factura. Con fecha 30 de octubre se factura el albarán nº 2 (de 23 de octubre) del cliente Regalo, S.L.

* En la sección superior de la ventana Agrupar albaranes a clientes se incluye el cliente del que vamos a agrupar los albaranes, la fecha de la factura a crear y el período de tiempo (albaranes desde/hasta) dentro del cual buscarlos. Tras pulsar sobre el botón Actualizar sabremos qué albaranes cumplen con las condiciones definidas y decidiremos cuáles de ellos se incluirán y cuáles no.
Téngase en cuenta que sólo se pueden agrupar distintos albaranes en una factura cuando tengan el mismo proveedor, la misma serie de facturación, la misma divisa y la misma forma de pago. Si existieran varios almacenes y se deja en blanco este campo, el programa creará una factura distinta por cada uno de ellos, otras combinaciones darían lugar a facturas erróneas por no respetar los ajustes previos.

* Una vez realizada la práctica, las ventanas de Pedidos, Albaranes y Facturas a clientes quedarían como se muestra a continuación.



####Facturas rectificativas a clientes

Podremos encontrarnos con los siguientes casos que obligan a realizar una factura rectificativa:

1. Rectificación de una factura por incumplimiento de requisitos formales, errores de aplicación de precios, cantidades o descuentos, y modificaciones que afectan a la base imponible. 
1. Devoluciones de mercancía o anulación de operaciones. 
1. Descuentos por alcanzar un volumen de compra (rappels). 

* La gestión de las facturas es exactamente igual a la de los proveedores, por lo que nos remitimos a lo allí expuesto.

####Tesorería/recibos a clientes

A través de esta opción podremos ver cuándo y por qué importe se generarán los diferentes recibos, lo que nos ayudará al control de la tesorería y de los vencimientos. 

* Para acceder a ella se hará a través del módulo Tesorería, menú Tesorería, opción Recibos a Clientes.


* Una vez seleccionada la opción visualizaremos los diferentes recibos que se hayan generado. Los mismos tendrán tres posibles estados: Emitido, Pagado o Devuelto.

* Pago de recibos en fecha vencimiento

* [23] El 30 de noviembre se cobra el recibo correspondiente a la primera factura.

* Para realizar manualmente el pago de un recibo, cuando el mismo venza, se edita pulsando el botón Modificar registro.


* Nota: La fecha de Vencimiento es el día 30 y no el 23 (a los 30 días ajustados a 1 mes) porque el cliente tiene establecidos como Días de pago el 15 y el 30.

* En la sección Pagos y Devoluciones se pulsa sobre el botón Insertar registro, apareciendo la figura siguiente:

* En el caso de que el recibo tenga como estado Pagado, y una vez registrado, junto al recibo se creará en nuestra contabilidad el asiento del pago, tal y como se recoge en la siguiente figura.



####Devolución de recibos

[24] Devolución el 1 de diciembre del recibo cobrado anteriormente. El cliente no tenía fondos suficientes en su cuenta bancaria.

* Si un recibo Pagado por el cliente se devolviera por el motivo que fuese, habría que editar el recibo que se cobró y pulsar, dentro de la sección Pagos y Devoluciones sobre el botón Insertar registro. El programa generará el movimiento contrario, es decir, Devuelto. Podremos modificar la fecha, no así la cantidad, que deberá ser la que figure en el recibo.

* Asimismo se generará en nuestra contabilidad el asiento correspondiente a esa devolución.


* En el caso de que el recibo figurase como Devuelto al seleccionarlo y pulsar sobre el botón Insertar registro de la sección Pagos y Devoluciones, se generaría un Pago.

####Tesorería/remesas a clientes.

La remesa es la entrega al banco de la empresa del listado de recibos de nuestros clientes. Se utiliza para facilitar los cobros, siendo nuestro banco el que intermedie con el resto de bancos de los clientes para cobrar los importes correspondientes.

* Desde la opción Tesorería/Remesas seleccionaremos los recibos que van a formar parte de cada una de las remesas que llevaremos a la entidad financiera para su gestión y cobro a clientes. Este hecho conllevará un asiento contable indicando el cobro de dichos recibos.


* [25] El 30 de noviembre se remesan los recibos de noviembre correspondientes a la factura 2.

* Los primeros campos a rellenar serán la fecha de la remesa y la cuenta bancaria (pueden pulsar F4) donde nos ingresarán los pagos.


* Para introducir los diferentes recibos debemos pulsar el botón Agregar recibos . Aparecerá una ventana con los recibos pendientes de cobrar en la parte superior, y los recibos que agregaremos a nuestra remesa en la parte inferior. Seleccionando los recibos y pulsando el botón Seleccionar podremos ir incluyendo los recibos en la remesa. Elijamos el recibo de la factura 2 con vencimiento el 25 de noviembre (código 00010A000002-01).


* Una vez seleccionados los recibos y aceptado el formulario nos queda la siguiente figura:


* Al grabar la remesa obtendremos la siguiente figura, donde se indica el número de recibos remesados y el importe total entre otros datos.



* Si abren de nuevo la remesa y seleccionan la pestaña Contabilidad podrán ver el asiento generado por el total remesado:



* La información que se resume en la pestaña Contabilidad recoge solo los datos que aparecen en los asientos relacionados con la remesa. Si posteriormente se devuelve un recibo remesado, la contabilización de la devolución puede verse en el mismo recibo devuelto.

* [26] El 1 de diciembre es devuelto el recibo remesado de la factura nº 2.

* Abran de nuevo los Recibos a Clientes, y devuelvan el recibo en Estado Pagado (fíjense también en la palabra REMESADO que aparece en la ventana abierta). Vuelvan a abrir la devolución (doble clic de ratón) para ver la pestaña Contabilidad.


##ANEXO

Los procesos de compra y venta descritos a lo largo de este manual han considerado que todas las actividades se realizan durante el mismo ejercicio económico (Ejercicio 1 en nuestro caso). 

* Si, por cualquier circunstancia, tuviéramos que generar un albarán o factura en el ejercicio siguiente procedente de un pedido del ejercicio anterior, el programa nos mostraría el siguiente mensaje: 


* Dado que la práctica, como se ha indicado, se realiza en el año AA, en esta ventana deberemos incluir una fecha comprendida entre el 01/01/AA y el 31/12/AA para que la aplicación nos permita continuar realizando la práctica sin errores.

* En el caso de que el documento (pedido, albarán o factura de proveedores o a clientes) correspondiese al ejercicio AA+1, tendríamos que seleccionar el ejercicio AA+1 en el Módulo Principal del Área de Facturación, editando la empresa ENVOLTOSA en la ventana de Empresa (menú Principal/Empresa).

