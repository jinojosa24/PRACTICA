# PRACTICA ###Comandos de Docker
## 1. Descargar e comprobar que unha imaxe está no teu equipo
Para descargar la imagen utilizando el comando `**sudo docker pull**`. Luego si queremos comprobar que estan las imagenes con el comando `**docker images**` 
## 2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?
Utilizando el comando `**docker run**` y el sistema se encarga de generar el nombre y arraca directamente. Para poder visualizar se usara el comando `** docker ps -a**` y nos lista los contenedores creados.
## 3. Crea un contenedor coo nome 'u1', cómo accedes a el?
Para crear un contenedor con nombre con el comando `**docker run -d --name u1**` y accedemos a el con el comando `**docker -it u1 bash**` nos abrira en un apartado mas grafico.

## 4. Comproba a súa ip e fai ping a google.com
Para comprobar la interfaz de red y al IP de contenedor `**ip addr show**` y para hacer el ping `**ping -c google.com**` con esto podremos saber la ip y realizar el ping.

## 5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?
Con el comando `**docker run mas el nombre**` crearemos el contenedor bono y luego para realizar ping entre contenedores usamos el siguiente comando `**docker -it u1 bash -- ip addr show -- docker -ot bono bash -- ping IP_DE_U1 **` se reemplazara por las ip que nos a proporcionado. Los contenedor en la misma red de docker puede comunicarse entre si ya que se encuentran dentro de la misma red.
## 6. Se pechas as terminales, qué pasa coo contenedor?
No, los contenedor seguiran en segundo plano.

## 7. Cánta memoria no disco duro ocupaches? usa docker para calculalo
si usamos el comando `** docker system df**` nos da los resultados de cuanto ocupa en este caso al probarlo las imagenes ocupan mucha mas memoria que el contenedor.

## 9. Cómo fixeches para clonar o repositorio
si utilizamos el comando `**git clone https://github.com/jinojosa24/PRACTICA.git')**` se clonara el repositorio.
## 10. Cómo engades o arquivo readme2.md
Para añadir el readme2.md `**git add readme2.md**` se añadira el fichero dentro de la carpeta.

## 11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md
Lsita los comandos `** git add readme.md readme2.md -- git commit -m asd -- git push**` al realizar estos comando se nos subira el nuevo archivo.
git add añade los cambios, commit, crea un commit con los cambios y push sube los cambios al repositorio remoto.
## 12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.
en la terminal usamos el comando `** git fetch**` y nos actulizara la informacion sobre el repositorio remoto. Y con `**git dif origin/main**` mnostrara las diferencias entre repositorio local y remoto.
