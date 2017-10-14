# Desarrollo basado en pruebas

## Ejercicio 1

### Descargar y ejecutar las pruebas de alguno de los proyectos anteriores, y si sale todo bien, hacer un pull request a este proyecto con tests adicionales, si es que faltan (en el momento que se lea este tema).

Todas las funciones cuentan con su test correspondiente.

## Ejercicio 2

### Para la aplicación que se está haciendo, escribir una serie de aserciones y probar que efectivamente no fallan. Añadir tests para una nueva funcionalidad, probar que falla y escribir el código para que no lo haga (vamos, lo que viene siendo TDD).

[Tests de la aplicación usando unittest](https://github.com/alvaromgs/proyectoIV-1718/blob/master/bot/test.py)

## Ejercicio 3

### Convertir los tests unitarios anteriores con assert a programas de test y ejecutarlos desde mocha, usando descripciones del test y del grupo de test de forma correcta. Si hasta ahora no has subido el código que has venido realizando a GitHub, es el momento de hacerlo, porque lo vas a necesitar un poco más adelante.

Ya que en mi aplicación estoy usando Python, optaré por la versión para dicho lenguaje llamada pocha.

Adaptamos 3 de los tests escritos previamente a la sintaxis de este marco de testeo y definimos el grupo de test *Tests de listas*:

```
from pocha import describe, it
from listas import *

@describe('Tests de listas')
def _():

    @it('Verifica que las listas se renombran correctamente')
    def testrenameList():
        renameList("Pendientes", "Pendientesv2")
        assert ("Pendientesv2" in getLists()) == True

    @it('Verifica que las puntuaciones son de tipo numerico')
    def testgetRating():
        assert (isinstance(getRating("Vistas", "Cadena perpetua"), (int, float))) == True

    @it('Verifica que las peliculas se actualizan correctamente')
    def testupdateMovie():
        nota = 9
        updateMovie("Vistas", "Cadena perpetua", nota)
        updateMovie("Vistas", "El truco final", nota)
        assert (getRating("Vistas", "Cadena perpetua")) == nota
        assert ("El truco final" in getMovies("Vistas")) == True
```

El resultado de la ejecución es el siguiente:

![alt text](https://github.com/alvaromgs/ejerciciosIV-1718/blob/master/img/tema2ej3.png "Resultado de la ejecución del test")

## Ejercicio 4

### Instalar alguno de los entornos virtuales de node.js (o de cualquier otro lenguaje con el que se esté familiarizado) y, con ellos, instalar la última versión existente, la versión minor más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).

He instalado el entorno virtualenv de Python con la siguiente orden:

```sudo apt install virtualenv python-virtualenv```

Seguidamente creo el entorno especificando la versión, en este caso la 3.5, y lo activo y desactivo:

![alt text](https://github.com/alvaromgs/ejerciciosIV-1718/blob/master/img/tema2ej4.png "Gestionando el entorno virtual")

