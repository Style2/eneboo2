* CREADO POR: [Universidad de Sevilla](http://www.us.es): Mariano Aguayo Camacho; Esther Chávez Miranda; Miguel Ángel Domingo Carrillo; Guillermo Molleda Jimena
* ACTUALIZADO Y ADAPTADO A ENEBOO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 31 de enero de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Area-Financiera-Contabilidad-COMPLETO-UNIV.SEVILLA)

----
####EN CONSTRUCCIÓN


###ÁREA FINANCIERA - CONTABILIDAD 

#### Indice:

* (Ciclo Completo. Manual inicial cedido por la Universidad de Sevilla)

1. [ÁREA FINANCIERA CONFIGURACIÓN:](#1-area-financiera---configuracion)
     * `1.1-  Cuentas Especiales`
     * `1.2-  Conceptos de partidas`
     * `1.3-  Códigos de balance`
     * `1.4-  Códigos de balance 08-Correspondencias 90-08`
2. [ÁREA FINANCIERA - CUADRO DE CUENTAS:](#2-area-financiera---cuadro-de-cuentas)
3. [ÁREA FINANCIERA - INTRODUCCIÓN DE ASIENTOS EN LA CONTABILIDAD DE FORMA MANUAL:](#3-introduccion-de-asientos-en-la-contabilidad-de-forma-manual)
4. [ÁREA FINANCIERA - INTRODUCCIÓN DE ASIENTOS EN LA CONTABILIDAD DE FORMA AUTOMÁTICA:](#4-introduccion-de-asientos-en-la-contabilidad-de-forma-automatica)
5. [RESUMEN:](#5-resumen)
6. [CONSULTAS Y OTROS PROCESOS:](#6-consultas-y-otros-procesos)
     * 6.1 Proceso de cierre trimestral del IVA.
     * 6.2 Procesos al final del ejercicio.
7. [CAMBIO DE EJERCICIO:](#7-cambio-de-ejercicio)

[volver al índice](#indice)

--

# 1. AREA FINANCIERA - CONFIGURACION:

Al igual que en el Área de Facturación lo primero que es necesario realizar es la configuración. Recordemos que ya hemos realizado parte de esa configuración con anterioridad de forma simultánea a la configuración de la Facturación. En realidad, ambos procesos deben realizarse de forma simultánea por cada departamento responsable, pero a efectos pedagógicos, nosotros hemos preferido impartirlos secuencialmente. Ello facilitará la comprensión de los conceptos que se van a analizar.

La configuración del Área Financiera se realiza en el "Área Financiera", Módulo "Principal". Allí encontramos las siguientes opciones:

#### Subindice:

1. [Configuración - Cuentas Especiales:](#1-configuracion---cuentas-especiales)
2. [Configuración - Conceptos de partidas:](#2-configuracion---conceptos-de-partidas)
3. [Configuración - Códigos de balance:](#3-configuracion---codigos-de-balance)
4. [Configuración - Códigos de balance PGC-2008:](#4-configuracion---codigos-de-balance-pgc-2008)
4.b- Correspondencias PGC 1990-2008.

--
####1. Configuracion - Cuentas especiales.
**Área Financiera> Principal/Cuentas especiales**

La opción Cuentas Especiales permite asignar una subcuenta determinada a un proceso automático del programa. Así, por ejemplo, al crear una subcuenta de IVA Soportado, es necesario que Eneboo sepa que el saldo de esta subcuenta recoge las cuotas soportadas por este impuesto y cuando se realice una anotación en el diario utilizando dicha cuenta, ese importe se anote también en la gestión fiscal del programa. De esta manera, podrá calcular correctamente la declaración de IVA, el modelo 347 y listar el libro registro de facturas recibidas. Lo mismo ocurre con el resto de tipos de subcuentas que aparece en el listado.

![Listado subcuentas](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-1.PNG)

[volver al sub-índice](#subindice)

[volver al índice](#indice)

--

####2. Configuracion - Conceptos de partidas.
**Área Financiera> Principal/Conceptos de partidas**

Los conceptos de partidas, segunda opción que aparece en este menú hace referencia a lo que comúnmente se denomina “conceptos contables”. Los conceptos contables son pequeñas leyendas que se incorporan a los apuntes contables y que aportan información sobre el mismo o explican si es necesario lo que se está contabilizando. Suelen constar de una parte fija y otra variable. Desde esta opción podemos realizar el alta, baja y modificaciones de los conceptos contables. Como ejemplo, vamos a dar de alta los siguientes conceptos contables genéricos:

Código: 01
Descripción: TRANSFERENCIA BANCARIA

Código: 02
Descripción: NOMINA DEL MES

Código: 03
Descripción: COBRO POR CAJA

![Conceptos de partidas](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-2.PNG)

[volver al sub-índice](#subindice)

[volver al índice](#indice)

--
####3. Configuracion - Codigos de Balance.
**Área Financiera> Principal/Códigos de Balance**

Sirve para especificar a Eneboo la forma en que deben agruparse los saldos y cómo deben ordenarse para conformar el Balance de Situación y la Cuenta de Pérdidas y Ganancias según el PGC anterior al del 2008. Esta opción no debe modificarse para no alterar la estructura de ambos estados contables salvo que se tengan profundos conocimientos de Eneboo y de contabilidad.


[volver al sub-índice](#subindice)

[volver al índice](#indice)

--

####4. Configuracion - Codigos de Balance PGC-2008.
**Área Financiera> Principal/Códigos de Balance 08**

Sirve para especificar a Eneboo la forma en que deben agruparse los saldos y cómo deben ordenarse para conformar el Balance de Situación y la Cuenta de Pérdidas y Ganancias con el plan contable de 2008. Esta opción no debe modificarse para no alterar la estructura de ambos estados contables salvo que se tengan profundos conocimientos de Eneboo y de contabilidad.

[volver al sub-índice](#subindice)

[volver al índice](#indice)

--

####1.4.b- Correspondencias 90-08.
**Área Financiera>Configuración/Correspondencias 90-08**

Sirve para especificar a Eneboo la forma en que deben agruparse los saldos y cómo deben ordenarse para conformar el Balance de Situación y la Cuenta de Pérdidas y Ganancias para adaptar una contabilidad llevada según el PGC de 1990 al del 2008. Esta opción no debe modificarse para no alterar la estructura de ambos estados contables salvo que se tengan profundos conocimientos de Eneboo y de contabilidad.

[volver al índice](#indice)

---
###2. AREA FINANCIERA - CUADRO DE CUENTAS.
**Área Financiera>Principal/Cuadro de cuentas**

La opción de Cuadro de cuentas presenta las siguientes opciones:

1. Grupo.
1. Subgrupo.
1. Cuenta.
1. Subcuenta.

Al crear el Plan contable de la empresa tras la creación del ejercicio, se dan de alta todos los datos básicos del mismo. Así, se copian en la empresa los registros necesarios tanto en todas estas tablas.

![Desglose plan contable](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-3.PNG)

Nótese que cada uno de los desgloses del plan contable se asigna a un determinado ejercicio. Esto quiere decir que tras la creación del ejercicio, siempre será necesario crear el plan contable de la empresa y que los saldos y movimientos registrados en cada subcuenta, se van a mantener independientes del resto de los ejercicios. Por esta razón, cuando se vaya a contabilizar una factura, ya sea de compra o venta, Eneboo comprobará que se contabiliza en el mismo ejercicio en el que se emite, de manera que no haya descuadres posteriores entre la facturación y la contabilidad.

![Aviso fecha asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-4.PNG)

En el apartado Grupos, subgrupos y cuentas no es normal que se tengan que añadir nuevos registros a los existentes. No ocurre lo mismo con las subcuentas, que suelen personalizarse para cada empresa. Así no es lo mismo un plan contable de una empresa de enseñanza, que la de una empresa que se dedica a vender regalos, ya que los tipos de operaciones son distintos y las cuentas suelen recoger descripciones que hagan una referencia clara al hecho contable que van a registrar.

* La creación de una subcuenta se puede realizar de varias formas:

1. Creación automática. Cuando se crea una ficha de un proveedor o un cliente, Eneboo da de alta automáticamente la subcuenta asociada a la misma.
1. Desde la opción Área Financiera>Principal/Cuadro de cuentas/Subcuentas, opción que veremos a continuación.
1. Desde la gestión de asientos, de forma que el usuario pueda dar de alta la subcuenta que le interesa a la vez que registra el movimiento en ella.

Al crear las subcuentas de IVA en la personalización de la aplicación ya vimos cómo se crean subcuentas. No obstante, repetiremos el proceso para dotarlo de mayor claridad, al ser el IVA una subcuenta Especial.

Al insertar una nueva cuenta se nos despliega la siguiente ventana:

![Nueva cuenta](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-5.PNG)

El proceso es tan simple que basta con rellenar los campos correspondientes. Vamos a crear la subcuenta con código “6290000001” y descripción “GASTOS DIVERSOS”.

Para ello en el campo cuenta introducimos los códigos correspondientes a la cuenta: 629. Nótese que en este campo, se introducen los códigos de la cuenta y no de la subcuenta; por esta razón, solo se especifican los 3 o 4 primeros dígitos del código de la subcuenta y no el código completo. Este dato debe introducirse en el campo siguiente: Código. A continuación introducimos la descripción o denominación de la cuenta y se especifica si es una cuenta de tipo Especial.

![Cuenta especial](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-6.PNG)

En este caso, no se corresponde con ningún tipo Especial, por lo que dejamos este campo en blanco. En las carpetas Otros datos y Modelos no es necesario rellenar ningún dato, por lo que la cuenta queda tal y como sigue:
 
![Edicion subcuentas](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-7.PNG)

Crear las siguientes subcuentas:
* Código: 6290000002
* Descripción: MATERIAL DE OFICINA.
* Tipo Especial:

* Código: 6250000001
* Descripción: SEGURO ALMACÉN AC
* Tipo Especial:

* Código: 6210000001
* Descripción: ALQUILER LOCAL COMERCIAL 
* Tipo Especial: 

[volver al índice](#indice)

---
### 2. AREA FINANCIERA - INTRODUCCION DE ASIENTOS EN LA CONTABILIDAD DE FORMA MANUAL.
**Área Financiera>Principal/Asientos**

Al igual que en la mayoría de los programas de contabilidad y ERP’s, la introducción de asientos en Eneboo se puede realizar de dos formas distintas: manual o automáticamente. 

La introducción de asientos por el primer método obliga al usuario a especificar todos los datos necesarios para dar de alta el asiento: subcuenta, importe, concepto, etc. Por el contrario, la introducción automática de asientos es una herramienta que permite contabilizar de forma los hechos contables que se definan sin intervención del usuario, variando el grado de automatización en función del tipo de asiento en cuestión.
Vamos a comenzar dando de alta asientos en el diario de forma manual. Para ello, es necesario que tengamos presentes los siguientes aspectos:

Se pueden introducir asientos en cualquier fecha del ejercicio, con independencia de que se hayan introducido algunos con fechas posteriores.

El concepto contable del apunte se puede introducir bien escribiéndolo entero o bien tecleando uno de los códigos dados de alta y completando, si es necesario, el texto. También es posible dar de alta los conceptos contables desde la introducción de asientos.

En este programa los apuntes se introducen siempre a nivel de subcuentas. Al introducir el código de la subcuenta, aparecerán automáticamente su descripción y saldo si está dada de alta. En caso contrario, se la dará de alta desde esa misma ventana.

Para facilitar la introducción de los códigos de las subcuentas, se puede utilizar la notación abreviada, por la cual el punto completa a ceros por la derecha. Por ejemplo, si tecleamos 4., el programa completará el código como 4000000, si tecleamos 572.11, el código quedará 5720011.

Este programa admite tanto importes negativos como nulos.

Se pueden realizar correcciones (añadir, borrar o modificar) en los apuntes ya introducidos. Para ello, se tecleará el número del asiento y se seleccionará el apunte en cuestión. Para dar de baja un apunte basta con pinchar el icono adecuado. Para dar de baja un asiento completo deberá ejecutar la opción destinada a tal efecto.

Cada vez que se introducen apuntes en las cuentas de IVA es necesario introducir la información fiscal necesaria para que Eneboo pueda facilitar los modelos tributarios correspondientes.

Para introducir los asientos de forma manual es necesario acudir a la opción Área Financiera>Principal/Financiera/Opciones del diario/Asientos. Al entrar en esta opción se nos muestra el diario de la contabilidad, tal y como aparece en la siguiente imagen.

![Listado diario](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-8.PNG)

Los asientos aparecen con la numeración correspondiente y se muestran algunos de los datos del mismo: fecha, importe del primer apunte, etc. Al igual que en ocasiones anteriores, para dar de alta un nuevo asiento, es necesario pulsar el botón Insertar y accedemos a la siguiente ventana:

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-9.PNG)

El primer dato a introducir es el número de asiento, el cual viene ya propuesto por Eneboo. A continuación habrá que indicar la fecha en la que se va a contabilizar la operación correspondiente. Dicha fecha tiene que pertenecer necesariamente al período que esté activo en la empresa; en caso contrario, Eneboo no permitirá continuar.

El siguiente dato a introducir es el concepto contable que se va a utilizar en el asiento. Como hemos comentado con anterioridad, los conceptos contables son pequeñas leyendas que se incorporan a los apuntes contables y que aportan información sobre el mismo o explican si es necesario lo que se está contabilizando. Suelen constar de una parte fija y otra variable. Desde esta opción podemos realizar el alta, baja y modificaciones de los conceptos contables. Ya tenemos algunos dados de alta, por lo que seguimos con el desarrollo del caso. El concepto que se introduce en esta primera pantalla sirve para que aparezca en el listado de diarios de la ventana de Asientos, pero no aparecerán en los listados de mayor. Por eso, en caso de que se desee que aparezcan allí, deberán introducirse en cada uno de los apuntes que componen el asiento. No es necesario introducirlos todos, sino que basta con hacerlo en el primer apunte, para que luego éste se proponga automáticamente en el resto.

A continuación debe introducirse el número de documento. El documento es un código que hace referencia a la ubicación del documento físico que respalda el hecho contable: facturas, escrituras, extractos bancarios, etc. Este dato suele omitirse si la empresa no tiene muchos documentación ya que es fácil encontrarla en el archivo de la misma. Junto con este campo, se puede especificar también el Tipo de Documento, campo con valores preestablecidos por la aplicación. Los distintos tipos que existen son: Recibo, factura de cliente o factura de proveedor. Habrá que elegir el que corresponda en cada momento.

En la parte inferior de la ventana, están los botones que sirven para gestionar los distintos apuntes que conformarán el asiento. También aparece el campo Plantilla que sirve para introducir asientos automáticos y que veremos más adelante.

Primer asiento: Asiento simple sin IVA.

Parar empezar a trabajar, vamos a introducir el asiento de apertura del ejercicio económico, el cuál consta de los siguientes datos:

* Número: Campo automático
* Fecha 01-01
* ID Concepto: 
* Concepto: ASIENTO DE APERTURA
* Documento:
* Tipo de documento:
* Partidas:
* CÓDIGO
* DESCRIPCIÓN
* DEBE
* HABER
* 216.1
* MOBILIARIO
* 3.000,00

* 217.1
* ORDENADOR
* 1.000,00

* 217.2
* IMPRESORA LASER HP
* 750,00

* 3.1
* EXISTENCIAS ABANICOS
* 35.000,00

* 3.2
* EXISTENCIAS BOMBAY 
* 20.500,00

* 3.3
* EXISTENCIAS CARTAS 
* 7.500,00

* 43.1
* CLIENTES EUROS
* 2.500,00

* 43.2
* REGALO
* 16.268,00

* 470.0
* H.P.DEUDOR POR IVA A COMPENSAR
* 35.398,00

* 57.0
* CAJA EUROS
* 12.202,00

* 572.1
* BANCO ZARAGOZANO
* 107.594,00

* 1.0
* CAPITAL SOCIAL

24.000,00
129.11
BENEFICIOS PP Y GG 2011

12.198,00
2816.1
AMORT. ACUM. MOBILIARIO

3.000,00
2817.1
AMORT. ACUM. ORDENADOR

1.000,00
2817.2
LASER AMORT. ACUM.

380,00
400.1
PROVEEDORES EUROS

26.623,00
400.2
ABANICATE

59.830,00
400.3
ALMAYOR

14.602,00
400.4
ALYBEBIDAS

61.217,00
465.0
REMUNER. PENDIENTES PAGO 

15.793,00
4751000
H.P. ACREED. RETEN. PRACTICADAS

15.090,00
4760000
ORG. SEGURIDAD SOCIAL ACREED.

7.979,00

![Insertar partidas](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-10.PNG)


Como puede observarse, la introducción de este tipo de asientos simples es muy sencilla. Basta con introducir cada uno de los distintos conceptos en su campo correspondiente. 
Segundo asiento: Asiento con IVA.

No obstante, la introducción de asientos de hechos contables que devenguen IVA resulta un poco más complejo. A continuación, seguiremos contabilizando la adquisición de un ordenador portátil con fecha 21 de octubre mediante el siguiente asiento:

Número:
Fecha 21-10
ID Concepto: 04 
Concepto: SU FACTURA Nº. 1.567/12
Documento:
Tipo de documento: Factura de proveedor
Partidas:
CÓDIGO
DESCRIPCIÓN
DEBE
HABER
217.3
ORDENADOR PORTÁTIL
743,80

472.21
IVA SOPORTADO 21%
156,20

523.1
COMPONENTES INFORMATICOS, S.L.

900,00
523.1
COMPONENTES INFORMATICOS, S.L.
900,00

572.1
C/C 345.892 B. CENTRAL H. 0049

900,00

Comenzaremos contabilizando el alta del ordenador en el inmovilizado de la empresa. Nótese que como Tipo de documento hemos señalado Factura de Proveedor. Como contrapartida hemos seleccionado la cuenta del proveedor del inmovilizado. De esta manera, cuando consultemos el mayor de la compra del inmovilizado, sabremos con quién realizamos la compra. Este campo es opcional, simplemente sirve para aportar mayor información cuando se consulte el mayor de la cuenta en la que se realiza la anotación.

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-11.PNG)

A continuación, introducimos la partida IVA. Nótese que al introducir el código de cualquier subcuenta de IVA, se abren los campos correspondientes al cuadro de IVA. Esto sirve para que se introduzcan aquellos datos que son necesarios para la gestión fiscal. Con ellos, Eneboo será capaz de:
1. Calcular el modelo de declaración trimestral de IVA 303.
2. Confeccionar el modelo de declaración de operaciones con terceros superior a 3.005,06€.
3. Confeccionar los libros registros de facturas emitidas y recibidas.

Por esta razón, es muy importante tener especial cuidado a la hora de introducir estos datos. Es igualmente relevante introducir el CIF del proveedor, ya que no hemos creado una ficha en la tabla de proveedores a Componentes Informáticos SA.

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-12.PNG)

En la ventana Modelo 303, se debe seleccionar [24-25] IVA Deducible por cuotas soportadas en operaciones interiores con bienes de inversión.
Como hemos utilizado la subcuenta del proveedor de inmovilizado en la contrapartida, Eneboo nos ofrece en la siguiente partida dicha subcuenta por defecto, de manera que aprovechamos para completar la partida de dicho apunte. En este caso no hemos especificado contrapartida alguna.

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-13.PNG)
El asiento completo queda de la siguiente manera:

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-14.PNG)

Aunque éste sería el asiento según la estructura tradicional, en la práctica suele resultar más adecuado empezar contabilizando en primer lugar el apunte referente al proveedor, a continuación el gasto y después el apunte de IVA.

Tercer asiento: Asientos con cuentas de varios.

Contabilizar con fecha 16 de octubre unas compras de material de oficina para uso interno por importe de 300,10 € (IVA incl..), realizadas en la COPISTERIA ABC. Suponemos que el pago se ha realizado por caja.
Número:
Fecha 16-10
ID Concepto: 
Concepto: 
Documento:
Tipo de documento: 
Partidas:
CÓDIGO
DESCRIPCIÓN
DEBE
HABER
629.2
MATERIAL DE OFICINA
247,93

472.21
IVA SOPORTADO 21%
52,07

41.0
ACREEDORES EUROS

300,00
41.0
ACREEDORES EUROS
300,00

57.0
CAJA EUROS

300,00

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-15.PNG)

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-16.PNG)

En la ventana Modelo 303, se debe seleccionar [22-23] IVA Deducible por cuotas soportadas en operaciones interiores con bienes corrientes.

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-17.PNG)

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-18.PNG)


Al ser un asiento contabilizado en la cuenta de varios, activamos el campo: Excluir de 347, ya que este tipo de movimientos no debe aparecer en dicha declaración.

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-19.PNG)


Cuarto asiento: Asiento con IVA Exento.
Con esa misma fecha se contabilizará el servicio recibido por un curso de formación impartido por ACADEMIA PIRATÍN, S.L. por valor de 3.300,00 € (exento de IVA), mediante su factura NÚMERO 325.10. Esta factura queda pendiente de pago:
Número:
Fecha 16-10
ID Concepto: 04 
Concepto: SU FACTURA Nº. 325.10
Documento:
Tipo de documento: Factura de proveedor
Partidas:
CÓDIGO
DESCRIPCIÓN
DEBE
HABER
629.3
CURSOS RECIBIDOS
3.300,00

472.0
H.P. IVA EXENTO / NO DEDUCIBLE
0,00

41.3
ACREEDORES EUROS

3.300,00

Cuando se debe registrar un asiento con una operación exenta de IVA o con IVA no deducible, desde un punto de vista contable no es necesario realizar apunte alguno en la cuenta de IVA, ya que éste no se devenga. Ahora bien, si pretendemos que Eneboo nos facilite de forma correcta las declaraciones fiscales correspondientes, esto no se realizase así, ya que al no utiliza cuanta de IVA no se recoge la información necesaria para confeccionar el Modelo 347 ni los libros registro de IVA. Por esta razón, hay que anotar un movimiento con IVA 0€ en una cuenta de IVA Soportado expresamente creada para ello.

Para ello, lo primero que es necesario, es crear un tipo de IVA Exento, de forma similar a como lo hicimos con el tipo 21% anteriormente.

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-20.PNG)


![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-21.PNG)

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-22.PNG)


A continuación modificamos las subcuentas de IVA 472.0 y 477.0 (que ya están creadas) para hacerlas corresponder con este nuevo tipo de IVA que estamos dando de alta:

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-23.PNG)

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-24.PNG)

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-25.PNG)



Y una vez todo listo, procedemos a dar de alta el asiento del curso recibido. Para ello, introducimos de forma similar a la anterior los apuntes correspondientes al gasto realizado y la deuda con el acreedor:

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-26.PNG)

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-27.PNG)



Y a continuación, contabilizamos el apunte en la cuenta de IVA Exento:

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-28.PNG)

En la ventana Modelo 303, se debe seleccionar [24-25] IVA Deducible por cuotas en operaciones interiores con bienes de inversión. Al ser una cuota de 0€, no afectará a esta declaración.
El asiento completo quedaría así:

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-29.PNG)

![Insertar asiento](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-30.PNG)


El mismo tratamiento debe recibir el IVA no deducible.

[volver al índice](#indice)

---
### 4. INTRODUCCION DE ASIENTOS EN LA CONTABILIDAD DE FORMA AUTOMATICA.
**Área Financiera>Principal/Asientos predefinidos**

Como hemos comentado con anterioridad, es posible introducir asientos en el diario de forma automática. La introducción de asientos en el diario de la contabilidad podía suponer el 80% del tiempo dedicado al proceso contable en una empresa. Aunque este tiempo haya disminuido, en gran parte, gracias a la integración entre distintas áreas de la empresa mediante el uso de un ERP y la generación automática de asientos desde sus distintos módulos; sigue existiendo la necesidad de introducir manualmente asientos en la contabilidad. Es necesario hacer más ágil, fiable y segura la creación de asientos en la contabilidad y por ello se han creado las plantillas de asientos.

Las plantillas de asientos son asistentes que sirven para dar de alta apuntes contables de forma automatizada en la contabilidad de la empresa. Estos asientos ya predeterminados se conocen por diversos nombres como asientos tipo, predefinidos, automáticos, modelos, máscaras, patrones o plantillas de asientos, en función del programa que se esté utilizando. En Eneboo se denominan “Asientos predefinidos”.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-31.PNG)

El uso de estos asistentes tiene varias ventajas importantes, las cuales enumeramos a continuación:

Permite registrar hechos contables sin tener conocimientos de contabilidad. Si programamos el proceso de introducción de apuntes convenientemente, o sea, separando los documentos que originen los asientos por conceptos: ventas, nóminas, etc. es posible que un usuario sin conocimientos contables se encargue de dar entrada a estos documentos.

Evita errores en la introducción de apuntes. Debido a que reduce la participación del factor humano en su elaboración.

Agiliza la entrada de asientos repetitivos. Se reduce al mínimo el proceso de captura de apuntes y por ello será más rápido.

Incrementa la productividad del Sistema de Información Contable. Las tres ventajas anteriores suponen que el coste operativo de llevar la contabilidad disminuye; disminución que será mayor cuanto más elevado sea el número de apuntes repetitivos y el número de contabilidades gestionadas con el programa.

La predefinición de asientos es una prestación ya incorporada a la mayoría de los programas de gestión contable. Estos asientos programados por el usuario para su utilización durante la introducción de apuntes permite que el operador seleccione el asistente que responda al hecho contable que va a reflejar y luego sólo ha de completar algunos datos, si fuera necesario.

La incorporación de estos asistentes de asientos en Eneboo se hizo en la versión 2.1 del módulo de contabilidad. No viene creado al instalar el software ninguna plantilla de asiento, en este apartado vamos a aprender a dar de alta este tipo de asientos para su posterior uso en la contabilidad de la empresa.
Comencemos dirigiéndonos al módulo Financiera – Principal del programa. En la ventana del módulo debemos pulsar la opción del menú Financiera – Opciones de diario – Asientos predefinidos:

En la nueva ventana abierta, se puede observar una tabla con tres campos: Código asignado al asiento tipo, Descripción del mismo y un tercer campo llamado Concatenar con que si contiene el código de otra plantilla de asiento, servirá para comenzar ese nuevo predefinido al terminar de dar de alta el asiento en curso.
Para la creación de un asiento predefinido es necesario tener muy claro el resultado que se espera del mismo, por ello es necesario en primer lugar realizar el asiento contable en un papel con la idea de sacar un esquema o boceto que nos guíe luego para su creación.

Vamos a recrear el apunte contable a que daría lugar el alquiler del local donde se ubica la empresa; el IVA soportado por este alquiler sería del 21% del total. Veamos el asiento tal como se introduciría en la contabilidad, una partida del asiento en cada fila de la tabla:

Número:
Fecha 16-10
ID Concepto: 
Concepto: 
Documento:
Tipo de documento: Factura de proveedor
Partidas:
CÓDIGO
DESCRIPCIÓN
DEBE
HABER
4100000005
INMOBILIARIA DEL SUR

968,00
6210000001
ALQUILER LOCAL COMERCIAL
800,00

4720000021
H.P. IVA SOPORTADO 21%
168,00

---
**Nota**: La  Fundación Sur cumple los requisitos para estar exenta de hacerle la retención de IRPF.
A la hora de crear el boceto de un asiento debemos hacernos algunas preguntas sobre lo que queremos conseguir, así nos fijaremos en varios puntos:

* Subcuenta: ¿Cada subcuenta utilizada será siempre la misma o puede variar? Por ejemplo en un asiento de nóminas, la subcuenta de sueldos y salarios puede ser distinta para cada empleado (640.1, 640.2, ...) o bien usar siempre la subcuenta general 640.0. En nuestro caso utilizaremos siempre una misma subcuenta para el acreedor y dueño del local.

* Importe: ¿Los importes respectivos guardan una relación permanente entre ellos?, ¿son importes siempre repetidos o en caso de pedir alguno se pueden hallar los demás con una fórmula?, En el caso actual son siempre los mismos, ya que todos los meses pagamos la misma cantidad en concepto de alquiler, es el caso más fácil y por ello lo utilizamos en nuestro primer asiento predefinido.

Para definir mejor el asiento predefinido, es necesario conocer los distintos tipos de datos que se pueden utilizar en su creación (al final de este manual tienen un resumen de los pasos a seguir para elegir la mejor opción de cada apartado existente en las partidas del predefinido):

Subcuenta
* Establecer: Se saben todos los dígitos de la subcuenta, 430.1
	Definir sirve para guardar la subcuenta en una variable
* Pedir: Faltan algunos dígitos (ej: no sé el cliente exacto: 430)
	Definir sirve para guardar la subcuenta en una variable
* Definida: Se utilizará el Valor guardado en la variable introducida en Definir, que deberá haber sido creada antes.

Importe
* Pedir: El importe debe ser introducido al crear el asiento
	Definir sirve para guardar el importe en una variable
* Calcular: Para introducir una cantidad fija o bien una fórmula utilizando una variable creada antes.
* Cuadrar: Se calculará sola la cantidad que saldará el asiento

Concepto
* Establecer: Si el texto será permanente y completo
* Pedir: Se podrá completar su contenido al crear el asiento.
* Último: Se usará el mismo concepto de la partida anterior
* Definido: Se utilizará el Valor guardado en la variable introducida en Definir, que deberá haber sido creada antes.

Documento
* Establecer: Si el texto será permanente y completo
* Pedir: Se podrá completar su contenido al crear el asiento.
* Último: Se usará el mismo contenido de la partida anterior

Factura
* Pedir: Al crease el asiento, se pedirá el número de factura.
* No pedir: No se pedirá el número al crearse el asiento.

Base Imponible
* Pedir: Se pedirá el neto de la factura. No usar.
* Calcular: Fórmula para hallar gasto o ingreso del asiento.

Contrapartida
* Establecer: Se saben todos los dígitos de la subcuenta, 430.1
	Definir sirve para guardar la subcuenta en una variable
* Pedir: Faltan algunos dígitos (ej: no sé el cliente exacto: 430)
	Definir sirve para guardar la subcuenta en una variable
* Definida: Se utilizará el Valor guardado en la variable introducida en Definir, que deberá haber sido creada antes.

Una vez leída la tabla anterior, y en referencia al asiento predefinido que estamos creando, resaltemos dos aspectos importantes:

En todos los asientos predefinidos donde aparezca alguna subcuenta de IVA, la partida del IVA será forzosamente de tipo establecer y el código de subcuenta será el que corresponda al porcentaje de IVA utilizado en la factura. En la partida de IVA es obligatorio rellenar el campo contrapartida con el código de subcuenta del sujeto pasivo del impuesto, es decir, la subcuenta del cliente, proveedor o acreedor al que se refiere el asiento.

Siempre hay que cuadrar una de las partidas de forma automática, para evitar cualquier error en los cálculos o problemas derivados de redondeos con las cifras, de esta forma nos aseguramos que el asiento nunca quede descuadrado. Las fórmulas, aunque sean correctas, pueden dar lugar a decimales que se redondean a dos dígitos, según la moneda utilizada, por ello uno de los valores debe ser directamente el valor que cuadre al asiento.
Con esta nueva información podemos escribir el boceto del asiento tipo:

Tipo
Establecer
Pedir
Definida ®
Establecer
Pedir
Último
Definido ®
Pedir
Calcular
Cuadrar
Establecer
Pedir
Definida ®

Nº orden
Subcuenta
Concepto
Importe
Contrapartida



D/H
Valor

1
Establecer: 410.5
Definir: Acrdor
Establecer:
Alquiler local
H
Calcular: 968,00 €

2
Establecer: 621.1
Último
D
Calcular: 800,00 €

3
Establecer: 472.21
Último
D
Cuadrar
Definida: Acrdor

Fijaos en los textos en negrita, Acrdor es una variable creada ad hoc donde guardaremos la subcuenta del acreedor, esta variable podrá usarse en las siguientes partidas como por ejemplo para introducir la contrapartida del IVA. La palabra Último sirve para que el programa copie la información anterior mientras que Cuadrar se utiliza para calcular el importe que deja el asiento cerrado con saldo cero. Continuamos con el alta del predefinido.
Respecto a los nombres de variables utilizadas, por ejemplo Acrdor, es necesario resaltar tienen un límite de 6 caracteres alfanuméricos, no deben incluir espacios ni símbolos extraños al alfabeto inglés, así como tampoco deben empezar por un carácter numérico.

**Alta de un nuevo asiento predefinido**

El primer paso puede ser comprobar que existan las subcuentas que vamos a utilizar en nuestro asiento: 410.5  Fundación Sur, 621.0 Arrendamientos y 472.21 IVA soportado al 21%. De estas subcuentas tendremos que crear la de  Fundación Sur porque no existe, y si no lo hacemos el programa nos avisará cuando utilicemos el predefinido. Vamos, en el módulo principal del área financiera, al menú P.G.C. - Subcuentas o pulsen las teclas Control y S asociadas a esa opción:

A continuación pulsamos el botón Insertar nuevo registro () e introducimos los datos sobre el acreedor  Fundación Sur:

* Cuenta: 410
* Código: 410.5
* Descripción:  Fundación Sur

![Insertar acreedor](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-32.PNG)

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-33.PNG)



**Nota**: Los botones de las ventanas han cambiado 
En realidad, el alta de asientos correspondientes a cualquier cliente, proveedor o acreedor de la empresa debe hacerse en el área de facturación, para así poder introducir datos como el D.N.I. o el N.I.F. como exige la normativa. En ese caso abriríamos una nueva ficha de proveedor en el área principal de facturación, teniendo el cuidado de modificar la subcuenta en la pestaña contabilidad escribiendo el código 410.5 en el recuadro oportuno.
Tras aceptar los datos de alta de  Fundación Sur volvemos a la ventana de asientos predefinidos. En ella el botón insertar registro () abrirá una ventana que cumplimentaremos con los siguientes datos:
Código: Alqloc
Descripción: Alquiler del local

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-35.PNG)

Añadamos la primera partida a la plantilla de asientos, para ello pulsen el botón de insertar registro en el marco Partidas de la plantilla. Y rellenen los diferentes campos con la información aparecida en nuestro boceto de predefinido:

Tipo:
Establecer
Pedir
Definida ®
Establecer
Pedir
Último
Definido ®
Pedir
Calcular
Cuadrar
Establecer
Pedir
Definida ®

Nº orden
Subcuenta
Concepto
Importe
Contrapartida



D/H
Valor

1
Establecer: 410.5
Definir: Acrdor
Establecer:
Alquiler local
H
Calcular: 968,00 €

2
Establecer: 621.1
Último
D
Calcular: 800,00 €

3
Establecer: 472.21
Último
D
Cuadrar
Definida: Acrdor

Para la primera partida los campos a rellenar serían los siguientes:
Plantilla de asiento
	Nº de Orden: 1
Datos principales
	Haber
	Subcuenta: Tipo Establecer, Valor 410.5, Definir Acrdor
	Importe: Tipo Calcular, Valor 968,00
	Concepto: Tipo Establecer, Valor Alquiler local
	Documento: Tipo Establecer, Origen Recibo

En la siguiente imagen pueden observar cómo quedaría la primera partida:


![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-36.PNG)

Antes de seguir hay que resaltar dos puntos que no han sido comentados, por un lado tenemos un campo llamado Nº de orden, éste guarda el orden de ejecución de las distintas partidas del asiento y por defecto se ordenan de forma consecutiva y creciente. Otro aspecto a resaltar es la asignación de un nombre de variable (Acrdor) a la subcuenta de acreedores utilizada, esto es necesario para poder especificar el sujeto pasivo cuando lleguemos a la partida correspondiente al IVA; aunque en este caso, al ser siempre la misma subcuenta, se podría obviar y escribir de nuevo el código de subcuenta en la contrapartida.
Para trabajar con la siguiente partida debemos pulsar bien el botón de aceptar y continuar () o la tecla F9 asociada al mismo. Los datos serían:

* Plantilla de asiento
	Nº de Orden: 2

* Datos principales
	Debe (elegirlo aunque parezca ya activado)
	Subcuenta: Tipo Establecer, Valor 621.1
	Importe: Tipo Calcular, Valor 800,00
	Concepto: Tipo Último
	Documento: Tipo Último

Pulsar de nuevo el botón () o la tecla F9 y continuar con la partida de IVA:
Plantilla de asiento
	Nº de Orden: 3
Datos principales
	Debe (elegirlo aunque parezca ya activado)
	Subcuenta: Tipo Establecer, Valor 472.21
	Importe: Tipo Cuadrar
	Concepto: Tipo Último
	Documento: Tipo Último

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-37.PNG)


