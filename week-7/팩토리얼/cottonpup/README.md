# 포기
```js
function solution(n) {
  let i = 1;
  let factorial = 1;

  // i의 팩토리얼 값이 n 이하가 될 때까지 반복합니다.
  while (factorial <= n) {
    i++; // 다음 숫자로 이동합니다.
    factorial *= i; // 현재의 팩토리얼 값에 i를 곱합니다.
  }

  // 팩토리얼 값이 n을 초과한 경우, 조건을 만족하는 가장 큰 i는 i - 1입니다.
  return i - 1;
}
```

- 팩토리얼 문제가 생각보다 많은 것 같은데 제대로 구현하는 방법을 다시 고민해봐야겠다.
