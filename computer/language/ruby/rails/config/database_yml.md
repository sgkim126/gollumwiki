# database.yml
 * mysql 예제
 * 다음 3가지 타입을 가진다.
  1. production
  1. development
  1. test

## sample

        development:
          adapter: mysql
          encoding: utf8
          database: databasename
          pool: 5
          timeout: 5000
          username: username
          password: password
