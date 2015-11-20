* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 25 de octubre de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Lenguajes-de-programaci%C3%B3n.-Introducci%C3%B3n)

----

Lenguajes de programación. Introducción
-----------------------------

####SINTAXIS POR LENGUAJES:

Se utilizan dos tipos de lenguajes:

1.- **Lenguaje QSA**. Es el utilizado en los **scripts** de los módulos, basado en ECMAScript (y por tanto muy parecido a **JavaScript**). No necesita ser compilado.

1.- **Lenguaje C++**. Es el utilizado para crear el núcleo de Eneboo (esto es, las aplicación base). Se utiliza el Qt, una biblioteca multiplataforma para desarrollar interfaces gráficas de usuario. Utiliza el lenguaje **C++** pero permite usar también C, Python y Perl, además cuenta con soporte para acceder a bases de datos mediante SQL, XML y API para el manejo de ficheros.

--

* **Nota**: Python utiliza retornos de carro para separar sentencias y los dos puntos y el sangrado para reconocer bloques de código. C++ y Java usan punto y coma para separar sentencias, y llaves para indicar bloques de código.

--

####ESTRUCTURA DE UN MÓDULO POR TIPOS DE ARCHIVOS:

Cada tipo de archivo tiene "su" lenguaje o forma de escribir las órdenes, y en la MEZCLA se agrupan por carpetas:

* **forms**. Definiciones de los formularios. Cada formulario se define en un archivo de extensión ui

* **queries**. Definiciones de las consultas. Cada consulta se define en un archivo de extensión qry

* **reports**. Definiciones de los informes. Cada informe se define en un archivo de extensión kut

* **scripts**. Definiciones de los scripts. Cada script se define en un archivo de extensión qs

* **tables**. Definiciones de las tablas. Cada tabla se define en un archivo de extensión mtd

* **translations**. Listados de traducciones. Cada listado de traducciones para un determinado idioma se define en un archivo de extensión ts


---

1. FORMS

1. QUERIES

1. REPORTS

1. SCRIPTS:

Ejemplo:

        function nomFuncion()
        {
            ........
            ........
            return x;
        }

1. TABLES

1. TRANSLATIONS

