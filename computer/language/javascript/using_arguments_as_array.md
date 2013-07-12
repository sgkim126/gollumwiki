# arguments를 완전히 array처럼 사용하기
  * 함수에서 arguments는 인자를 배열처럼 쓸 수 있게 해준다.
  * 하지만 Array()의 instance인 배열이 아니고, Object의 instance가 배열처럼 행동하는 것이다.
  * 따라서 arguments를 바로 배열처럼 쓰지 못한다.
  * 그래서 다음과 같은 과정을 거쳐야만 한다.


        var args = function() {
          return Array().slice.call(arguments);
        }
