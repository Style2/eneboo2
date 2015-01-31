https://groups.google.com/forum/#!topic/eneboo/eVkmQNMUzGQ


1. **mfdezp    27/8/12 **
 
Hola Aulla Sistemas (todavía no tengo controlado tu nombre).

Me acabo de Instalar el Python en Windows, pero siguiendo la guia de las Eneboo-tools, me dice que lo primero que hay que hacer es tener una serie de librerías (que no sé como tenerlas operativas para python en windows) y luego hacer un 
_sudo make install_ (que entiendo que es la instalación en linux). 

1. **Aulla Sistemas**
Mi recomendación es que te instales un linux tipo ubuntu 10.10 en una máquina virtual.

1. **David Martínez Martí**
En windows las librerías de python se descargan como ejecutables (instaladores). Para cada versión menor de Python  (2.5.x, 2.6.x) hay un instalador distinto. 

Entonces, en resumen, lo que hay que hacer es: 

- Identificar tu versión de Python, supongamos que es 2.7.3 
- Identificar el paquete, por ejemplo "python-lxml" 
- Buscar la página del proyecto con google (por ejemplo, busca <python lxml>) 
- Localizar las descargas del proyecto para Windows, y bajar la 
adecuada para tu versión de Python 
- Ejecutar el instalador y seguir los pasos (siguiente, siguiente, etc) 

Y se repite el proceso para el resto de librerías. 

De todos modos, la consola de Windows se quedará un poco "corta" para 
manejar estos programas.... y yo recomendaría la solución de Aulla, 
una máquina virtual. 


