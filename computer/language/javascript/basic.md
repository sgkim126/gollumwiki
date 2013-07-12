# Javascript 기본
  * 본 글은 "기본"이라고 쓰여 있지만 정말 기본적인 문법들은 다루지 않는다.
  * 하지만 javascript로 코딩한다면 이정도는 알아야 한다고 생각하는 내용들이다.

  동적인 웹환경이 뜨면서 같이 부상한 언어가 javascript다. 많이 쓰이고 있기는 하지만, 제대로 알고 쓰는 사람이 별로 없다.
  "대강 써도 돌아가게 만드는 웹브라우저들 만세."가 아니라 대강 쓰는 웹 개발자를 때려야 한다.
  사실 따지고 보면 굉장히 알아야 할게 많은 언어이다.
  일반적인 프로그래밍 언어와는 다른 javascript의 특징들을 살펴보겠다.

## type system
  * javascript에는 3개의 primitive type이 있다.
    - Number
    - String
    - Boolean
  * javascript에는 3개의 composite type이 있다.
    - Object
    - Array
    - Function
  * javascript에는 2개의 special type이 있다.
    - null
    - undefined
  * javascript는 dynamic & weak type이다.

### dynamic type
  * dynamic type이라는 것은 varialbe이 type을 가지지 않는 것을 의미한다.


        var x;
        x=3;    //이때의 x는 number type의 value를 가지는 varialbe다.
        x="3";  //이때의 x는 string type의 value를 가지는 varialbe다.
        x=true; //이때의 x는 boolean type의 value를 가지는 varialbe다.

  * 주의할 점은 variable이 type을 가지지 않는다는 것이지, value가 type을 가지지 않는건 아니라는 것이다.

### weak type
  * weak type이라는 것은 value가 implict하게 conversion이 일어날 수 있다는 것이다.

#### 예시 - parseInt
  * parseInt의 정확한 선언은, string과 number를 받아서, number를 return하는 함수이다.
  * 그러므로 정확하게는 아래와 같이 써야 한다.

        parseInt("31",8);
        parseInt((31).toString(),8);

  * 하지만 number를 string으로 implicit하게 convert할 수 있으므로, 아래와 같이 간단하게 쓸 수 있다.

        parseInt(31,8);

#### +, - on number
  * string conversion이 일어나면, +, -의 순서에 따라 결과가 달라지게 된다.

        "1"+2-3;  // 9
        "1"-3+2;  // 0

  * 위의 식은
    - number 2를 string "2"로 convert한다.
    - string "1"과 convert된 string "2"를 합친다.
    - 결과 "12"를 얻는다.
    - 결과를 number로 convert한다.
    - convert된 12와 3을 뺀다.
  * 의 결과이고,
  * 아래의 식은
    - string "1"을 number 1로 convert한다.
    - 1과 3을 뺀다.
    - -2를 얻는다.
    - 2를 더한다.
  * 의 결과이다.

#### == ===
  * javascript에는 compare operator가 2개 있다.

##### ==
  * ==는 type을 비교하지 않고 값만을 비교한다.

        1 == 1;     //true
        1 == "1";   //true
        false == 0; //true
        true == 1;  //true

  * javascript는 string value를 다루는 경우가 많기 때문에 자주 쓰인다.

##### ===

  * ===은 값과 type을 같이 비교한다.

        1 === 1;    //true
        1 === "1";   //false
        false === 0; //false
        true === 1;  //false

##### 공백문자
  * /[ \t\n\r]+/와 empty string은 다르다.
  * 하지만 /[ \t\n\r]+/와 false를 ==로 비교하면 true가 return된다.

        "\r\t\n " == "";    //false
        "\r\t\n " == false; //true

##### 결론
  * ==를 쓰지마라.
  * ===을 써라.

### falsy value
  * javascript에는 6개의 falsy value가 있다.
  * falsy value는 false로취급된다.
    - false
    - 0
    - ""
    - NaN
    - undefined
    - null

        false ? 1 : 0;     //0
        0 ? 1 : 0;         //0
        "" ? 1 : 0;        //0
        null ? 1 : 0;      //0
        undefined ? 1 : 0; //0
        NaN ? 1 : 0;       //0

  * 빈 object나 빈 array는 falsy value가 아니다.
  * 하지만 falsy value라고 전부 같은 것은 아니다.