IVA
	Base Imponible: Tipo Calcular, Valor 800,00
Contrapartida
	Contrapartida: Tipo Definida, Definir Acrdor

La ventana quedaría así:


![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-38.PNG)

No es necesario acordarse del nombre exacto del campo Definir, pulsando el botón de su derecha el programa recuerda los nombres utilizados para este tipo de campo (código de subcuenta) en las partidas anteriores.

Debemos resaltar el uso del mismo importe para Base Imponible que para el importe de la subcuenta de gasto en la partida anterior, este punto lo trataremos de nuevo con el próximo predefinido. Es importante ahora que observen la Contrapartida de la partida de IVA, la legislación vigente obliga a informar en la contrapartida del Sujeto Pasivo (persona física o jurídica prestadora o destinataria de la operación gravada por el impuesto), por ello es necesario introducir de nuevo la subcuenta del acreedor, proveedor o del cliente, según sea la operación contabilizada. En esta caso concreto, al ser una subcuenta fija la del acreedor, podríamos haber elegido directamente el tipo de contrapartida Establecer y escrito como valor 410.5 de nuevo.

Al pulsar el botón aceptar () o la tecla asociada F10, verán de nuevo la ventana del asiento predefinido, pulsar de nuevo aceptar para finalizar el alta del asiento predefinido.


