# func_get_arg($index)
 * offset이 $i인 인자를 가져온다.

    function Arg($i) {
        return func_get_arg($i);
    };
    Arg(0, "a", "b", "c");  // 0
    Arg(1, "a", "b", "c");  // "a"
    Arg(2, "a", "b", "c");  // "b"
    Arg(3, "a", "b", "c");  // "c"
