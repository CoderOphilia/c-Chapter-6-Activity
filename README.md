using System;
namespace Loops
{
    class Program
    {
        static void Main(string[] args)

            
        {
            //-----------------task 1------------------------------------------------------------------------------------------------
            /*for (int i = 1; i<=5; i++)
            {
               Console.WriteLine(Math.Pow(i,2));
            }*/

            //-------------- task 2 -----------------------------------------------------------------------------------------------------
            /*
            for (int i = 1; i <= 5; i++) ; //if we put a semicolon here then it will not show any error instead it will only print the statement once
            {
                Console.WriteLine("hello");
            }
            */
            
            //---------------task 3 : add the 5 numbers entered by the user -------------------------------------------------------------
            string userInput;
            double sum = 0;
            double userValue;

            /*for(int i = 0; i<5; i++)
            {
                Console.Write("Enter a number: ");
                userInput = Console.ReadLine();
                userValue = double.Parse(userInput);
                sum = sum + userValue;
            }*/

            //Console.WriteLine($"The sum is {sum}");

            //-----task 4 : user should decide how many times the numbers should be taken for the addition
            /*Console.Write("How many times the numbers should be taken from the user? ");
            int numCount = int.Parse(Console.ReadLine());
            for (int i = 0; i < numCount; i++)
            {
                Console.Write("Enter a number: ");
                userInput = Console.ReadLine();
                userValue = double.Parse(userInput);
                sum = sum + userValue;
            }
            */
            //Console.WriteLine($"The sum is {sum}");

            //--------task 5: while loop ------------------------------------------------------------------------------------------------

            /*
             * int i = 1;
            while (i <= 5)
            {
                Console.Write("Enter a number: ");
                userInput = Console.ReadLine();
                userValue = double.Parse(userInput);
                sum = sum + userValue;
                i++;
            }
            Console.WriteLine($"The sum is {sum}");
            */

            //-----------task 6: do - while----here the statement runs atleast once eventhough the condition is not met
           
            /*
             do
            {
                Console.Write("Enter a number: ");
                userInput = Console.ReadLine();
                userValue = double.Parse(userInput);
                sum = sum + userValue;
            }
            while (5 >= 0);
            Console.WriteLine($"The sum is {sum}");
            */

            //-----------task 7 : TryParse()
            ![image](https://github.com/CoderOphilia/c-Chapter-6-Activity/assets/159889719/a0fac906-f3fd-4c82-8032-7943d010aca1)

/*Console.Write("How many times the numbers should be taken from the user? ");
int numCount = int.Parse(Console.ReadLine());
bool isValid;
for (int i = 0; i < numCount; i++)
{
    do
    {
        Console.Write("Enter a number: ");
        userInput = Console.ReadLine();

        isValid = double.TryParse(userInput, out userValue); //TryParse will return two values [the result and the boolean]
        sum += userValue;

        if (isValid == false)
        {
            Console.WriteLine("Enter a numberic value: ");
        }
    }
    while (isValid == false);
    
} */
//Console.WriteLine($"The sum is {sum}");

//task 8: The above loop should be repeated as long as the usevalue is not zero
int numCount;
do
{
    Console.WriteLine("How many times the numbers should be taken from the user? ");
    numCount = int.Parse(Console.ReadLine());
    bool isValid;
    for (int i = 1; i <= numCount; i++)
    {
        do
        {
            Console.Write($"Enter a number {i}: ");
            userInput = Console.ReadLine();

            isValid = double.TryParse(userInput, out userValue); //TryParse will return two values [the result and the boolean]
            sum += userValue;

            if (isValid == false)
            {
                Console.WriteLine("Enter a numberic value: ");
            }
        }
        while (isValid == false);

    }
    
    if (numCount !=0)
    {
        Console.WriteLine($"The sum is {sum}");
    }
}
while(numCount != 0);

Console.ReadKey();
        }
    }
}
