# 上課 VM 環境

### VM 環境

* 要切到 user 帳號
* 密碼：password

### C9 IDE

<http://localhost:9083>

### 環境異常

* Selenium Server 沒打開

![](mise/assets/connect-error.png)

```
webdriver-manage start
```

* Selenium Server 打開後還是有問題

更新瀏覽器驅動程式

```
webdriver-manage update
```

**測試環境的步驟**

* 先啟動 selenium server

```
webdriver-manager start
```

* 再啟動前端測試

```
cd ~/webdriverio-env-test
npm test
```

### VM 異常

* [如何啟用 Intel VT-x 和 AMD SVM?](https://www.qnap.com/zh-hk/how-to/faq/article/%E5%A6%82%E4%BD%95%E5%95%9F%E7%94%A8-intel-vt-x-%E5%92%8C-amd-svm)

### 重新安裝 firefox

```
sudo apt-get -y remove firefox
sudo apt-get -y install firefox
```

### Firefox 異常

```
firefox -p
find ~/ -mount ! -user $(whoami)
sudo chown -hR user:user /home/user/.cache
sudo chown -hR user:user .mozilla/
```
