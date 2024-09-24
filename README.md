using System;

namespace Calculator
{
    class Program
    {
        static void Main(string[] args)
        {
            // Основные операции
            Console.WriteLine("Введите первое число:");
            double num1 = double.Parse(Console.ReadLine());

            Console.WriteLine("Введите второе число:");
            double num2 = double.Parse(Console.ReadLine());

            Console.WriteLine("Выберите операцию (+, -, *, /, %):");
            string op = Console.ReadLine();

            double result = 0;

            switch (op)
            {
                case "+":
                    result = num1 + num2;
                    break;
                case "-":
                    result = num1 - num2;
                    break;
                case "*":
                    result = num1 * num2;
                    break;
                case "/":
                    if (num2 == 0)
                    {
                        Console.WriteLine("Деление на ноль невозможно.");
                    }
                    else
                    {
                        result = num1 / num2;
                    }
                    break;
                case "%":
                    result = num1 % num2;
                    break;
                default:
                    Console.WriteLine("Неизвестная операция.");
                    break;
            }

            Console.WriteLine("Результат: {0}", result);

            // Дополнительные операции
            Console.WriteLine("Выберите дополнительную операцию (pow, round, sin, cos, tan, asin, atan):");
            string extraOp = Console.ReadLine();

            switch (extraOp)
            {
                case "pow":
                    Console.WriteLine("Введите степень:");
                    double power = double.Parse(Console.ReadLine());
                    result = Math.Pow(result, power);
                    break;
                case "round":
                    Console.WriteLine("Введите количество знаков после запятой:");
                    int decimals = int.Parse(Console.ReadLine());
                    result = Math.Round(result, decimals);
                    break;
                case "sin":
                    result = Math.Sin(result);
                    break;
                case "cos":
                    result = Math.Cos(result);
                    break;
                case "tan":
                    result = Math.Tan(result);
                    break;
                case "asin":
                    result = Math.Asin(result);
                    break;
                case "atan":
                    result = Math.Atan(result);
                    break;
                default:
                    Console.WriteLine("Неизвестная операция.");
                    break;
            }

            Console.WriteLine("Результат: {0}", result);

            // Геометрические операции
            Console.WriteLine("Выберите геометрическую операцию (area, perimeter, radius, diameter):");
            string geoOp = Console.ReadLine();

            switch (geoOp)
            {
                case "area":
                    Console.WriteLine("Введите радиус круга:");
                    double radius = double.Parse(Console.ReadLine());
                    result = Math.PI * radius * radius;
                    break;
                case "perimeter":
                    Console.WriteLine("Введите радиус круга:");
                    radius = double.Parse(Console.ReadLine());
                    result = 2 * Math.PI * radius;
                    break;
                case "radius":
                    Console.WriteLine("Введите диаметр круга:");
                    double diameter = double.Parse(Console.ReadLine());
                    result = diameter / 2;
                    break;
                case "diameter":
                    Console.WriteLine("Введите радиус круга:");
                    radius = double.Parse(Console.ReadLine());
                    result = 2 * radius;
                    break;
                default:
                    Console.WriteLine("Неизвестная операция.");
                    break;
            }

            Console.WriteLine("Результат: {0}", result);
        }
    }
}
