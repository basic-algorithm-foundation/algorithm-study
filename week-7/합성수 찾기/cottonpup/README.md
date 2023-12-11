# 포기
```js
// 합성수: 1과 자기 자신 이외에 다른 자연수로도 나눌 수 있는 1보다 큰 자연수를 말합니다. 다시 말해, 최소한 하나 이상의 다른 자연수 약수를 가지고 있는 수죠.

function isComposite(number) {
  // 1과 자기 자신을 제외한 약수가 하나라도 있는지 확인
  for (let i = 2; i < number; i++) {
    if (number % i === 0) {
      // 나누어떨어지면 합성수
      return true;
    }
  }
  // 나누어떨어지는 약수가 없으면 합성수가 아님
  return false;
}

function solution(n) {
  let count = 0;
  // 가장 작은 합성수는 4에서 n까지 모든 숫자에 대해 합성수인지 확인
  for (let i = 4; i <= n; i++) {
    if (isComposite(i)) {
      count++;
    }
  }
  return count;
}
```
- 합성수란 무엇인가...(수포자라서 공부가 많이 필요한 것 같다)
- 수학관련 문제는 다시 한번 더 복습하고 여러번 풀어보자.
