#routes.rb
####root

        root :to => "controller#action"

###match

        match "path" => "controller#action"
        match "path/:param1/:param2" => "controller#action"

####get

        get "path" => "controller#action"
        get "path/:param1/:param2" => "controller#action"

####post

        post "path" => "controller#action"
        post "path/:param1/:param2" => "controller#action"
</code>

##resources
###Simple

        map.resources :controller, :action

###Nested

        map.resources :controller1 do |controller|
          controller.resources :controller2
        end

###Customized
