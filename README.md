using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace House_Price
{
    class Program
    {
        static void Main(string[] args)
        {
            double smallRoom = double.Parse(Console.ReadLine());
            double kitchen = double.Parse(Console.ReadLine());
            decimal pricePerMeter = decimal.Parse(Console.ReadLine());

            double middleRoom = smallRoom * 1.10;
            double LargeRoom = middleRoom * 1.10;
            double bathroom = smallRoom / 2.00;

            double houseArea = bathroom + smallRoom + middleRoom + LargeRoom + kitchen;
            houseArea *= 1.05;

            decimal housePrice = (decimal)houseArea * pricePerMeter;

            Console.WriteLine($"{housePrice:f2}");
        }
    }
}
