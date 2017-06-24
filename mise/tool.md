# 實用工具

### Chimp

> Develop acceptance tests & end-to-end tests with realtime feedback

通過即時回饋的方式開發驗收測試與前端測試

@focus,@dev,@watch

![](https://raw.githubusercontent.com/xolvio/chimp/master/images/realtime.gif)

```js
const assert = require('assert');

describe('Google search', function() {
  it('case 1: @watch', function() {
    browser.url('http://www.google.com/ncr');
    browser.setValue('[name=q]', 'alincode blog');
    browser.click('[name=btnG]');
    assert.equal(browser.getTitle(), 'Google');
  });
});
```

```
chimp --mocha --watch --path=test
```
