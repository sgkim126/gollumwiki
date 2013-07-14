# Drag & Drop API
  * HTML5에서 지원하는 drag api
  * img tag에만 먹히는듯 하다.

## attribute

#### draggable
  - true
  - false

## event
#### dragstart
  * drag 시작

#### drag
  * drag 중

#### dragend
  * drag 종료

#### dragenter
  * drag중인 마우스가 element에 들어감.

#### dragover
  * drag중인 마우스가 element위를 지나감.

#### dragleave
  * drag중인 마우스가 element를 떠남.

#### drop
  * drop

## dataTransfer
### attribute
#### dropEffect
#### effectAllowed
#### types
#### files
### method
#### clearData
  - type

#### setData
  - type
  - data

#### getData
  - type

#### setDragImage
  - image
  - x
  - y

#### addElement
  - element
