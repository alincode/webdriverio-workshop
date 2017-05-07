# 測試基礎

### 黑箱測試 vs 白箱測試

* 黑箱測試：假設看不到程式碼的方式去測試，主要透過使用者介面去測試功能。
* 白箱測試：假設看得到程式碼的方式去測試，會直接撰寫可與程式碼對接的測試程式。

### 功能測試 vs 效能測試

**功能測試**

* 邏輯功能測試
* 介面測試
* 好用性測試
* 安裝測試
* 相容性測試(ie9, ie10, ie11, android 版本?)

**效能測試**

* 時間效能：回應時間長短
* 空間效能：消耗的系統資源，例如：記憶體使用率、網路頻寬。

### 手動測試 vs 自動化測試

以自動化程度來劃分，可分成：

**手動測試 (Manual Testing)**

一個步驟一個步驟的手動去執行

**自動化測試 (Automation Testing)**

* 錄製測試步驟
* 撰寫自動化程式

**比較表**

項目 | 手動測試 | 自動化測試
---------------|-------------------
花費的時間 | 長 | 短
可測出的問題分佈 | 新功能的 bug | 已知的測試流程的 bug
同時測試數量  | 一次只能測一個 | 一次可以測多個

### 測試金字塔

由 Martin Fowler 所提出的分層測試概念。

* 單元測試：針對程式中的最小測試單元進行驗證。
* Postman / Http Unit
* UI 測試 / 前端 (end-to-end) 測試

**UI測試框架**

* Python：Robot Framework
* Javascript：Webdriver.IO、Nightwatch.js、...
* Java / Groovy：Geb

### 測試環境

![](https://i-msdn.sec.s-msft.com/dynimg/IC721395.png)

* 開發環境 (DEV)
* QA / UAT
* 跟 Production 一致的環境 (Staging)
* 正式環境 (Production)

### 開發性問答題

* 前端的痛？
* 為什麼前端測試這麼重要？

### 延伸閱讀

* [When to Start Automation Testing - GlobalSQA](http://www.globalsqa.com/start-automation-testing/)