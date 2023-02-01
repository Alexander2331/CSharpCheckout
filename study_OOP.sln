using System;
class Program
{
    static void Main(string[] args)
    {
        Console.Write("Введите размерность массива: ");
        int n = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine($"Введите {n} элементов");
        var temp = Console.ReadLine().Split(' ');
        int[] mas = new int[n];
        for (int i = 0; i < n; i++) mas[i] = Convert.ToInt32(temp[i]);
        Console.WriteLine("Парные элементы: ");
        foreach (int i in mas)
        {
            if (i % 2 == 0) Console.Write(i + " ");
        }
        Console.WriteLine();
        Console.WriteLine("Сумма между первым и последним нулевым элеметом");
        int firstZero = -1, lastZero = -1;
        for (int i = 0; i < n; i++)
        {
            if (mas[i] == 0)
            {
                firstZero = i;
                break;
            }
        }
        for (int i = n - 1; i >= 0; i--)
        {
            if (mas[i] == 0)
            {
                lastZero = i;
                break;
            }
        }
        if (firstZero == -1) Console.WriteLine("В массиве нет нулевых элеметов");
        else
        {
            int sum = 0;
            for (int i = firstZero; i < lastZero; i++) sum += mas[i];
            Console.WriteLine(sum);
        }
        Console.WriteLine("Массив ,где сначала все позитивные элементы, далее негативные");
        for (int i = 0; i < n; i++)
        {
            for (int j = 0; j < n - 1; j++)
            {
                if (mas[j] < 0 && mas[j + 1] >= 0)
                {
                    int tempEl = mas[j];
                    mas[j] = mas[j + 1];
                    mas[j + 1] = tempEl;
                }
            }
        }
        for (int i = 0; i < n; i++) Console.Write(mas[i] + " ");


    }
}
