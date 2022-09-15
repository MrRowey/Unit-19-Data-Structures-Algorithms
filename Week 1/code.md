```c#
static void Main(string[] args)
{
    // array declared of integers
    // containg 5 elements
    int[] a = new int[5];
    a[0] = 12;
    a[1] = 32;
    a[2] = 17;
    a[3] = 99;
    a[4] = 116;

    // short hand for adding in the element to the array and will auto size
    // this is lanauage spesific and would not work for C
    int[] c = new int[] { 1, 2, 3, 4 };

    // prints what is in the spesific element
    Console.WriteLine(a[3]);

    // prints out all the elements in the array
    for (int i =0; i <= 4; i++)
    {
        Console.WriteLine(a[i]);
    }

    // array of strings
    string[] s = new string[10];

    s[0] = "wolf";
    s[1] = "cat";
    s[2] = "dog";
    s[3] = "hamster";
    s[4] = "mouse";
    s[5] = "snake";
    s[6] = "mongoose";
    s[7] = "rabbit";
    s[8] = "rabbit";
    s[9] = "snake";

    string search = "rabbit";

    int location = -1;

    // linnear search
    for (int i = 0; i <= 9; i++)
    {
        if (s[i] == search)
        {
            location = i;
        }
    }

    Console.WriteLine("location was " + location);

    Console.WriteLine("hello world");

    Console.Write("press any key");
    Console.ReadKey();
}
```