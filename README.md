using System;

namespace MysticEcho
{
    class Program
    {
        static void Main(string[] args)
        {
            // Creating an instance of the RandomNumberGenerator class
            RandomNumberGenerator rng = new RandomNumberGenerator();
            int randomNum = rng.GenerateRandomNumber(1, 100);

            // Display the random number
            Console.WriteLine("Generated Random Number: " + randomNum);

            // Creating an instance of the EchoService class
            EchoService echoService = new EchoService();
            string echoedMessage = echoService.Echo("Hello, Mystic Echo!");

            // Display the echoed message
            Console.WriteLine("Echoed Message: " + echoedMessage);
        }
    }

    // A class to generate random numbers
    public class RandomNumberGenerator
    {
        private Random _random;

        public RandomNumberGenerator()
        {
            _random = new Random();
        }

        // Method to generate a random number within a specified range
        public int GenerateRandomNumber(int minValue, int maxValue)
        {
            return _random.Next(minValue, maxValue);
        }
    }

    // A class to echo a message
    public class EchoService
    {
        // Method to echo the input message
        public string Echo(string message)
        {
            return message;
        }
    }
}
