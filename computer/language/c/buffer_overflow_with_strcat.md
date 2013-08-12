# Buffer overflow with strcat

    #include<stdio.h>
    int main(void) {
        char s[4];
        char d[8];
        scanf("%3s",s);
        scanf("%7s",s);
        strcat(d,s);
        return 0;
    }

 * 아무런 제한이 없으므로 buffer overflow공격을 당할 수 있다.

        #include<stdio.h>
        int main(void) {
            char s[4];
            char d[8];
            scanf("%3s",s);
            scanf("%7s",s);
            strncat(d,s,sizeof(d));
            return 0;
        }

 * 언뜻 보면 맞는것 같지만 잘못된 작동을 할 수 있다.
 * strncat에서 size는 추가될 string의 길이이기 때문에 d의 길이를 벗어날 수 있다.

        #include<stdio.h>
        int main(void) {
            char s[4];
            char d[8];
            scanf("%3s",s);
            scanf("%7s",s);
            strncat(d,s,sizeof(d)-strlen(d));
            return 0;
        }

 * d의 길이를 빼서 입력한다.
 * 하지만 마지막 문자에 null character를 보장하지 못한다.

        #include<stdio.h>
        int main(void) {
            char s[4];
            char d[8];
            scanf("%3s",s);
            scanf("%7s",s);
            strncat(d,s,sizeof(d)-strlen(d)-1);
            d[sizeof(d)-1]='\0';
            return 0;
        }

 * 마지막 문자에 null character를 수동으로 넣어준다.
