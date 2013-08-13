# Date

    new Date() // current date and time
    new Date("December 6, 1988, 12:00:00") // month dd, yyyy hh:mm:ss
    new Date(yyyy, mm, dd, hh, mi, ss)  // 주어지지 않은 인자는 0으로 취급.
    new Date(milliseconds) //milliseconds since 1970/01/01

## method
### toString
### toUTCString
### toDateString
### toTimeString
### getTime
 * milliseconds since 1970/01/01

### getFullYear
 * for digit year

### getMonth
 * 0-11 월

### getDate
 * day of the month

### getDay
 * 일요일을 0으로해서 요일

### getHours
 * 0-23 시간

### getMinutes
 * 0-59 분

### getSeconds
 * 0-59 초

### getMilliseconds
 * 0-999

### getTimezoneOffset
 * GMT 시간과의 차이. 분으로 return

### setFullYear

    d.setFullYear(2010,0,14);

### setMonth

    d.setDate(d.getMonth()+5);

### setDate

    d.setDate(d.getDate()+5);

### setHours

    d.setDate(d.getHours()+5);

### setMinutes

    d.setDate(d.getMinutes()+5);

### setSeconds

    d.setDate(d.getSeconds()+5);

### setTime

    d.setTime(d.getTime()+5);
