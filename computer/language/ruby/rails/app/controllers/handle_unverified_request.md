# handle_unverified_request
 * rails에서 verified되지 않은 request에 대한 반응.
 * 재정의하지 않으면 post요청에 대해서 session이 초기화 된다.

 * 이것을 막으려면 아래와 같이 하면 된다.

        def handle_unverified_request
          true
        end

 * 기존의 검증을 유지하고 새로운 기능을 추가하고 싶으면 아래와 같이 한다.

        def handle_unverified_request
          super
          #append here
          true
        end
