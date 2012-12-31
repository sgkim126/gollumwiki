# Pointr

## []와 *의 차이
* \*로 선언하면, .rodata(readonly) section에 할당한 뒤, 그곳을 가리키는 포인터를이용해서 접근한다.
* []로 선언하면, .rodata section에 할당하지만 사용할때는 stack으로 copy하여 사용한다.

### Example.

        void func1(void) {
            int *a = {1, 2, 3};
            a[0] = 0;
        }

        void func2(void) {
            int a[] = {1, 2, 3};
            a[0] = 0;
        }

* func1은 .rodata sction의 값을 바꾸려고 하기때문에 segmantation falut를 발생시킨다.
* func2는 정상적으로 실행된다.
