* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 13 de marzo de 2016
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

copio los 4 archivos en el "repo-puente de klo" (local)...

...subo al "repo-puente de klo" (online)...


#### 9. UNIR LAS DOS RAMAS:

...ramifico ese "repo-puente-modificado" en el "repo-copia-de-eneboo-local"...

     ?????...quieres decir que el "fetch" era necesario?
     C:\github\eneboo-features-oficial [master]> git pull https://github.com/Miguel-J/eneboo-features

...subo cambios al "repo-copia-de-eneboo-online"...

     C:\github\eneboo-features-oficial [master]> git push https://github.com/Miguel-J/eneboo-features-oficial master

...hago "pull-request" desde "repo-copia-de-eneboo-online" con los commits de klo HACIA repo-eneboo-features de Eneboo...

...a esperar el "merge"...o no.

...borro "repo-puente-modificado" y vuelvo a hacer fork del "repo-klo"...

---

#### 10. VARIOS:

https://elbauldelprogramador.com/mini-tutorial-y-chuleta-de-comandos-git/

---

#### 11. UNIR SÓLO ALGUNOS COMMITS CON GIT CHERRY-PICK (PULL REQUESTS PARCIALES):

1. Han rechazado el Pull Request total

1. Elimino los dos repos (el copia de eneboo-oficial y el copia de klo) y los vuelvo a descargar

1. Hago un "git pull" del klo HACIA el eneboo-oficial....vuelve a dar error en "ext450"

1. Elimino la carpeta "ext450" en klo y le meto la "ext450" de "eneboo-oficial"

1. Hago un "add./commit-a/push" en el de klo-local hacia el klo-remoto

1. Vuelvo a hacer un "git pull" del klo-remoto HACIA el eneboo-oficial-local...lo aplica bien.

1. Hago un "push" en el de eneboo-oficial-local hacia el eneboo-oficial-remoto

1. Ahora LOS DOS REMOTOS SON IGUALES (con ext450 de "eneboo-oficial")

1. Hago un fork  en "Arreglogithub" de "eneboo-features-oficial", envío un Pull-Request TOTAL desde Miguel-J, borro el repo en Miguel-J y hago otro fork de "eneboo-features-oficial"

1. Ahora LOS DOS REMOTOS SON DISTINTOS: "klo-remoto" y "arreglogithub" son IGUALES (con ext450 de "eneboo-oficial") pero "eneboo-oficial" es el original de "eneboo-features".

--

1. Añado la relación del repo "arreglogithub" EN EL repo "eneboo-oficial":

        C:\GitHub\eneboo-features-oficial [master]> git remote add arreglogithub git://github.com/arreglogithub/eneboo-features-oficial.git

1. Añado el contenido de esa relación:

         C:\GitHub\eneboo-features-oficial [master]> git fetch arreglogithub
          remote: Counting objects: 286, done.
          Receiving objects: 100% (286/286), 148.51 KiB | 0 bytes/s, done.ed 140 eceiving objects:  97% (278/286)

          Resolving deltas: 100% (160/160), completed with 62 local objects.
          From git://github.com/arreglogithub/eneboo-features-oficial
          * [new branch]      master     -> arreglogithub/master
         C:\GitHub\eneboo-features-oficial [master]>

1. (Opcional): Lista de "commits":

         C:\GitHub\eneboo-features-oficial [master]> git log arreglogithub/master

1. Escoger el commit a importar/enviar:

         C:\GitHub\eneboo-features-oficial [master]> git cherry-pick c245e97
         [master ef86611] arreglo funcion vaciar tablas y añado el qry
          Date: Fri Nov 27 11:06:59 2015 +0100
          3 files changed, 34 insertions(+), 4 deletions(-)
          create mode 100644 ext0068-info_ventascli/patches/info_ventascli/i_ventascli.qry

1. Envio el cambio a eneboo-oficial-remoto con "push"

1. Envio el Pull-Request (PARCIAL) desde la web (eneboo-oficial-remoto) HACIA REPO-PADRE.

1. Volver a hacerlo para cada commit....bufff

---

###SOLUCIONAR CONFLICTOS

https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line/

Para desbloquear un conflicto si ya has borrado el archivo:

git reset
