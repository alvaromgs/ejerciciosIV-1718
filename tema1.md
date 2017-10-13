# Introducción a la infraestructura virtual: concepto y soporte físico

## Ejercicio 1

### Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años.

El servidor elegido es el [siguiente](https://www.amazon.es/dp/B018FUYLP6/ref=psdc_938009031_t2_B01LXZTH2Q). A su precio, 623.32€, habrá que descontarle el IVA (21%) para obtener la base imponible que es con lo que calcularemos los costes de amortización, es decir, 623.32 / 1.21 = 515.14€. Además, utilizaremos las siguientes fórmulas:

Porcentaje de amortización = 100 / vida útil estimada

Amortización anual = base imponible * porcentaje de amortización

#### A cuatro años

Porcentaje de amortización = 100 / 4 = 25%

Amortización anual = 515.14 * 0.25 = 128.785€

#### A siete años

Porcentaje de amortización = 100 / 7 = 14.29%

Amortización anual = 515.14 * 0.1429 = 73.59€

## Ejercicio 2

### Usando las tablas de precios de servicios de alojamiento en Internet "clásicos", es decir, que ofrezcan Virtual Private Servers o servidores físicos, y de proveedores de servicios en la nube, comparar el coste durante un año de un ordenador con un procesador estándar (escogerlo de forma que sea el mismo tipo de procesador en los dos vendedores) y con el resto de las características similares (tamaño de disco duro equivalente a transferencia de disco duro) en el caso de que la infraestructura comprada se usa sólo el 1% o el 10% del tiempo.

Compararemos el servidor virtual [VPS SSD 3](https://www.ovh.es/vps/vps-ssd.xml) y el proveedor de servicios en la nube [S1-8](https://www.ovh.es/public-cloud/instancias/precios/). Estas dos opciones ofrecen prestaciones similares: 2 vCores de procesador, 8GB de RAM y 40GB de almacenamiento SSD. En cuanto a su precio, la opción del VPS serían 11.99€ al mes, mientras que los servicios en la nube nos costarían 0.033€/hora. Si tenemos en cuenta el coste total anual:

#### VPS

11.99€/mes * 12 meses = 143.88€

#### Cloud

10% de uso: 876 horas/año * 0.033€/hora = 28.9€

1% de uso: 87.6 horas/año * 0.033€/hora = 2.89€


Se aprecia una diferencia de precios considerable, y es que contratando los servicios en la nube se paga por las horas de utilización mientras que con VPS existe una cuota fija al mes independientemente del uso que hayamos hecho de los recursos.

## Ejercicio 3

### En general, cualquier ordenador con menos de 5 o 6 años tendrá estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden? Si usas una máquina virtual, ¿qué resultado da? ¿Y en una Raspberry Pi o, si tienes acceso, el procesador del móvil?

Procesador: Intel(R) Core(TM) i5-2450M

Salida del comando:

![alt text](https://github.com/alvaromgs/ejerciciosIV-1718/blob/master/img/ej3.png "Salida del comando egrep '^flags.*(vmx|svm)' /proc/cpuinfo")

## Ejercicio 4

### Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden kvm-ok.

Como se puede observar en la siguiente captura, si que cuenta con este módulo:

![alt text](https://github.com/alvaromgs/ejerciciosIV-1718/blob/master/img/ej4.png "Salida del comando kvm-ok")
