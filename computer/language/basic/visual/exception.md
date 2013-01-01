# Exception

        Module Module1
            Sub Main()
                Try 
                    Throw New ArgumentException("exception test")
                Catch ex As Exception
                    System.Console.WriteLine(Err.Description)
                    System.Console.WriteLine(Err.ToString)
                    System.Console.WriteLine(ex.Message)
                    System.Console.WriteLine(ex.ToString)
                End Try
            End Sub
        End Module

## result

        exception test
        Microsoft.VisualBasic.ErrObject
        exception test
        System.ArgumentException: exception test
           at ConsoleApplication1.Module1.Main() in Module1.vb:line 4
