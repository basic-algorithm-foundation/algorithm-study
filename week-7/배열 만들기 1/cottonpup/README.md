```js
function solution(n, k) {
    const result = [];
    
    for(let i = 1; i <= n; i++){
        if(k * i <= n){
        result.push(k * i)
        }
    }
    return result;
}
```