![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-39.PNG)

Una vez terminada el alta es el momento de comprobar si funciona.

**Uso de un asiento predefinido**

La creación de asientos, tanto manualmente como usando predefinidos, se realiza en la ventana abierta con la opción del menú Financiera – Opciones del diario – Asientos o pulsando la combinación de teclas Control y A asociada a dicha opción.

Si en la ventana abierta comprueban la existencia de varios asientos, son asientos generados automáticamente desde otros módulos como el de Facturación. Pero hay numerosos hechos contables que deberán ser recogidos directamente, vamos a contabilizar el pago del alquiler del local para el mes de diciembre con el predefinido creado en el apartado anterior.


![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-40.PNG)

Pulsar el botón de insertar registro y en la ventana de Insertar Asientos verán como se calcula el número de asiento de forma automática, la fecha debemos establecerla en el 28 de diciembre y el asiento predefinido a seleccionar con el botón plantilla será Alqloc:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-41.PNG)

Pulsen el botón de ejecución del asiento predefinido  y vean como el asiento completo es generado de forma automática:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-42.PNG)

Hasta aquí hemos visto la forma más sencilla de generar un predefinido. Veamos otras posibilidades en el siguiente punto.

**Predefinido para la compra de suministro de combustible**

Igual que antes, debemos crear un boceto del asiento, vamos a pensar en el asiento que representa el hecho contable producido por la compra de combustible:
Número:
Fecha 
ID Concepto: 
Concepto: 04
Documento: SU FACTURA Nº.
Tipo de documento: Factura de proveedor
Partidas:
CÓDIGO
DESCRIPCIÓN
DEBE
HABER
410000000X


