using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

internal class Program
{
    public double fraction(double x) // 1.1
    {
        int intPart = (int)x;

        double fractionPart = x - intPart;

        return fractionPart;

    }
    

    public int charToNum(char x) // 1.3
    {
        return x - 48;
    }
    
    
    public bool is2Digits(int x) // 1.5
    {
        string strX = x.ToString();
        if (strX.Length == 2)
                return true;
            else
                return false;
    }
    
    
    public bool IsInRange(int a, int b, int num) // 1.7
    {
        return num >= Math.Min(a, b) && num <= Math.Max(a, b);
    }
    
    
    public bool isEqual(int a, int b, int c) // 1.9
    {
        return a == b && b == c;
    }
    
    
    public int abs(int x) // 2.1
    {
        if (x >= 0)
            return x;
        else
            return x * (-1);
    }
    
    
    public bool is35(int x) // 2.3
    {
        if ((x % 3 == 0 && x % 5 != 0) || (x % 3 != 0 && x % 5 == 0))
            return true;
        else
            return false;
    }
    
    
    public int max3(int x, int y, int z) // 2.5
    {
            if (x >= y && x >= z)
                return x;
            else if (y >= x && y >= z)
                return y;
            return z;
    }
    
    
    public int Sum2(int x, int y) // 2.7
    {
        int sum = x + y;
        if (sum >= 10 && sum <= 19)
            return 20;
        else
            return sum;
    }
    
    
    public string Day(int x) // 2.9
    {
        switch (x)
        {
            case 1:
                return "Понедельник";
            case 2:
                return "Вторник";
            case 3:
                return "Среда";
            case 4:
                return "Четверг";
            case 5:
                return "Пятница";
            case 6:
                return "Суббота";
            case 7:
                return "Воскресенье";
            default:
                return "Это не день недели";
        }
    }
    
    
    public string listNums(int x) // 3.1
    {
        string result = ""; // Хранение результата
        for (int i = 0; i <= x; i++)
        {
            result += i + " ";
        }
        return result;
    }
    
    
    public string Chet(int x) // 3.3
    {
        string result = "";
        for (int i = 0; i <= x; i+=2)
        {
            result +=  i + " ";
        }
        return result;
    }
    
    
    public int NumLen(long x) // 3.5
    {
        int len1 = 0;
        
        if (x == 0)
        {
            return 1;
        }
        
        if (x < 0)
        {
            x = -x;
        }
        
        while (x > 0)
        {
            x = x / 10;
            len1++;
        }
        return len1;
    }
    
    
    public void Square(int x) // 3.7
    {
        for (int i = 0; i < x; i++)
        {
            for (int j = 0; j < x; j++)
            {
                Console.Write("*");
            }
            Console.WriteLine();
        }
    }
    
    
    public void rightTriangle(int x) // 3.9
    {
        for (int i = 1; i <= x; i++)
        {
            for (int j = 1; j <= x - i; j++)
            {
                Console.Write(" ");
            }
            for (int k = 1; k <= i; k++)
            {
                Console.Write("*");
            }
            Console.WriteLine();
        }
    }
    
    
    public int FindFirst(int[] arr, int x) // 4.1
    {
        for (int i = 0; i < arr.Length; i++)
        {
            if (arr[i] == x)
            {
                return i;
            }
        }
        return -1;
    }
    
    
    public int maxAbs(int[] arr) // 4.3
    {
        int maxValue = Math.Abs(arr[0]);
        
        for (int i = 1; i < arr.Length; i++)
        {
            int absValue = Math.Abs(arr[i]);
            if (absValue > maxValue)
            {
                maxValue = absValue;
            }
        }
        
        return maxValue;
    }
    
    
    public int[] Add(int[] arr, int[] ins, int pos) // 4.5
    {
        int[] result = new int[arr.Length + ins.Length];
    
        // Копирование элементов из исходного массива до позиции вставки
        for (int i = 0; i < pos; i++)
        {
            result[i] = arr[i];
        }
    
        // Копирование для вставки
        for (int i = 0; i < ins.Length; i++)
        {
            result[pos + i] = ins[i];
        }
    
        // Копирование оставшихся элементов 
        for (int i = pos; i < arr.Length; i++)
        {
            result[pos + ins.Length + i - pos] = arr[i];
        }
    
        return result;
    }
    
    
    public int[] reverseBack(int[] arr) // 4.7
    {
        int[] res = new int[arr.Length];
        for (int i = 0; i < arr.Length; i++)
        {
            res[i] = arr[arr.Length - i - 1];
        }
        return res;
    }
    
    
    public int[] FindAll(int[] arr, int x) // 4.9
    {
        int count = 0;
        for (int i = 0; i < arr.Length; i++)
        {
            if (arr[i] == x)
                count++;
        }

        int[] index = new int[count];
        int j = 0;
        for (int i = 0; i < arr.Length; i++)
        {
            if (arr[i] == x)
                index[j++] = i;
        }

        return index;
    }
    

