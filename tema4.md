##Ejercicios 1: Instala LXC en tu versión de Linux favorita. Normalmente la versión en desarrollo, disponible tanto en GitHub como en el sitio web está bastante más avanzada; para evitar problemas sobre todo con las herramientas que vamos a ver más adelante, conviene que te instales la última versión y si es posible una igual o mayor a la 1.0.
He instalado LXC y como se puede comprobar en la siguiente captura la versión que he instalado ha sido 1.0.6:
![lxc](/tema4/Captura0.png)
![lxc](/tema4/captura1.png)


##Ejercicios 2: Comprobar qué interfaces puente se han creado y explicarlos.
He creado un contenedor debian y lo he arrancado:
```
sudo lxc-create -t debian -n contUbuntu
sudo lxc-start -n contUbuntu
```
Y estas son las interfaces que se han creado:
![lxc](/tema4/captura2.png)

##Ejercicios 3: 1. Crear y ejecutar un contenedor basado en Debian. 2. Crear y ejecutar un contenedor basado en otra distribución, tal como Fedora. Nota En general, crear un contenedor basado en tu distribución y otro basado en otra que no sea la tuya. Fedora, al parecer, tiene problemas si estás en Ubuntu 13.04 o superior, así que en tal caso usa cualquier otra distro. Por ejemplo, Óscar Zafra ha logrado instalar Gentoo usando un script descargado desde su sitio, como indica en este comentario en el issue.
El contenedor basado en Ubuntu es el creado anteriormente contUbuntu. El contenedor creado y ejecutado basado en otra distrubución que he creado ha sido un contenedor de ubuntu que he creado como se puede ver en la siguiente imagen:
![contUC](/tema4/Captura3.png)

##Ejercicios 4: 1. Instalar lxc-webpanel y usarlo para arrancar, parar y visualizar las máquinas virtuales que se tengan instaladas.
He instalado lxc-webpanel con el siguiente comando:
```
wget https://lxc-webpanel.github.io/tools/install.sh -O - | bash
```
Introducimos nuestra IPlocal:5000 y como usuario y contraseña una vez en lxc-webpanel ponemos admin en los dos campos:
![login](/tema4/Captura6.png)
Se puede ver algunas máquinas paradas y otras que están arrancadas:
![maquinas](/tema4/Captura4.png)
##4:2. Desde el panel restringir los recursos que pueden usar: CPU shares, CPUs que se pueden usar (en sistemas multinúcleo) o cantidad de memoria.
Para restringir los recursos de una máquina primero la paramos, y cambiamos el valor por defecto de CPU shares y CPUs:
![recursos](/tema4/Captura5.png)

Por último arrancamos la máquina y usará los recursos tal y como hemos especificado.


##Ejercicios 5: Comparar las prestaciones de un servidor web en una jaula y el mismo servidor en un contenedor. Usar nginx.


##Ejercicios 6: Instalar docker.
He instalado docker con el siguiente comando:
```
sudo apt-get -y install docker.io
```
Una vez instalado lo he arrancado con **sudo docker -d &**

Cada vez que arranquemos debemos borrar el archivo **docker.pid** con:
```
sudo rm /var/run/docker.pid
```
