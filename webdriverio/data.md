# 測試帳號與資料的管理

不建議存入資料庫

**方法一**

```js
content: {
  get: () => {
    return {
      email: 'demo@keystonejs.com',
      correctPassword: 'demo',
      worryPassword: '1111',
      errorMessage: 'The email and password you entered are not valid.',
      alertDanger: '.Alert--danger'
    };
  }
},
```

```js
LoginPage.email.setValue(LoginPage.content.email);
LoginPage.password.setValue(LoginPage.content.worryPassword);
```

**方法二**

```js
var config = require('./test-data.json');
```

```json
{
  "email": "demo@keystonejs.com",
  "correctPassword": "demo",
  "worryPassword": "1111",
  "errorMessage": "The email and password you entered are not valid.",
  "alertDanger": "alertDanger"
}
```
