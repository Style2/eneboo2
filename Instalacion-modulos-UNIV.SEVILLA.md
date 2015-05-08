* CREADO POR: [Universidad de Sevilla](http://www.us.es): Guillermo Molleda Jimena y adaptado por: miguelajsmaps@gmail.com
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 8 de mayo de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalacion-modulos-UNIV.SEVILLA)

----
###nota: El presente manual fue desarrollado para AbanQ, antecedente de Eneboo, que comparten la misma estructura de archivos...


####INSTALACIÓN DE LOS MÓDULOS DEL ERP AbanQ




Índice de contenido
Instalación de los módulos del ERP AbanQ:	2
Requisitos para la instalación	2
Instalación de los módulos	2

##Instalación de los módulos del ERP AbanQ:

###Requisitos para la instalación

Debemos tener instalado el cliente AbanQ y un servidor de bases de datos, éste puede ser PostgreSQL o MySQL.

Existen dos posibles formas de instalar los módulos, la primera a partir de los ficheros fuente de los mismos, esta será la manera que explicaremos en este capítulo; la segunda sería a partir de una copia de seguridad con los módulos ya instalados, la creación de copias de seguridad y su restauración se explicó en el apartado correspondiente al servidor de bases de datos, por lo que no vemos necesario volver a explicarlo aquí.

En el aula de informática no es necesario realizar este proceso, pues ya está creada la base de datos con los módulos del ERP (Enterprise Resource Planning) instalados.

###Instalación de los módulos

Antes de empezar a instalar los módulos debemos bajarlos de internet y descomprimir los ficheros descargados en nuestro disco duro. Aunque en la web de AbanQ hay unos módulos básicos de contabilidad y facturación gratuitos, nosotros utilizaremos los módulos personalizados disponibles en la plataforma de enseñanza virtual de la asignatura. Sigan los siguientes pasos:

1. Descarguen el fichero 'modulos.zip'
2. Descompriman el fichero, para ello abran la carpeta del disco duro donde hayan guardado 'modulos.zip' y pulsen sobre el mismo con el botón derecho del ratón, entre las opciones elijan 'Extraer aquí', 'Extraer todo' o la que crean que descomprimirá el fichero (dependerá del programa de compresión que tengan instalado en el equipo). Si os pregunta el directorio donde descomprimirlo, elijan la raíz del disco local C:.
3. Tras lo anterior debe haberse creado una carpeta llamada 'modulos', si no preguntó dónde descomprimirla, muevan la carpeta a la raíz de la unidad C:, de tal forma que quede como en la imagen de debajo. En los sistemas operativos GNU/Linux o Mac OS X, descompriman el fichero en la carpeta del usuario (/home/Usuario).

Comencemos creando la base de datos, ejecuten el programa AbanQ, pulsen el botón vertical de la derecha y elijan los siguientes datos:

Base de datos: envoltosa
Usuario: postgres
Contraseña: alumno
Controlador: PostreSQL o MySQL según el gestor de bases de datos instalado.
Servidor: localhost
Puerto: 5432 si se usa PostgreSQL, 3306 si usa MySQL.


Atención: Posible ventana de error. Si en este paso aparece el error de conexión fallida, y la razón del error: “No se puede conectar a la base de datos”. Reinicien el servidor PostgreSQL con el menú Inicio - Todos los programas – PostgreSQL 8.X – Stop service seguido de Start service en el mismo lugar. Si esto no arreglara el problema, vuelvan a intentar instalar PostgreSQL (desinstalándolo primero como se indica en el apartado correspondiente).

Otro error puede darse por una incorrecta carga del controlador de la base de datos, en este caso se resolvió desinstalando y volviendo a instalar el programa cliente AbanQ:


Si todo ha ido bien, nos preguntará si deseamos crear la nueva base de datos, a lo que responderemos que sí:
El programa AbanQ se abre presentando una ventana con un botón para Salir de la aplicación y tres apartados llamados áreas: Sistema, Configuración y Ayuda.
En el área de Sistema tenemos cargado un módulo de Administración con el cual después podremos agregar nuestros módulos personalizados; en el área de Configuración podremos modificar el tipo de letra o fuente utilizadas por la interfaz del programa, así como cambiar el aspecto del mismo con una serie de estilos predeterminados. En el área de Ayuda se puede ver un enlace a la documentación del programa en Internet y la información referente a licencias y créditos sobre sus autores.

Abran el módulo Administración del Área de Sistema para comenzar con la instalación del resto de módulos. Al principio puede preguntar si queremos que se carguen automáticamente los módulos gratuitos de facturación y financiera: Digan que NO.


Los módulos que vamos a usar deben descargarlos de la web de la asignatura y  descomprimirlos en el directorio C:\modulos o en un directorio cuya ruta conozcamos (en GNU/Linux y Mac OS X en /home/Usuario/modulos). La ventana que se abre al pulsar Administración tiene varios botones en la barra de herramientas, pulsen sobre el tercero para abrir la tabla de módulos cargados en nuestra base de datos, o bien usen el menú Principal - Módulos:


Al principio sólo está cargado el módulo de Administración (sys), elijan la opción del menú Principal – Cargar módulo y contestar sí a la pregunta sobre que hagan antes una copia de seguridad y no existan usuarios conectados:
En la ventana de elección del módulo a cargar, busquen en primer lugar el módulo Principal del área de Facturación situado en C:\modulos\1facturacion\1principal. Como pueden comprobar, los directorios de la carpeta módulos son las áreas en que se de divide el ERP: Facturación, colaboración, contabilidad y CRM, mientras que dentro de cada área se encuentran los módulos que la componen. Además se ha añadido un '1' delante del nombre de algunas carpetas para señalar las primeras que hay que instalar.


El motivo de comenzar por Facturación – Principal es que se trata del centro neurálgico del sistema de módulos de AbanQ, contiene una serie de tablas y datos básicos que lo hacen esencial para los demás módulos del ERP. Por tanto prosigamos con la carga de este módulo seleccionando el fichero flfactppal.mod como vemos en la siguiente ilustración:


Una vez que abramos el módulo aparecerá el acuerdo de licencia del mismo para que lo aceptemos (ver la ilustración 12) y tras hacerlo nos avisará de la creación si no existiera de una nueva Área de módulos (ilustraciónes 13 y 14).

####En general lo importante es que la carga de los módulos debe empezar por el llamado Principal, ya que contiene información y tablas necesarias para el resto de módulos de cada Área.



A continuación se ejecuta la carga del módulo en una ventana como la de la ilustración 15.



Si al querer instalar el primer módulo en AbanQ, tras crear el área de Facturación y una vez comienza la carga del módulo, apareciera el error “QPSQL: La consulta a la base de datos ha fallado. ERROR: Transaccion abortada, las consultas serán ignoradas hasta el fin de bloque de transacción". Este error puede aparecer por haber instalado la versión 8.3 de PostgreSQL, en vez de la 8.2 como se especifica en el manual. Si fuera el caso, habría que desinstalar PostgreSQL 8.3 e instalar PostgreSQL 8.2, aunque es posible tener ambas, habría que configurar puertos de conexión diferentes para conectar AbanQ con la base de datos, el puerto por defecto es el 5432. Debido al error, tal vez tengan que reiniciar el equipo para recuperar el control del mismo.

Si el error del programa fuera el cierre repentino de la aplicación durante la carga de cualquier módulo, deben repetir el último paso de carga con el mismo módulo que se estuviera trabajando en el momento del cierre, ya que podría no haberse completado esa última operación de carga de todos los ficheros necesarios.

Una vez terminado todo el proceso de instalación de módulos, deben entrar primero en el área de facturación - módulo principal, tras crear la empresa, accedan al área de facturación – módulo almacén para crear un almacén y finalmente en el área de contabilidad – módulo principal para crear el plan general contable.
