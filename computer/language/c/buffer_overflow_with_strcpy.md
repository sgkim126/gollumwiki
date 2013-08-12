# strcpy

    #include<stdio.h>
    int main(void) {
        char s[8];
        char d[4];
        fgets(s,sizeof(s),stdin);
        strcpy(d,s);
        return 0;
    }

 * 아무런 제한이 없으므로 buffer overflow공격을 당할 수 있다.

        #include<stdio.h>
        int main(void) {
            char s[8];
            char d[4];
            fgets(s,sizeof(s),stdin);
            strncpy(d,s,sizeof(d));
            return 0;
        }

 * 언뜻 보면 맞는것 같지만 잘못된 작동을 할 수 있다.
 * strncpy는 마지막 문자에 null character가 오는 것을 보장하지 않는다.

        #include<stdio.h>
        int main(void) {
            char s[8];
            char d[4];
            fgets(s,sizeof(s),stdin);
            strncpy(d,s,sizeof(d)-1);
            d[sizeof(d)-1]='\0';
            return 0;
        }

 * 수동으로 마지막 문자에 '\0'을 넣어준다.
