# Buffer overflow with scanf
 * scanf뿐 아니라 sscanf, fscanf도 마찬가지다.
## bad_scanf.c
 * 사용자 입력에 따라 무한한 입력이 가능하기 때문에 좋지 않다.

        #include<stdio.h>
        int main(void)
        {
            char s[4];
            scanf("%s",s);
            return 0;
        }

## another_bad_scanf.c
 * "%4s"라고 하면, 4 characters만 입력받는다.
 * 그러므로 buffer overflow공격을 당할 일은 없다.
 * 하지만 4 characters 후에 null character가 들어간다.
 * 즉, s[4]다음 메모리가 오염된다.

        #include<stdio.h>
        int main(void)
        {
            char s[4];
            scanf("%4s",s);
            return 0;
        }

### example

        #include<stdio.h>
        int main(void) {
            char x = \x00
            char s[6];
            s[4]='-';
            s[5]='+';
            scanf("%4s",s);
            printf("%s\n",s);
            printf("%c\n",s[0]);
            printf("%c\n",s[1]);
            printf("%c\n",s[2]);
            printf("%c\n",s[3]);
            printf("%c\n",s[4]);
            printf("%c\n",s[5]);
            return 0;
        }

#### result
 * 아래와같이 1byte의 null character가 들어간다.

        $./a.out
        1234
        1234
        1
        2
        3
        4

        +

## good_scanf.c
 * 마지막에 1byte의 여유를 주자.

        #include<stdio.h>
        int main(void)
        {
            char s[5];
            scanf("%4s",s);
            return 0;
        }
