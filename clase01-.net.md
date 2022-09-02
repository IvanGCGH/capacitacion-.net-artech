# Clase 01 - .NET (C#)

## Introducción a .NET (lenguaje de tecnologias)

### C# -> conjunto de tecnologias que ofrece .NET

Próximamente veremos ASP.NET = desarrollo de paginas web

* Lenguajes interpretados -> analisis de linea a linea de codigo
Agarra el codigo fuente y lee linea por linea y se fija si hay o no errores de sintáxis. En javascript el motor es el navegador. Sus ventajas son que se puede trabajar o programar con cualquier editor de text (bloc de notas). Desventaja, el menor tiempo de ejecucion, es mas lento ya que va linea a linea. . Ejemplos, PHP, Python, etc. ¿Por qué optan por lenguajes de este tipo? Por la facilidad de desarrollo y accesibilidad, por lo que cuando se trabaja con sitios chicos se eligen estos lenguajes interpretados, me puedo meter al servidor y modificar el codigo desde ahi, es mas rapido de sacar algo productivo de ello.

Codigo fuente -> interprete -> entrada/salida.

* Lenguajes compilados -> hay un programa comopilador que agrra todo el codigo fuente, agarra un analisis sintactico, si encuentra un error no lo va a ejecutar. A partir del codigo fuente genera un programa ejecutable en binario (lenguaje maquina), por lo que luego de que se ejecute este programa no va a dar error de compilacion.  La ventaja es optimizacion y levantamiento mas rapido en la ejecucion. Desventaja = requiere re-compilar el codigo cada vez que se cambie el codigo y volver a ejecutarlo. C++, .NET, Java, VB. ¿Por qué se usan? Porque hay empresas que le dan mayor prioridad a la performance.

Codigo fuente -> compilador (error) -> programa ejecutable -> salida.

