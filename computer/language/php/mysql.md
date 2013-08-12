# MYSQL
 * [Prepared Statement](http://www.ultramegatech.com/blog/2009/07/using-mysql-prepared-statements-in-php/)

## Connect
#### mysql_ping

    $bool= mysql_ping ([ resource $link_identifier ] )

### Open
#### mysql_connect

    $resource= mysql_connect ([ string $server [, string $username [, string $password [, bool $new_link [, int $client_flags ]]]]] )

#### mysql_pconnect

    $resource= mysql_pconnect ([ string $server [, string $username [, string $password [, int $client_flags ]]]] )

### Close
#### mysql_close

    $bool= mysql_close ([ resource $link_identifier ] )

### User
#### mysql_change_user

    $int= mysql_change_user ( string $user , string $password [, string $database [, resource $link_identifier ]] )

## Database
#### mysql_list_dbs

    $resource= mysql_list_dbs ([ resource $link_identifier ] )

#### mysql_db_name

    $string= mysql_db_name ( resource $result , int $row [, mixed $field ] )

#### mysql_create_db

    $bool= mysql_create_db ( string $database_name [, resource $link_identifier ] )

#### mysql_drop_db

    $bool= mysql_drop_db ( string $database_name [, resource $link_identifier ] )

#### mysql_select_db

    $bool= mysql_select_db ( string $database_name [, resource $link_identifier ] )

## Table
#### mysql_list_tables

    $resource= mysql_list_tables ( string $database [, resource $link_identifier ] )

#### mysql_tablename

    $string= mysql_tablename ( resource $result , int $i )

## Query
#### mysql_query

    $resource= mysql_query ( string $query [, resource $link_identifier ] )

#### mysql_db_query

    $resource= mysql_db_query ( string $database , string $query [, resource $link_identifier ] )

#### mysql_unbuffered_query

    $resource= mysql_unbuffered_query ( string $query [, resource $link_identifier ] )

#### mysql_affected_rows
#### mysql_free_result

    $bool= mysql_free_result ( resource $result )

#### mysql_info

    $string= mysql_info ([ resource $link_identifier ] )

### Fetch
#### mysql_fetch_array
#### mysql_fetch_assoc
#### mysql_fetch_field
#### mysql_fetch_lengths
#### mysql_fetch_object
#### mysql_fetch_row

### Field
#### mysql_field_flags
#### mysql_field_len
#### mysql_field_name
#### mysql_field_seek
#### mysql_field_table
#### mysql_field_type

## etc.
#### mysql_errno

    $int= mysql_errno ([ resource $link_identifier ] )

#### mysql_error

    $string= mysql_error ([ resource $link_identifier ] )

#### mysql_list_processes

    $resource= mysql_list_processes ([ resource $link_identifier ] )

#### mysql_real_escape_string

    $string= mysql_real_escape_string ( string $unescaped_string [, resource $link_identifier ] )

### System
#### mysql_stat

    $string= mysql_stat ([ resource $link_identifier ] )

#### mysql_get_client_info

    $string= mysql_get_client_info ()

#### mysql_get_host_info

    $string= mysql_get_host_info ([ resource $link_identifier ] )

#### mysql_get_server_info

    $string= mysql_get_server_info ([ resource $link_identifier ] )

#### mysql_get_proto_info

    $int= mysql_get_proto_info ([ resource $link_identifier ] )

#### mysql_set_charset

    $bool= mysql_set_charset ( string $charset [, resource $link_identifier ] )

#### mysql_client_encoding

    $string= mysql_client_encoding ([ resource $link_identifier ] )
