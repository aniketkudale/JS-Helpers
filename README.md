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
