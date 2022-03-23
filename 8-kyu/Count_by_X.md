## [Count by X](https://www.codewars.com/kata/5513795bd3fafb56c200049e)

### Instructions

---

Create a function with two arguments that will return an array of the first (n) multiples of (x).

Assume both the given number and the number of times to count will be positive numbers greater than 0.

Return the results as an array (or list in Python, Haskell or Elixir).

Examples:

```python
count_by(1,10) #should return [1,2,3,4,5,6,7,8,9,10]
count_by(2,5) #should return [2,4,6,8,10]
```


---

### Starting Code


```python
def count_by(x, n):
    """
    Return a sequence of numbers counting by `x` `n` times.
    """
```

---

### Solution


```python
def count_by(x, n):
    return [i * x for i in range(1, n + 1)]
```

---

### Sample Tests

```python
import codewars_test as test
from solution import count_by

@test.describe("Fixed Tests")
def basic_tests():
    @test.it("Fixed tests")
    def fixed_tests():   
        test.assert_equals(count_by(1, 5), [1, 2, 3, 4, 5])
        test.assert_equals(count_by(2, 5), [2, 4, 6, 8, 10])
        test.assert_equals(count_by(3, 5), [3, 6, 9, 12, 15])
        test.assert_equals(count_by(50, 5), [50, 100, 150, 200, 250])
        test.assert_equals(count_by(100, 5), [100, 200, 300, 400, 500])
    
```
