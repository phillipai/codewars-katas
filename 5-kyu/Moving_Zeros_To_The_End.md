## [Moving Zeros To The End](https://www.codewars.com/kata/52597aa56021e91c93000cb0)

### Instructions

Write an algorithm that takes an array and moves all of the zeros to the end, preserving the order of the other elements.


```Python
move_zeros([1, 0, 1, 2, 0, 1, 3]) # returns [1, 1, 2, 1, 3, 0, 0]
```

---

### Starting Code


```python
def move_zeros(array):
    return array
```

---

### Solution


```python
def move_zeros(array):
    if 0 not in array:
        return array
    
    count = 0
    for e in array:
        if e == 0:
            count += 1
    array = list(filter((0).__ne__, array))
    
    for e in range(0, count):
        array.append(0)
    return(array)
```

---

### Sample Tests

```python
import codewars_test as test
from solution import move_zeros

@test.it("Basic tests")
def youarecute():
    test.assert_equals(move_zeros(
        [1, 2, 0, 1, 0, 1, 0, 3, 0, 1]),
        [1, 2, 1, 1, 3, 1, 0, 0, 0, 0])
    test.assert_equals(move_zeros(
        [9, 0, 0, 9, 1, 2, 0, 1, 0, 1, 0, 3, 0, 1, 9, 0, 0, 0, 0, 9]),
        [9, 9, 1, 2, 1, 1, 3, 1, 9, 9, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0])
    test.assert_equals(move_zeros([0, 0]), [0, 0])
    test.assert_equals(move_zeros([0]), [0])
    test.assert_equals(move_zeros([]), [])
```
