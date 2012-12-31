# Cast
## dynamic_cast
 * run time에 cast.
 * primitive type에 대해서는 사용할 수 없고, 객체의 pointer나 reference에 대해서만 사용 가능하다.
 * casting할 수 없으면 null을 return한다.
## static_cast
 * C의 casting과 같은 일을 한다.
 * primitive type을 객체나 구조체로 만들 수 없다. and vice versa.
 * casting 불가능할때는 null을 return.
## reinterpret_cast
## const_cast
 * const -> non-const
 * non-const -> const
