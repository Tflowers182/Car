using System;

class Car
{
    public string model;
    public string color;
    public int year;

    // Display car details
    public void Display()
    {
        Console.WriteLine("Car Details:");
        Console.WriteLine("Model: " + model);
        Console.WriteLine("Color: " + color);
        Console.WriteLine("Year: " + year);
    }

    // Problem 1: Method with no parameters
    public void Start()
    {
        Console.WriteLine("The car is starting.");
    }

    // Problem 2: Method with a parameter
    public void Drive(int miles)
    {
        Console.WriteLine("The car drove " + miles + " miles.");
    }

    // Problem 3: Method that returns a value
    public string GetDescription()
    {
        return year + " " + color + " " + model;
    }

    // Problem 4: Method that updates a field
    public void Repaint(string newColor)
    {
        color = newColor;
        Console.WriteLine("The car has been repainted to " + color + ".");
    }
}

class Program
{
    static void Main()
    {
        // Create a new Car object
        Car myCar = new Car();
        myCar.model = "Civic";
        myCar.color = "Black";
        myCar.year = 2020;

        // Show car details
        myCar.Display();

        // Problem 1: Start the car
        myCar.Start();

        // Problem 2: Drive the car
        myCar.Drive(50);

        // Problem 3: Get and print car description
        string description = myCar.GetDescription();
        Console.WriteLine(description);  // Output: 2020 Black Civic

        // Problem 4: Repaint the car
        myCar.Repaint("red");

        // Confirm color changed
        Console.WriteLine("New color: " + myCar.color);
    }
}