    private static void Main(string[] args)
    {
        Program p = new Program();
        Console.WriteLine("Вариант 1");
        Console.WriteLine("Выберите упражнение:");
        Console.WriteLine("Упражнение 1");
        Console.WriteLine("Упражнение 2");
        Console.WriteLine("Упражнение 3");
        Console.WriteLine("Упражнение 4");
        Console.Write("Упражнение: ");
        int taskNumber = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("");

        switch (taskNumber)
        {
            case 1:
                Console.WriteLine("Выберите задачу:");
                Console.WriteLine("Задача 1");
                Console.WriteLine("Задача 3");
                Console.WriteLine("Задача 5");
                Console.WriteLine("Задача 7");
                Console.WriteLine("Задача 9");
                Console.Write("Задача: ");
                int task = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("");

                switch (task)
                {
                    case 1:
                        Console.Write("Введите число: ");
                        double userInput1;
                        while (!double.TryParse(Console.ReadLine(), out userInput1))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите число.");
                            Console.Write("Введите число: ");
                        }
                        double fractionalPart = p.fraction(userInput1);
                        Console.WriteLine($"Дробная часть числа: {fractionalPart}");
                        break;
                    
                    case 3:
                        Console.Write("Введите число от 0 до 9: ");
                        char x;
                        while (!char.TryParse(Console.ReadLine(), out x))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите цифру от 0 до 9.");
                            Console.Write("Введите число от 0 до 9: ");
                        }
                        int result1 = p.charToNum(x);
                        Console.WriteLine("Результат: " + result1);
                        break;
                    
                    case 5:
                        Console.Write("Введите число: ");
                        int userInput2;
                        while (!int.TryParse(Console.ReadLine(), out userInput2))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите число: ");
                        }
                        bool result2 = p.is2Digits(userInput2);
                        if (result2)
                        {
                            Console.WriteLine($"true");
                        }
                        else
                        {
                            Console.WriteLine($"false");
                        }
                        break;
                    
