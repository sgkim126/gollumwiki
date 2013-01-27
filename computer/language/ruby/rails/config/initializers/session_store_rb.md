# session_store.rb
## session_store
### cookie_store

        ApplicationName::Application.config.session_store :cookie_store, :key => 'session_key'

### active_record_store

        ApplicationName::Application.config.session_store :active_record_store, :key => 'session_key'

        rails generate session_migration
        rake db:migrate

### drb_store

        ApplicationName::Application.config.session_store :drb_store, :key => 'session_key'

### mem_cache_store

        ApplicationName::Application.config.session_store :mem_cache_store, :key => 'session_key'
