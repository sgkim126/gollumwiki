#assert

        assert boolean[, msg]
        boolean

###assert_equal

        assert_equal object1, object2[, msg]
        object1 == object2

###assert_not_equal

        assert_not_equal object1, object2[, msg]
        object1 != object2

###assert_same

        assert_same object1, object2[, msg]
        object1.equals?(object2)

###assert_not_same

        assert_not_same object1, object2[, msg]
        not object1.equals?(object2)

###assert_nil

        assert_nil object[, msg]
        object.nil?

###assert_not_nil

        assert_not_nil object[, msg]
        not object.nil?

###assert_match

        assert_match regexp, string, [, msg]
        string =~ regexp

###assert_not_match

        assert_not_match regexp, string, [, msg]
        not string =~ regexp

###assert_in_delete

        assert_in_delta expecting, actual, delta[, msg]

###assert_throws

        assert_throws (symbol[, msg]) { block }

###assert_raise

        assert_raise (exception1[, exception_n...][, msg]) { block }

###assert_nothing_raised

        assert_not_raised (exception1[, exception_n...][, msg]) { block }

###assert_instance_of

        assert_instance_of class, object[, msg]

###assert_kind_of

        assert_kind_of calss, object[, msg]

###assert_respond_to

        assert_respond_to object, symbol[, msg]

###assert_operator

        assert_operator object1, operator, object2[, msg]
        object1.operator(object2)

###assert_send

        assert_send array[, msg]
        (array[0]).(array[1]) (array[2..last])

###assert_valid
 * Deprecated.
 * Use assert(record.valid?) instead.

        assert_valid record

###assert_difference

        assert_difference expressions[, difference][, msg]

###assert_difference

        assert_no_difference expressions[, msg], &block

###assert_recognizes

        assert_recognizes expected_options, path[, extras][, msg]

###assert_generates

        assert_generates expected_options[, defaults][, extras][, msg]

###assert_response

        assert_response type[, msg]
<table><tr><td>
:success
</td><td>
200
</td></tr><tr><td>
:redirect
</td><td>
300-399
</td></tr><tr><td>
:missing
</td><td>
404
</td></tr><tr><td>
:error
</td><td>
500-599
</td></tr></table>

###assert_redirected_to

        assert_redirected_to [options][, msg]

###assert_template

        assert_template [expected][, msg]

##flunk
  * NotImplementeException

        flunk[ msg]
