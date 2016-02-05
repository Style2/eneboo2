* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 3 de febrero de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/GITHUB---avanzado---repos-y-ramas)

----

# GITHUB - avanzado - repos y ramas

fuente: https://git-scm.com/book/es/v1

#### 1. LISTAR LAS RAMAS:

     $ git branch

Si lo lanzas sin argumentos, obtienes una lista de las ramas presentes en tu proyecto:

#### 2. ASOCIAR OTROS REPOS:

Para añadir un nuevo repositorio Git remoto, asignándole un nombre con el que referenciarlo fácilmente, ejecuta git remote add [nombre] 

     C:\github\eneboo-features-oficial [master]> git remote add ef git://github.com/Miguel-J/eneboo-features.git

#### 3. LISTAR REPOS ASOCIADOS:

     `C:\github\eneboo-features-oficial [master]> git remote -v`
     `ef      git://github.com/Miguel-J/eneboo-features.git (fetch)`
     `ef      git://github.com/Miguel-J/eneboo-features.git (push)`
     `origin  https://github.com/Miguel-J/eneboo-features-oficial (fetch)`
     `origin  https://github.com/Miguel-J/eneboo-features-oficial (push)` 

#### 4. IMPORTAR EL CÓDIGO DE OTRO REPO EN SUB-"RAMAS"

     C:\github\eneboo-features-oficial [master]> git fetch ef

#### 5. CREAR UNA RAMA:

     C:\github\eneboo-features-oficial [master]> git branch ef/master

#### 6. CAMBIAR DE RAMA:

     `C:\github\eneboo-features-oficial [master]> git checkout ef/master`
     `warning: refname 'ef/master' is ambiguous.`
     `Switched to branch 'ef/master'`
     `C:\github\eneboo-features-oficial [ef/master]>`

#### 7. TRAER CAMBIOS DEL OTRO REPO:

C:\github\eneboo-features-oficial [ef/master]> git pull https://github.com/Miguel-J/eneboo-features

     remote: Counting objects: 270, done.
     Receiving objects: 100% (270/270), 170.52 KiB | 0 bytes/s, done.sed 129
     `Resolving deltas: 100% (152/152), completed with 62 local objects.`
     `From https://github.com/Miguel-J/eneboo-features`
     `* branch            HEAD       -> FETCH_HEAD`
     `Auto-merging ext0450-envio_mail/patches/envio_mail/masterpresupuestoscli.qs`
     `CONFLICT (content): Merge conflict in ext0450-envio_mail/patches/envio_mail/masterpresupuestoscli.qs`
     `Auto-merging ext0450-envio_mail/patches/envio_mail/masterpedidoscli.qs`
     `CONFLICT (content): Merge conflict in ext0450-envio_mail/patches/envio_mail/masterpedidoscli.qs`
     `Auto-merging ext0450-envio_mail/patches/envio_mail/masterfacturascli.qs`
     `CONFLICT (content): Merge conflict in ext0450-envio_mail/patches/envio_mail/masterfacturascli.qs`
     `Auto-merging ext0450-envio_mail/patches/envio_mail/masteralbaranescli.qs`
     `CONFLICT (content): Merge conflict in ext0450-envio_mail/patches/envio_mail/masteralbaranescli.qs`
     `Automatic merge failed; fix conflicts and then commit the result.`
     `C:\github\eneboo-features-oficial [ef/master +32 ~36 -0 !4 | +0 ~0 -0 !4]>`

#### 8. ELIMINAR PROBLEMAS:

????

     "error: you need to resolve your current index first"

http://schacon.github.io/git/user-manual.html#resolving-a-merge

     `"All you need to do is edit the files to resolve the conflicts, and then`
     `$ git add file.txt`
     `$ git commit`
     `"`
--

copio los 4 archivos en el "repo-puente de klo"...

...subo al "repo-puente de klo"...

...ramifico ese "repo-puente-modificado" en el "repo-copia-de-eneboo-local"...

...subo cambios al "repo-copia-de-eneboo-online"...

...borro "repo-puente-modificado" y vuelvo a hacer fork del "repo-klo"...

...hago "pull-request" desde "repo-copia-de-eneboo-online" con los commits de klo HACIA repo-eneboo-features de Eneboo...



9. UNIR LAS DOS RAMAS:

