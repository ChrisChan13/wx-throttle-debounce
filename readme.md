# wx-throttle-debounce

🙌 Throttle & Debounce functions for Wechat MiniProgram

## Usage

```
npm i -S wx-throttle-debounce --production
```

## Doc

### debounce(func, wait, options)

#### Arguments

*func (Function)*: The function to debounce.

*\[wait=0\] (number)*: The number of milliseconds to delay.

*\[options={}\] (Object)*: The options object.

*\[options.leading=false\] (boolean)*: Specify invoking on the leading edge of the timeout.

*\[options.maxWait\] (number)*: The maximum time func is allowed to be delayed before it's invoked.

*\[options.trailing=true\] (boolean)*: Specify invoking on the trailing edge of the timeout.

#### Return

*(Function)*: Returns the new debounced function.

### throttle(func, wait, options)

#### Arguments

*func (Function)*: The function to throttle.

*\[wait=0\] (number)*: The number of milliseconds to throttle invocations to.

*\[options={}\] (Object)*: The options object.

*\[options.leading=true\] (boolean)*: Specify invoking on the leading edge of the timeout.

*\[options.trailing=true\] (boolean)*: Specify invoking on the trailing edge of the timeout.

#### Return

*(Function)*: Returns the new throttled function.

## Example

```
import { debounce, throttle } from 'wx-throttle-debounce';

Page({
  ...
  debouncedFunc: debounce(function(events) {
    // do somthing
  }, 100, { /* some options */ }),
  throttledFunc: throttle(function(events) {
    // do somthing
  }, 100, { /* some options */ }),
  ...
});
```
