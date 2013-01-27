# select_tag

        <%= select_tag(:field, 
            option_for_select(
                [['text1', value1], ['text2', value2], ['text3', value3]],
                 2)) %>

        <select name="field" id="field">
        <option value="value1">text1</option>
        <option value="value2" selected="selected">text2</option>
        <option value="value3">text3</option>
        </select>

## option_for_select

        <%= option_for_select(
            [['text1', value1], ['text2', value2], ['text3', value3]],
             2)) %>

        <option value="value1">text1</option>
        <option value="value2" selected="selected">text2</option>
        <option value="value3">text3</option>
