# ng2-datetime v1.0.3
Datetime picker plugins wrapper for Angular2.
Tested with __angular 2.0.0-rc.1__

##### DEMO: https://nkalinov.github.io/ng2-datetime

## Dependencies
- [Bootstrap3 (__CSS only__)](http://getbootstrap.com/)
- [jQuery 2.x](http://jquery.com/)
- [Bootstrap-timepicker __(JS+CSS)__](http://jdewit.github.io/bootstrap-timepicker/)
`npm install --save bootstrap-datepicker` or use the bundled version from `src/vendor/bootstrap-datepicker`
- [Bootstrap-datepicker __(JS+CSS)__](http://eternicode.github.io/bootstrap-datepicker/)
`npm install --save bootstrap-timepicker` or use the bundled version from `src/vendor/bootstrap-timepicker`

## Installation
`npm install --save ng2-datetime`

## Usage
1. import some way or another the required dependencies
If you want to use the bundled versions, you can import them like this:
```
import 'ng2-datetime/src/vendor/bootstrap-datepicker/bootstrap-datepicker.min.js';
import 'ng2-datetime/src/vendor/bootstrap-timepicker/bootstrap-timepicker.min.js';
```
The bundled CSS is in the same folder, it's up to you to decide how to import those.
2. `import {NKDatetime} from 'ng2-datetime/ng2-datetime';`
3. Add to your component's directives property
```
@Component({
    ...
    directives: [NKDatetime],
    ...
})
```
- Basic usage: `<datetime [(ngModel)]="date"></datetime>`
See the [__DEMO__](https://nkalinov.github.io/ng2-datetime) and it [__source__](https://github.com/nkalinov/ng2-datetime/tree/master/demo) for more information.

## Options
- `[datepicker]="{Object} || false"` - Object with [Datepicker options](http://bootstrap-datepicker.readthedocs.org/en/latest/options.html) or `false` if you want to remove the datepicker
__Ex.__ `<datetime [datepicker]="{daysOfWeekDisabled: [0,6]}" [(ngModel)]="date"></datetime>`

- `[timepicker]="{Object} || false"` - Object with [Timepicker options](http://jdewit.github.io/bootstrap-timepicker/) or `false` if you want to remove the timepicker
__Ex.__ `<datetime [timepicker]="{showMeridian: false, minuteStep: 1}" [(ngModel)]="date"></datetime>`

## Contributing
Fork > Create > Pull request

#### Thanks
- @jdewit for the [timepicker plugin](https://github.com/jdewit/bootstrap-timepicker)
- @eternicode for the [datepicker plugin](https://github.com/eternicode/bootstrap-datepicker)
- @alexanza for the idea of removing one of the two pickers by passing `false` to the options

## TODO:
- find out how to test implemented ControlValueAccessor interface
- test jQuery plugins init and events