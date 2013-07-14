# memorize 사용하기
  * dp문제의 일종을 풀때 많이 사용된다.

        var arguments.callee = function(x) {
          var n1, n2;
          if(!arguments.callee.memory)
            arguments.callee.memory = {};
          if(x <= 2 ) {
            arguments.callee.memory[x] = 1;
            return 1;
          }
          n1 = arguments.callee.memory[x-1] ? arguments.callee.memory[x-1] : arguments.callee(x-1);
          n2 = arguments.callee.memory[x-2] ? arguments.callee.memory[x-2] : arguments.callee(x-2);
          arguments.callee.memory[x] = n1 + n2;
          return n1 + n2;
        }
