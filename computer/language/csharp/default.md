# default

        using System.Text;
        namespace DefaultKeyword
        {
            class Program
            {
                static void Main(string[] args)
                {
                    bool b = default(bool);
                    System.Console.WriteLine(b);
                    int i = default(int);
                    System.Console.WriteLine(i);
                    float f = default(float);
                    System.Console.WriteLine(f);
                    char c = default(char);
                    System.Console.WriteLine(c);
                    string s = default(string);
                    System.Console.WriteLine(s);
                }
            }
        }
