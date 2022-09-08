# Clase 02 - .NET (C#)

Vamos a empezar la clase desestructurando los metodos que hicimos la clase anterior:

Creamos una función:

```sh
using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            public static int Sumatoria(int desde, int hasta)
            {
                int total = 0;
                for (int i = desde; i <= hasta; i++)
                    total += i;
    
                return total;
            }
        }
    }
}
```

```sh
using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            public static void ImprimirCuadrado()
            {
                Console.WriteLine(Environment.NewLine + "EJERCICIO A");

                int sumatoria = 0;

                for (int i = 0; i <= numero; i++)
                {
                    sumatoria += i
                }

                Console.WriteLine($"La sumatoria de 1 a {numero} es: {sumatoria}")  
            }
        }
    }
}
```

* void -> "vacío", la función no retornará nada.

* En las aplicaciones en consola siempre se usa la clase main

* Control + R + R -> renombro una variable o metodo del programa.

* Siempre es recomendable que los nombres de las variables y de las funciones sean descriptivos con respecto a su función.

* Los arrays tienen tamaño fijo, por lo que hay que asignarles un valor fijo de elementos que quiero que tenga. Si yo quiero almacenar una cantidad cualquiera de elementos voy a tener que usar una lista y no un array.  

* A los numeros los ordena antes porque estan primeros dentro del codigo ASCII 

* Método .Trim -> limpia los espacios de un string.

* static -> fundamental para acceder directamente al objeto sin necesidad de instanciar una clase.

## Objetos - abstracciones 

Un objeto se puede interpretar como una abstracción de la realidad, la cual tiene sus correspondientes propiedades (definidos en atributos) y comportamientos (definidos en métodos)

Una clase vendría a ser un molde o plantilla que va a servir como modelo para los objetos que voy a crear posteriormente. Comúnmente a las clases se las nombra en singular, por ejemplo:

Ejemplos:

* clase -> Usuario

* objeto -> Usuario1

* atributo -> Nombre

* método -> Ingresar

* Nota: los valores de las propiedades de cada objeto no serán los mismos entre sí, y a estos atributos se los puede acceder a través de metodos publicos que interactúan con estas propiedades.

* Nota: el constructor siempre tiene que ser público, ya que al instanciar un objeto generalmente le vamos a tener que pasar como argumento aquellas características propias que quiero que tenga este objeto y que por lo tanto lo va a hacer diferente a los demás.  

* Palabra clave override -> sobreescribe el metodo del objeto padre (object). El objeto padre de .NET se conoce como "Object" (algo similar es el objeto Window en Javascript), este objeto tiene dentro todas los métodos que me van a ser posibles utilizar en .NET, por ejemplo, métodos como .Sort, .Reverse, etc. Hay veces en las que nosotros vamos a necesitar "pisar" estos métodos predefinidos en C# por uno que realice unas acciones similares pero con nuestro toque de código agregado, para esto es la palabra clave "override". 




