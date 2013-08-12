# arguments
 * 함수 내에서 인자로 받은 변수들을 index로 접근할 수 있다.

## arguments.callee
 * 함수 내에서 호출하는 함수 그 자체.

        var fact = function(n) {
            return n>0 ? arguments.callee(n-1) * n : 1;
        }
