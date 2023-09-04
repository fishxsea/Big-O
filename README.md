# Big-O Notation

### Simplify Expressions

- O(n + 10)
  - O(n)
    <br>
- O(100 \* n)
  - O(n)
    <br>
- O(25)
  - O(1)
    <br>
- O(n^2 + n^3)
  - O(n^3)
    <br>
- O(n + n + n + n)
  - O(n)
    <br>
- O(1000 \* log(n) + n)
  - O(n)
    <br>
- O(1000 \* n \* log(n) + n)
  - O(n log n)
    <br>
- O(2^n + n^2)
  - O(2^n)
    <br>
- O(5 + 3 + 1)
  - O(1)
    <br>
- O(n + n^(1/2) + n^2 + n \* log(n)^10)
  - O(n^2)

---

### Calculate Time Complexity

_Time Complexity_: **O(n)**

```js
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
```

<br>

_Time Complexity_: **O(n)**

```js
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
```

<br>

_Time Complexity_: **O(1)**

```js
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
```

<br>

_Time Complexity_: **O(n)**

```js
function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
```

<br>

_Time Complexity_: **O(n^2)**

```js
function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
```

<br>

_Time Complexity_: **O(n)**

```js
function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if (vowels.includes(char)) {
      if (char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
```

---

### Short Answer

- True or false: n^2 + n is O(n^2).
  - True
    <br>
- True or false: n^2 \* n is O(n^3).
  - True
    <br>
- True or false: n^2 + n is O(n).
  - False
    <br>
- What’s the time complexity of the .indexOf array method?
  - O(n)
    <br>
- What’s the time complexity of the .includes array method?
  - O(n)
    <br>
- What’s the time complexity of the .forEach array method?
  - O(n)
    <br>
- What’s the time complexity of the .sort array method?
  - O(n log n)
    <br>
- What’s the time complexity of the .unshift array method?
  - O(n)
    <br>
- What’s the time complexity of the .push array method?
  - O(1)
    <br>
- What’s the time complexity of the .splice array method?
  - O(n)
    <br>
- What’s the time complexity of the .pop array method?
  - O(1)
    <br>
- What’s the time complexity of the Object.keys() function?
  - O(n)
    <br>
- What’s the space complexity of the Object.keys() function?
  - O(n)
