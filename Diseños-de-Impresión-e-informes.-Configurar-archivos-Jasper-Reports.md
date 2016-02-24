* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 26 de agosto de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Dise%C3%B1os-de-Impresi%C3%B3n-e-informes%3A-Configurar-archivos-Jasper-Reports)

---


##### PASO PREVIO 1.- INSTALAR LAS EXTENSIONES +ext9002-jasper_plugin Y +ext1058-jplugin_plus EN EL MÓDULO "INFORMES" CON ENEBOO-TOOLS

Visitar:

https://github.com/Miguel-J/eneboo/wiki/eneboo-reports

##### PASO PREVIO 2.- INSTALAR JAVA Y EL ENLACE A JASPER REPORTS EN EL SERVIDOR DE ENEBOO

https://github.com/Miguel-J/eneboo/wiki/Dise%C3%B1os-de-Impresi%C3%B3n-e-informes.-Instalar-el-enlace-a-Jasper-Reports
 
####REPOSITORIOS GITHUB CON ARCHIVOS YA HECHOS LISTOS PARA USAR:

https://github.com/eneboo/reports4eneboo-reports

---

####INSTALAR JASPER STUDIO (editor de los Jasper-Report)

1. Descargarlo de:

http://community.jaspersoft.com/project/jaspersoft-studio

2. Yo descargo la:

"TIBCOJaspersoftStudio-6.2.0.final-windows-x86_64.zip"

3. En la siguiente ventana poner ABAJO-A-LA-DERECHA: "No, thanks" y te lleva a "sourceforge"...

Tarda 20 minutos...¿?¿?

4. Manual de creación/configuración de archivos .jrxml (en inglés)

http://community.jaspersoft.com/wiki/designing-report-jaspersoft-studio

http://community.jaspersoft.com/wiki/introduction-jaspersoft-studio

* varios tutoriales:

http://community.jaspersoft.com/wiki/jaspersoft-studio-tutorials-archive

---

####ESTRUCTURA DE UN .jrxml

* **PARTE 1**.

`      <?xml version="1.0" encoding="UTF-8"?>`

* **PARTE 2. NOMBRE-TITULO DEL INFORME JASPER**:

`     <jasperReport xmlns="http://jasperreports.sourceforge.net/jasperreports" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports http://jasperreports.sourceforge.net/xsd/jasperreport.xsd" name="SIN LINEAS" language="groovy" pageWidth="595" pageHeight="842" columnWidth="555" leftMargin="20" rightMargin="20" topMargin="20" bottomMargin="20" uuid="f56b01a9-9a77-44db-85ed-a8201e567af9">`

* **PARTE 3. LÍMITES DEL INFORME JASPER**:

`	<property name="ireport.zoom" value="1.5"/>`

	`<property name="ireport.x" value="0"/>`

	`<property name="ireport.y" value="262"/>`

--

* **PARTE 4. ENLACE CON LAS CLÁUSULAS DELIMITADORAS DE ENEBOO**:

`     <parameter name="WHERE" class="java.lang.String" isForPrompting="false">`
      `(...)`
     `<parameter name="ORDERBY" class="java.lang.String" isForPrompting="false">`

NOTA: Esta es la parte más importante del enlace,

EJEMPLO:

...porque "co_i_masterdiario.qs" llama a "flcontinfo.qs" (flcontinfo.iface.pub_lanzarInforme) pero este vuelve a llamar a "flfactinfo.qs" (flfactinfo.iface.pub_mostrarInformeVisor), que es donde está el enlace al jasper (WHERE y ORDERBY)...

--

* **PARTE 5. DEFINIR TABLAS Y COLUMNAS QUE SE USARÁN (y traducirlas al nombre de FIELD-campos que usará Jasper para reconocerlas)**:

NOTA: Cuidado, que TODAS acaban con una COMA....EXCEPTO LA ÚLTIMA....si no: nos dará un ERROR...

`	<queryString>`

		`<![CDATA[SELECT 	facturascli.idfactura as idfactura,`

	`facturascli.codigo as codigofactura,`

	`facturascli.codserie as codserie,`

