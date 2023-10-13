using System;

class Program
{
     
    static void Main(string[] args)
    {
        while (true)
        {
            Console.Clear(); 
            Console.WriteLine("█████╗░░█████╗░███╗░░██╗██╗░░░██╗███████╗██████╗░████████╗");
            Console.WriteLine("██╔══██╗██╔══██╗████╗░██║██║░░░██║██╔════╝██╔══██╗╚══██╔══╝");
            Console.WriteLine("██║░░╚═╝██║░░██║██╔██╗██║╚██╗░██╔╝█████╗░░██████╔╝░░░██║░░░");
            Console.WriteLine("██║░░██╗██║░░██║██║╚████║░╚████╔╝░██╔══╝░░██╔══██╗░░░██║░░░");
            Console.WriteLine("█████╔╝╚█████╔╝██║░╚███║░░╚ ██╔╝░░███████╗██║░░██║░░░██║░░░");
            Console.WriteLine("░╚════╝░░╚════╝░╚═╝░░╚══╝░░░╚═╝░░░╚══════╝╚═╝░░╚═╝░░░╚═╝░░░");
            Console.WriteLine("Choose what to convert:");
            Console.WriteLine("1. Length");
            Console.WriteLine("2. Area");
            Console.WriteLine("3. Mass");
            Console.WriteLine("4. Volume");
            Console.WriteLine("5. Exit");

            int choice = int.Parse(Console.ReadLine());

            switch (choice)
            {
                case 1:
                    ConvertLength();
                    break;
                case 2:
                    ConvertArea();
                    break;
                case 3:
                    ConvertMass();
                    break;
                case 4:
                    ConvertVolume();
                    break;
                case 5:
                    Environment.Exit(0);
                    break;
                default:
                    Console.WriteLine("Invalid choice. Please select a valid option.");
                    break;
            }
        }
    }

    static void ConvertLength()
    {
        Console.WriteLine("Choose the unit to convert from:");
        Console.WriteLine("1. Inch");
        Console.WriteLine("2. Millimeter");
        Console.WriteLine("3. Centimeter");
        Console.WriteLine("4. Yard");
        Console.WriteLine("5. Meter");
        Console.WriteLine("6. Mile");
        Console.WriteLine("7. Kilometer");

        int fromUnit = int.Parse(Console.ReadLine());

        Console.WriteLine("Enter the value to convert:");
        double value = double.Parse(Console.ReadLine());

        Console.WriteLine("Choose the unit to convert to:");
        int toUnit = int.Parse(Console.ReadLine());

        double result = 0;

        double[] conversionFactors = { 25.4, 0.0393701, 0.1, 0.00109361, 0.0254, 1.57828e-5, 2.54e-5 };

        result = value * conversionFactors[fromUnit - 1] / conversionFactors[toUnit - 1];

        Console.WriteLine($"{value} from unit {fromUnit} to unit {toUnit} is {result}");
        ReturnToMainMenu();
    }

    static void ConvertArea()
    {
        Console.WriteLine("Choose the unit to convert from:");
        Console.WriteLine("1. Square Inch");
        Console.WriteLine("2. Square Millimeter");
        Console.WriteLine("3. Square Centimeter");
        Console.WriteLine("4. Square Yard");
        Console.WriteLine("5. Square Meter");
        Console.WriteLine("6. Square Mile");
        Console.WriteLine("7. Square Kilometer");
        Console.WriteLine("8. Hectare");
        Console.WriteLine("9. Acre");

        int fromUnit = int.Parse(Console.ReadLine());

        Console.WriteLine("Enter the value to convert:");
        double value = double.Parse(Console.ReadLine());

        Console.WriteLine("Choose the unit to convert to:");
        int toUnit = int.Parse(Console.ReadLine());

        double result = 0;

        double[] conversionFactors = { 1, 645.16, 6.4516, 0.000771605, 0.00064516, 1.59423e-7, 2.47105e-10, 2.47105, 0.000247105 };

        result = value * conversionFactors[fromUnit - 1] / conversionFactors[toUnit - 1];

        Console.WriteLine($"{value} from unit {fromUnit} to unit {toUnit} is {result}");
        ReturnToMainMenu();
    }

    static void ConvertMass()
    {
        Console.WriteLine("Choose the unit to convert from:");
        Console.WriteLine("1. Grain");
        Console.WriteLine("2. Ounce");
        Console.WriteLine("3. Gram");
        Console.WriteLine("4. Pound");
        Console.WriteLine("5. Kilogram");
        Console.WriteLine("6. Short Ton");
        Console.WriteLine("7. Metric Ton");
        Console.WriteLine("8. Long Ton");

        int fromUnit = int.Parse(Console.ReadLine());

        Console.WriteLine("Enter the value to convert:");
        double value = double.Parse(Console.ReadLine());

        Console.WriteLine("Choose the unit to convert to:");
        int toUnit = int.Parse(Console.ReadLine());

        double result = 0;

        double[] conversionFactors = { 1, 1/7000.0, 1/15.4324, 1/7000.0, 1/35.2739, 1/15432.4, 1/2204.62, 1/15.4324 };

        result = value * conversionFactors[fromUnit - 1] / conversionFactors[toUnit - 1];

        Console.WriteLine($"{value} from unit {fromUnit} to unit {toUnit} is {result}");
        ReturnToMainMenu();
    }

    static void ConvertVolume()
    {
        Console.WriteLine("Choose the unit to convert from:");
        Console.WriteLine("1. Teaspoon");
        Console.WriteLine("2. Milliliter");
        Console.WriteLine("3. Tablespoon");
        Console.WriteLine("4. Liter");
        Console.WriteLine("5. Fluid Ounce");
        Console.WriteLine("6. Gallon");
        Console.WriteLine("7. Cup");
        Console.WriteLine("8. Pint");
        Console.WriteLine("9. Cubic Meter");

        int fromUnit = int.Parse(Console.ReadLine());

        Console.WriteLine("Enter the value to convert:");
        double value = double.Parse(Console.ReadLine());

        Console.WriteLine("Choose the unit to convert to:");
        int toUnit = int.Parse(Console.ReadLine());

        double result = 0;

        double[] conversionFactors = { 1, 1, 3, 0.001, 0.0351951, 0.000219969, 0.000264172, 0.000473176, 1e-6 };

        result = value * conversionFactors[fromUnit - 1] / conversionFactors[toUnit - 1];

        Console.WriteLine($"{value} from unit {fromUnit} to unit {toUnit} is {result}");
        ReturnToMainMenu();
    }

    static void ReturnToMainMenu()
    {
        Console.WriteLine("Press Enter to return to the main menu...");
        Console.ReadLine();
        Console.Clear();
        Main(new string[] { });
    }
}