                    case 7:
                        Console.Write("Введите значение a: ");
                        int a1;
                        while (!int.TryParse(Console.ReadLine(), out a1))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите значение a: ");
                        }
                    
                        Console.Write("Введите значение b: ");
                        int b1;
                        while (!int.TryParse(Console.ReadLine(), out b1))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите значение b: ");
                        }
                    
                        Console.Write("Введите значение num: ");
                        int num1;
                        while (!int.TryParse(Console.ReadLine(), out num1))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите значение num: ");
                        }
                    
                        bool result3 = p.IsInRange(a1, b1, num1);
                        Console.WriteLine($"Результат: {result3}");
                        break;
                    
                    case 9:
                        Console.Write("Введите значение a: ");
                        int a2;
                        while (!int.TryParse(Console.ReadLine(), out a2))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите значение a: ");
                        }
                    
                        Console.Write("Введите значение b: ");
                        int b2;
                        while (!int.TryParse(Console.ReadLine(), out b2))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите значение b: ");
                        }
                    
                        Console.Write("Введите значение c: ");
                        int c2;
                        while (!int.TryParse(Console.ReadLine(), out c2))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите значение c: ");
                        }
                    
                        bool result4 = p.isEqual(a2, b2, c2);
                        Console.WriteLine($"Результат: {result4}");
                        break;
                    
                    default:
                        Console.WriteLine("Неправильный выбор задачи");
                        break;

                }
                break;
            case 2:
                Console.WriteLine("Выберите задачу:");
                Console.WriteLine("Задача 1");
                Console.WriteLine("Задача 3");
                Console.WriteLine("Задача 5");
                Console.WriteLine("Задача 7");
                Console.WriteLine("Задача 9");
                Console.Write("Задача: ");
                int task2 = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("");

                switch (task2)
                {
                    case 1:
                        Console.Write("Введите число: ");
                        int x3;
                        while (!int.TryParse(Console.ReadLine(), out x3))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите число: ");
                        }
                        Console.WriteLine("Модуль числа: " + p.abs(x3));
                        break;
                    
                    case 3:
                        Console.Write("Введите число: ");
                        int x4;
                        while (!int.TryParse(Console.ReadLine(), out x4))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите число: ");
                        }
                        bool result5 = p.is35(x4);
                        Console.WriteLine("Результат: " + result5);
                        break;
                    
                    case 5:
                        Console.Write("Введите первое число: ");
                        int x5;
                        while (!int.TryParse(Console.ReadLine(), out x5))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите первое число: ");
                        }
                    
                        Console.Write("Введите второе число: ");
                        int y5;
                        while (!int.TryParse(Console.ReadLine(), out y5))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите второе число: ");
                        }
                    
                        Console.Write("Введите третье число: ");
                        int z5;
                        while (!int.TryParse(Console.ReadLine(), out z5))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите третье число: ");
                        }
                    
                        int max = p.max3(x5, y5, z5);
                        Console.WriteLine("Максимальное число: " + max);
                        break;
                    
                    case 7:
                        Console.Write("Введите число x: ");
                        int x6;
                        while (!int.TryParse(Console.ReadLine(), out x6))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите число x: ");
                        }
                    
                        Console.Write("Введите число y: ");
                        int y6;
                        while (!int.TryParse(Console.ReadLine(), out y6))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите число y: ");
                        }
                    
                        int result6 = p.Sum2(x6, y6);
                        Console.WriteLine("Результат: " + result6);
                        break;
                    
                    case 9:
                        Console.Write("Введите день недели (1-7): ");
                        int x7;
                        while (!int.TryParse(Console.ReadLine(), out x7) || x7 < 1 || x7 > 7)
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите число от 1 до 7.");
                            Console.Write("Введите день недели (1-7): ");
                        }
                    
                        string result = p.Day(x7);
                        Console.WriteLine(result);
                        break;
                    
                    default:
                        Console.WriteLine("Неправильный выбор задачи");
                        break;

                }
                break;
            case 3:
                Console.WriteLine("Выберите задачу:");
                Console.WriteLine("Задача 1");
                Console.WriteLine("Задача 3");
                Console.WriteLine("Задача 5");
                Console.WriteLine("Задача 7");
                Console.WriteLine("Задача 9");
                Console.Write("Задача: ");
                int task3 = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("");

                switch (task3)
                {
                    case 1:
                        Program p11 = new Program();
                        Console.Write("Введите число: ");
                        int x;
                        while (!int.TryParse(Console.ReadLine(), out x))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите число: ");
                        }
                        string result7 = p11.listNums(x);
                        Console.WriteLine("Результат: " + result7);
                        break;
                    
                    case 3:
                        Program p12 = new Program();
                        Console.Write("Введите число: ");
                        int x8;
                        while (!int.TryParse(Console.ReadLine(), out x8))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите число: ");
                        }
                        string result8 = p12.Chet(x8);
                        Console.WriteLine("Четные числа от 0 до " + x8 + ": " + result8);
                        break;
                    
                    case 5:
                        Program p13 = new Program();
                        Console.Write("Введите число: ");
                        long x9;
                        while (!long.TryParse(Console.ReadLine(), out x9))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите число: ");
                        }
                        int length1 = p13.NumLen(x9);
                        Console.WriteLine("Количество знаков в числе: " + length1);
                        break;
                    
                    case 7:
                        Program p14 = new Program();
                        Console.Write("Введите размер квадрата: ");
                        int x10;
                        while (!int.TryParse(Console.ReadLine(), out x10))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите размер квадрата: ");
                        }
                        Console.WriteLine("");
                        p14.Square(x10);
                        break;
                    
                    case 9:
                        Program p15 = new Program();
                        Console.Write("Введите высоту треугольника: ");
                        int x11;
                        while (!int.TryParse(Console.ReadLine(), out x11))
                        {
                            Console.WriteLine("Некорректный ввод. Пожалуйста, введите целое число.");
                            Console.Write("Введите высоту треугольника: ");
                        }
                        p15.rightTriangle(x11);
                        break;
                    
                    default:
                        Console.WriteLine("Неправильный выбор задачи");
                        break;

                }
                break;
                
                
            case 4:
                Console.WriteLine("Выберите задачу:");
                Console.WriteLine("Задача 1");
                Console.WriteLine("Задача 3");
                Console.WriteLine("Задача 5");
                Console.WriteLine("Задача 7");
                Console.WriteLine("Задача 9");
                Console.Write("Задача: ");
                int task4 = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("");

                switch (task4)
                {
                    case 1:
                        Program p16 = new Program();
                        Console.Write("Введите элементы массива через пробел: ");
                        string[] inputArr = Console.ReadLine().Split(' ');
                        int[] arr1 = new int[inputArr.Length];
                        for (int i = 0; i < inputArr.Length; i++)
                        {
                            arr1[i] = Convert.ToInt32(inputArr[i]);
                        }
                
                        Console.Write("Введите число для поиска: ");
                        int x12 = Convert.ToInt32(Console.ReadLine());
                
                        int result9 = p16.FindFirst(arr1, x12);
                        if (result9 != -1)
                        {
                            Console.WriteLine("Первое вхождение " + x12 + " находится по индексу " + result9);
                        }
                        else
                        {
                            Console.WriteLine(x12 + " не найдено в массиве");
                        }
                        break;
                    case 3:
                        Program p17 = new Program();
                        Console.Write("Введите элементы массива через пробел: ");
                        string[] input1 = Console.ReadLine().Split(' ');
                        int[] arr2 = new int[input1.Length];
                        for (int i = 0; i < input1.Length; i++)
                        {
                            arr2[i] = int.Parse(input1[i]);
                        }
                        int result10 = p17.maxAbs(arr2);
                        Console.WriteLine("Максимальное значение: " + result10);
                        break;
                    case 5:
                        Program p18 = new Program();
                        Console.Write("Введите элементы начального массива через пробел: ");
                        string[] arrInput = Console.ReadLine().Split(' ');
                        int[] arr3 = Array.ConvertAll(arrInput, int.Parse);
                        Console.Write("Введите элементы добавляемого массива через пробел: ");
                        string[] insInput = Console.ReadLine().Split(' ');
                        int[] ins3 = Array.ConvertAll(insInput, int.Parse);
                        Console.Write("Введите позицию вставки: ");
                        int pos3 = int.Parse(Console.ReadLine());
                        int[] result11 = p18.Add(arr3, ins3, pos3);
                        Console.WriteLine("Результат: [" + string.Join(", ", result11) + "]");
                        break;
                    case 7:
                        Program p19 = new Program();
                        Console.Write("Введите элементы массива через пробел: ");
                        string[] input2 = Console.ReadLine().Split(' ');
                        int[] arr4 = new int[input2.Length];
                        for (int i = 0; i < input2.Length; i++)
                        {
                            arr4[i] = int.Parse(input2[i]);
                        }
                        int[] res = p19.reverseBack(arr4);
                        Console.WriteLine("Результат: [" + string.Join(", ", res) + "]");
                        break;
                    case 9:
                        Program p20 = new Program();
                        Console.Write("Введите элементы массива через пробел: ");
                        string[] inputArr1 = Console.ReadLine().Split(' ');
                        int[] arr5 = new int[inputArr1.Length];
                        for (int i = 0; i < inputArr1.Length; i++)
                        {
                            arr5[i] = int.Parse(inputArr1[i]);
                        }
                        Console.Write("Введите число для поиска: ");
                        int x13 = int.Parse(Console.ReadLine());
                        int[] result12 = p20.FindAll(arr5, x13);
                        Console.WriteLine("Нахождение индексов" + x13 + " в массиве: [" + string.Join(", ", result12) + "]");
                        break;
                    default:
                        Console.WriteLine("Неправильный выбор задачи");
                        break;
                }
                break;
            
            
            default:
                Console.WriteLine("Неправильный выбор задания");
                break;
        }
    }

}
