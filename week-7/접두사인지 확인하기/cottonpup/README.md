```js
function solution(my_string, is_prefix) {
  const prefix = [];
  for (let i = 1; i <= my_string.length; i++) {
    prefix.push(my_string.slice(0, i));
  }
  console.log(prefix, is_prefix);
  return prefix.includes(is_prefix) ? 1 : 0;
}
```
