# 필터
## Form Filter
### :input

    <input />

##### :enabled

    <input />

##### :disabled

    <input disabled="disabled" />

#### :button

    <input type="button" />

#### :checkbox

    <input type="checkbox" />

##### :checked

    <input type="checkbox" checked="checked" />

#### :password

    <input type="password" />

#### :radio

    <input type="radio" />

#### :reset

    <input type="reset" />

#### :submit

    <input type="submit" />

#### :text

    <input type="text" />

#### :hidden

    <input type="hidden" />

#### image

    <input type="image " />

#### file

    <input type="file" />

### selected

    <select>
      <option selected="selected"></option>
    </select>

## index
#### :eq(index)
 * 0부터 시작.

#### :even
#### :odd
#### :first
 * 첫번째 요소. 하나만 반환.

#### :last
 * 마지막 요소. 하나만 반환.

#### :gt(index)
#### :lt(index)

## child
#### :first-child
 * :first와 달리 해당하는 요소를 전부 선택

#### :last-child
 * :last와 달리 해당하는 요소를 전부 선택

#### :only-child
 * 유일한 자식을 선택.

#### :nth-child
 * index
 * odd
 * even

## 기타
#### :header
 * h1, h2, h3

#### :not(selector)
#### :animated
#### :focus
