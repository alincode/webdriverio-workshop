# 測試報表

### Dot

**安裝**

```
npm install wdio-spec-reporter --save-dev
```

**設定檔**

```js
// wdio.conf.js
module.exports = {
  // ...
  reporters: ['dot'],
  // ...
};
```

**畫面範例**

![](http://webdriver.io/images/dot.png)


### Spec

**設定檔**

```js
// wdio.conf.js
module.exports = {
    // ...
    reporters: ['spec', 'junit'],
    reporterOptions: {
        junit: {
            outputDir: './'
        }
    },
    // ...
};
```

**安裝**

```
npm install wdio-junit-reporter --save-dev
```

**畫面範例**

![](http://webdriver.io/images/spec.png)

### Junit

**畫面範例**

![](http://webdriver.io/images/jenkins-final.png)

<!--
http://webdriver.io/guide/testrunner/jenkins.html
-->

### Allure

### Teamcity

### Json

### Concise

### Tap

### Customreporter