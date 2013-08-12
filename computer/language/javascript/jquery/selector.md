# selector

## *
 * all

## #id
 * id로 가져오기.

### .class
 * class로 가져오기.

### :contans(str)
 * str을 text로 포함하는 element

### :not(filter)
 * filter이외의 selector

## status
### :animated
 * 현재 에니메이션이 적용되고 있는 element

### :checked
 * checked checkbox or radio

### :selected
### :hidden
### :visible
### :disabled
### :enabled

## tag
### :input
 * input, select, textarea, button

### :text
 * input[type=text]

### :password
 * input[type=password]

### :checkbox
 * input[type=checkbox]

### :radio
 * input[type=radio]

### :submit
 * input[type=submit]

### :reset
 * input[type=reset]

### :button
 * input[type=button], button

### :image
 * input[type=image]

### :file
 * input[type=file]

### :header
 * h1 ~ h6

## Order
### :first
### :last
### :odd
### :even
### :eq(n)
### :gt(n)
### :lt(n)

## :parent
 * 자식을 가지는 element

## Child
### :first-child
### :last-child
### :nth-child(n)
### :nth-child(odd)
### :nth-child(even)
### :only-child

## Hierarchy
### descedant

    $("ancestor descendant");

### child

    $("parent > child");

### sibling

    $("selector ~ sibling");

### next

    $("prev + next");

## attribute
### $(selector[attribute])
 * attribute를 속성으로 가지는 요소.

### $(selector[attribute="value"])
 * attribute가 value인 요소.

### $(selector[attribute!="value"])
 * attribute가 value가 아닌 요소.

### $(selector[attribute^="value"])
 * attribute가 value로 시작하는 요소.

### $(selector[attribute$="value"])
 * attribute가 value로 끝나는 요소.

### $(selector[attribute*="value"])
 * attribute가 value를 포함하는 요소.

### $(selector[attribute~="value"])
 * attribute의 값이, value를 정확히 포함하는 요소.
