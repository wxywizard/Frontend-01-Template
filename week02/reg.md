#### 匹配所有 Number 直接量

```js
reg = /^[-\+]?(\.\d+|(0|[1-9]\d*)\.?\d*?)([eE][-\+]?d+)?$|^0[bB][01]+$|^0[oO][0-7]+$|^0[xX][0-9a-fA-F]+$/
```

#### 匹配所有的字符串直接量

```js
reg = /^['"\\bfnrtv/dxu]$|^u[0-9a-fA-F]{4}$|^u(10|0?[0-9a-fA-F])[0-9a-fA-F]{0,4}$/
```