### 題目

脫氧核糖核酸組由核酸對組成。 基本配對的字符是 AT and CG，這些字符形成了 DNA 雙螺旋的構件。

DNA 鏈缺少配對元素。 寫一個函數來匹配缺失的 DNA 字符串。 對於提供的字符串中的每個字符，找出基本的配對字符。 返回二維數組的結果。

例如，傳入 GCG 時，應返回 [["G", "C"], ["C","G"], ["G", "C"]]。

字符和它的配對組成一個數組，所有配對數組放在一個數組裏。

### 解法

```js

const DNA = { 'G': 'C', 'A': 'T' }

const findDNA = (val) => Object.keys(DNA).find(key => DNA[key] === val) || DNA[val]

function pairElement(str) {
  const arr = [...str]
  let ans = []

  arr.forEach(item => {
    const tmp = findDNA(item)
    ans.push([item, tmp])
  })

  return ans;
}

```
