# Pthon 2.x에서 3.x로 변하면서 바뀐점.
 * 애초에 파이썬을 개발용으로 배운게 아니라, 해킹을 배우면서 간간히 배운거라 그리 많이 쓰이지는 않았다.
 * 게다가 3.x가 나온 뒤로 2.x와 문법 차이가 너무 많아진 뒤로 거의 안 쓰고 있었다.
 * 이번에 irc용 bot을 만들면서 python 3.x를 쓰기 시작했다.
 * 이번 글은 개발하면서 알게 된 3.x와 2.x의 차이에 관한 것이다.

# print
 * 2.x에서는 print가 function이 아니라 keyword였다.
 * 3.x가 되면서 function이 되었다.

        print "2.x"

        print("3.x")

# range
 * python2.x에서는 range를 이용하면 즉시 list를 만들고,
   * xrange를 이용하면 xrange라는 type을 만들어 낸다.
 * python3.x에서는 range를 이용하면 range라는 type을 만들어낸다.

        type(range(10))
        #&lt;type 'list'\&gt;
        type(xrange(10))
        #&lt;type 'xrange'\&gt;

        type(range(10))
        #&lt;class 'range'\&gt;
