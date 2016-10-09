# proyecto-iv

Ejercicio 1:

Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años. Consultar este artículo en Infoautónomos sobre el tema.

Yo he elegido el servidor HP ProLiant ML310e G8 XE E3-1220/8GB/2TB , que he buscado en pccomponentes( en concreto, https://www.pccomponentes.com/hp-proliant-ml310e-g8-xe-e3-1220-8gb-2tb )

El precio con IVA(28%) es de 729€ y sin IVA es de 602.48€.

Amortización a 4 años:

Como sólo podemos un 25% cada año, sobre el precio sin IVA, pues quedaría así:

Por cada año pagaremos : 0.25 * 602.48 = 150.62

Lo que hará un total de 602.48 €

Amortización a 7 años: (14.28 % cada año , y el último año 14.32 % ) .

Los 6 primeros años : 86,034144 € / año El 7 año : 86,275136 €.

Ejercicio 2:

Como servidor VPS he escogido uno arsys, Servidor VPS Linux S Las características del mismo son : 4 GB de RAM ,100 GB de Disco Duro. El precio es de 60€/mes ó 648€/año (10% de descuento).

Y como servidor en la nube, he escogido uno de Azure, utilizando la calculadora Las características son las siguientes: 2 núcleos, 3.5 GB de RAM , 489GB de SSD y sale a 0.135€/hora , 100,39 €/MES.

Vamos a calcular el coste durante un año con un porcentaje de utilización del 1% y del 10%.

**El 1% son 87.6 horas( redondearemos a 88 horas). Por tanto: En el primer caso: El rpecio sería 60€, ya que es por meses. En el segundo caso: 11,87 €/MES.

**El 10% son 876 horas. Por lo tanto: En el primer caso: Son 36.5 días, el precio sería de 60x2 , 120€, ya que sería dos meses. En el segundo caso : El precio sería de 100,39 €.


Ejercicio 4:

Comprobar si el procesador o procesadores instalados tienen estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden?

Debemos ejecutar la siguiente orden : egrep '^flags.*(vmx|svm)' /proc/cpuinfo. Podemos ver la salida a continuación:

Ejecución

Ejercicio 5:

Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden kvm-ok. No me funciona la orden kvm-ok. Previamente he instalado el paquete cpu-checker pero no me funciona. Lo volveré a intentar.

Instalar un hipervisor para gestionar máquinas virtuales, que más adelante se podrá usar en pruebas y ejercicios.

Yo ya estoy usando VMware para otras asignaturas, con máquinas virtuales instaladas. El proceso de instalación es sencillo y se puede ver en la página web del mismo.