using System;

class Program { static void Main(string[] args) {
    while (true) { Console.Clear();
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
        Console.Write("Select an option: ");
        int mainChoice = int.Parse(Console.ReadLine());

        if (mainChoice == 5)
        {
            Console.WriteLine("Exiting the program.");
            break;
        }

        switch (mainChoice)
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
            default:
                Console.WriteLine("Invalid option. Please choose a valid option.");
                break;
        }

        Console.WriteLine("Press Enter to continue...");
        Console.ReadLine();
    }
}

static void ConvertLength()
{
    Console.Clear();
    Console.WriteLine("Choose a length unit to convert from:");
    Console.WriteLine("1. Inch");
    Console.WriteLine("2. Millimeter");
    Console.WriteLine("3. Centimeter");
    Console.WriteLine("4. Yard");
    Console.WriteLine("5. Foot");
    Console.WriteLine("6. Meter");
    Console.WriteLine("7. Mile");
    Console.WriteLine("8. Kilometer");

    int lengthChoice = int.Parse(Console.ReadLine());
    Console.Write("Enter the value to convert: ");
    double value = double.Parse(Console.ReadLine());
    double result = 0;

    Console.WriteLine("Choose a length unit to convert to:");
    int lengthConversionChoice = int.Parse(Console.ReadLine());

    switch (lengthChoice)
    {
        case 1: // Inch
            switch (lengthConversionChoice)
            {
                case 2: // Millimeter
                    result = value * 25.4;
                    break;
                case 3: // Centimeter
                    result = value * 2.54;
                    break;
                case 4: // Yard
                    result = value * 0.0277778;
                    break;
                case 5: // Foot
                    result = value * 0.0833333;
                    break;
                case 6: // Meter
                    result = value * 0.0254;
                    break;
                case 7: // Mile
                    result = value * 0.0000157828;
                    break;
                case 8: // Kilometer
                    result = value * 0.0000254;
                    break;
            }
            break;
        case 2: // Millimeter
            switch (lengthConversionChoice)
            {
                case 1: // Inch
                    result = value * 0.0393701;
                    break;
                case 3: // Centimeter
                    result = value * 0.1;
                    break;
                case 4: // Yard
                    result = value * 0.00109361;
                    break;
                case 5: // Foot
                    result = value * 0.00328084;
                    break;
                case 6: // Meter
                    result = value * 0.001;
                    break;
                case 7: // Mile
                    result = value * 6.2137e-6;
                    break;
                case 8: // Kilometer
                    result = value * 1e-6;
                    break;
            }
            break;
        case 3: // Centimeter
            switch (lengthConversionChoice)
            {
                case 1: // Inch
                    result = value * 0.393701;
                    break;
                case 2: // Millimeter
                    result = value * 10;
                    break;
                case 4: // Yard
                    result = value * 0.0109361;
                    break;
                case 5: // Foot
                    result = value * 0.0328084;
                    break;
                case 6: // Meter
                    result = value * 0.01;
                    break;
                case 7: // Mile
                    result = value * 6.2137e-5;
                    break;
                case 8: // Kilometer
                    result = value * 1e-5;
                    break;
            }
            break;
        case 4: // Yard
            switch (lengthConversionChoice)
            {
                case 1: // Inch
                    result = value * 36;
                    break;
                case 2: // Millimeter
                    result = value * 914.4;
                    break;
                case 3: // Centimeter
                    result = value * 91.44;
                    break;
                case 5: // Foot
                    result = value * 3.048;
                    break;
                case 6: // Meter
                    result = value * 0.9144;
                    break;
                case 7: // Mile
                    result = value * 0.000568182;
                    break;
                case 8: // Kilometer
                    result = value * 0.0009144;
                    break;
            }
            break;
        case 5: // Foot
            switch (lengthConversionChoice)
            {
                case 1: // Inch
                    result = value * 12;
                    break;
                case 2: // Millimeter
                    result = value * 304.8;
                    break;
                case 3: // Centimeter
                    result = value * 30.48;
                    break;
                case 4: // Yard
                    result = value * 0.333333;
                    break;
                case 6: // Meter
                    result = value * 0.3048;
                    break;
                case 7: // Mile
                    result = value * 0.000189394;
                    break;
                case 8: // Kilometer
                    result = value * 0.0003048;
                    break;
            }
            break;
        case 6: // Meter
            switch (lengthConversionChoice)
            {
                case 1: // Inch
                    result = value * 39.3701;
                    break;
                case 2: // Millimeter
                    result = value * 1000;
                    break;
                case 3: // Centimeter
                    result = value * 100;
                    break;
                case 4: // Yard
                    result = value * 1.09361;
                    break;
                case 5: // Foot
                    result = value * 3.28084;
                    break;
                case 7: // Mile
                    result = value * 0.000621371;
                    break;
                case 8: // Kilometer
                    result = value * 0.001;
                    break;
            }
            break;
        case 7: // Mile
            switch (lengthConversionChoice)
            {
                case 1: // Inch
                    result = value * 63360;
                    break;
                case 2: // Millimeter
                    result = value * 1609344;
                    break;
                case 3: // Centimeter
                    result = value * 160934.4;
                    break;
                case 4: // Yard
                    result = value * 1760;
                    break;
                case 5: // Foot
                    result = value * 5280;
                    break;
                case 6: // Meter
                    result = value * 1609.34;
                    break;
                case 8: // Kilometer
                    result = value * 1.60934;
                    break;
            }
            break;
        case 8: // Kilometer
            switch (lengthConversionChoice)
            {
                case 1: // Inch
                    result = value * 39370.1;
                    break;
                case 2: // Millimeter
                    result = value * 1e+6;
                    break;
                case 3: // Centimeter
                    result = value * 1e+5;
                    break;
                case 4: // Yard
                    result = value * 1094;
                    break;
                case 5: // Foot
                    result = value * 3280.84;
                    break;
                case 6: // Meter
                    result = value * 1000;
                    break;
                case 7: // Mile
                    result = value * 0.621371;
                    break;
            }
            break;
        default:
            Console.WriteLine("Invalid option.");
            break;
    }

    Console.WriteLine($"Result: {value} is equivalent to {result} in the selected unit.");
}

