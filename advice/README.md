# 實用建議

## 撰寫前端測試程式注意事項建議

### 常常遇到拋出 element，不存在的 error？

多用 waitFor

少用 browser.pause(3000)

### 用 ReactJS, AngularJS 寫的網站，可不可以測？

## 導入網站自動化測試建議
<!--### 前端測試的使用時機-->

### 導入的時機

* 專案開發到後期，UI 已經不會很頻繁的變動。

### 適合使用在什麼樣的情境

* 使用在驗收測試
* 需要支援多種環境的軟體專案

### 與 Docker

* [GitHub - SeleniumHQ/docker-selenium: Docker images for Selenium Standalone Server](https://github.com/SeleniumHQ/docker-selenium)

<!--
Xvfb 是什麼呢，他的名稱是 virtual framebuffer X server for X Version 11， Xvfb 可以直接處理 Window 的圖形化功能，並且不會把圖像輸出到螢幕上，也就是說，就算你的電腦沒有啟動 Xwindow ， 你仍然可以執行任何圖形程式。
-->

<!--
https://www.puritys.me/docs-blog/article-262-%E5%AE%89%E8%A3%9D-XVFB-%E5%81%9A-Selenium-%E6%B8%AC%E8%A9%A6.html
-->