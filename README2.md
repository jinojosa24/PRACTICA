#PRACTICA 2 SRI
## Comproba que a tes a imaxe httpd
Utilizando el comando _`**docker images**`_ listamos las imagenes y comprabamos que tenemos una imagen httpd.


## Mapea o porto 80 do contenedor có 8080 da túa máquina. Utiliza bind mount para que o directorio do apache2 'htdocs' estea montado nun directorio da túa elección.
### Crea un contenedor de nome 'asir_httpd'.

Utilizando el comando `**docker run --name asir_httpd -d -p 8080:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd**` se creara el contenedor y a su vez se va a mapear. 
Este comando incia un servidor apache en un contenedor docker, accesible desde el puerto _8080_, y utiliza nuestro servidor local para servir los archivos.

## Mostra unha páxina html aloxada no apache2 dende o teu navegador.
![](Screenshot_20241004_183605-1.png)
Para mostrar la pagina html creada abrimos el navegador y colocamos `**http:localhost:8080**` y nos mostrara el html creado.

## Crea un contenedor 'asir_web1' que use este mesmo directorio para 'htdocs' e o puerto 8000

Ahora con este comando se creara un segundo contender en _docker_ `**sudo docker run --name asir_web1 -d -p 8000:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd**`.Y utiliza el mismo servidor local.

## Crea outro contenedor 'asir_web2' có el mesmo directorio e otro puerto, como o 8090. Comproba que los dous servidores mostran a mesma páxina.
Utiliznado el mismo comando solo cambiare el puerto por _8090_ y se creara el contenedor y utlizara el mismo servidor. `**sudo docker run --name asir_web2 -d -p 8090:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd**`