static void ConvertArea()
{
    Console.Clear();
    Console.WriteLine("Choose an area unit to convert from:");
    Console.WriteLine("1. Square Inch");
    Console.WriteLine("2. Square Foot");
    Console.WriteLine("3. Square Meter");
    Console.WriteLine("4. Square Yard");
    Console.WriteLine("5. Square Kilometer");
    Console.WriteLine("6. Square Mile");
    Console.WriteLine("7. Hectare");
    Console.WriteLine("8. Acre");

    int areaChoice = int.Parse(Console.ReadLine());
    Console.Write("Enter the value to convert: ");
    double value = double.Parse(Console.ReadLine());
    double result = 0;

    Console.WriteLine("Choose an area unit to convert to:");
    int areaConversionChoice = int.Parse(Console.ReadLine());

    switch (areaChoice)
    {
        case 1: // Square Inch
            switch (areaConversionChoice)
            {
                case 2: // Square Foot
                    result = value * 0.00694444;
                    break;
                case 3: // Square Meter
                    result = value * 0.00064516;
                    break;
                case 4: // Square Yard
                    result = value * 0.000771605;
                    break;
                case 5: // Square Kilometer
                    result = value * 6.4516e-10;
                    break;
                case 6: // Square Mile
                    result = value * 2.4909766860524e-10;
                    break;
                case 7: // Hectare
                    result = value * 6.4516e-8;
                    break;
                case 8: // Acre
                    result = value * 1.5942e-7;
                    break;
            }
            break;
        case 2: // Square Foot
            switch (areaConversionChoice)
            {
                case 1: // Square Inch
                    result = value * 144;
                    break;
                case 3: // Square Meter
                    result = value * 0.092903;
                    break;
                case 4: // Square Yard
                    result = value * 0.111111;
                    break;
                case 5: // Square Kilometer
                    result = value * 9.2903e-8;
                    break;
                case 6: // Square Mile
                    result = value * 3.587e-8;
                    break;
                case 7: // Hectare
                    result = value * 9.2903e-6;
                    break;
                case 8: // Acre
                    result = value * 2.2957e-5;
                    break;
            }
            break;
        case 3: // Square Meter
            switch (areaConversionChoice)
            {
                case 1: // Square Inch
                    result = value * 1550;
                    break;
                case 2: // Square Foot
                    result = value * 10.7639;
                    break;
                case 4: // Square Yard
                    result = value * 1.19599;
                    break;
                case 5: // Square Kilometer
                    result = value * 1e-6;
                    break;
                case 6: // Square Mile
                    result = value * 3.861e-7;
                    break;
                case 7: // Hectare
                    result = value * 0.0001;
                    break;
                case 8: // Acre
                    result = value * 0.000247105;
                    break;
            }
            break;
        case 4: // Square Yard
            switch (areaConversionChoice)
            {
                case 1: // Square Inch
                    result = value * 1296;
                    break;
                case 2: // Square Foot
                    result = value * 9;
                    break;
                case 3: // Square Meter
                    result = value * 0.836127;
                    break;
                case 5: // Square Kilometer
                    result = value * 8.3613e-7;
                    break;
                case 6: // Square Mile
                    result = value * 3.2283e-7;
                    break;
                case 7: // Hectare
                    result = value * 0.0000836;
                    break;
                case 8: // Acre
                    result = value * 0.000206612;
                    break;
            }
            break;
        case 5: // Square Kilometer
            switch (areaConversionChoice)
            {
                case 1: // Square Inch
                    result = value * 1.55e+9;
                    break;
                case 2: // Square Foot
                    result = value * 1.076e+7;
                    break;
                case 3: // Square Meter
                    result = value * 1e+6;
                    break;
                case 4: // Square Yard
                    result = value * 1.19599e+6;
                    break;
                case 6: // Square Mile
                    result = value * 0.386102;
                    break;
                case 7: // Hectare
                    result = value * 100;
                    break;
                case 8: // Acre
                    result = value * 247.105;
                    break;
            }
            break;
        case 6: // Square Mile
            switch (areaConversionChoice)
            {
                case 1: // Square Inch
                    result = value * 6.273e+9;
                    break;
                case 2: // Square Foot
                    result = value * 4.354e+7;
                    break;
                case 3: // Square Meter
                    result = value * 2.58999e+6;
                    break;
                case 4: // Square Yard
                    result = value * 3.0976e+6;
                    break;
                case 5: // Square Kilometer
                    result = value * 2.58999;
                    break;
                case 7: // Hectare
                    result = value * 258.999;
                    break;
                case 8: // Acre
                    result = value * 640;
                    break;
            }
            break;
        case 7: // Hectare
            switch (areaConversionChoice)
            {
                case 1: // Square Inch
                    result = value * 1.55e+7;
                    break;
                case 2: // Square Foot
                    result = value * 107639;
                    break;
                case 3: // Square Meter
                    result = value * 10000;
                    break;
                case 4: // Square Yard
                    result = value * 11959.9;
                    break;
                case 5: // Square Kilometer
                    result = value * 0.01;
                    break;
                case 6: // Square Mile
                    result = value * 0.00386102;
                    break;
                case 8: // Acre
                    result = value * 2.47105;
                    break;
            }
            break;
        case 8: // Acre
            switch (areaConversionChoice)
            {
                case 1: // Square Inch
                    result = value * 6.273e+6;
                    break;
                case 2: // Square Foot
                    result = value * 43560;
                    break;
                case 3: // Square Meter
                    result = value * 4046.86;
                    break;
                case 4: // Square Yard
                    result = value * 4840;
                    break;
                case 5: // Square Kilometer
                    result = value * 0.00404686;
                    break;
                case 6: // Square Mile
                    result = value * 0.0015625;
                    break;
                case 7: // Hectare
                    result = value * 0.404686;
                    break;
            }
            break;
        default:
            Console.WriteLine("Invalid option.");
            break;
    }

    Console.WriteLine($"Result: {value} is equivalent to {result} in the selected unit.");
}