1.210,00
6280000000
SUMINISTROS LOCAL COMERCIAL
1.000,00

4720000021
H.P. IVA SOPORTADO 21%
210,00


Antes de terminar de crear el boceto de este asiento debemos hacernos siempre estas preguntas:

* Subcuenta: ¿Cada subcuenta utilizada será siempre la misma o puede variar? La subcuenta de Acreedor va a variar cada vez que compremos combustible, ya que normalmente acudiremos a distintas estaciones de servicio, por eso le hemos puesto una X a la subcuenta.

* Importe: ¿Los importes respectivos guardan una relación permanente entre ellos? Sí. ¿Son importes siempre repetidos o en caso de pedir alguno se pueden hallar los demás con una fórmula? Pues sí, sabes que el total de la factura es igual a la suma del gasto más el IVA. Hay que pedir el total de la factura y calcular mediante fórmulas el resto de valores. Para comprobar la fórmula una vez realizada, hemos pensado en unos valores fáciles de calcular (total de 1.210,00 €, gasto de 1.000,00 € e IVA de 210,00 €), pero éstos cambiarían para cada asiento creado.

* Por último el concepto también debe variar en cada uso del asiento para introducir el número de factura de la compra. Es muy común introducir el número de factura como parte del concepto de las partidas.
Con todo ello el boceto del asiento predefinido quedaría así:

Tipo:
Establecer
Pedir
Definida ®
Establecer
Pedir
Último
Definido ®
Pedir
Calcular
Cuadrar
Establecer
Pedir
Definida ®

Nº orden
Subcuenta
Concepto
Importe
Contrapartida



D/H
Valor

1
Pedir: 410
Definir: Acrdor
Pedir:
Carburante
H
Pedir, Definir: Total

2
Establecer: 628.0
Último
D
Calcular: Total/1.21

3
Establecer: 472.21
Último
D
Cuadrar
Definida: Acrdor

La explicación a los cambios realizados los exponemos a continuación: En nuestro caso vamos a crear una variable para el acreedor del carburante (Acrdor) utilizando para ello el campo Definir, y así luego podremos utilizarla como contrapartida del IVA soportado. También hemos creado otra variable (Total) para el montante de la factura recibida, esta variable nos va a servir para calcular otros importes, como por ejemplo el correspondiente a la subcuenta de gasto. El importe del gasto intuimos que es posible calcularlo mediante una fórmula, calcularla en otros tipos de asientos puede ser un proceso más o menos complicado, en este caso hemos seguido el siguiente razonamiento:

Neto + 21% del Neto de IVA = Total de la factura
Neto + Neto*0.21 = Total
Neto * (1+0.21) = Total
Neto*1.21 = Total
Neto = Total/1.21
Neto es el Debe de la partida de gasto de Suministros.

Vamos a crear el predefinido correspondiente, los datos iniciales son:
Código: Sumcom
Descripción: Compra de suministro combustible


![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-43.PNG)

Y los datos de la primera partida serán:
Plantilla de asiento
	Nº de Orden: 1
Datos principales
	Haber
	Subcuenta: Tipo Pedir, Valor 410, Definir Acrdor
	Importe: Tipo Pedir, Definir Total
	Concepto: Tipo Pedir, Valor Fra. Carburante:
	Documento: Tipo Establecer, Origen Recibo


![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-44.PNG)

La segunda partida contendrá la siguiente información:
Plantilla de asiento
	Nº de Orden: 2
Datos principales
	Debe (elegirlo aunque parezca ya activado)
	Subcuenta: Tipo Establecer, Valor 628.0
	Importe: Tipo Calcular, Valor Total/1.21
	Concepto: Tipo Último
	Documento: Tipo Último

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-45.PNG)

Recuerden que, en el campo Valor del Importe, podemos pulsar el botón a la derecha de Definir para que el programa recuerde el nombre de variable dada en el formulario de la partida anterior: Total, y luego completar escribiendo /1.21 para calcular el importe neto sin IVA.

La tercera partida es la correspondiente al IVA soportado y en ella se debe prestar atención a la Base Imponible y a la contrapartida, ambos datos son automatizados gracias al uso de variables, hagan pruebas con ellas para comprender mejor sus posibilidades. La información será la siguiente:

* Plantilla de asiento
	Nº de Orden: 3
* Datos principales
	Debe (elegirlo aunque parezca ya activado)
	Subcuenta: Tipo Establecer, Valor 472.21
	Importe: Tipo Cuadrar
	Concepto: Tipo Último
	Documento: Tipo Último
* IVA
	Base Imponible: Tipo Calcular, Valor Total/1.21
* Contrapartida
	Contrapartida: Tipo Definida, Definir Acrdor

Respecto a la fórmula utilizada para la Base Imponible volvemos a resaltar que siempre que una cantidad pueda ser calculada a partir de las demás, se utilizará la fórmula que consiga el resultado correcto (con la excepción del uso de Cuadrar la partida). En este caso se trata de repetir la fórmula para hallar el importe neto del gasto en combustible, ya calculado en la partida anterior.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-46.PNG)

Tanto en el campo Base Imponible, como en la Contrapartida, podemos usar el botón a la derecha de Definir para que el programa recuerde el nombre de las variables utilizadas: Total y Acrdor.
Finalmente, la plantilla del asiento quedaría así:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-47.PNG)

Probad el asiento con la compra el 29 de diciembre de carburante a Repsol YPF (subcuenta 410.6 que habrá que crear, directamente o mediante alta de ficha proveedores en la facturación) por un importe total de 2.420,00 €.

---
**Predefinido para contabilizar las nóminas**

Vamos a crear un predefinido para la contabilización del pago de las nóminas de los trabajadores, este tipo de asiento es algo más complicado, y podría hacerse automáticamente si se dispusiera de un módulo de Recursos Humanos; la dificultad de estos asientos se debe a las continuas variaciones que las nóminas de los trabajadores sufren durante el ejercicio, donde las desgravaciones aplicables dependen también de situaciones personales variables como tener un hijo, subir de categoría, etc.

El asiento por la entrega de las nóminas podría ser realizado una vez por cada empleado o bien se podrían recoger todos los pagos en un único asiento con las cantidades conjuntas, vamos a hacerlo de forma agrupada:

Número:
Fecha 
ID Concepto: 02
Concepto: NÓMINAS DEL MES
Documento: 
Tipo de documento: 
Partidas:
CÓDIGO
DESCRIPCIÓN
DEBE
HABER
6400000000
SUELDOS Y SALARIOS
Bruto

4760000000
ORG. DE LA SEG. SOCIAL ACREED.

Cuota obrera
4751000000
H.P. ACREED. RETENC. PRACTIC.

Retención
4650000000
REMUNERACIONES PTES. PAGO

Líquido

Volvemos a hacernos las preguntas de rigor:
* Subcuenta: ¿Cada subcuenta utilizada será siempre la misma o puede variar? En este caso, al contabilizar de forma agrupada todas las nóminas, los códigos de subcuenta utilizados son siempre los mismos.
* Importe: ¿Los importes respectivos guardan una relación permanente entre ellos? Aunque guardan una relación, no es permanente. La Seguridad Social (SS) y la retención por el impuesto de la renta (IRPF) son porcentajes del importe bruto de la nómina, pero esos porcentajes cambian entre los trabajadores según el sueldo o el contrato (progresividad del impuesto) e incluso en el mismo ejercicio para un trabajador concreto, por razones familiares (nacimiento de hijos) o por contractuales (renovación de contrato), entre otras.
* Más de importes: ¿Son importes siempre repetidos o en caso de pedir alguno se pueden hallar los demás con una fórmula? No, ni son siempre los mismos importes, ni pueden hallarse directamente con una simple fórmula ya que cada nómina es calculada aplicando porcentajes diferentes.
* Concepto: ¿Cual va a ser el concepto de las partidas? El concepto servirá para introducir el mes de pago de las nóminas, podría introducirse el código del documento de nómina o de seguridad social de cada trabajador si se contabilizaran las nóminas individualmente.

Y el boceto de asiento predefinido quedaría así:

Tipo:
Establecer
Pedir
Definida ®
Establecer
Pedir
Último
Definido ®
Pedir
Calcular
Cuadrar
Establecer
Pedir
Definida ®

Nº orden
Subcuenta
Concepto
Importe
Contrapartida



D/H
Valor

1
Establecer: 640.0
Establecer: 02
D
Pedir

2
Establecer: 476.0
Último
H
Pedir

3
Establecer: 4751.0
Último
H
Pedir

4
Establecer: 465.0
Último
H
Cuadrar


Mientras que en el primer asiento predefinido que realizamos, el de alquileres, todos los importes estaban preestablecidos; y en la segunda plantilla de asiento, el de compra de carburante, todos los importes podían calcularse a partir del primero. Es curioso este tercer tipo, no es posible calcular ninguno de los importes de las partidas a partir de ninguna de las demás, como mucho la última partida podrá simplemente cuadrar el asiento.

Con la información suministrada vamos a crear el nuevo asiento predefinido, es importante notar que no está permitido usar en el código caracteres Especiales, por ejemplo las tildes o la Ñ:
* Código: nomina
* Descripción: Pago de nóminas del mes

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-48.PNG)

Los datos de la primera partida serán los correspondientes a Sueldos y Salarios:
Plantilla de asiento
	Nº de Orden: 1
Datos principales
	Debe
	Subcuenta: Tipo Establecer, Valor 640.0
	Importe: Tipo Pedir
	Concepto: Tipo Pedir, Valor Nóminas mes:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-49.PNG)

La segunda partida contendrá la información sobre la cuota de los trabajadores a la Seguridad Social:
* Plantilla de asiento
	Nº de Orden: 2
* Datos principales
	Haber
	Subcuenta: Tipo Establecer, Valor 476.0
	Importe: Tipo Pedir
	Concepto: Tipo Último
	Documento: Tipo Último


La tercera partida es la correspondiente a las retenciones por el Impuesto sobre la Renta de las Personas Físicas (IRPF):

Plantilla de asiento
	Nº de Orden: 3
Datos principales
	Haber
	Subcuenta: Tipo Establecer, Valor 4751.0
	Importe: Tipo Pedir
	Concepto: Tipo Último
	Documento: Tipo Último

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-50.PNG)

La última partida representa el sueldo neto de los trabajadores, que se obtiene por diferencia del resto de partidas y será contabilizado en la subcuenta 465.0 Remuneraciones pendientes de pago a la espera de que los trabajadores pasen por caja a retirar su dinero:
* Plantilla de asiento
	Nº de Orden: 4
* Datos principales
	Haber
	Subcuenta: Tipo Establecer, Valor 465.0
	Importe: Tipo Cuadrar
	Concepto: Tipo Último
	Documento: Tipo Último

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-51.PNG)

La plantilla quedaría como se muestra en la imagen:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-52.PNG)

Comprobar el resultado con las nóminas del mes de diciembre, la fecha del asiento será el 30 de diciembre y el importe total de las nóminas serán 21.568,78 €, las cuotas de la Seguridad Social a cargo de los trabajadores sumarían 6.958,24 € en total y las retenciones por IRPF serían 1.590,85€. El asiento debería quedar así:

Número:
Fecha 
ID Concepto: 02
Concepto: NÓMINAS DEL MES
Documento: 
Tipo de documento: 
Partidas:
CÓDIGO
DESCRIPCIÓN
DEBE
HABER
6400000000
SUELDOS Y SALARIOS
21.568,78

4760000000
ORG. DE LA SEG. SOCIAL ACREED.

6.958,24
4751000000
H.P. ACREED. RETENC. PRACTIC.

1.590,85
4650000000
REMUNERACIONES PTES. PAGO

13.019,69