#### falsy value끼리의 비교.
  * falsy value끼리 비교했을 때 전부 같은 값이라고 하지 않는다.
    - false, 0, ""
    - undefined, null
    - NaN

        false == 0;         //true
        false == "";        //true
        false == undefined; //false
        false == null;      //false
        false == NaN;       //false

        0 == "";            //true
        0 == undefined;     //false
        0 == null;          //false
        0 == NaN;           //false

        "" == undefined;    //false
        "" == null;         //false
        "" == NaN;          //false

        undefined == null;  //true
        undefined == NaN;   //false

        null == NaN;        //false

## function scope
  * 다른 언어들과 다르게 javascript는 block scope가 아니라, function scope를 채택했다.
  * 따라서 고대의 pure C처럼 와 같은 식으로 함수 맨 앞에 변수를 선언해야 한다.

### 변수의 선언

        var g = 0;
        var unexpectedResult = function() {
          var res = g;
          var g;
          return res;
        }
        var expectedResult = function() {
          var res = g;
          return res;
        }
        unexpectedResult();  //undefined
        expectedResult();    //0

  * unexpectedResult라는 함수에서는 undefined를 return하고,
    * expectedResult라는 함수에서는 0을 return한다.
  * 이유는 간단하다.
  * javascript는 함수 내부에서 쓰인 변수의 선언을 전부 함수의 시작부분으로 옮겨서 해석한다.
    * 따라서 unexpectedResult에서 res에 넣은 g라는 변수는 함수내부에서 선언한 변수이고,
    * 따라서 expectedResult에서 res에 넣은 g라는 변수는 전역변수로 있었던 g이다.
  * 짧은 함수에서는 상관 없다고 생각할지 몰라도, 함수의 길이가 길어지면, 놓치기 쉬운 버그가 되어 버린다.

### 적절한 if 사용법

        function badIf() {
          if(arguments[0]) {
            var bar = arguments[1];
          } else {
            var bar = arguments[2];
          }
          return bar;
        }
        function goodIf() {
          var bar;
          if(arguments[0]) {
            bar = arguments[1];
          } else {
            bar = arguments[2];
          }
          return bar;
        }

### 적절한 for 사용법

        function badFor() {
          var sum;
          for(var index=0;index<argument.length;index++) {
            sum+=arguments[index];
          }
          return sum;
        }
        function badFor() {
          var sum, index;
          for(index=0;index<argument.length;index++) {
            sum+=arguments[index];
          }
          return sum;
        }

## new Object, new Array

        var obj = new Object();
        var arr = new Array();

        var obj = {};
        var arr = [];

  * 위의 코드와 아래의 코드중에서 어느것을 많이 쓰는가?
  * 다른 언어를 쓰다가 온 사람들은 위의 코드를 쓰는 경우가 많이 있다.
    * array라면 몰라도 object를 literal하게 만드는 것에 대해 거부감을 느끼는 사람을 여럿 보았다.
  * 하지만 javascript에서는 literal하게 선언 할 수 있는 경우에는 literal한 선언을 쓰는 게 더 좋다.
  * 정확히 말하면 new라는 operator를 안 쓰는것을 추천한다.
    * 왜냐하면 javascript는 calss based object-oriented language가 아니라 prototype based object-oriented language이기 때문이다.
  * new operator를 사용해야 하는 경우는 pseudoclassical Constructor를 사용해야 할때로 한정하는게 좋다.
    * 자세한 내용은 [[ http://yuiblog.com/blog/2006/11/13/javascript-we-hardly-new-ya/ | 여기 ]]를 참고하길.

##### p.s.
  * 그래도 납득할 수 없는 사람을 위해 한마디 더하자면, new Array, new Object를 사용하지 않는 것은

        var num = new Number(0);
        var str = new String("");
        var bool = new Boolean(false);
        var func = new Function("/* body */);

  * 위의 코드대신

        var num = 0;
        var str = "";
        var bool = false;
        var func = function("/* body */);

  * 위의 코드를 사용하는것과 비슷한 것이다.

## java나 c#의 문법을 피하라. javascript의 문법을 사용하라.
