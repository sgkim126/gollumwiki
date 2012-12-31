# pragma
## \#pragma pack
 * 구조체의 alignment를 정의.
 * 32bit 머신에서 기본값으 4byte.

        #include <iostream>
        struct struct8 {
            char c;
            int i;
        };
        #pragma pack(push, 1)
        struct struct5 {
            char c;
            int i;
        };
        #pragma pop
        int main(void) {
            std::cout<< sizeof(struct8) << std::endl;  //8
            std::cout<< sizeof(struct5) << std::endl;  //5
        }
