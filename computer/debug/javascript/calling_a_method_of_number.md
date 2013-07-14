# number object의 함수 쓰기
  * 아래와 같은 코드는 에러다.

        1.toString();

  * 1뒤의 .을 float의 .으로 인식하기 때문이다.

## Solution

        1..toString();
        1 .toString();
        (1).toString();

  - .을 두번찍기.
  - .앞에 빈칸을 찍기.
  - number를 괄호로 감싸기.