static void ConvertMass()
{
    Console.Clear();
    Console.WriteLine("Choose a mass unit to convert from:");
    Console.WriteLine("1. Grain");
    Console.WriteLine("2. Ounce");
    Console.WriteLine("3. Gram");
    Console.WriteLine("4. Pound");
    Console.WriteLine("5. Kilogram");
    Console.WriteLine("6. Short Ton");
    Console.WriteLine("7. Metric Ton");
    Console.WriteLine("8. Long Ton");

    int massChoice = int.Parse(Console.ReadLine());
    Console.Write("Enter the value to convert: ");
    double value = double.Parse(Console.ReadLine());
    double result = 0;

    Console.WriteLine("Choose a mass unit to convert to:");
    int massConversionChoice = int.Parse(Console.ReadLine());

    switch (massChoice)
    {
        case 1: // Grain
            switch (massConversionChoice)
            {
                case 2: // Ounce
                    result = value * 0.00228571;
                    break;
                case 3: // Gram
                    result = value * 0.0647989;
                    break;
                case 4: // Pound
                    result = value * 0.000142857;
                    break;
                case 5: // Kilogram
                    result = value * 6.47989e-5;
                    break;
                case 6: // Short Ton
                    result = value * 7.14286e-8;
                    break;
                case 7: // Metric Ton
                    result = value * 6.47989e-8;
                    break;
                case 8: // Long Ton
                    result = value * 5.71429e-8;
                    break;
            }
            break;
        case 2: // Ounce
            switch (massConversionChoice)
            {
                case 1: // Grain
                    result = value * 437.5;
                    break;
                case 3: // Gram
                    result = value * 28.3495;
                    break;
                case 4: // Pound
                    result = value * 0.0625;
                    break;
                case 5: // Kilogram
                    result = value * 0.0283495;
                    break;
                case 6: // Short Ton
                    result = value * 3.125e-5;
                    break;
                case 7: // Metric Ton
                    result = value * 2.83495e-5;
                    break;
                case 8: // Long Ton
                    result = value * 2.5e-5;
                    break;
            }
            break;
        case 3: // Gram
            switch (massConversionChoice)
            {
                case 1: // Grain
                    result = value * 15.4324;
                    break;
                case 2: // Ounce
                    result = value * 0.03527396;
                    break;
                case 4: // Pound
                    result = value * 0.00220462;
                    break;
                case 5: // Kilogram
                    result = value * 0.001;
                    break;
                case 6: // Short Ton
                    result = value * 1.10231e-6;
                    break;
                case 7: // Metric Ton
                    result = value * 1e-6;
                    break;
                case 8: // Long Ton
                    result = value * 8.8185e-7;
                    break;
            }
            break;
        case 4: // Pound
            switch (massConversionChoice)
            {
                case 1: // Grain
                    result = value * 7000;
                    break;
                case 2: // Ounce
                    result = value * 16;
                    break;
                case 3: // Gram
                    result = value * 453.592;
                    break;
                case 5: // Kilogram
                    result = value * 0.453592;
                    break;
                case 6: // Short Ton
                    result = value * 0.0005;
                    break;
                case 7: // Metric Ton
                    result = value * 0.000453592;
                    break;
                case 8: // Long Ton
                    result = value * 0.000446429;
                    break;
            }
            break;
        case 5: // Kilogram
            switch (massConversionChoice)
            {
                case 1: // Grain
                    result = value * 15432.4;
                    break;
                case 2: // Ounce
                    result = value * 35.27396;
                    break;
                case 3: // Gram
                    result = value * 1000;
                    break;
                case 4: // Pound
                    result = value * 2.20462;
                    break;
                case 6: // Short Ton
                    result = value * 0.00110231;
                    break;
                case 7: // Metric Ton
                    result = value * 0.001;
                    break;
                case 8: // Long Ton
                    result = value * 0.000984207;
                    break;
            }
            break;
        case 6: // Short Ton
            switch (massConversionChoice)
            {
                case 1: // Grain
                    result = value * 1.4e+7;
                    break;
                case 2: // Ounce
                    result = value * 32000;
                    break;
                case 3: // Gram
                    result = value * 907185;
                    break;
                case 4: // Pound
                    result = value * 2000;
                    break;
                case 5: // Kilogram
                    result = value * 907.185;
                    break;
                case 7: // Metric Ton
                    result = value * 0.907185;
                    break;
                case 8: // Long Ton
                    result = value * 0.892857;
                    break;
            }
            break;
        case 7: // Metric Ton
            switch (massConversionChoice)
            {
                case 1: // Grain
                    result = value * 1.5432e+7;
                    break;
                case 2: // Ounce
                    result = value * 35274;
                    break;
                case 3: // Gram
                    result = value * 1e+6;
                    break;
                case 4: // Pound
                    result = value * 2204.62;
                    break;
                case 5: // Kilogram
                    result = value * 1000;
                    break;
                case 6: // Short Ton
                    result = value * 1.10231;
                    break;
                case 8: // Long Ton
                    result = value * 0.984207;
                    break;
            }
            break;
        case 8: // Long Ton
            switch (massConversionChoice)
            {
                case 1: // Grain
                    result = value * 1.6e+7;
                    break;
                case 2: // Ounce
                    result = value * 35840;
                    break;
                case 3: // Gram
                    result = value * 1.01605e+6;
                    break;
                case 4: // Pound
                    result = value * 2240;
                    break;
                case 5: // Kilogram
                    result = value * 1016.05;
                    break;
                case 6: // Short Ton
                    result = value * 1.12;
                    break;
                case 7: // Metric Ton
                    result = value * 1.01605;
                    break;
            }
            break;
        default:
            Console.WriteLine("Invalid option.");
            break;
    }

    Console.WriteLine($"Result: {value} is equivalent to {result} in the selected unit.");
}

