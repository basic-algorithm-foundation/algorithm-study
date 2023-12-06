```js
function solution(my_string) {
  const result = [];

  for (let i = 0; i < my_string.length; i++) {
    result.push(my_string.slice(i));
  }

  return result.sort();
}
```

- 알파벳, 사전순 정렬은 그냥 sort() 메서드를 사용하면 된다.
