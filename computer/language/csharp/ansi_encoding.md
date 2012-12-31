# ansi 파일 읽기
 * C#에서 ansi파일을 제대로 읽기 위해서는 인코딩설정을 해줘야 한다.
## Example

        Encoding encode = coding.GetEncoding("ks_c_5601-1987");
        TextReader reader = new StreamReader(filename, encode);
