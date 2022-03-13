## [Find the smallest integer in the array](https://www.codewars.com/kata/55a2d7ebe362935a210000b2)

### Instructions

---

Given an array of integers your solution should find the smallest integer.

For example:

- Given `[34, 15, 88, 2]` your solution will return `2`
- Given `[34, -345, -1, 100]` your solution will return `-345`
You can assume, for the purpose of this kata, that the supplied array will not be empty.

---

### Starting Code


```python
def find_smallest_int(arr):
    # Code here
```

---

### Solution


```python
def find_smallest_int(arr):
    return min(arr)
```

---

### Sample Tests

```python
import codewars_test as test

# for backward compatibility
try:
    from solution import findSmallestInt as find_smallest_int
except ImportError:
    from solution import find_smallest_int

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(find_smallest_int([78, 56, 232, 12, 11, 43]), 11)
        test.assert_equals(find_smallest_int([78, 56, -2, 12, 8, -33]), -33)
        test.assert_equals(find_smallest_int([0, 1-2**64, 2**64]), 1-2**64)
```
