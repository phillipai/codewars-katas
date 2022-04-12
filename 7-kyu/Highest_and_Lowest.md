## [Highest and Lowest](https://www.codewars.com/kata/554b4ac871d6813a03000035)

### Instructions

---

In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.

#### Examples

```python
high_and_low("1 2 3 4 5")  # return "5 1"
high_and_low("1 2 -3 4 5") # return "5 -3"
high_and_low("1 9 3 4 -5") # return "9 -5"
```

#### Notes
- All numbers are valid Int32, no need to validate them.
- There will always be at least one number in the input string.
- Output string must be two numbers separated by a single space, and highest number is first.


---

### Starting Code


```python
def high_and_low(numbers):
    # ...
    return numbers
```

---

### Solution


```python
def high_and_low(numbers):
    list = []
    numbers = numbers.split()
    for e in numbers:
        list.append(int(e))
    maxi = str(max(list))
    mini = str(min(list))
    return (maxi) + " " + (mini)
```

---

### Sample Tests

```python
import codewars_test as test
from solution import high_and_low

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(high_and_low("8 3 -5 42 -1 0 0 -9 4 7 4 -4"), "42 -9");
        test.assert_equals(high_and_low("1 2 3"), "3 1");
```
