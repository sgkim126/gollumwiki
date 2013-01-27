# Buffer overflow with gets
 * 사용자의 입력을 무한히 받는다.

## bad_gets.c

        #include<stdio.h>
        int main(void) {
            char s[4];
            gets(s);
            return 0;
        }

## good_fgets.c
 * 사용자의 입력을 s의 size만큼으로 제한했다.

        #include<stdio.h>
        int main(void) {
            char s[4];
            fgets(s,sizeof(s),stdin);
            return 0;
        }

## bad_fgets.c

        #include<stdio.h>
        int main(void) {
            char s[4];
            fgets(s,sizeof(s)-1,stdin);
            return 0;
        }

 * 동작 자체에는 아무런 문제도 없다.
 * 하지만 fgets는 주어진 size 보다 1적은 개수의 입력을 받아들인다.
 * 즉, 위의 코드는 1byte의 메모리를 낭비한다.
 * 어떨때는 예상했던 대로 돌아가지 않을 수 도 있다.
### bad_output.c

        #include<stdio.h>
        int main(void) {
            char s[4];
            s[0]='0';
            s[1]='1';
            s[2]='2';
            s[3]='3';
            fgets(s,sizeof(s),stdin);
            printf("%c\n",s[0]);
            printf("%c\n",s[1]);
            printf("%c\n",s[2]);
            printf("%c\n",s[3]);
            printf("%s\n",s);
            return 0;
        }

### result

        $./a.out
        abcd
        a
        b
        c

        abc
