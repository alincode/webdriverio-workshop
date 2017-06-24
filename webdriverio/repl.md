# REPL 模式

<http://webdriver.io/guide/usage/repl.html#description>

![](http://webdriver.io/images/repl.gif)

**啟動 REPL**

```
npm install webdriverio
node_module/.bin/wdio repl firefox
node_module/.bin/wdio repl chrome
```
**啟動 debug mode**

```js
browser.debug();
```

**範例：取得 Dcard 的頭條**

```js
browser.url('https://www.dcard.tw/signup');
browser.getTitle();
browser.click('[href="/f"]');
browser.getAttribute('#search input', 'placeholder');
browser.$('.PostEntry_container_245XM strong').getText();
```