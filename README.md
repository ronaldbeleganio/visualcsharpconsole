# visualcsharpconsole
Simple Visual C# Console Application

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace FOR_CJ
{
    class Program
    {
        static void Main(string[] args)
        {
            int capacity,totalcapacity;
            int weight;
            int space;
            char yn1, yn2;
            bool valid = false;

            Console.WriteLine("Enter the capacity:");
            capacity = Convert.ToInt32(Console.ReadLine());
            totalcapacity = capacity;

            do
            {
                Console.WriteLine("Enter the weight");
                weight = Convert.ToInt32(Console.ReadLine());

                Console.WriteLine("Do you want to load? Y / N");
                yn1 = Convert.ToChar(Console.ReadLine());

                while (!valid)
                {
                    if (yn1 == 'Y')
                    {
                        if (weight > capacity)
                        {
                            Console.WriteLine("Overload");
                            break;
                        }
                        else
                        {
                            capacity = capacity - weight;
                            space = capacity;
                            Console.WriteLine("Total Capacity: " + totalcapacity);
                            Console.WriteLine("Free Space: " + space);
                            break;
                        }
                    }
                    else
                    {
                        break;
                    }
                }
                Console.WriteLine("Do you want to exit? Y / N");
                yn2 = Convert.ToChar(Console.ReadLine());

                if (yn2 == 'Y')
                {
                    return;
                }

            } while (yn2 == 'N');
            Console.ReadKey();
        }
    }
}
