# JS-Helpers
Frequently used JavaScript Techniques while solving Data Structures and Algorithms Problems


### 1. Maintaining a count of item using Map?
```
let map = new Map()
for (let i = 0; i < items.length; i++) {
  if (map.has(items[i]) {
    map.set(items[i], map.get(items[i]) + 1)
  } else {
    map.set(items[i], 1)
  }
}
```

### 2. Getting Key based on Value from Map?
```
function getKeyByValue(map, target) {
  for (let [key, value] of map.entries()) {
    if (value === target) {
      return key
    }
  }
}
```

### 3. Getting Unique values from an Array?
```
[...new Set([1,2,3,4])]

or

Array.from(new Set([1,2,3,4,1]))
```

### 4. Swap variables?
```
let a = 10, b = 20;
// Old way
let temp = a
a = b
b = temp

or

// ES6 Way

[a, b] = [b, a]
```
