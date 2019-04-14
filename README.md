# Same_Class_Name_In_Different_Namespace
Same_Class_Name_In_Different_Namespace, How to use same class name with other namespace

```
using ClassStructs2;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

using f = ClassStructs2;   /*Specify namespace here*/

namespace ClassStructs
{
    public class Test
    {
        public int Id { get; set; }
        public string Nmae { get; set; }
        public Test()
        {
            Id = 100;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            ////Object initializor
            //Test test = new Test() {
            //    Id =121,
            //    Nmae="Rajesh"
            //};

            //Call Other namespace class with same name
            f.Test test = new f.Test();
            Console.WriteLine(test.Id);

        }
    }
}

namespace ClassStructs2
{
    public class Test
    {
        public int Id { get; set; }
        public string Nmae { get; set; }

        public Test()
        {
            Id = 101;
        }
    }
}

```

