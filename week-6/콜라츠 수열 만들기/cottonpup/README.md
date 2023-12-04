```js
function solution(n) {
    const result = [n]; // 시작 값 추가

    while(n !== 1) {
        if(n % 2 === 0) {
            n = n / 2; // n을 2로 나눔
        } else {
            n = (3 * n) + 1; // n이 홀수일 때의 처리
        }
        result.push(n); // 수정된 n 값을 배열에 추가
    }
    return result;
}

```
- 마지막에 챗지피티 도움을 받았다.
- push 의 위치가 잘못되었다
- 각 반복 단계에서 n의 값을 변경하고, 그 변경된 값을 포함시키는 것이 필요하다