.NET (framework) es un conjunto de tecnologias compuesto por los lenguajes de programacion (C#, VB y F#). Cuando instalo .NET me viene con un paquete base de librerias para utilizar y hacer mas productivo el codigo. 

Roslyn -> compilador de C# (tambien esta Visual C++).

## SU HISTORIA

Sale en 2002 la primera version, .NET Framework, era gratuito pero de código propietario, solo corria en windows, requeria visual studio para desarrollar, para compilar y para ejecutar.

A partir del 2016 Microsoft cambia el framework de tecnologias de .NET (.NET Core). Es gratuito y open source, es multiplataforma. Se puede desarrollar con cualquier editor y compilar por consola.

## ¿Que podemos hacer en .NET?

Tipos de proyectos: 

* Aplicaciones de consola (recomendable introducción en lenguaje)
* Aplicaciones de escritorio (programas que uno instala en la maquina)
* Servicio de Windows (programas que se ejecutan de fondo en el SO)
* Biblioteca de clase (compilar pedazos de codigo y compartirlo para el entorno)
* Aplicaciones Mobile con Xamarin (se puede programar con C# y compilar para IOS (multiplataforma))
* Aplicaciones web con ASP.NET.
* WEB API (metodos para extraer información, se usa ASP.NET)
* Aplicacion Web Blazor (trabaja con componentes como React) 
* Azure Functions.
* Complementos de Windows (funcionalidades para el paquete de Office).

## Versiones

2019 o 2022 -> en Visual Studio viene todo ya más armado (con Interfáz de GIT integrada) 

En el VS Code se requiere instalar SDK y extensiones de .NET de acuerdo al tipo de proyecto.

## ¿Como se compone la interfaz?

Es parecida al resto de los programas de windows (la mas común es la 2019)

> Factor importante: boton de Play para compilar.

Explorador de soluciones -> Los proyectos trabajan con tres niveles principales de jerarquía, el primero es la solución el cual es el conjunto de proyectos, el segundo son los proyectos en si, y en el tercero vendrian a ser las clases, librerias, etc. 

> Sobre un archivo: con un click la vista es previa, pero con dos click me abre el archivo en si. 

* Consola de administrador de paquetes NuGet -> para poder trabajar con librerias externas y descargarse dependencias de microsoft.

## Su sintaxis

* Parecido en C++ y Java

* Case sensitive -> una variable con mayúscula no es la misma que una con minúscula pero del mismo nombre.

* Fuertemente tipado -> cada vez que creo una variable le tengo que decir un tipo de datos y tengo que trabajar con eso.

* Orientado a objetos -> todo lo que escriba va a estar adentro de una clase. Todo tiene que estar adentro de una clase, por lo que se va a interactuar constantemente con objetos.

### Bibliografía:
<hhtps://es.wikipedia.org/wiki/c-sharp>

## Tipos de datos:

* Enteros: int, short, long, byte
* Decimales: float, double, decimal
* Texto: string, char
* Booleanos: bool (true or false)
* Fechas: DateTime (empieza con mayuscula porque es un objeto, por un lado me guarda el dia, por otro el año, se compone de varios int, a diferencia de otros que son datos primitivos)

* Tipos de datos nullables: int?, decimal?, byte?, DateTime?

Cuando creo que una variable int y no le asigno nada me va a poner como valor por defecto 0, con un bool el valor será false. En cambio si le asigno el signo de pregunta a la palabra clave que expresa el tipo de dato me va a poner null como valor por defecto. Si creo un string y no le pongo nada ya acepta null por defecto. 

* Arrays: int[], decimal[], byte[], DateTime[], string[] (esto es en el caso de los arrays homogéneos, es decir, que los elementos de dicha matriz serán del mismo tipo de dato)

## Ejercicios:

1) Reciba su nombre, sexo e idioma y devuelva un mensaje de bienvenida (ej: Leandro, M, ES => "¡Bienvenido Leandro!")

Lo primero que hacemos es abrir el Visual Studio. 

Elegimos la opción de crear un proyecto

Nos da a elegir el tipo de proyecto: en nuestro caso vamos a elegir el de "aplicación de consola" y elegimos el lenguaje de C# 

Lo nombramos como "ejercicios1", marcamos la ubicacion de la carpeta y el nombre de la solucion (conjunto de proyectos), en este caso la solucion se llamara ejerciciosclase1 (es lo que va a englobar todos los ejercicios)

Luego elegimos la version de .NET Core (convenientemente la ultima que nos aparezca)

Cuando hago click en el nombre del proyecto me abre un archivo XML que nos va a dar la informacion de compilacion, etc del proyecto. (no relevante)

* Dependencias -> Librerias que instale para llevar a cabo el proyecto o vincular otros proyectos al actual.

* program.cs -> se produce cuando ejecute el programa por consola. 

* Using System -> te proporciona los componentes necesarios para trabajar en el proyecto.

* namespace -> para agrupar clases, dentro de uno mismo no puedo tener dos clases con el mismo nombre pero si puedo crear dos namespaces separadas con mismo nombre.

* class -> define una clase, y como se produce dentro de clases, me crea la clase program que va a poner la lógica principal de nuestro programa.

#### Comandos principales:

* Console.WriteLine() -> para escribir un dato en la consola
* Console.ReadLine() -> leer un dato por consola (produce salto de linea)

### 1er ejercicio:

```sh
using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            Console.Write("Ingrese su nombre: ");
            string nombre = Console.ReadLine();

            Console.Write("Ingrese su sexo: ");
            string sexo = Console.ReadLine();

            Console.Write("Ingrese su idioma: ");
            string idioma = Console.ReadLine();

            Console.WriteLine("Bienvenido " + nombre + "!") // concatenacion comun
            Console.WriteLine($"Bienvenido {nombre} !") // concatenacion por template

            // trabajo con condicionales:

            if(idioma.ToUpper() == "ES")
            {
                if (sexo == "M" || sexo == "m") // operador or (||) operador and (&&)
                {
                    Console.WriteLine($"¡Bienvenido {nombre}!")
                }

                else if (sexo == "F" || sexo == "f")
                {
                    Console.WriteLine($"¡Bienvenido {nombre}!")
                }

                else
                {
                    Console.WriteLine($"¡Bienvenidx {nombre}!")
                }
            } 
            else if(idioma.ToUpper() == "ES")
            {
                Console.WriteLine($"Welcome {nombre}!")
            }

            else 
            {
                Console.WriteLine("Idioma incorrecto")    
            }
        }
    }
}
```

```sh
// Lo mismo que lo anterior pero con switch

using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            switch (sexo)
            {
                case "M":
                case "m":
                    Console.WriteLine($"¡Bienvenido {nombre}!")
                    break

                case "F":
                case "f":
                    Console.WriteLine($"¡Bienvenida {nombre}!")
                    break

                default:
                    Console.WriteLine($"¡Bienvenidx {nombre}!")
                    break
            }
        }
    }
}
```

### 2do ejercicio: 

Armar otra aplicacion de consola que reciba dos numeros, devuelva la suma, resta, multiplicacion, division entre ambos.

Dentro de la misma solución creamos otro proyecto, para ejecutarlo lo seleccionamos al lado del boton de RUN y en el Explorador de Soluciones se marcará en negrita.

```sh
// si escribo Read solo (sin el Line) me leerá solo el primer carácter que ingrese. 

using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            try
            {
                Console.Write("Ingrese el primer número: ");
                int numero1 = Convert.ToInt32(Console.ReadLine()); // metodo para convertir la devolucion del string a entero

                Console.Write("Ingrese el segundo número: ");
                int numero1 = int.Parse(Console.ReadLine()); // lectura de dos numeros de forma distinta    

                // Console.WriteLine("La suma es: " + numero1 + numero2); esto me va a devolver una concatenacion y no una suma

                int suma = numero1 + numero2;
                Console.WriteLine("La suma es: " + (numero1 + numero2));

                int resta = numero1 - numero2;
                Console.WriteLine("La resta es: " + (numero1 - numero2));

                int multiplicacion = numero1 * numero2;
                Console.WriteLine("La multiplicacion es: " + (numero1 * numero2));

                if (numero != 0)
                {
                    double division = Math.Round((double)numero1 / numero2, 2);
                    Console.WriteLine("La division es: " + (numero1 / numero2));
                }
                else
                {
                    Console.WriteLine("El resultado es basura");
                }

            }
            catch
            {
                Console.Write("El valor ingresado no es numérico.");
            }
        }
    }
}
```

* Errores en tiempo de ejecución -> excepciones

* Si yo divido dos enteros, el resultado sera entero, para que pase lo contrario tengo que convertir alguno de los numeros a float

* Un float se puede almacenar adentro de un double ya que el float es mas chico que el double.

* Comunmente en la división si se le pasa 0 daria un error, pero este es un caso extraño que no devuelve una excepcion.

### 3er ejercicio: 

Reciba tres numeros enteros (hora, minutos, segundos) e indique si es un numero valido.

```sh
using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            Console.Write("Hora: ");
            int hora = Convert.ToInt32(Console.ReadLine());
            Console.Write("Minutos: ");
            int minutos = Convert.ToInt32(Console.ReadLine());
            Console.Write("Segundos: ");
            int segundos = Convert.ToInt32(Console.ReadLine());

            if (hora >= 0 && hora <= 23 &&
                minutos >= 0 && minutos <= 59 &&
                segunddos >= 0 && <= 59)
                {
                    Console.WriteLine("Hora valida");
                    Console.WriteLine($"{hora}:{minutos}:{segundos}");
                }
        }
    }
}
```

## Trabajo con BUCLES - EJERCICIOS

### 1er ejercicio:

Realizar un cuadrado de caracteres dado un valor numero ingresado por el usuario.

```sh
using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            int numero = Convert.ToInt32(Console.ReadLine());
            int sumatoria = 0;

            for (int i = 0; i <= numero; i++)
            {
                sumatoria += i
            }

            Console.WriteLine($"La sumatoria de 1 a {numero} es: {sumatoria}")
        }
    }
}
```

### 2do ejercicio:

Realizar ahora un triángulo creciente.

```sh

using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            Console.WriteLine(Environment.NewLine + "EJERCICIO B"); //TRIANGULO CRECIENTE

            for (int i = 0; i < numero; i++)
            {
                for (int j = 0; j <= i; j++)
                {
                    Console.Write("1 ");
                }
                Console.Write(Environment.NewLine);
            }
        }
    }
}

```

### 3er ejercicio:

Realizar ahora un triángulo decreciente.

```sh
using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            int numero =  Convert.ToInt32(Console.ReadLine());

            for (int i = 0; i < length; i++)
            {
                for (int j = 0; j < numero; j++)
                {
                    Console.Write("1 ");
                }
                Console.Write(Environment.NewLine); // inserto salto de linea
            }
        }
    }
}
```

### 4to ejercicio:

Realiza ahora un triángulo decreciente espejado.

```sh
using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            int numero =  Convert.ToInt32(Console.ReadLine());

            for (int i = 0; i < length; i++)
            {
                for (int j = 0; j < numero; j++)
                {
                    Console.Write("1 ");
                }
                Console.Write(Environment.NewLine); // inserto salto de linea
            }
        }
    }
}
```

### 5to ejercicio:

Realizar una cruz.

```sh
using System;

namespace ConsoleApp
{
    public class Program
    {
        public static void Main(string[] args)
        {
            Console.WriteLine(Environment.NewLine + "EJERCICIO F"); //CRUZ

            for (int i = 0; i < numero; i++)
            {
                for (int j = 0; j < numero; j++)
                {
                    if (i == j || i == numero - j - 1)
                    {
                        Console.Write("1 ");
                    }
                    else
                    {
                        Console.Write("0 ");
                    }
                }
                Console.Write(Environment.NewLine);
            }
        }
    }
}
```
