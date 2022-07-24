{   
// Задача 34: Задайте массив заполненный случайными положительными трёхзначными числами. 
//Напишите программу, которая покажет количество чётных чисел в массиве.
//[345, 897, 568, 234] -> 2
int[] array = new int [4];
FillArray(array, 100, 999);
PrintArray(array);
PrintCount(array);
}

void FillArray(int[] array, int FirstNumber = 0, int LastNumber = 1)
{
    LastNumber++;
    Random random = new Random();
    for (int i = 0; i < array.Length; i++)
    {
        array[i] = random.Next(FirstNumber, LastNumber);
    }
}

void PrintArray(int[] array)
{
    Console.WriteLine("Вывод массива:");
    for(int i = 0; i < array.Length; i++)
    {
        Console.Write(array[i] + "\t");
    }
    Console.WriteLine();
}

void PrintCount(int[] array)
{
    int count = 0;
    for (int i = 0; i < array.Length; i++)
    {
        if(array[i] % 2 == 0) count++;
    }
    Console.WriteLine("В массиве четных чисел " + count);
}

void Zadacha36()
{
    //Задача 36: Задайте одномерный массив, заполненный случайными числами. 
    //Найдите сумму элементов, стоящих на нечётных позициях.
    //[3, 7, 23, 12] -> 19
    //[-4, -6, 89, 6] -> 0
    int[] array = new int [4];
    FillArray(array, 3, 30);
    PrintArray(array);

    int sum = 0;
    for (int i = 0; i < array.Length; i++)
    {
        if (i % 2 == 1) sum += array[i];
    }
    Console.WriteLine("Сумма элементов, стоящих на нечетных позициях, равна " + sum);

}

{
//Задача 38: Задайте массив вещественных чисел. Найдите разницу между максимальным 
//и минимальным элементов массива.
//[3 7 22 2 78] -> 76
Random random = new Random();
double[] array = new double[10];
for (int i = 0; i < array.Length; i++)
{
    array[i] = Math.Round(random.NextDouble() * 10 - 5,2);
}

Console.WriteLine("Вывод массива:");
for(int i = 0; i < array.Length; i++)
{
    Console.Write(array[i] + "\t");
}
Console.WriteLine();

double max = array[0];
double min = array[0];
for(int i = 1; i < array.Length; i++)
{
    if (array[i] > max) max = array[i];
    else if (array[i] < min) min = array[i];
}
Console.WriteLine();
Console.WriteLine("Максимальное значение равно" + max);
Console.WriteLine("Минимальное значение равно" + min);
Console.WriteLine("Их разность равна" + (max - min));
}
