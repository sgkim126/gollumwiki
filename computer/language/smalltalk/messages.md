# Messages
 * 모든 message는 public이다.
 * 모든 message는 기본적으로 self를 return한다.

## Type of messages
### Unary message
 * 인자가 없는 message.

        3 class

### Binary message
 * 특수 기호를 사용한 message.
 * 한 개의 인자를 가진다.

        1 + 1

### Keyword message
 * 여러개의 인자를 가지는 message.
 * 인자는 keyowrd로 분류한다.

        5 between: 1 and: 10
        Array new: 3

 * 위의 beween: and:의 경우 "between:and:"(붙여서 쓴것)를 selector로 가진다.

## Priority of message
 - Unary message.
 - Binary message.
 - Keyword message.
 * 샅은 priority의 message는 왼쪽에서 오른쪽으로 실행된다.

## Chainning message and Cascading message
### Chainning message
 * method에서 return된 값이 다음 message의 receiver가 된다.

        1 + 2 + 3 +4

### Cascading message
 * message의 receiver가 다시 다음 message의 receiver가 된다.

        1 + 2; + 3; + 4
