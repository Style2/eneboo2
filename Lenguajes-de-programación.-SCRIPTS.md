* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 22 de noviembre de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Lenguajes-de-programaci%C3%B3n.-SCRIPTS)

----

Lenguajes de programación. SCRIPTS
-----------------------------


#####Extensión de archivos: .qs

Se pueden abrir con:

* "Wordpad".
* "Sublime Text2" y luego con "Ctrl + Shift + P" y elegir "S" y buscar "Set Syntax: JavaScript".....oculta las líneas inactivas y separa por colores los distintos elementos...

---

#####Añadir un comentario:

`/**********`
`**aquí escribes lo que quieras, para aclarar lo que hace ese código`
`*****************/`

---

#####ESTRUCTURA:

1. Título
1. Declaración de funciones
1. Definición de funciones

--
1. Título:

ejemplo:

     `/***************************************************************************`
                      `i_masterclientes.qs  -  description`
                             `-------------------`
         `begin                : mar jun 27 2006`
         `copyright            : (C) 2006 by InfoSiAL S.L.`
         `email                : mail@infosial.com`
      `***************************************************************************/`

      `/***************************************************************************`
      `*                                                                         *`
      `*   This program is free software; you can redistribute it and/or modify  *`
      `*   it under the terms of the GNU General Public License as published by  *`
      `*   the Free Software Foundation; either version 2 of the License, or     *`
      `*   (at your option) any later version.                                   *`
      `*                                                                         *`
      `***************************************************************************/`

--

2. Declaración de funciones

Sirve para "informar" al programa sobre TODAS las funciones en juego, y así se evita tener que poner las funciones en orden y que dé error porque no se ha definido una función: le dice al programa que **"si no tienes definida una función, que la busques más adelante"** en la zona de **"Definición de funciones"**.

ejemplo:


     `/** @class_declaration interna */`
     `////////////////////////////////////////////////////////////////////////////`
     `//// DECLARACION ///////////////////////////////////////////////////////////`
     `////////////////////////////////////////////////////////////////////////////`

     `//////////////////////////////////////////////////////////////////`
     `//// INTERNA /////////////////////////////////////////////////////`
     `class interna {`
         `aquí se pone un listado de las variables y funciones`
     `}`
     `//// INTERNA /////////////////////////////////////////////////////`
     `//////////////////////////////////////////////////////////////////`


--

3. Definición de funciones

Desarrollo de lo que hace cada función

ejemplo:


     `/** @class_definition interna */`
     `////////////////////////////////////////////////////////////////////////////`
     `//// DEFINICION ////////////////////////////////////////////////////////////`
     `////////////////////////////////////////////////////////////////////////////`

     `//////////////////////////////////////////////////////////////////`
     `//// INTERNA /////////////////////////////////////////////////////`
     `function interna_init()`
     `{`
        	`connect (this.child("toolButtonPrint"), "clicked()", this, "iface.lanzar()");`
     `}`
     `//// INTERNA /////////////////////////////////////////////////////`
     `/////////////////////////////////////////////////////////////////`

