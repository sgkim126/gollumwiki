# application.rb

##config
### encoding

        config.encoding = "utf-8"

### action_view
#### javascript_expansions

        config.action_view.javascript_expansions[:defaults] = %w(jsfilename1 jsfilename2 jsfilename3)

### filter_parameters
  * 해당하는 파라미터는 local cache를 사용하지 않는다.

        config.filter_parameters += [:parametername1, :parametername2]
