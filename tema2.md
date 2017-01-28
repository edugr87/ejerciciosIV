##Ejercicios 1: Instalar alguno de los entornos virtuales de node.js (o de cualquier otro lenguaje con el que se esté familiarizado) y, con ellos, instalar la última versión existente, la versión minor más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).
El lenguaje de programacion que he elegido ha sido python, por lo que he instalado virtualenv:
![proceso instalación](/tema2/Captura1.png)
![proceso instalación](/tema2/captura2.png)
![proceso instalación](/tema2/captura3.png)


##Ejercicios 2: Como ejercicio, algo ligeramente diferente: una web para calificar las empresas en las que hacen prácticas los alumnos. Las acciones serían crear empresa y listar calificaciones para cada empresa, crear calificación y añadirla (comprobando que la persona no la haya añadido ya), borrar calificación (si se arrepiente o te denuncia la empresa o algo) y hacer un ránking de empresas por calificación, por ejemplo. Crear un repositorio en GitHub para la librería y crear un pequeño programa que use algunas de sus funcionalidades. Si se quiere hacer con cualquier otra aplicación, también es válido. Se trata de hacer una aplicación simple que se pueda hacer rápidamente con un generador de aplicaciones como los que incluyen diferentes marcos MVC. Si cuesta mucho trabajo, simplemente prepara una aplicación que puedas usar más adelante en el resto de los ejercicios.##

![Aplicacion funcionando](/tema2/captura4.png)
![Aplicacion funcionando](/tema2/captura5.png)
![Aplicacion funcionando](/tema2/captura6.png)
Para el ejercicio se ha creado una web basica en django que nos redirecciona a varias paginas diferentes, dependiendo de la dirección.

##Ejercicios 3: Ejecutar el programa en diferentes versiones del lenguaje. ¿Funciona en todas ellas?

Se ha ejecutado en varias versiones y me he encontrado con varios erros debido a funciones que se han quedado obsoletas y cambio de sintaxis.

![Archivo requirements.txt](/tema2/captura7.png)

##Ejercicios 4: Crear una descripción del módulo usando package.json. En caso de que se trate de otro lenguaje, usar el método correspondiente.

En el caso de Python he creado el fichero requerimientos.txt en el cual he metido la descripción del módulo con la orden: pip freeze > requerimientos.txt. Este ha sido el resultado:


##Ejercicios 5: Automatizar con grunt y docco (o algún otro sistema) la generación de documentación de la librería que se cree. Previamente, por supuesto, habrá que documentar tal librería.

En mi caso he instalado pydoc, que es una herramienta que facilita la creación de la documentación para python, ya que viene instalado por defecto y es facil de manejar. Para usarlo hay que importarlo en nuestro código con la siguiente línea import sys, pydoc.

el programa al ejecutar busca las lineas que estan entre """ """ y coge el contenido del interno que es el del metodo que se ha documentado. Dejo 2 imagenes una con el codigo documentado y otra con la salida de pydoc

![pydoc](/tema2/captura8.png)
![pydoc](/tema2/captura9.png)
