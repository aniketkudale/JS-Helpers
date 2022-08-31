# JS-Helpers
Frequently used JavaScript Techniques and Templates while solving Data Structures and Algorithms Problems


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

or

const counts = new Map();
for (const num of arr) {
  const count = counts.get(num);
  counts.set(num, count ? count + 1 : 1);
}

or

items.forEach(x => {
  if (!map.has(x))
    map.set(x, 1)
  map.set(x ,map.get(x) + 1)
})
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

### 5. Get Map Keys/Values in an Array?
```
// Get Map Keys in an Array
let keys = [...map.keys()]

// Get Map Values in an Array
let values = [...map.values()]
```

### 6. Fill an Array with certain value?
```
// Creates an Array with length 10, of zeros
new Array(10).fill(0)

// Create an Array of M x N, with values 
Array.from(Array(M), () => Array(N).fill(0))
```

### 7. Remove an Element from an Array?
```
let arr = [0, 1, 2, 3, 4, 5]

// removes 1 element from ith index
arr.splice(2, 1)
// [ 0, 1, 3, 4, 5 ]
```

### 8. Remove first Element from an array?
```
let arr = [0, 1, 2, 3, 4, 5]

// removes 1st element from array
arr.shift() // return 0

// Now arr becomes [1, 2, 3, 4, 5]
// [1, 2, 3, 4, 5 ]
```

### 9. Remove last Element from an array?
```
let arr = [0, 1, 2, 3, 4, 5]

// removes last element from array
arr.pop() // return 5

// Now arr becomes [0, 1, 2, 3, 4]
// [0, 1, 2, 3, 4]
```

### 10. Breath First Search - Tree
```
var searchBST = function(root, val) {
    if (!root) return [];
 
    let Q = [], res = null;
    
    Q.push(root);
    
    while(Q.length) {
        let size = Q.length;
        
        for(let i=0; i<size; i++) {
            let node = Q.shift();
            
            if (node.left) 
                Q.push(node.left);
            
            if (node.right)
                Q.push(node.right);
            
            if(node.val === val)
                res = node;
        }
    }
    return res;
};
```

### 11. Depth First Search - Tree
```
var searchBST = function(root, val) {
    let res = null;
    
    function traverse(node) {
        if (!node) return;
        
        if (node)
            traverse(node.left);
        
        if (node.val == val)
            res = node;
        
        if (node)
            traverse(node.right);
    }
    
    traverse(root);
    return res;
};
```
