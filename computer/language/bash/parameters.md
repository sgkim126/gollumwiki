# Parameters
## Special Parameters
<table>
<tr>
<td>
$_
</td>
<td>
가장 최근에 실행한 process의 절대 경로 + name
</td>
</tr>
<tr>
<td>
$?
</td>
<td>
가장 최근 종료한 foreground 프로세스의 exit값
</td>
</tr>
<tr>
<td>
$!
</td>
<td>
가장 최근에 종료한 background process ID
</td>
</tr>
<tr>
<td>
$$
</td>
<td>
현재 shell의 process id
</td>
</tr>
<tr>
<td>
$-
</td>
<td>
현재의 flag
</td>
</tr>
</table>

## Positional parameters
<table>
<tr>
<td>
$0
</td>
<td>
script 이름
</td>
</tr>
<tr>
<td>
$1 ~ $9, ${n}
</td>
<td>
n번째 argument.
</td>
</tr>
<tr>
<td>
$#
</td>
<td>
argument 개수
</td>
</tr>
<tr>
<td>
$@
</td>
<td>
argument 리스트
</td>
</tr>
<tr>
<td>
$*
</td>
<td>
argument 리스트
</td>
</tr>
</table>

### $@와 $*의 차이

        echo '"$@:"'"$@"
        echo '"$*:"'"$*"
        echo '$@:'"$@"
        echo '$*:'"$*"

        echo 'for i in "$@":'
        for i in "$@"
        do
            echo $i
        done
        echo 'for i in "$*":'
        for i in "$*"
        do
            echo $i
        done
        echo 'for i in $@:'
        for i in $@
        do
            echo $i
        done
        echo 'for i in $*:'
        for i in $*
        do
            echo $i
        done

#### result

        $./quote.sh 1 "2 3" 4
        "$@:"1 2 3 4
        "$*:"1 2 3 4
        $@:1 2 3 4
        $*:1 2 3 4
        for i in "$@":
        1
        2 3
        4
        for i in "$*":
        1 2 3 4
        for i in $@:
        1
        2
        3
        4
        for i in $*:
        1
        2
        3
        4
