# A로 B 만들기

## 문제 링크

https://school.programmers.co.kr/learn/courses/30/lessons/120886
<br>

## 나의 풀이

```js
function solution(before, after) {
  return before.split("").sort().join("") === after.split("").sort().join("") ? 1 : 0
}
```