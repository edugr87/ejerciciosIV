##Ejercicios 1: Instalar chef en la máquina virtual que vayamos a usar.

Chef lo instalamos con el siguiente comando:
```
curl -L https://www.opscode.com/chef/install.sh | sudo bash
```

![install](/tema6/1.png)



##Ejercicios 2: Crear una receta para instalar la aplicación que se viene creando en la asignatura en alguna máquina virtual o servidor en la nube..



##Ejercicios 3: Desplegar la aplicación de DAI con todos los módulos necesarios usando un playbook de Ansible

Dejo el archivo de ansible con el que se realiza un despliegue en un servidor.

```
- hosts: all
  sudo: true
  tasks:
  - name: Actualizar cache
    apt: update_cache=yes
  - name: Actualizamos repos.
    shell: sudo apt-get update && sudo apt-get upgrade -y
  - name: Instalar python-setuptools
    apt: name=python-setuptools state=present
  - name: Instalar build-essential
    apt: name=build-essential state=present
  - name: Instalar pip
    apt: name=python-pip state=present
  - name: Instalar git
    apt: name=git state=present
  - name: Ins Pyp
    apt: pkg=python-pip state=present
  - name: Instalar python-dev
    apt: pkg=python-dev state=present
  - name: Obtener aplicacion de git
    git: repo=https://github.com/edugr87/proyecto-iv.git  dest=TheWeather clone=yes force=yes
  - name: Permisos de ejecucion
    command: chmod -R +x TheWeather
  - name: Instalar requisitos
    command: sudo pip install -r TheWeather/requirements.txt
  - name: ejecutar
    command: nohup sudo python TheWeather/manage.py runserver 0.0.0.0:80
```

se usa el archivo ansible.cfg.
```
[defaults]

private_key_file=/eduardo.pem

[ssh_connection]
control_path = %(directory)s/ssh-%%C
```


para la conexion por ssh con el servidor web se necesita crear una clave ssh correctamente configurada.

##Ejercicios 4: Instalar una máquina virtual Debian usando Vagrant y conectar con ella.

instalamos vagrant:
```
sudo apt-get install vagrant
```

nos descarga la imagen de debian:

```
vagrant box add debian https://github.com/holms/vagrant-jessie-box/releases/download/Jessie-v0.1/Debian-jessie-amd64-netboot.box
```

![install](/tema6/downloadbox.png)

creamos el fichero Vagrantfile:

```
vagrant init debian
```

iniciamos con vagrant up

```
vagrant up
```
![install](/tema6/vagrantup.png)