`(...)`

        `empresa.rmercantil AS rmercantil,`

    	`facturascli.totaleuros AS totaleuros`

`FROM empresa, facturascli`

`INNER JOIN lineasfacturascli ON facturascli.idfactura = lineasfacturascli.idfactura`

`INNER JOIN formaspago ON facturascli.codpago = formaspago.codpago`

`INNER JOIN clientes ON clientes.codcliente = facturascli.codcliente`

`LEFT OUTER JOIN albaranescli ON albaranescli.idalbaran = lineasfacturascli.idalbaran`

`WHERE $P!{WHERE}`

`ORDER BY $P!{ORDERBY}]]>`

	`</queryString>`

* PARTE 6. DEFINIR QUÉ TIPO DE FIELD-CAMPOS SON LOS ELEGIDOS EN EL PASO ANTERIOR:

NOTA: Cuidado, que si no salen todas las anteriores nos dará un ERROR...

`	<field name="idfactura" class="java.lang.Integer"/>`

	`<field name="codigofactura" class="java.lang.String"/>`

	`<field name="codserie" class="java.lang.String"/>`

	`<field name="fechafactura" class="java.sql.Date"/>`

	`<field name="totalfactura" class="java.lang.Double"/>`

* PARTE 7. DEFINIR LAS VARIABLES

`	<variable name="sumaysigue" class="java.math.BigDecimal" resetType="Group" resetGroup="IDfactura" calculation="Sum">`

		`<variableExpression><![CDATA[$F{pvptotallinea}]]></variableExpression>`

	`</variable>`

* PARTE 8. LOCALIZAR CADA FIELD-campo EN EL LUGAR CORRESPONDIENTE:

ZONAS DISPONIBLES:

`		<groupHeader>`

			`<band height="341">`

EJEMPLO:

`                                <textField>`

					`<reportElement x="102" y="272" width="65" height="14" uuid="74a60195-67ff-463d-a72e-13be600801de"/>`

					`<textElement textAlignment="Center" verticalAlignment="Middle">`

						`<font fontName="Arial" size="10" isBold="false"/>`

					`</textElement>`

					`<textFieldExpression><![CDATA[$F{codigofactura}]]></textFieldExpression>`

				`</textField>`




cont´


####JASPER STUDIO - CONCEPTOS


Antes de trabajar con Objetos en IReport debemos realizar algo muy importante, definir las clases que vamos a mostrar en el reporte en el classpath de IReport. Para eso vamos a realizar los siguiente vamos a las opciones de IReport: Tools > Options

---

Este es el navegador, paso a explicar algunos de los ítems.

* Styles: A cada reporte se le puede aplicar distintos estilos, es acá donde se ubican los mismos.

* Parameters: son los parámetros que recibe un reporte a la hora de su creación en tiempo de ejecución, el parámetro fundamental es OBJECT donde se ubica el objeto PRINCIPAL del reporte. Mas a delante voy a explicar con más detalle este parámetro cuando explique el patrón de impresión.

* Fields: los fields son los datos que se van a mostrar en cada una de las filas en el detalle, es decir si nosotros en el detalle vamos a mostrar un detalle de factura, y ese detalle tiene cantidad, descripción, precio unitario y subtotal, entonces en fields tendremos esos atributos, por cada vuelva imprimiremos esos datos. Los fields se puede definir a partir de una consulta o de un JavaBeansDataSource que es caso que vamos a utilizar nosotros.

* Variables: Las variables son usadas para realizar cálculos y guardarlos para luego ser mostrados en el reporte. Las variables por defecto son cantidad de páginas, cantidad de columnas, página actual, etc.


---

Actualmente se tiene las siguientes formas de impresión:

printToPDFArchive(Object object, String pathToExport, InputStream pathJRXML): imprime en pDF. (Ver JavaDoc)

printToPrinter(Object object, boolean withDialog, String pathJRXML): impresión a dispositivo de impresión. (Ver JavaDoc).

---