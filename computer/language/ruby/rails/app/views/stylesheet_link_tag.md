# stylesheet_link_tag
 * css file을 include해준다.

        stylesheet_link_tag "cssfilename"

        link href="/stylesheets/cssfilename.css" media="screen" rel="Stylesheet" type="text/css"

## media
        stylesheet_link_tag 'cssfilename', :media => “all”

        link href="/stylesheets/cssfilename.css" media="all" rel="Stylesheet" type="text/css"

## 여러 파일 불러오기

        stylesheet_link_tag 'cssfilename1', 'cssfilename2'

        link href="/stylesheets/cssfilename1.css" rel="Stylesheet" type="text/css"
        link href="/stylesheets/cssfilename2.css" rel="Stylesheet" type="text/css"

### :all
  * public/stylesheets의 모든 파일을 가져온다.

        stylesheet_link_tag :all
