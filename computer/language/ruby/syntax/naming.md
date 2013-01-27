# Naming
 * 첫글자가 역할을 결정.

<table><tr><td>
\_, 소문자
</td><td>
local variable, method, parameter
</td></tr><tr><td>
대문자
</td><td>
Class, Module, Constant
</td></tr><tr><td>
$
</td><td>
전역변수
</td></tr><tr><td>
@
</td><td>
Instance 변수
</td></tr><tr><td>
@@
</td><td>
Class 변수
</td></tr></table>


## Special Global Variables
<table><tr><td>
$!
</td><td>
마지막 error message
</td></tr><tr><td>
$@
</td><td>
에러 위치.
</td></tr><tr><td>
$_
</td><td>
마지막으로 gets로 읽은 string
</td></tr><tr><td>
$.
</td><td>
interpreter가 마지막에 읽은 line
</td></tr><tr><td>
$&
</td><td>
string last matched by regexp
</td></tr><tr><td>
$~
</td><td>
the last regexp match, as an array of subexpressions
</td></tr><tr><td>
$n
</td><td>
the nth subexpression in the last match
</td></tr><tr><td>
$=
</td><td>
case-insensitivity flag
</td></tr><tr><td>
$/
</td><td>
input record separator
</td></tr><tr><td>
$\
</td><td>
output record separator
</td></tr><tr><td>
$0
</td><td>
읽고 있는 ruby 스크립트 파일의 이름
</td></tr><tr><td>
$*
</td><td>
the command line arguments
</td></tr><tr><td>
$$
</td><td>
interpreter's process ID
</td></tr><tr><td>
$?
</td><td>
exit status of last executed child process
</td></tr></table>
