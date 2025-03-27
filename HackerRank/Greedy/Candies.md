# Candies

## 문제 링크

https://www.hackerrank.com/challenges/candies/problem?isFullScreen=true

<br>

## 나의 풀이

```js
function candies(n, arr) {
  let dp = new Array(n).fill(1);

  for (let i = 1; i < n; i++) {
    if (arr[i] > arr[i - 1]) {
      dp[i] = dp[i - 1] + 1;
    }
  }

  for (let i = n - 2; i >= 0; i--) {
    if (arr[i] > arr[i + 1]) {
      dp[i] = Math.max(dp[i], dp[i + 1] + 1);
    }
  }

  return dp.reduce((sum, curr) => sum + curr, 0);
}
```
