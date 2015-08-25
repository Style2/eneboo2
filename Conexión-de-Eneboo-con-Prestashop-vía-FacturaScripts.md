* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 20 de agosto de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Conexi%C3%B3n-de-Eneboo-con-Prestashop-v%C3%ADa-FacturaScripts)

----
###MANUAL DE CONEXIÓN DE ENEBOO CON PRESTASHOP (A TRAVÉS DE FACTURASCRIPTS)



####0.- PASO 0: PREPARAR LA BASE DE DATOS-PRELIMINARES:


#####0.A.- PASO PREVIO B: VERIFICAR CÓDIGOS DE IMPUESTOS:
Ir a la parte de “Area Facturación-Principal-Impuestos” y verificar que no hay impuestos duplicados. En principio para 2015 debe haber sólo:
a) impuesto general= 21% =”GEN”
b) impuesto reducido= 7%=”RED”
c) impuesto super-reducido= 4%=”SRED”
d) impuesto exportación-EU= 0%=”EU VAT”

NOTA-1: lineasalbaranescli...tiene marcados todos como tipo “3” cuando el resto es “GEN”...????
UPDATE lineasalbaranescli SET codimpuesto=”GEN”; 

NOTA-2: lineasivafactcli...tiene marcados ALGUNOS como tipo “3” cuando el resto es “GEN”...????
UPDATE lineasivafactcli SET codimpuesto=”GEN”; 

NOTA-1: lineasalbaranesfact...tiene marcados todos como tipo “3” cuando el resto es “GEN”...????
UPDATE lineasalbaranesfact SET codimpuesto=”GEN”; 


#####0.B.- PASO PREVIO B: COMPROBAR QUE TODOS LOS PRODUCTOS TIENEN SU FAMILIA 
(articulos.codfamilia)

#####0.C.- PASO PREVIO C: AÑADIR UNA SERIE PARA VENTAS DE PRESTASHOP
Te ahorra problemas de sincronización luego (número de factura, etc).


#####0.D.- PASO PREVIO D: COMPROBAR QUE TODOS LOS PRODUCTOS TIENEN PRECIO
El proceso no permite productos con precio 0...
Ejemplo: 

UPDATE articulos SET pvp=990 WHERE pvp=0;

#####0.E.- PASO PREVIO E: COMPROBAR QUE TODOS LOS PRODUCTOS TIENEN “STOCK” POSITIVO
El proceso no permite productos con stock negativo...

a)TABLE: articulos COLUMN: stockfis
UPDATE articulos SET stockfis=888 where stockfis=0;----------BIEN
UPDATE articulos SET stockfis=888 where stockfis IS NULL;----BIEN
UPDATE articulos SET stockfis=888 where stockfis=0;----------BIEN
b) TABLE:stocks COLUMN:cantidad
UPDATE stocks SET cantidad=990;----------BIEN
c)TABLE:stocks COLUMN:disponible
UPDATE stocks SET disponible=990;----------BIEN


#####0.F.- PASO PREVIO F: COMPROBAR QUE LOS ARTICULOS NO TENGAN SÍMBOLOS “RAROS” EN NOMBRES O DESCRIPCIONES.

El proceso NO TOLERA: “=”, etc...

---

***

1.- PASO 1: CREAR UNA BASE DE DATOS EN UN SERVIDOR

2.- PASO 2: CARGAR LOS DATOS DE LA COPIA DE SEGURIDAD

3.- PASO 3: COPIAR FACTURASCRIPTS EN UN DIRECTORIO DEL SERVIDOR

4.- PASO 4: ABRIR UN NAVEGADOR Y VISITAR EL DIRECTORIO DONDE SE HA COPIADO FACTURASCRIPTS

5.- PASO 5: INSTALAR FACTURASCRIPTS SOBRE LA BASE DE DATOS DE ENEBOO

6.- PASO 6: INSTALAR PRESTASHOP 1.6.1

7.- PASO 7: IR A web service

8.- PASO 8: IR A PANEL DE CONTROL Y PONER LA CLAVE WEB

9.- PASO 9: COORDINAR LOS IMPUESTOS DE FACTURASCRIPT CON LOS DE PRESTASHOP

10.- PASO 10: COPIAR LAS FAMILIAS DE ENEBOO COMO CATEGORIAS DE PRESTASHOP





20.- PASO 9: ACTIVAR EL CRON EN FACTURASCRIPTS

21.- PASO 10: IR AL PANEL DE CONTROL DEL HOSTING Y BUSCAR TAREAS CRON

11.- PASO 11: 
