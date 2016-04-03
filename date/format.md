# 日期格式化

轻量简单的日期格式化工具函数，毕竟很多时候我们并不想引入`moment`这个大块头。

``` javascript
import format from 'vux/src/components/datetime/format'

const time1 = new Date('2016/01/03 19:19:19')
const time2 = new Date('2016/01/03 09:09:09')

expect(format(time1, 'YYYY-MM-DD')).toBe('2016-01-03')
expect(format(time1, 'YY-MM-DD')).toBe('16-01-03')

expect(format(time1, 'YYYY-MM-DD HH:mm:ss')).toBe('2016-01-03 19:19:19')

// hours
expect(format(time1, 'HH')).toBe('19')
expect(format(time1, 'hh')).toBe('07')

expect(format(time2, 'HH')).toBe('09')
expect(format(time2, 'hh')).toBe('09')

// minute
expect(format(time1, 'mm')).toBe('19')

expect(format(time2, 'mm')).toBe('09')
expect(format(time2, 'm')).toBe('9')

// seconds
expect(format(time1, 'ss')).toBe('19')
expect(format(time2, 'ss')).toBe('09')

expect(format(time2, 's')).toBe('9')
```