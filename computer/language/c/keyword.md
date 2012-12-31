# Keyword
## Type qualifier
### volatile

        volatile int a;

 volatile을 쓰는 변수에 대해서 최적화하지 않는다.
* lazy evaluation도 하지않는다.
* register에 들어있는 값도 항상 메모리에서 읽는다.

#### in VC
 VC에서는 변수의 순서를 선언한 순서대로 메모리에 할당하는것을 보장해준다.
