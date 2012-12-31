# Functional

        namespace Functional
        {
            class Program
            {
                public delegate int intIntToInt(int x, int y);
                public static void Main()
                {
                    intIntToInt sum1 = (x, y) => x + y;
                    intIntToInt mul1 = (x, y) => x * y;

                    System.Linq.Expressions.Expression<intIntToInt> sum2 = (x, y) => x + y;
                    System.Linq.Expressions.Expression<intIntToInt> mul2 = (x, y) => x * y;

                    System.Func<int, int, int> sum3 = (x, y) => x + y;
                    System.Func<int, int, int> mul3 = (x, y) => x * y;
                }
            }
        }
