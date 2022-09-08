Cálculo de la complejidad del algoritmo de búsqueda de 
raíces por bisección implementado:


Para la ejecución, este algoritmo depende del intervalo [a, b] 
y δ, puesto que se va a obtener una raíz x±δ en el intervalo.

Luego, la única operación que se realiza es reducir el 
intervalo dado, entonces encontrar la respuesta bf - af ≤ δ, 
esto se obtiene dividiendo repetidamente el intervalo en 
dos partes iguales, por lo que se puede asegurar que se 
realizaran iteraciones en función del intervalo inicial y un 
número k de iteraciones expresadasa como:


δ <=  (b-a) / 2^k

Entonces, se puede desarrollar de la siguiente forma

δ <  (b-a) / 2^k

Intercambiando δ con 2^k

2^k <  (b-a) / δ

Aplicando log:

k < log2  (b-a) / δ


De esta forma, se demuestra que k está acotado por arriba por los parametros 
de la función y que esta tiene complejidad logarítmica en relación con el intervalo y el inverso de la tolerancia.

Se demuestra entonces que esta función es de orden Log(n).


