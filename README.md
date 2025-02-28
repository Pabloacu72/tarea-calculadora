# tarea-calculadora
tarea calculadora
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace calculadora
{
    using System;

    class Program
    {
        static void Main()
        {
            while (true)
            {
                Console.Clear();
                Console.WriteLine("Bienvenidos");
                Console.WriteLine("Seleccione una operación:");
                Console.WriteLine("1. Suma");
                Console.WriteLine("2. Resta");
                Console.WriteLine("3. Multiplicación");
                Console.WriteLine("4. División");
                Console.WriteLine("5. Salir");

                Console.Write("Ingrese su opción: ");
                string opcion = Console.ReadLine();

                if (opcion == "5")
                {
                    break;
                }

                Console.Write("Ingrese el primer número: ");
                double num1 = Convert.ToDouble(Console.ReadLine());

                Console.Write("Ingrese el segundo número: ");
                double num2 = Convert.ToDouble(Console.ReadLine());

                double resultado = 0;
                switch (opcion)
                {
                    case "1":
                        resultado = num1 + num2;
                        break;
                    case "2":
                        resultado = num1 - num2;
                        break;
                    case "3":
                        resultado = num1 * num2;
                        break;
                    case "4":
                        if (num2 != 0)
                            resultado = num1 / num2;
                        else
                            Console.WriteLine("No se puede dividir por cero.");
                        break;
                    default:
                        Console.WriteLine("Opción no válida.");
                        continue;
                }

                Console.WriteLine($"El resultado es: {resultado}");
                Console.WriteLine("Presione una tecla para continuar...");
                Console.ReadKey();
            }
        }
    }

}
