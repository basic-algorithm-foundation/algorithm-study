```js
function solution(names) {
    const result = [];
    
    for(let i = 0; i < names.length; i+= 5){
        result.push(names[i])
    }
    return result;
}
```
- i값에서 5를 더할 수 있다. (처음 알았다!!)
