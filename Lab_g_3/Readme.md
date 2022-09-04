Búsqueda con fuerza bruta
=========================

Utilizando fuerza bruta, se diseña un algoritmo con el objetivo de
encontrar un segmento problema (ACATTACA) en el genoma del Covid 19.

**Objetivos:** - Buscar el segmento "problema" en el "target" - imprimir
la posición final - Imprimir la cantidad de recurrencias en el "Target",
con sus respectivas ubicaciones - hacer un [análisis de
eficiencia](#Eficiencia) del algoritmo en cuestión

Creación Algorítmo
------------------

se genera la función *busqueda\_subcadena* que acepta un texto ( el
target) y una subcadena (el segmento problema) y retorna una tupla de la
forma int repeticiones - lista de index

-   Repeticiones hace referencia a la cantidad de repeticiones que
    aparece la subcadena en texto.
-   Lista de index hace referencia a una lista que contiene tuplas de la
    forma (INDICE INICIAL - INDICE FINAL)

Eficiencia
----------

Para hacer un análisis del peor caso empezaremos tomando cada una de las
lineas en la función principal *busqueda\_subcadena* y tomando como n,
el valor de la longitud del texto target

     def  busqueda_subcadena(texto, subcadena):
         index = 0                                                      #O(1)
         repeticiones = 0                                               #O(1)
         apariciones = []                                               #O(1)
         for i in texto:                                                #O(n)
             if (i == subcadena[0]  and 
             texto[index:len(subcadena)+index] == subcadena):           #O(1)
                 apariciones.append((index, index+len(subcadena)-1  ))  #O(1)
                 repeticiones = repeticiones + 1                        #O(1)
             index = index+1                                            #O(1)
         return  (repeticiones, apariciones)                            #O(1)

como segundo paso debemos realizar el cálculo de la eficiencia de la
función en cuestión
$$ {O_1 + O_1 + O_1 + O_n[O_1 (O_1+O_1) + O_1] +O_1 = }$$
$$ {O_1 + O_1 + O_1 + O_n +O_1 = }$$ $$ {O_n  }$$

Con este análisis vemos que el algoritmo de fuerza bruta para buscar una
subcadena dentro de un Target es O(n).

Para averiguar la eficiencia del programa completo, vamos a analizar las
demás líneas de código en el programa.

    texto = "AQUÍ VA EL TEXTO TARGET"                                   #O(1)
    cadena = "CADENA OBJETIVO"                                          #O(1)
    resultado = busqueda_subcadena(texto,cadena)                        #O(1)
    print(resultado[0])                                                 #O(1)
    print(resultado[1])                                                 #O(1)
    for i in resultado:                                                 #O(n)
        print(texto[i[0]:i[1]+1])                                       #O(1)
                                        

como segundo paso debemos realizar el cálculo de la eficiencia del
programa completo $$ {O_n + O_1 + O_1 +O_1 +O_1 +O_n[O_1]  = }$$
$$ {O_n + O_1 + O_1 +O_1+O_1  + O_n = }$$ $$ {O_n  }$$

Conclusiones
------------

Gracias! \<3
