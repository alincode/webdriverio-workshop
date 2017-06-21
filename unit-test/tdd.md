# TDD (Test-driven development) 測試驅動開發

TDD 是一種程式開發的技巧，簡單來說就是**先寫測試程式，然後才實作功能**，藉由先定義規格，在尚未實作前就能知道開發方向是否正確，實作完成後能讓下一個開發者藉由測試快速得知輸入和輸出結果。

* 從測試去思考程式如何實作
* 用自然語言描述測試案例
  * 使用者和工程師用同一種語言，避免溝通成本
  * 測試後的輸出結果可以直接做為文件閱讀

![TDD lift circle](http://www.agilenutshell.com/assets/test-driven-development/tdd-circle-of-life.png)

剛開始寫測試時會先定義 function 的輸入輸出，一開始測試會 Test fail，實作 function 後能讓測試能順利通過，實作完成為了增加程式碼的可讀性、重用性、效能等等因素重構，導致 Test fail 直至重構完成，測試能快速驗證重構後的結果，不會導致其他狀況發生，形成 TDD 的正向循環。

### TDD 的優點

* 快速驗證 function 正確性
* 寫測試就是寫文件，有輸入輸出
* 多人有效並無障礙的溝通
* 程式完成後不怕重構

### 單元測試

單元測試三步驟：3A Pattern

* Arrange：預先安排與配置
* Act：執行我們要測試的程式
* Assert：斷言或驗證執行結果是否符合預期

[Mocha](https://mochajs.org/) 測試框架

**安裝 Mocha**

```
npm install mocha -g
```

```js
var assert = require('assert');

describe('test suite', () => {
  beforeEach(() => {});
  before(() => {});
  after(() => {});
  afterEach(() => {});
  it('test case 1', () => {});
  it('test case 2', () => {});
  it('test case 3', () => {});
});
```

**單獨測試**

```js
it.only('單獨測試', async (done) => done());
```

**略過測試**

```js
it.skip('略過測試', async (done) => done());
```

<https://github.com/alincode/calc>

```js
// lib/app.js
exports.addition = function(x, y){
  return x + y;
}
exports.subtraction = function(x, y){
  return x - y;
}
exports.multiplication = function(x, y){
  return x * y;
}
exports.division = function(x, y){
  return x / y;
}
```

```js
// test/app.js
var app = require('../lib/app.js');
var assert = require('assert');

describe('計算機', () => {
  it('加', () => {
    var result = app.addition(1, 2);
    assert.equal(result, 3);
  });
  it('減', () => {
    var result = app.subtraction(2, 1);
    assert.equal(result, 1);
  });
  it('乘', () => {
    var result = app.multiplication(2, 3);
    assert.equal(result, 6);
  });
  it('除', () => {
    var result = app.division(6, 3);
    assert.equal(result, 2);
  });
});
```

**執行方式**

```
npm test
```

### 練習題

* 撰寫一個 BMI 的單元測試程式
* <https://github.com/alincode/bmi>
