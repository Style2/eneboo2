

back-on-business....a mi me pasaba lo mismo: en wampserver tienes que:
A) ir a la W verde - botón izquierdo mouse - Apache - apache modules - bajar por la lista y activar el "ssl_module" 
Y ADEMÁS:
B) ir a la W verde - botón izquierdo mouse - PHP - PHP extensions - a mitad de la lista y activar el "php_openssl" 
...Y LUEGO  ir a la W verde - botón izquierdo mouse - "Restart all services"
...Y YA QUE ESTÁS, ACTIVA TAMBIÉN EL "CURL" EN:
C)  ir a la W verde - botón izquierdo mouse - PHP - PHP extensions - a mitad de la lista y activar el "php_curl" 
...Y LUEGO  ir a la W verde - botón izquierdo mouse - "Restart all services"