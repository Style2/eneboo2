https://groups.google.com/forum/#!topic/eneboo/eVkmQNMUzGQ


1. **mfdezp    27/8/12**
Me acabo de Instalar el Python en Windows, pero siguiendo la guia de las Eneboo-tools, me dice que lo primero que hay que hacer es tener una serie de librerías (que no sé como tenerlas operativas para python en windows) y luego hacer un 
_sudo make install_ (que entiendo que es la instalación en linux). 

2. **Aulla Sistemas**
Mi recomendación es que te instales un linux tipo ubuntu 10.10 en una máquina virtual.

3. **David Martínez Martí**
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

###esto lo meto aquí, de momento:



2º) Me leeré la documentación de las toos, aunque con lo que me acabas de enviar empiezo a entender cosas. En cuanto tenga instalada las tools y acceso al Git. Empezaré a practicar. hablas de ficheros qs, xml y qsdir (que no se que es lo que es). Pero y qué pasa con los forms, las querys y los informes? Me pones que se reescriben, eso que significa que no podré saber las diferencias? ¿De las tablas (.mtd) tampoco?





los "formatos" son eso, formatos. Hay muchas extensiones con el mismo formato. Y varios "formatos" para la misma extensión. 




Por ejemplo, QS y QSDir son para ficheros *.qs; lo único es que el segundo es más .... agresivo, llega más lejos extrayendo y aplicando cambios. El primero sólo pone y quita clases.




En el caso de los XML, prácticamente todos los otros ficheros son XML. Actualmente reconoce *.ui (formularios), *.mtd (tablas) y *.xml (acciones). Experimentalmente soporta *.kut (reports).




Pero en el caso de los folder-diff y folder-patch, las extensiones *.qry, *.kut directamente se sobreescribirán. 

El motivo de que se sobreescriban es que la herramienta original de InfoSial lo hacía así y mi objetivo inicial era conseguir el mismo resultado.


 


3º) Aunque ya se que es una tontería, cómo monto, por ejemplo en ubuntu Python (me imagino que de esto si habrá cosas en internet). Pero por si hay que hacer algo específico. Tampoco entiendo la instalación de las eneboo-tools.






Todo funciona con paquetes en Linux. Ubuntu tiene un instalador de paquetes, no sé si el synaptics. En ese programa buscas python y el resto de dependencias (nombres de paquete), le das a instalar y listo. Él se encarga de todo.




O para instalar desde consola sería: $ sudo apt-get install $paquete1 $paquete2 $paqueteN




... es indiferente si lo instalas por consola o por entorno gráfico, el resultado es idéntico.

