#rake db
###create
 * 개발용 db를 만든다.

        rake db:create

###drop
 * 개발용 db를 지운다.

        rake db:drop

###migrate
 * 테이블 변경 반영

        rake db:migrate

###test
####clone
 * 변경된 db schema로 새로 db를 만든다.

        rake db:test:clone
####clone_structure
 * 개발 환경과 같은 db를 다시 만든다.

        rake db:test:clone_structure

####load
 * schema.rb에 맞추어서 db를 새로 만든다.

        rake db:test:load
####prepare
 * test db를 migrate

        rake db:test:prepare

####purge
 * test database를 비운다.

        rake db:test:purge

##production으로 db 반영하기

        rake db:create RAILS_ENV="production"
