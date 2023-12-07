```js
function solution(a, b) {
    
    let result = 0;
    
    if(a % 2 !== 0 && b % 2 !== 0){
        result += (a * a) + (b * b);
    } else if(a % 2 !== 0 || b % 2 !== 0){
        result += 2 * (a + b);
    } else if(a % 2 === 0 && b % 2 === 0){
        result += Math.abs(a - b);
    }
    return result;
}
```
