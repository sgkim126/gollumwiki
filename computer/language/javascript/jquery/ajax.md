# ajax calling
 - load
 - getJson
 - get
 - post
 - ajax

## load

    $(selector).load(url[, data][, function(responseText, textStatus, XMLHttpRequest){}]);

 * selector의 원소를 치환한다.
 * url은 "주소"가 될 수도 있고, "주소 selector"가 될 수도 있다.

## getJSON

    $.getJSON(url[, data][, function(data,textStatus, jqXHR){}]);

 * 특정 주소의 json을 가져온다.

## get

    $.get(url[, data][, function(data,textStatus, jqXHR){}][, dataType]);

 * get method를 이용하여 data를 불러온다.
 * dataType에는 xml, json, script, html 등이 올 수 있다.

## post

    $.post(url[, data][, function(data,textStatus, jqXHR){}][, dataType]);

 * post method를 이용하여 data를 불러온다.
 * dataType에는 xml, json, script, html 등이 올 수 있다.

## ajax

    $.ajax(url[, settings]);

#### get

    $.ajax({
        [type:'GET',]
        url: url,
        data: data,
        success: success,
        dataType: dataType
    });

#### post

    $.ajax({
        type: 'POST',
        url: url,
        data: data,
        success: success,
        dataType: dataType
    });

### settings

    $.ajax(settings);
    $.ajaxSetup();

<table><tr><th> field </th><th> description </th><th> default </th></tr>
<tr><th> accepts </th><td> accept할 dataType </td><td> dataType에 따라 다름. </td></tr>
<tr><th> async </th><td> 비동기 호출인지 아닌지.
dataType이 jsonp일 경우 동기호출을 지원하지 않는다. </td><td> true </td></tr>
<tr><th> beforeSend(jqXHR, settings) </th><td> 요청 전에 수행 될 callback function </td><td>  </td></tr>
<tr><th> cache </th><td> cache를 사용할 지 안 할지 </td><td> true
dataType이 script나 jsonp이면 false </td></tr>
<tr><th> complete(jqXHR, textStatus) </th><td> 요청이 모두 끝난 뒤 수행할 callback function.
success, error 뒤에 수행. </td><td>  </td></tr>
<tr><th> contents </th><td>  </td><td>  </td></tr>
<tr><th> contentType </th><td>  </td><td> application/x-www-form-urlencoded </td></tr>
<tr><th> context </th><td>  </td><td>  </td></tr>
<tr><th> converters </th><td>  </td><td> <code javascript>{"* text": window.String,
 "text html": true,
 "text json": jQuery.parseJSON,
 "text xml": jQuery.parseXML
}</code> </th><td>
<tr><th> crossDomain </th><td>  </td><td> same-domain : false
cross-domain : true </td></tr>
<tr><th> data </th><td> 요청할 data </td><td>  </td></tr>
<tr><th> dataFilter(data, type) </th><td>  </td><td>  </td></tr>
<tr><th> dataType </th><td> 서버에서 받을 data type.
xml, json, script, html </td><td>  </td></tr>
<tr><th> error(jqXHR, textStatus, errorThrown) </th><td> 호출 실패시 실행될 callback function. </td><td>  </td></tr>
<tr><th> global </th><td>  </td><td>  </td></tr>
<tr><th> headers </th><td>  </td><td>  </td></tr>
<tr><th> ifModified </th><td>  </td><td>  </td></tr>
<tr><th> isLocal </th><td>  </td><td>  </td></tr>
<tr><th> jsonp </th><td>  </td><td>  </td></tr>
<tr><th> jsonpCallback </th><td>  </td><td>  </td></tr>
<tr><th> mimeType </th><td>  </td><td>  </td></tr>
<tr><th> password </th><td> HTTP access authentication request에서 사용할 비밀번호. </td><td>  </td></tr>
<tr><th> processData </th><td>  </td><td>  </td></tr>
<tr><th> scriptCharset </th><td>  </td><td>  </td></tr>
<tr><th> statusCode </th><td> 해당 status에서 사용할 callback function.
<code javascript>{404: function() {}, 400: function() { } };</code> </td><td>  </td></tr>
<tr><th> success(data, textStatus, jqXHR) </th><td> 호출 성공시 실행될 callback function. </td><td>  </td></tr>
<tr><th> timeout </th><td> 대기 시간.(milliseconds) </td><td>  </td></tr>
<tr><th> traditional </th><td>  </td><td>  </td></tr>
<tr><th> type </th><td> get, post
put, delete 등 도 사용할 수 있지만, 모든 브라우저에서 지원하지는 않는다. </td><td> get </td></tr>
<tr><th> url </th><td> URL </td><td> 현재 페이지 </td></tr>
<tr><th> username </th><td> HTTP access authentication request에서 사용할 이름. </td><td>  </td></tr>
<tr><th> xhr </th><td>  </td><td>  </td></tr>
<tr><th> xhrFields </th><td>  </td><td>  </td></tr></table>
