# func_get_args()
 * 함수 안에서 쓰이면 인자를 전부 배열로 가져온다.

    function Arg() {
        return func_get_args();
    };
    $a = Arg("a", "b");            //["a", "b", "c"]
    $b = Arg("a", "b", "c", "d");  //["a", "b", "c", "d"]
    $c = Arg();                    //[]
