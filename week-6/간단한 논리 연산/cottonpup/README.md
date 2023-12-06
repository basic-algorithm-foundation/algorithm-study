# 틀린 답
```js
return (x1 && x2) || (x3 && x4)
```
# 고친 답
```js
return (x1 || x2) && (x3 || x4)
```
- `V` === OR Operation
- `∧` === AND Operation