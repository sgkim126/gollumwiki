# dynamic, var, object
## dynamic
 * compile time type check를 하지 않음.
 * type에 어긋나는 행동을 하면, runtime error가 발생한다.

        using System;
        namespace ConsoleApplication1
        {
            class Program
            {
                static void Main(string[] args)
                {
                    dynamic a = 0;
                    Console.WriteLine(a is int);      //True
                    Console.WriteLine(a is double);   //False
                    a += 0.1;
                    Console.WriteLine(a is int);      //False
                    Console.WriteLine(a is double);   //True
                    Console.Read();
                }
            }
        }

## var
 * Initialize시 type을 추정하여 결정한다.
 * 그렇기 때문에 선언시 initialize해야 한다.

        using System;
        namespace ConsoleApplication1
        {
            class Program
            {
                static void Main(string[] args)
                {
                    var a = 0;                       //a는 int
                    a += 0.1;                        //여기서 컴파일에러.
                    Console.Read();
                }
            }
        }

## object
 * 모든 class의 부모인 class.
 * 실제로 type이 결정된게 아니기 때문에, 사용할때 명시적으로 casting해야 한다.

        using System;
        namespace ConsoleApplication1
        {
            class Program
            {
                static void Main(string[] args)
                {
                    object a = 0;
                    a = (int)a + 3;
                    Console.WriteLine(a);
                    Console.Read();
                }
            }
        }
