# Javascript 基礎

**宣告**

```js
var message;
```

**字串**

```js
var message = '哈囉';
var name = "alincode";
```
**數字**

```js
var num1 = 1;
var num2 = 1.5;
```

**等於**

* ===：Strict equality
* ==：Loose equality

```js
var x = 5;
console.log(x == 5); 
console.log(x == "5");
console.log(x === "5");
```

**陣列**

```js
var people = [{
    firstname: 'ailin',
    lastname: 'liou'

  },{
    firstname: 'Jane',
    lastname: 'Doe'
  }
];

var lang = ['中文', '英文'];

// 陣列長度
lang.length;

lang.forEach(function(item) {
    console.log(item);
});
```

**函式**

```js
function greet() {
	console.log('哈囉');
}

greet();
```

**callback 函式**

```js
var lang = ['中文', '英文'];

function callback(item) {
    console.log(item);
}

lang.forEach(callback);
```