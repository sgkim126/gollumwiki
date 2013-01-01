# array convert

        Array.ConvertAll(Of Object, String)(input_array, New Converter(Of Object, String)(AddressOf Convert.ToString))

## .net 2.0 이하

        DirectCast(input_array.ToArray(GetType(String)), String())
