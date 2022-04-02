## [Quarter of the year](https://www.codewars.com/kata/5ce9c1000bab0b001134f5af)

### Instructions

---

Given a month as an integer from 1 to 12, return to which quarter of the year it belongs as an integer number.

For example: month 2 (February), is part of the first quarter; month 6 (June), is part of the second quarter; and month 11 (November), is part of the fourth quarter.

---

### Starting Code


```python
def quarter_of(month):
    # your code here
```

---

### Solution


```python
def quarter_of(month):
    if 1 <= month <= 3:
        return 1
    elif 4 <= month <= 6:
        return 2
    elif 7 <= month <= 9:
        return 3
    elif 10 <= month <= 12:
        return 4
```

---

### Sample Tests

```python
import codewars_test as test
from solution import quarter_of

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(quarter_of(3), 1)
        test.assert_equals(quarter_of(8), 3)
        test.assert_equals(quarter_of(11), 4)
```