[volver al índice](#indice)

---
### 5. RESUMEN:

Pasos a seguir para crear un asiento predefinido o una plantilla de asiento:
1.- Leer el enunciado y escribir en un papel el asiento contable con los datos disponibles:
Apuntar para cada partida: 
 A-Debe o Haber.
 B-Subcuenta con algunos (PEDIR) o todos (ESTABLECER) los dígitos.
 C-Importe conocido (CALCULAR) o desconocido (posible CALCULAR usando una fórmula o PEDIR al usuario.
 D-Concepto explícito o no se dice nada al respecto (en general usar PEDIR para que el usuario escriba un número de factura u otro identificador del documento relacionado.
 E-Si la subcuenta es de IVA Soportado o IVA Repercutido, habrá que completar el cuadro IVA (si no está activado, mirar que la subcuenta contable exista y tenga asignado un tipo de IVA en la pestaña “Otros datos”.
 F-Contrapartida: Si se activa E, hay obligación de completar la contrapartida, en otro caso se puede usar para dar mayor información en el libro mayor de cada subcuenta.
Esta información debe verse para cada partida o línea con subcuenta del asiento.
1.- Crear el asiento predefinido, escribiendo un código (caracteres del alfabeto inglés, sin eñes ni vocales acentuadas). Luego pulsar el botón para insertar la primera partida.
1.- Creación de cada partida: Comenzar por la partida de la cual tengamos más posibilidades de conocer el importe cuando creemos un asiento real: Ya sea porque se especifique en el mismo enunciado del predefinido o conozcamos el importe cuando hagamos el asiento en el libro diario (el precio total, el precio sin IVA, el sueldo bruto, etc.)

3.A) Marcar la opción de Debe o de Haber según corresponda. Aunque salga marcada una opción, volver a elegirla para asegurar que queda marcada la correcta.

3.B) Para la subcuenta:
¿Se ha usado la subcuenta anteriormente en otra partida (seguramente en la contrapartida)?
	Ruta 3.B.Sí: En la otra partida debieron escribir una palabra en el campo Definir de la contrapartida. En esta ocasión elijan Tipo: Definida y vuelvan a escribir la misma palabra en el campo Definir (pueden pulsar el botón de la derecha para que el programa recuerde las palabras memorizadas). Fin.
Ruta 3.B.No: ¿Tiene todos los dígitos de la subcuenta? (si tiene el código de subcuenta facilitado un punto o bien tiene más de 4 dígitos y coincide su número con los dígitos usados. Si no saben cuantos dígitos se usan estime que serán de 7 a 12 normalmente. Si la partida es de IVA, se entiende que se tienen todos los dígitos en función de tipo de IVA usado, por ejemplo si es del 21% para una compra la subcuenta sería la 472.21 de IVA soportado, y si es una venta sería la 477.21 de IVA repercutido).
	Ruta 3.B.No.Sí: Tipo Establecer, Valor el código de subcuenta facilitado, Definir: Si la subcuenta va a ser usada en otra partida (por ejemplo como contrapartida del IVA), entonces escriba una palabra que describa a la subcuenta (de 6 caracteres como máximo y sin Espacios, ni eñes, ni acentos). Fin.
	Ruta 3.B.No.No: Tipo Pedir, Valor con los dígitos de la subcuenta que se hayan facilitado, Definir: Exactamente igual a lo explicado en la ruta 3.B.No.Sí anterior. Fin.

3.C) Importe:
¿Es la última partida del asiento?
	Ruta 3.C.Sí: Tipo Cuadrar. Fin.
Ruta 3.C.No. ¿Se da un importe en euros?
	Ruta 3.C.No.Sí: Tipo Calcular, Valor el importe numérico, Definir: Escriba una palabra que describa el importe (de 6 caracteres como máximo y sin Espacios, ni eñes, ni acentos, ejemplos serían Total, Neto, Bruto, Base, BI, ...). Fin.
Ruta 3.C.No.No: ¿Se puede calcular el importe en función de un importe utilizado en una partida anterior dentro de este mismo asiento predefinido?
	Ruta 3.C.No.No.Sí: Tipo Calcular, Valor una fórmula que tenga como resultado el importe correcto, para realizar dicha fórmula habrá que usar como variable la palabra escrita en el campo Definir del importe de la partida anterior. Definir: Escriba una palabra que describa el importe (de 6 caracteres como máximo y sin Espacios, ni eñes, ni acentos, ejemplos serían Total, Neto, Bruto, Base, BI, ...), esta palabra o nueva variable se podría usar para calcular otros importes posteriores mediante una fórmula. Fin.
	Ruta 3.C.No.No.No: Tipo Pedir, Valor no se rellena, Definir: Exactamente como se explica en la respuesta anterior del Sí. Fin.

3.D) Concepto:
3.D.a) ¿Se dice expresamente en el enunciado qué hay que poner en el concepto?
	Ruta 3.D.a.No: Utilicen de concepto uno que pida la identificación del documento físico que da lugar al asiento, ejemplos “Nº Factura:”, “Nº de documento:”, y sigan como si le hubieran especificado el concepto. Si no hubiera ningún documento pues inventen algún texto que describa al asiento completo (no a la subcuenta de la partida), también pueden pedir el mes del hecho contable o algo parecido (Nóminas del mes:).
Ruta 3.D.a.No.parte2) ¿El concepto necesita algún dato en el momento de crear un asiento real? Ejemplo un número de factura o documento, o el nombre del mes, etc.
	Ruta 3.D.a.No.parte2.Sí: Tipo Pedir, Valor un texto que pida el dato que falte. Continua en 3.D.b.
	Ruta 3.D.a.No.parte2.No: Tipo Establecer, Valor el texto. Continua en 3.D.b.
Ruta 3.D.a.Sí: Apliquen el apartado anterior (ruta 3.D.a.No.parte2).
3.D.b) ¿Se va a usar el mismo concepto en todas las partidas?
	Ruta 3.D.b.Sí: Si no es la primera partida, elijan Tipo Último. Fin.
	Ruta 3.D.b.No: Apliquen la pregunta 3.D.a. a cada partida del asiento predefinido. Fin.

3.E) IVA
En este caso en el apartado 3.B es obligatorio usar Establecer y la subcuenta exacta del IVA como se explica en la ruta 3.B.No. Con ello se habrá activado el cuadro de IVA.
Campo Factura: No pedir. Se podría pedir, pero ya hemos preguntado esta información en el concepto del asiento (Su factura:).
Base Imponible: Tipo Calcular, Base imponible: Fórmula a partir de algún importe anterior (usar las variables memorizadas con el campo Definir de ese importe, ejemplo: Total/1.21 ó simplemente Neto).

3.F) Contrapartida
Si la subcuenta de esta partida era de IVA (472.X o 477.X), la contrapartida debe ser la subcuenta correspondiente al sujeto pasivo (la persona física o jurídica con la que realizamos el intercambio de la compra o la venta).
¿Ha sido esta subcuenta ya usada en otra partida anterior?
	Ruta 3.F.Sí: Tipo Definida, Definir: Copiar la palabra usada en el campo Definir de la subcuenta del sujeto pasivo (pulsando el botón más a la derecha aparecen las palabras memorizadas). Fin.
Ruta 3.F.No: ¿Tiene todos los dígitos de la subcuenta? (si tiene el código de subcuenta facilitado un punto o bien tiene más de 4 dígitos y coincide su número con los dígitos usados por la contabilidad. Si no saben cuántos dígitos se usan estime que serán de 7 a 12 normalmente.)
	Ruta 3.F.No.Sí: Tipo Establecer, Valor el código de subcuenta facilitado, Definir: Escriba una palabra que describa a la subcuenta (de 6 caracteres como máximo y sin Espacios, ni eñes, ni acentos). Fin.
	Ruta 3.F.No.No: Tipo Pedir, Valor con los dígitos de la subcuenta que se hayan facilitado, Definir: Exactamente como se explica en la respuesta anterior (ruta 3.F.No.Sí). Fin.

[volver al índice](#indice)

---
### 6. CONSULTAS Y OTROS PROCESOS:

Ejercicios a realizar:
1.- Se desean localizar los apuntes contables existentes cuyo importe sea de 900,00 €. 
Para ello, basta con seleccionar Importe en el campo Buscar e introducir el importe deseado:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-54.PNG)

2.- Se desea visualizar el mayor del cliente REGALO, SL.
Para ello es necesario acudir al Menú Cuadro de Cuentas y entrar en la opción subcuentas. Una vez allí se busca la cuenta deseada y se selecciona Libro Mayor. Eneboo mostrará en una ventana independiente el mayor de la subcuenta seleccionada.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-55.PNG)

Los listados de Mayor también se pueden obtener de la opción Libro Mayor del menú Listados del Módulo Principal del área Financiera creando un listado en la misma.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-56.PNG)

En el ejemplo, hemos creado un listado de mayor de todas las cuentas para el ejercicio 2012. Cada vez que se ejecute, listará todas las cuentas de mayor con los movimientos regitrados en la contabilidad del 2012.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-51.PNG)

3.- Además se quiere modificar el asiento de las nóminas, ya que se contabilizaron erróneamente. El asiento correcto es el que mostramos a continuación:
Número:
Fecha 
ID Concepto: 02
Concepto: NÓMINAS DEL MES
Documento: 
Tipo de documento: 
Partidas:
CÓDIGO
DESCRIPCIÓN
DEBE
HABER
6400000000
SUELDOS Y SALARIOS
21.568,87

