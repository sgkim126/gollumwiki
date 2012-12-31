# at method
## at과 []의 차이
 * []는 range를 넘어가도 상관안하지만
 * at method는 out_of_range exception을 발생시킨다.
### Example
#### []

        #include <iostream>
        #include <vector>
        int main(void) {
            std::vector<int> vec(3,1);
            for(int index = 0; index < 4; index++) {
                std::cout << vec[index] << std::endl;
            }
            return 0;
        }

##### result

        1
        1
        1
        135153

#### .at()

        #include <iostream>
        #include <vector>
        int main(void) {
            std::vector<int> vec(3,1);
            for(int index = 0; index < 4; index++) {
                std::cout << vec.at(index) << std::endl;
            }
            return 0;
        }

##### result

        1
        1
        1
        terminate called after throwing an instance of 'std::out_of_range'
          what():  vector::_M_range_check
        중지됨
