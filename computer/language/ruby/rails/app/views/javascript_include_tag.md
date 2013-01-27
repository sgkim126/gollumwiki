# javascript_include_tag
 * javascript파일을 include해준다.

        javascript_include_tag "jsfilename"
        <script src="jsfilename.js" type="text/javascript"></script>

## :all
 * public/javascripts의 모든 파일을 가져온다.

        javascript_include_tag :all

## :default
 * config/application.rb에서 기본값으로 설정한 파일을 가져온다.

        javascript_include_tag :default
