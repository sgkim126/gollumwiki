# C++의 비oop스러운 점.
## []

        #include <iostream>
        int main(void) {
            int aa[] = {0,1,2,3};
            std::cout<<aa[2] << std::endl;
            std::cout<<*(aa+2) << std::endl;
            std::cout<<*(2+aa) << std::endl;
            std::cout<<2[aa] << std::endl;
        }

 * 결과는 전부 2.
 * 첫번째 줄은 aa array의 3번째 인자이므로 당연히 2이다.
 * 두번째 줄은 (aa+2)의 결과값이 int*인 aa에 2*(sizeof int)를 더한 aa+8이 지정하는 값이므로 당연히 2이다.
 * 세번째 줄은 의외로 결과값이 2가 나온다.
 * 만약 c++이 객체지향적인 언어였다면, 이 값은 int 2에 int*인 aa를 더한 값이 가리키는 값을 가졌어야 한다.
  * 즉 little endian일 경우 65535, big endian에서는 1이 되어야 한다.
  * 하지만 C++이 비객체지향적 언어이므로, 이건 그냥 int*에 int를 더한것과 똑같은 값이 나온다.
 * 가장 황당한건 마지막 줄이 2가 나온다는 것이다.
  * a[b]는 컴파일러 상에서 *(a+b)가 된다나 어쩐다나