4760000000
ORG. DE LA SEG. SOCIAL ACREED.

6.958,24
4751000000
H.P. ACREED. RETENC. PRACTIC.

1.590,85
4650000000
REMUNERACIONES PTES. PAGO

13.019,78

4.- Modificar la fecha del asiento que contabiliza el curso recibido por importe de 3.300,00 € pasándolo al mes siguiente.

5.- Listar por pantalla los asientos correspondientes al mes de febrero. En este caso, vamos a crear un listado específico para este informe. Para ello, nos situamos en el Módulo Informes del Área Financiera y allí seleccionamos Listados -- Libro Diario. 
Una vez allí, añadimos un tipo de listado y rellenamos los datos que deseamos que aparezcan en el listado. En nuestro caso, le denominaremos Listado octubre, incluiremos los datos del IVA en el mismo y  no lo deseamos agrupado por meses. Seleccionamos el ejercicio del que queremos extraer los datos y el rango de fechas que nos interesan: del 1 al 31de octubre y activamos los campos oportunos

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-52.PNG)


Con ello, obtenemos el siguiente listado:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-53.PNG)

##PROCESO DE CIERRE TRIMESTRAL DEL IVA.

Para comenzar el cierre trimestral del IVA, se deben obtener en primer lugar los libros registros de facturas emitidas y de facturas recibidas provisionales del trimestre. Para ello, acudimos al Módulo Informes del Área Financiera y accedemos a la opción Facturas Recibidas del Menú IVA y creamos un listado del libro:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-54.PNG)

Quedando de la siguiente manera:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-55.PNG)

Para obtener el listado no hay más que hacer clic en el botón Listar Tabla y se obtiene la siguiente imagen.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-56.PNG)

Se repite a continuación la operación para las facturas emitidas, obteniendo otro listado similar.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-57.PNG)

A continuación es necesario obtener el modelo 303 de declaración trimestral del IVA. Para ello, acudimos al Módulo Modelos del Área Financiera y desde allí en el menú Modelos seleccionamos el 303 y creamos un nuevo modelo. 

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/Dibujo-58.PNG)

Una vez seleccionado el trimestre correspondiente y comprobadas las fechas a tener en cuenta para calcular la declaración es necesario hacer clic en el botón “Calcular datos” situado en la esquina superior derecha de la pantalla. Tras ello, Eneboo calcula automáticamente los datos de la declaración los cuales deben cuadrar con los listados de facturas anteriormente obtenidos. En caso de descuadre habrá que parar el proceso de cierre trimestral y buscar el error. Para esta tarea es especialmente útil el desglose de las subcuentas de IVA por tipos impositivos y naturalezas.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-59.png)

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-60.png)

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-61.png)

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-62.png)

Nótese que hay campos en los que el usuario tiene que introducir datos, como por ejemplo el importe a compensar de trimestres anteriores, el campo sin actividad, la fecha de obtención de la declaración o el lugar de firma.

Una vez obtenida, se puede generar un fichero para su presentación telemática.

A continuación es necesario contabilizar la liquidación del IVA obtenida, para ello, desde el Módulo Principal del Área Financiera, entramos en el menú Financiera Opciones del IVA, regularización del IVA.

Una vez allí, creamos la regularización del cuarto trimestre. Para ello basta con introducir los datos oportunos y hacer clic en el candado. De esta forma, se generará el asiento correspondiente en la contabilidad.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-63.png)
 
[volver al índice](#indice)

--

##PROCESOS AL FINAL DEL EJERCICIO.

El proceso del cierre de la contabilidad al final del ejercicio comienza por cerrar previamente la declaración trimestral del IVA siguiendo el proceso que hemos explicado en el apartado anterior. Es importante comprobar que las facturas recibidas y emitidas que tenemos archivadas por fecha, coincidan con el número de orden que le corresponda según el Libro Registro.
Junto con la declaración del último trimestre hay que presentar la Declaración Resumen-Anual del IVA, modelo 390. Para ello basta con acudir a la opción Modelos, Modelo 390 del Módulo Modelos del área Financiera y crear una nueva declaración. 

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-64.png)

Para obtener la declaración es suficiente con pulsar el botón Calcular datos al igual que en las declaraciones anteriores y Eneboo calculará los datos correspondientes a la declaración. Previamente, se deberán rellenar los datos de las diversas ventanas para que se obtenga la declaración completa.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-65.png)

Posteriormente debe obtenerse la declaración de operaciones con terceros superiores a 3.005,06 €. Es necesario tener en cuenta que en este Modelo no deben incluirse aquellos sujetos que hayan figurado en el Modelo 190. Además, deberá comprobarse los volúmenes de operaciones con los mayores de proveedores y clientes o similares, por si existen errores en los apuntes de IVA. La fecha tope para la entrega de este Modelo es el 31 de marzo de cada año. Esta declaración la facilita Eneboo en el Módulo Modelos, menú Modelos, opción Modelo 347.

Al entrar en esta opción, nos aparece parcialmente rellena. Lo único que debemos hacer es comprobar la veracidad de los datos y corregir aquellos que puedan ser erróneos. En nuestro caso, hemos modificado el importe mínimo especificando 3.005,06 y el número de justificante. 

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-66.png)

Antes de calcular el modelo, es conveniente leer las instrucciones que aparecen en la ventana Condiciones, ya que son un recordatorio importante que pretende evitar la obtención de datos erróneos al calcular esta declaración.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-67.png)

Una vez comprobado que todo está correcto, procedemos a calcular la declaración, haciendo clic en el botón Calcular datos se calcula el contenido de la declaración.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-68.png)

A continuación se deben contabilizar los ajustes previos al cierre que procedan:

1. Amortización.
2. Pérdidas de valor.
3. Variación de existencias
4. Provisiones
5. Ajustes en moneda extranjera
6. Periodificación.
7. Reclasificación de deudas.
8. Impuesto de Sociedades

Sólo falta obtener la documentación mercantil relacionada con la contabilidad: los Balances de Comprobación o de Sumas y Saldos trimestrales para incluirlos en el Libro de Inventarios y Cuentas Anuales, así como las cuentas anuales en formato abreviado. También será necesario confeccionar la memoria de Envoltosa y el ejemplar de las cuentas anuales que se debe depositar en el Registro Mercantil. 

Todos estos listados se encuentran en el menú Balances del Módulo Informes del Área Financiera. Dejamos como tarea a los alumnos que los obtengan ellos.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-69.png)

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-70.png)

Por último, es necesario cerrar el ejercicio. Esta operación y la apertura del siguiente se realizan de forma simultánea. Para ello acudimos a la opción Apertura y Cierre del Menú Ejercicio del Módulo Principal del Área Financiera.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-71.png)

Haciendo clic en Cerrar se accede a la siguiente ventana:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-72.png)

En ella ya aparecen introducidos por defecto los datos necesarios, sólo falta especificar a qué ejercicio se va a trasladar el asiento de apertura. 

Para ello, hacemos clic en el botón , apareciéndonos en pantalla la ventana de creación de ejercicios. 

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-73.png)


Pulsando en secuencias por serie añadiremos las series A y AG del ejercicio actual:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-74.png)

Al aceptar la ventana, el programa avisará de:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-75.png)

Pulsando dicho botón, es importante que seleccionemos un ejercicio anterior pues no podemos olvidar que lo que tratamos de hacer es enlazar dos ejercicios. Seleccionamos el ejercicio anterior para que el programa realice el enlace y de esta forma daremos por finalizado el proceso:

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-80.png)
![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-81.png)

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-82.png)

Una vez creado el ejercicio, volvemos a la ventana anterior donde hacemos clic en Cerrar ejercicio.

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-83.png)

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-84.png)

[volver al índice](#indice)

[volver al índice](#indice)

---
###7. CAMBIO DE EJERCICIO.
**Área Financiera>Principal/Ejercicio**

Contenido de Ejercicio:

1. Cambiar actual.
2. Apertura y cierre.
3. Ver todos.

El menú Ejercicio contiene las opciones relacionadas con la gestión de los ejercicios económicos de Eneboo. Ya hemos visto con anterioridad cómo se realiza la creación de los ejercicios, por lo que no insistiremos en este aspecto en estos momentos.

####Cambiar actual.
Esta opción sirve para cambiar de ejercicio. Al hacer clic en ella se nos abre la ventana que mostramos a continuación y que permite

![Asientos predefinidos](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/univ-sevilla-CONTABILIDAD/eneboo-sevilla-conta-85.png)

Esta opción es especialmente útil cuando se está trabajando a caballo entre dos ejercicios, ya que Eneboo no permite introducir los datos de un ejercicio en otro diferente. Para poder hacerlo, previamente es necesario cambiar de ejercicio.

[volver al índice](#indice)

--

