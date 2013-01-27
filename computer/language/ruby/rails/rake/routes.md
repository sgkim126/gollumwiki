# routes
 * route정보를 보여준다.

## 예제
        Ledger::Application.routes.draw do
          resources :users do
            resources :accounts do
              resources :trades
            end
          end
          resources :conventions
        end
### 
        rake routes
###
            user_account_trades GET    /users/:user_id/accounts/:account_id/trades(.:format)          {:controller=>"trades", :action=>"index"}
                                POST   /users/:user_id/accounts/:account_id/trades(.:format)          {:controller=>"trades", :action=>"create"}
         new_user_account_trade GET    /users/:user_id/accounts/:account_id/trades/new(.:format)      {:controller=>"trades", :action=>"new"}
        edit_user_account_trade GET    /users/:user_id/accounts/:account_id/trades/:id/edit(.:format) {:controller=>"trades", :action=>"edit"}
             user_account_trade GET    /users/:user_id/accounts/:account_id/trades/:id(.:format)      {:controller=>"trades", :action=>"show"}
                                PUT    /users/:user_id/accounts/:account_id/trades/:id(.:format)      {:controller=>"trades", :action=>"update"}
                                DELETE /users/:user_id/accounts/:account_id/trades/:id(.:format)      {:controller=>"trades", :action=>"destroy"}
                  user_accounts GET    /users/:user_id/accounts(.:format)                             {:controller=>"accounts", :action=>"index"}
                                POST   /users/:user_id/accounts(.:format)                             {:controller=>"accounts", :action=>"create"}
               new_user_account GET    /users/:user_id/accounts/new(.:format)                         {:controller=>"accounts", :action=>"new"}
              edit_user_account GET    /users/:user_id/accounts/:id/edit(.:format)                    {:controller=>"accounts", :action=>"edit"}
                   user_account GET    /users/:user_id/accounts/:id(.:format)                         {:controller=>"accounts", :action=>"show"}
                                PUT    /users/:user_id/accounts/:id(.:format)                         {:controller=>"accounts", :action=>"update"}
                                DELETE /users/:user_id/accounts/:id(.:format)                         {:controller=>"accounts", :action=>"destroy"}
                          users GET    /users(.:format)                                               {:controller=>"users", :action=>"index"}
                                POST   /users(.:format)                                               {:controller=>"users", :action=>"create"}
                       new_user GET    /users/new(.:format)                                           {:controller=>"users", :action=>"new"}
                      edit_user GET    /users/:id/edit(.:format)                                      {:controller=>"users", :action=>"edit"}
                           user GET    /users/:id(.:format)                                           {:controller=>"users", :action=>"show"}
                                PUT    /users/:id(.:format)                                           {:controller=>"users", :action=>"update"}
                                DELETE /users/:id(.:format)                                           {:controller=>"users", :action=>"destroy"}
                    conventions GET    /conventions(.:format)                                         {:controller=>"conventions", :action=>"index"}
                                POST   /conventions(.:format)                                         {:controller=>"conventions", :action=>"create"}
                 new_convention GET    /conventions/new(.:format)                                     {:controller=>"conventions", :action=>"new"}
                edit_convention GET    /conventions/:id/edit(.:format)                                {:controller=>"conventions", :action=>"edit"}
                     convention GET    /conventions/:id(.:format)                                     {:controller=>"conventions", :action=>"show"}
                                PUT    /conventions/:id(.:format)                                     {:controller=>"conventions", :action=>"update"}
                                DELETE /conventions/:id(.:format)                                     {:controller=>"conventions", :action=>"destroy"}
