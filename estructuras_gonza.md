Red
---
* 0 -> dicc(compu, conj(tupla (interfaz, interfaz, compu)))

DCNet
-----
* 1 -> dicc(compu, dicc(compu, compu)) TRIE
* 2 -> dicc(compu, (tupla(colaPrior(paq),
                          conj(tupla(paq, it_3)),
                          conj(paq),
                          nat)))                          TRIE

* 3 -> secu(secu(compus))
* 4 -> itdicc             º
* 5 -> tupla(nat,compu)

crearPaquete
------------


1. Busco la compu en la que tiene que ir en 2 (L)
2. Lo agrego en la cola de prioridad de paquetes (log(k))
3. Lo agrego en el conjunto de tuplas(paq, it) y el de paquetes (log(k) + log(k))


avanzarSegundo
--------------

1. Para las n computadoras (n) busco el paquete que tiene que ir a continuación (1), edito el contador y actualizo la que mas envió si es necesario (1), pongo tupla (paq,it_3) en una secuencia (1), lo elimino de los conjuntos (O(log(k) + log(k))   (Total de este paso: n\*(1+1+log(k)+log(k)))

2. Para cada paquete en la lista, agrego la computadora de la que esta saliendo a la lista apuntada por el iterador (L). Despues lo pongo en la computadora que tiene que ir y edito 3 agregandole al final ese elemento (n\* (L + L + L+ L+ log(k) + log(k)))

caminoRecorrido
---------------
1. Recorro con 4 para buscar el elemento y por cada uno busco el elemento, cuando lo encuentro listo (n\*log(k))




