## [Find the middle element](https://www.codewars.com/kata/545a4c5a61aa4c6916000755)

### Instructions

---

As a part of this Kata, you need to create a function that when provided with a triplet, returns the index of the numerical element that lies between the other two elements.

The input to the function will be an array of three distinct numbers (Haskell: a tuple).

For example:
```python
gimme([2, 3, 1]) => 0
```

2 is the number that fits between 1 and 3 and the index of 2 in the input array is 0.

Another example (just to make sure it is clear):

```python
gimme([5, 10, 14]) => 1
```

10 is the number that fits between 5 and 14 and the index of 10 in the input array is 1.

---

### Starting Code


```python
def gimme(input_array):
    # Implement this function
```

---

### Solution


```python
def gimme(input_array):
    high = max(input_array)
    low = min(input_array)
    for i in input_array:
        if i != high and i != low:
            return input_array.index(i)
```

---

### Sample Tests

```python
import codewars_test as test
from solution import gimme

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(gimme([2, 3, 1]), 0, 'Finds the index of middle element')
        test.assert_equals(gimme([5, 10, 14]), 1, 'Finds the index of middle element')
```
