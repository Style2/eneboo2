* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 3 de febrero de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/GITHUB---avanzado---repos-y-ramas)

----

# GITHUB - avanzado - repos y ramas

fuente: https://git-scm.com/book/es/v1

1. LISTAR LAS RAMAS:

$ git branch

Si lo lanzas sin argumentos, obtienes una lista de las ramas presentes en tu proyecto:

2. ASOCIAR OTROS REPOS:

Para añadir un nuevo repositorio Git remoto, asignándole un nombre con el que referenciarlo fácilmente, ejecuta git remote add [nombre] 

C:\github\eneboo-features-oficial [master]> git remote add ef git://github.com/Miguel-J/eneboo-features.git

3. LISTAR REPOS ASOCIADOS:

`C:\github\eneboo-features-oficial [master]> git remote -v`
`ef      git://github.com/Miguel-J/eneboo-features.git (fetch)`
`ef      git://github.com/Miguel-J/eneboo-features.git (push)`
`origin  https://github.com/Miguel-J/eneboo-features-oficial (fetch)`
`origin  https://github.com/Miguel-J/eneboo-features-oficial (push)` 

4. IMPORTAR EL CÓDIGO DE OTRO REPO EN SUB-"RAMAS"

C:\github\eneboo-features-oficial [master]> git fetch ef

5. CREAR UNA RAMA:

C:\github\eneboo-features-oficial [master]> git branch ef/master

6. CAMBIAR DE RAMA:

`C:\github\eneboo-features-oficial [master]> git checkout ef/master`
`warning: refname 'ef/master' is ambiguous.`
`Switched to branch 'ef/master'`
`C:\github\eneboo-features-oficial [ef/master]>`

