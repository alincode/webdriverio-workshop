# 組織測試專案

```js
// wdio.conf.js
exports.config = {

    // define all tests
    specs: ['./test/specs/**/*.spec.js'],      

    // define specific suites
    suites: {
        login: [
            './test/specs/login.success.spec.js',
            './test/specs/login.failure.spec.js'
        ],
        otherFeature: []
    }
}
```

```
wdio wdio.conf.js --suite login
wdio wdio.conf.js --suite login,otherFeature
```