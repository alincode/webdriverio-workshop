# 介紹 WebdriverIO

### 有兩種模式 (Mode)

**Standalone Mode (獨立執行模式)**

```js
var webdriverio = require('webdriverio');
var options = {
    desiredCapabilities: {
        browserName: 'firefox'
    }
};
webdriverio
    .remote(options)
    .init()
    .url('http://www.google.com')
    .getTitle().then(function(title) {
        console.log('Title was: ' + title);
    })
    .end();
```

**The WDIO Testrunner**

> a test runner that helps you to build a reliable test suite that is easy to read and maintain

```js
describe('測試', function() {
  it('測試一', function() {
    browser.url('http://demo.keystonejs.com/keystone/signin');
  });
});
```

### Test Runner

> The test runner is an abstraction of popular test frameworks like Mocha, Jasmine or Cucumber. 

**支援的測試框架**

* Mocha：<https://mochajs.org/>
* Jasmine：<https://jasmine.github.io/>
* Cucumber

<https://npmcompare.com/compare/mocha,jasmine,cucumber>