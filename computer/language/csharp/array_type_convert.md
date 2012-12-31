# Array type convert

        string[] stringArray = Array.ConvertAll<object, string>(
            objectArray,
            delegate(object o) {
                return o.ToString();
            }
        );
