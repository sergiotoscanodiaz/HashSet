# HashSet
Esta clase implementa a la interfaz Set, respaldada por una tabla hash (en realidad, una instancia de HashMap). 
No garantiza el orden de iteración del conjunto; en particular, no garantiza que la orden del código se mantendrá constante en el tiempo. Esta clase permite el valor nulo. Esta clase no está sincronizada. Sin embargo, se puede sincronizar explícitamente de esta manera: 
Set s = Collections.synchronizedSet (nuevo HashSet (...));

Puntos a tener en cuenta sobre HashSet:

-HashSet no mantiene ningún orden, los elementos se devolverán en cualquier orden aleatorio.

-HashSet no permite duplicados. Si intenta agregar un elemento duplicado en HashSet, se sobrescribirá el valor anterior.

-HashSet permite valores nulos; sin embargo, si inserta más de un valor nulo, aún devolverá solo un valor nulo.

-HashSet no está sincronizado.

-El iterador devuelto por esta clase es a prueba de fallos, lo que significa que el iterador arrojará ConcurrentModificationException si HashSet se ha modificado después de la creación del iterador, por cualquier medio, excepto el método de eliminación del iterador.

Ejemplo de HashSet:

      import java.util.HashSet;
        public class HashSetExample {
           public static void main(String args[]) {
      
             // Declaración de HashSet
      
              HashSet<String> hset = 
                       new HashSet<String>();

              // Añadiendo elementos al HashSet
              hset.add("Apple");
              hset.add("Mango");
              hset.add("Grapes");
              hset.add("Orange");
              hset.add("Fig");
              //Añadiendo elementos duplicados           
              hset.add("Apple");
              hset.add("Mango");
              //Añadiendo valores nulos
              hset.add(null);
              hset.add(null);

              //Mostrando los elementos del HashSet
              System.out.println(hset);
            }
        }

Salida:
--->[null, Apple, Grapes, Fig, Mango, Orange]

Como puede observar, todos los valores duplicados no están presentes en la salida, incluido el valor nulo duplicado.
Este ejemplo confirma algunas de las características citadas anteriormente.

***

Métodos HashSet:

-add boolean (Elemento e): Agrega el elemento e a la lista.

-void clear (): elimina todos los elementos de la lista.

-Object clone (): este método devuelve una copia superficial de HashSet.

-boolean contains (Object o): Comprueba si el Object o está presente en la lista o no. Si se ha encontrado el objeto, devuelve verdadero o falso.

-boolean isEmpty (): devuelve verdadero si no hay ningún elemento presente en el conjunto.

-int size (): da el número de elementos de un conjunto.

-boolean (Object o): elimina el Object o especificado del Set.
