Primeros pasos con Abanq
En este breve documento veremos el funcionamiento general de la aplicación en cuanto a módulos, áreas y formularios.
Organización de los módulos
La configuración está estructurada en los siguientes elementos: 
Áreas. Representan grandes agrupaciones funcionales (facturación, contabilidad, producción,...). 
Módulos. Cada área, a su vez, está dividida en módulos, que cubren una determinada faceta del área a la que pertenecen (por ejemplo, en el área Facturación, los módulos tesorerí­a, almacén...). 
Acciones. Las acciones determinan las posibles operaciones que el usuario puede realizar en un determinado módulo (por ejemplo en el módulo almacén del área Facturación, están las acciones de gestión de artí­culos, gestión de stocks, etc.). Generalmente, accedemos a las acciones desde la ventana principal de cada módulo. 
Dependencias. Los módulos están integrados unos con otros. Por ejemplo, al usar el módulo facturación del área Facturación para dar de alta un pedido a cliente, podemos seleccionar dicho cliente de una lista que reside en el módulo principal del área de Facturación. Esta integración, necesaria para reaprovechar datos y funcionalidad existentes, implica que algunos módulos no pueden ser instalados sin haber instalado previamente aquellos de los que dependen. Abanq controla estas dependencias y avisa al usuario cuando alguna de ellas no se cumple. 
Modo general de funcionamiento
Abanq muestra la información al usuario siguiendo un esquema maestro - detalle. La interfaz de usuario se estructura de la siguiente forma:
Ventana de inicio
El la ventana de inicio por defecto de Abanq, y la que da acceso a las áreas. Cada área despliega sus módulos. También accedemos a las opciones generales del programa (Configuración).
Ventana de inicio
Ventana principal del módulo
Cada módulo tiene una ventana en la que se ofrece al usuario el conjunto de acciones disponibles. Estas acciones son accesibles desde la barra de menú o la barra de herramientas de la ventana.
En cada una de las ventanas principales disponemos de un menú Módulos que permite cambiar a otras áreas y módulos.
Ventana principal del módulo de facturación.Vemos los menús y barra de herramientas
Formulario maestro
En primer lugar, accederemos siempre a un formulario maestro desde la opción de la página principal del módulo. En este formulario maestro se nos ofrece una lista con los registros que existen para la acción seleccionada. Desde aquí­ podemos seleccionar el registro sobre el que actuaremos y la operación a realizar (creación, modificación, borrado, copia, etc.).
Operaciones con un formulario maestro:
Buscar. En la casilla buscar podemos teclear el texto a buscar. Abanq lo buscará dentro de la primera de las columnas de la tabla. Se puede utilizar el carácter comodín %. Veamos algunos ejemplos suponiendo que la primera columna es el número de entidad bancaria en el formulario maestro de bancos. Si tecleamos %8 estamos buscando todos los bancos cuyo número de entidad termina por 8. Si tecleamos 0%2 obtenemos todas las entidades que comienzan por 0 y terminan por 2, y así sucesivamente.
Ordenar. El formulario maestro siempre ordena de menor a mayor por la primera de las columnas mostradas. Podemos cambiar la primera de las columnas mediante el control desplegable que aparece a la derecha del cuadro de búsqueda.
Formulario maestro de bancos, dentro del módulo principal de facturacion
Formulario de edición
Una vez seleccionados el registro y la operación a realizar, Abanq nos muestra un formulario de detalle, en el que podemos actuar sobre cada uno de los campos que componen el registro seleccionado. Es posible anidar esta estructura de forma que en un formulario de detalle se incluya una lista de registros que abra, a su vez, un segundo formulario de detalle.
Formulario de edición de bancos
Teclas de acceso rápido
Las teclas de acceso rápido facilitan y agilizan enormemente el trabajo diario. Veamos las más importantes:
Desde cualquier formulario
Cerrar una ventana. Esc. Para cerrar una ventana tanto de módulo como de formularios maestro o de edición, basta pulsar la tecla escape (Esc).
Desde un formulario maestro
Crear un nuevo registro. A. Cuando el foco está situado en una tabla, dentro de un formulario maestro o de edción, la pulsación de la tecla A equivale al botón Añadir registro, abriendo un formulario de introducción de un nuevo registro.
Editar un registro. M/Intro. Situado el cursor sobre un registro de una tabla en un formulario maestro o de edción, la pulsación de las teclas M o Intro equivale al botón Modificar registro, abriendo el registro seleccionado en modo edición.
Ver un registro en sólo lectura. V. Situado el cursor sobre un registro de una tabla en un formulario maestro o de edción, la pulsación de la teclas V equivale al botón Ver registro, abriendo el registro seleccionado en modo de sólo lectura.
Eliminar un registro. E/Supr. Situado el cursor sobre un registro de una tabla en un formulario maestro o de edción, la pulsación de las teclas E o Suprimir (Supr) equivale al botón Eliminar registro, borrando el registro seleccionado, previa confirmación del usuario.
Copiar un registro. C. Algunas tablas contienen este botón que permite hacer un duplicado del registro activo. No obstante el resultado depende de la tabla y es posible que sólo se copien los datos generales y no los registros relacionados si los hay. Situado el cursor sobre un registro de una tabla en un formulario maestro o de edción, la pulsación de la tecla C equivale al botón Copiar registro, creando un nuevo registro a partir del registro seleccionado.
Desde un formulario de edición
Saltar de campo. Tab/Intro. Al pulsar tabulador (Tab) o Intro saltamos al siguiente campo. El orden de tabulación está predefinido para cada formulario. Intro equivale a Tab salvo en los campos de texto largo en los que tiene su función normal de salto de línea.
Campos relacionados. F2/+. En un formulario de edición, son aquellos cuyo valor ha de seleccionarse escogiendo uno de los registros de otra tabla (tabla relacionada); por ejemplo, en una cuenta bancaria podemos seleccionar el campo relacionado Entidad escogiendo un registro de la tabla de bancos. Estos campos aparecen en el formulario de edición con el icono de búsqueda (una lupa). Situado el cursor en uno de estos campos se puede abrir la tabla relacionada pulsando F2 o la tecla +.
Navegar por los registros. F5-F8. Dentro del formulario de edición, es posible avanzar por los registros cuando estamos en modo de edición o de vista (sólo lectura). Las teclas son F5 (primer registro), F6 (registro anterior), F7 (registro siguiente), F8 (último registro)
Guardar un registro y cerrar el formulario. F10. Dentro del formulario de edición, en modo nuevo registro o edición, pulsando F10 se guarda el registro.
Guaradar un registro e insertar otro nuevo. F9. Dentro del formulario de edición, en modo nuevo registro o edición, pulsando F9 se guarda el registro y se abre otro nuevo en modo nuevo registro.
Actualizado el 01/10/2007
