```js
function solution(arr) {
    let answer = [];
    arr.forEach(el => {
        for(let i = 0; i < el; i++){
            answer.push(el)
        }
    })
    return answer;
}
```
