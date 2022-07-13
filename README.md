# js-ts-range
basic code to create a for loop with a range similar to Python using Typescript

Here's a good [explanation](https://writingjavascript.com/how-do-you-iterate-over-a-range-in-javascript)

```
RANGE = function* (from:number, to:number, step:number = 1) {
    let value:number = from;
    while (value <= to) {
      yield value;
      value += step;
    }
  }

```

**Usage**
```
<div *ngFor="let i of RANGE(2,10,2)">{{ i }}</div>
```

**Notes**
RANGE can also be used in the component itself vs being called in the template. Note while running in development there will be a 'ExpressionChangedAfterItHasBeenCheckedError' error in the console. Per [Angular Docs](https://angular.io/errors/NG0100) this only occurs in development and goes away in production. After spinning up a quick example on a production server, it is verified the error does go away.
