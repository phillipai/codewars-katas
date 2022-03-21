## [Sum The Strings](https://www.codewars.com/kata/5966e33c4e686b508700002d)

### Instructions

---

Create a function that takes 2 integers in form of a string as an input, and outputs the sum (also as a string):

Example: (Input1, Input2 -->Output)

```python
"4",  "5" --> "9"
"34", "5" --> "39"
"", "" --> "0"
"2", "" --> "2"
"-5", "3" --> "-2"
```

Notes:

- If either input is an empty string, consider it as zero.

- Inputs and the expected output will never exceed the signed 32-bit integer limit (`2^31 - 1`)

FUNDAMENTALS

---

### Starting Code


```python
def sum_str(a, b):
    # happy coding !
    pass
```

---

### Solution


```python
def sum_str(a, b):
    if a and b:
        a, b = int(a), int(b)
        return str(a + b)
    elif not a and b:
        return b
    elif not b and a:
        return a
    else:
        return "0"
```

---

### Sample Tests

```python
import codewars_test as test
from solution import sum_str

@test.describe("Fixed Tests")
def basic_tests():
    
    @test.it("Sample Tests")
    def sample_tests():
        test.assert_equals(sum_str("4","5"), "9")
        test.assert_equals(sum_str("34","5"), "39")

    @test.it("Tests with empty strings")
    def empty_string():
        test.assert_equals(sum_str("9",""), "9", "x + empty = x")
        test.assert_equals(sum_str("","9"), "9", "empty + x = x")
        test.assert_equals(sum_str("","") , "0", "empty + empty = 0")
```
