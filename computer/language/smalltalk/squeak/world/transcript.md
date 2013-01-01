# Transcript
 * TranscriptStream의 instance

## Method
## Access
### characterLimit
  * screen에 출력될 수 있는 최대 글자수.

        Transcript show: Transcript characterLimit

## Initialization
### closeAllViews
 * Transcript view를 닫는다.

        Transcript closeAllViews

### open
 * Transcipt view를 연다.

        Transcript open

### openLabel:
 * Transcript view를 이름을 붙여서 연다.

        Transcript openLabel: 'bar'

## Model protocol
### codePaneMenu: shifted:
 * Note that unless we override perform:orSendTo:, PluggableTextController will respond to all menu items
### perform: orSentTo:
 * Selector was just chosen from a menu by a user.  If can respond, then perform it on myself. If not, send it to otherTarget, presumably the editPane from which the menu was invoked.
### release
### step
 * Objects that may be models of SystemWindows need to respond to this, albeit vacuously

## Stream extensions
### bs
 * Transcript의 모든 문자를 지운다.

    Transcript show: 1.
    Transcript clear.

### clear
 * Transcript의 모든 문자를 지운다.

        Transcript show: 1.
        Transcript clear.

### endEntry
 * stream에 쌓여 있는 모든 문자를 출력한다.

        Transcript endEntry.

### flush

        Transcript flush.

### pastEntPut:
 * If the stream reaches its limit, just output the contents and reset.
### show

        Transcript show: 1.
        Transcript show: '1'.

## tool builder
### buildWith
