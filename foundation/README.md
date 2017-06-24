# 測試基礎

### 一個完整的測試

* 準備環境
* 準備資料
* 定義輸入
* 執行 function
* 驗證輸出 

### 測試環境

![](https://i-msdn.sec.s-msft.com/dynimg/IC721395.png)

  -  | DEV | QA / UAT | Staging | Production
---------|----------|---------|--------|---------
 資料庫內的資料 | 假資料 | 假資料 | 跟 Production 一致的環境 | 真實資料
 分支 | develop | release | master | master
 使用情境 | beta 功能 demo | 驗收功能 | * 上版前的最後測試 <br> * 預先測試 SQL 腳本 | 

UAT：全名叫 User Acceptance Testing 使用者驗收測試

### 測試需要使用到的資料

* 環境變數 & 環境設定檔

```
// test/conf
defaults.js
index.js
local.js
mobile.js
travis-ci.js
```

<https://github.com/webdriverio/webdriverio/blob/master/test/conf/defaults.js>


```
process.env._PORT
```

**Mac**

```
export TESTINGBOT_KEY=
export TESTINGBOT_SECRET=
```

**Window**

```
SET TESTINGBOT_KEY=
SET TESTINGBOT_SECRET=
```

#### fixtures

https://github.com/webdriverio/webdriverio/tree/master/test/fixtures

**測試專用資料庫**

* 匯入測試 sql 檔案至資料庫
* 將初始化專案的假資料存在 JSON

### 測試金字塔 (Test Pyramid)

![](https://img3.doubanio.com/lpic/s6246942.jpg)

測試金字塔的概念是由 Mike Cohn 所提出的一個測試開發概念，被 [Martin Fowler](http://search.books.com.tw/search/query/key/Martin+Fowler/adv_author/1/) 大師轉述而聲名大噪，相關細節描述在 [Succeeding with Agile](https://www.tenlong.com.tw/products/9780321579362) 這本書中，其中很重要的一點是強調你應該擁有更多低階的單元測試。

![](assets/test-pyramid.png)

層級 | 測試程式的數量 | 描述
---------|----------|---------
 第三層 | 10% | UI 測試 / 前端 (end-to-end) 測試
 第二層 | 20% | 商業邏輯測試 / 整合測試
 第一層 | 70% | 單元測試：針對程式中的最小測試單元進行驗證。

 相關資料來源：<https://martinfowler.com/bliki/TestPyramid.html>

<!--
[搞笑談軟工: BDD（21）從測試金字塔看BDD的自動化驗收測試](http://teddy-chen-tw.blogspot.tw/2017/03/bdd21bdd.html)
[软件测试反模式——杯型蛋糕 – ThoughtWorks洞见](http://insights.thoughtworkers.org/introducing-software-testing-cupcake-anti-pattern/)
-->

### 手動測試 vs 自動化測試

以自動化程度來劃分，可分成：

* 手動測試 (Manual Testing)：一個步驟一個步驟的手動去執行
* 自動化測試 (Automation Testing)

**錄製測試步驟**

![](http://www.seleniumhq.org/projects/ide/selenium-ide.gif)

**撰寫自動化程式**

```js
var webdriver = require('selenium-webdriver'),
    By = webdriver.By,
    until = webdriver.until;

var driver = new webdriver.Builder()
    .forBrowser('firefox')
    .build();

driver.get('http://www.google.com/ncr');
driver.findElement(By.name('q')).sendKeys('webdriver');
driver.findElement(By.name('btnG')).click();
driver.wait(until.titleIs('webdriver - Google Search'), 1000);
driver.quit();
```

**比較表**

項目 | 手動測試 | 自動化測試
---------------|-------------------
花費的時間 | 長 | 短
可測出的問題分佈 | 新功能的 bug | 已知的測試流程的 bug
同時測試數量  | 一次只能測一個 | 一次可以測多個 

### 延伸閱讀

* [The Deadline: 《軟體測試專案實作：技術、流程與管理》筆記](http://w1a2d3s4q5e6.blogspot.tw/2012/11/blog-post_7.html)