static void ConvertVolume()
{
    Console.Clear();
    Console.WriteLine("Choose a volume unit to convert from:");
    Console.WriteLine("1. Teaspoon");
    Console.WriteLine("2. Milliliter");
    Console.WriteLine("3. Tablespoon");
    Console.WriteLine("4. Liter");
    Console.WriteLine("5. Fluid Ounce");
    Console.WriteLine("6. Gallon");
    Console.WriteLine("7. Cup");
    Console.WriteLine("8. Pint");
    Console.WriteLine("9. Cubic Meter");

    int volumeChoice = int.Parse(Console.ReadLine());
    Console.Write("Enter the value to convert: ");
    double value = double.Parse(Console.ReadLine());
    double result = 0;

    Console.WriteLine("Choose a volume unit to convert to:");
    int volumeConversionChoice = int.Parse(Console.ReadLine());

    switch (volumeChoice)
    {
        case 1: // Teaspoon
            switch (volumeConversionChoice)
            {
                case 2: // Milliliter
                    result = value * 5.91939;
                    break;
                case 3: // Tablespoon
                    result = value * 0.333333;
                    break;
                case 4: // Liter
                    result = value * 0.00591939;
                    break;
                case 5: // Fluid Ounce
                    result = value * 0.2007;
                    break;
                case 6: // Gallon
                    result = value * 0.00156373;
                    break;
                case 7: // Cup
                    result = value * 0.0396825;
                    break;
                case 8: // Pint
                    result = value * 0.0198413;
                    break;
                case 9: // Cubic Meter
                    result = value * 5.9194e-6;
                    break;
            }
            break;
        case 2: // Milliliter
            switch (volumeConversionChoice)
            {
                case 1: // Teaspoon
                    result = value * 0.168936;
                    break;
                case 3: // Tablespoon
                    result = value * 0.06;
                    break;
                case 4: // Liter
                    result = value * 0.001;
                    break;
                case 5: // Fluid Ounce
                    result = value * 0.033814;
                    break;
                case 6: // Gallon
                    result = value * 0.000264172;
                    break;
                case 7: // Cup
                    result = value * 0.00422675;
                    break;
                case 8: // Pint
                    result = value * 0.00211338;
                    break;
                case 9: // Cubic Meter
                    result = value * 1e-6;
                    break;
            }
            break;
        case 3: // Tablespoon
            switch (volumeConversionChoice)
            {
                case 1: // Teaspoon
                    result = value * 3;
                    break;
                case 2: // Milliliter
                    result = value * 16.6667;
                    break;
                case 4: // Liter
                    result = value * 0.015;
                    break;
                case 5: // Fluid Ounce
                    result = value * 0.50721;
                    break;
                case 6: // Gallon
                    result = value * 0.00390625;
                    break;
                case 7: // Cup
                    result = value * 0.125;
                    break;
                case 8: // Pint
                    result = value * 0.0625;
                    break;
                case 9: // Cubic Meter
                    result = value * 1.6667e-5;
                    break;
            }
            break;
        case 4: // Liter
            switch (volumeConversionChoice)
            {
                case 1: // Teaspoon
                    result = value * 169.07;
                    break;
                case 2: // Milliliter
                    result = value * 1000;
                    break;
                case 3: // Tablespoon
                    result = value * 66.6667;
                    break;
                case 5: // Fluid Ounce
                    result = value * 33.814;
                    break;
                case 6: // Gallon
                    result = value * 0.264172;
                    break;
                case 7: // Cup
                    result = value * 4.22675;
                    break;
                case 8: // Pint
                    result = value * 2.11338;
                    break;
                case 9: // Cubic Meter
                    result = value * 0.001;
                    break;
            }
            break;
        case 5: // Fluid Ounce
            switch (volumeConversionChoice)
            {
                case 1: // Teaspoon
                    result = value * 4.92892;
                    break;
                case 2: // Milliliter
                    result = value * 29.5735;
                    break;
                case 3: // Tablespoon
                    result = value * 1.04084;
                    break;
                case 4: // Liter
                    result = value * 0.0295735;
                    break;
                case 6: // Gallon
                    result = value * 0.0078125;
                    break;
                case 7: // Cup
                    result = value * 0.125;
                    break;
                case 8: // Pint
                    result = value * 0.0625;
                    break;
                case 9: // Cubic Meter
                    result = value * 2.9574e-5;
                    break;
            }
            break;
        case 6: // Gallon
            switch (volumeConversionChoice)
            {
                case 1: // Teaspoon
                    result = value * 768;
                    break;
                case 2: // Milliliter
                    result = value * 3785.41;
                    break;
                case 3: // Tablespoon
                    result = value * 256;
                    break;
                case 4: // Liter
                    result = value * 3.78541;
                    break;
                case 5: // Fluid Ounce
                    result = value * 128;
                    break;
                case 7: // Cup
                    result = value * 16;
                    break;
                case 8: // Pint
                    result = value * 8;
                    break;
                case 9: // Cubic Meter
                    result = value * 0.00378541;
                    break;
            }
            break;
        case 7: // Cup
            switch (volumeConversionChoice)
            {
                case 1: // Teaspoon
                    result = value * 48;
                    break;
                case 2: // Milliliter
                    result = value * 240;
                    break;
                case 3: // Tablespoon
                    result = value * 16;
                    break;
                case 4: // Liter
                    result = value * 0.24;
                    break;
                case 5: // Fluid Ounce
                    result = value * 8;
                    break;
                case 6: // Gallon
                    result = value * 0.0625;
                    break;
                case 8: // Pint
                    result = value * 0.5;
                    break;
                case 9: // Cubic Meter
                    result = value * 0.00024;
                    break;
            }
            break;
        case 8: // Pint
            switch (volumeConversionChoice)
            {
                case 1: // Teaspoon
                    result = value * 96;
                    break;
                case 2: // Milliliter
                    result = value * 473.176;
                    break;
                case 3: // Tablespoon
                    result = value * 32;
                    break;
                case 4: // Liter
                    result = value * 0.473176;
                    break;
                case 5: // Fluid Ounce
                    result = value * 16;
                    break;
                case 6: // Gallon
                    result = value * 0.125;
                    break;
                case 7: // Cup
                    result = value * 2;
                    break;
                case 9: // Cubic Meter
                    result = value * 0.000473176;
                    break;
            }
            break;
        case 9: // Cubic Meter
            switch (volumeConversionChoice)
            {
                case 1: // Teaspoon
                    result = value * 169070;
                    break;
                case 2: // Milliliter
                    result = value * 1e+6;
                    break;
                case 3: // Tablespoon
                    result = value * 6e+6;
                    break;
                case 4: // Liter
                    result = value * 1000;
                    break;
                case 5: // Fluid Ounce
                    result = value * 33814;
                    break;
                case 6: // Gallon
                    result = value * 264.172;
                    break;
                case 7: // Cup
                    result = value * 4226.75;
                    break;
                case 8: // Pint
                    result = value * 2113.38;
                    break;
            }
            break;
        default:
            Console.WriteLine("Invalid option.");
            break;
    }

    Console.WriteLine($"Result: {value} is equivalent to {result} in the selected unit.");
}

static void Main1(string[] args)
{
    bool quit = false;

    while (!quit)
    {
        Console.WriteLine("Choose what to convert:");
        Console.WriteLine("1. Length");
        Console.WriteLine("2. Area");
        Console.WriteLine("3. Mass");
        Console.WriteLine("4. Volume");
        Console.WriteLine("5. Quit");

        int choice = int.Parse(Console.ReadLine());

        switch (choice)
        {
            case 1: // Length
                ConvertLength();
                break;
            case 2: // Area
                ConvertArea();
                break;
            case 3: // Mass
                ConvertMass();
                break;
            case 4: // Volume
                ConvertVolume();
                break;
            case 5: // Quit
                quit = true;
                break;
            default:
                Console.WriteLine("Invalid choice. Please try again.");
                break;
            }
        }
    }
}
