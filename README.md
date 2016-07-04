# ng2-my-datepicker

## Installation

To install this library, run:

```bash
$ npm install ng2-my-datepicker --save
```

## Use Example:

```ts
import {Component} from 'angular2/core';
import {FORM_DIRECTIVES} from 'angular2/common';
import {DatePicker} from 'ng2-my-datepicker';

class Test {
  date: string;
}

@Component({
  template: `
    <datepicker [(ngModel)]="test.date"></datepicker>
    <datepicker [(ngModel)]="test1.date" view-format="DD.MM.YYYY" model-format="YYY-MM-DD" init-date="2017-05-12"></datepicker>
  `,
  directives: [DatePicker, FORM_DIRECTIVES]
})

class App {
  test: Test;
  test1: Test;
  
  constructor() {
    this.test = Test();
    this.test1 = Test();
  }
}
```

Update the system.config
```
var map = {
	....
	'ng2-my-datepicker': 'node_modules/ng2-my-datepicker/dist'
};
var packages = {
	'ng2-my-datepicker': { main: 'index.js', defaultExtension: 'js' },
}
```

## Development

To generate all `*.js`, `*.js.map` and `*.d.ts` files:

```bash
$ npm run tsc
```

To lint all `*.ts` files:

```bash
$ npm run lint
```

## License

MIT © [Carlo Moretto](carlo.moretto@neposlab.com)
