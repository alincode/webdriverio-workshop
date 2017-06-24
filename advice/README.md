# 實用建議

## 撰寫前端測試程式注意事項建議

### 常常遇到拋出 element，不存在的 error？

多用 waitFor

少用 browser.pause(3000)

### 用 ReactJS, AngularJS 寫的網站，可不可以測？

<!-- 可以的 -->

## 導入網站自動化測試建議

### 適合使用在什麼樣的情境

* 使用在驗收測試
* 需要支援多種環境的軟體專案
* 遇到測試 Team 的極限，手動測試無法在符合期待時...

### 導入的時機

* 專案開發到後期，UI 已經不會很頻繁的變動。

### 與 Docker

* [GitHub - SeleniumHQ/docker-selenium: Docker images for Selenium Standalone Server](https://github.com/SeleniumHQ/docker-selenium)