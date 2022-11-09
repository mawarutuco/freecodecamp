### 題目

檢查謂詞（第二個參數）在集合（第一個參數）的所有元素是否爲 truthy。

換句話說，你將獲得一個對象的數組集合。 如果數組中的每個對象裏，pre 對應屬性值均爲 truthy，則返回 true。 否則，返回 false 。

JavaScript 中，如果一個值在 Boolean 的上下文中的執行結果爲 true，那麼我們稱這個值是 truthy 的。

別忘了，你可以使用點號表示法或方括號表示法（[]）來訪問對象的屬性

### 解法

```js

function truthCheck(collection, pre) {
  let ans = true
  for (let i = 0; i < collection.length; i++) {
    if (!collection[i][pre]) return ans = false
  }
  return ans
}

```
