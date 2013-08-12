# Buffer overflow with sprintf

    #include<stdio.h>
    int main(void) {
        char s[8];
        char d[4];
        fgets(s,sizeof(s),stdin);
        sprintf(d,"%s",s);
        return 0;
    }

 * 아무런 제한이 없으므로 buffer overflow공격을 당할 수 있다.

        #include<stdio.h>
        int main(void) {
            char s[8];
            char d[4];
            fgets(s,sizeof(s),stdin);
            snprintf(d,sizeof(d),"%s",s);
            return 0;
        }

 * snprintf는 '\0'을 포함하여, size 이상의 길이를 받지 않는다.


        #include<stdio.h>
        int main(void) {
            char s[8];
            char d[4];
            fgets(s,sizeof(s),stdin);
            snprintf(d,sizeof(d)-1,"%s",s);
            return 0;
        }

 * snprintf의 경우도 습관적으로 위의 경우처럼 1 줄여서 사용하는 경우가 많이 있다.
 * 하지만 이는 안좋은 코드이다.
 * 이유는 위의 [[.:gets | fgets]]에서 적었다.


        #include <stdio.h>
        int main(void) {
            char s[8];
            char d[4];
            fgets(s,sizeof(s),stdin);
            sprintf(d,"%3s",s);
            return 0;
        }

 * 위의 printf에서 설명했듯이 위와 같이 작성할 수 도 있다.
 * 하지만 이는 s의 길이를 제한할 뿐, d의 길이를 제한하지 못한다.
 * 여러개의 string을 복합적으로 묻거나, 여러 args를 이용한 string 생성에 적합하지 못하다.
