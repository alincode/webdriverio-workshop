# Selenium Remote Control

簡稱 **Selenium RC**，它提供可以遠端執行 Selenium 的 Client / Server 架構。

Selenium Server 是複雜控制瀏覽器行為，Selenium Client 則是用於撰寫測試腳本來跟 Selenium Server 溝通。

<!--
Selenium Server 包含：
* Launcher：啟動瀏覽器
* Http Proxy
* Core
-->

### 執行 Selenium Server

至 <http://www.seleniumhq.org/download/> 下載 selenium-server-standalone-3.4.0.jar 檔

```
java -jar selenium-server-standalone-3.4.0.jar
```

### 練習題

* 執行 Selenium Server

<!--
測試專案搭配持續整合（Continous Integration）伺服器使用時，例如我們的 Jenkins CI 可能裝在一部 CentOS Linux 伺服器，而且 Server 沒有 X11 桌面環境（headless）。但是我們希望被測試的網站，可以在不同作業系統搭配不同瀏覽器的異質環境執行。
-->
