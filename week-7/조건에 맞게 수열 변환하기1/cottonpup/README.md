```js
function solution(arr) {
    // arr의 각 원소에 대해 값이 50보다 크거나 같은 짝수면 2로 나누기
    // el <= 50 ===> el / 2
    
    // 50보다 작은 홀수면 2를 곱
    // else el * 2
    const answer = arr.map(el => {
        if(el >= 50 && el % 2 === 0){
            return el / 2;
        } else if(el < 50 && el % 2 !== 0){
            return el * 2;
        } else {
            return el;
        }
    })
    
    return answer;
}
```
