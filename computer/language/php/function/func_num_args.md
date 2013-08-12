# func_num_args()
 * 함수 내에서 쓰이면 함수의 인자 수를 가져온다.

    function Arg() {
        return func_num_args();
    }
    echo Arg("a");            //1
    echo Arg("a", "b", "c");  //3
    echo Arg();               //0
