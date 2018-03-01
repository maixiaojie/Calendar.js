# Calendar
A calendar component, based on jQuery. [Demo](//maixiaojie.github.io/Calendar/index.html)

---

在 [@yscoder/Calendar](https://github.com/yscoder/Calendar)的基础上添加了这两个功能。

- 标记工作日和假期
![avatar](/screenshots/markday.png)

- 日期多选
![avatar](/screenshots/multiselected.png)

**特别感谢  [@yscoder/Calendar](https://github.com/yscoder/Calendar)**

---

## Depend

```
<link rel="stylesheet" href="calendar.css">
<script src="jquery.js"></script>
<script src="calendar.js"></script>
```

## Use

```html
<div id="ca"></div>

<script>
$('#ca').calendar({
  // options
});
</script>
```

or

```html
<input type="text" id="in">
<div id="ca"></div>
<script>
$('#ca').calendar({
  trigger: '#in'
  // options
});
</script>
```

## Options

```js
{

    // width
    width: 280,

    // height,
    height: 280,

    // zIndex
    zIndex: 1,

    // set the trigger selector
    trigger: null,

    // offset position
    offset: [0, 1],

    // override class
    customClass: '',

    // set display view, optional date or month
    view: 'date',

    // set current date
    date: new Date(),

    // date format
    format: 'yyyy/mm/dd',

    // first day of the week
    startWeek: 0,

    // week format
    weekArray: ['日', '一', '二', '三', '四', '五', '六'],

    // month format
    monthArray: ['1月', '2月', '3月', '4月', '5月', '6月', '7月', '8月', '9月', '10月', '11月', '12月'],

    // optional date range
    // value: `[ start date[, end date] ]`
    // Fixed date range: [new Date(2016, 0, 1), new Date(2016, 11, 31)] or ['2016/1/1', '2016/12/1']
    // Starting today: [new Date(), null] or [new Date()]
    selectedRang: null,

    // display data when mouse hover
    // value: `[{ date: String || Date, value: object }, ... ]`
    // example: [ { date: '2016/1/1', value: 'A new Year'} ] or [ { date: new Date(), value: 'What to do'} ]
    data: null,

    // data label format
    // No display is set to `false`
    label: '{d}\n{v}',

    // arrow characters
    prev: '&lt;',
    next: '&gt;',

    // callback function when view changed
    // params: view, y, m
    viewChange: $.noop,

    // callback function when selected
    onSelected: function (view, date, value) {
        // body...
    },

    // callback function when mouseenter
    onMouseenter: $.noop,

    // callback function when closed
    onClose: $.noop,

    //callback function when multi-selected
    onMultiSelected: function(data) {

    }
}
```

# Methods

```js
$element.calendar(method, value)
```

* `setDate`：Setting selected date.
* `setData`：Setting hover data.
* `getMultiSelect`: Getting multi-selected date.
