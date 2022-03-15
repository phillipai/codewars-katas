## [Short Long Short](https://www.codewars.com/kata/50654ddff44f800200000007)

### Instructions

---

Given 2 strings, a and b, return a string of the form short+long+short, with the shorter string on the outside and the longer string on the inside. The strings will not be the same length, but they may be empty ( zero length ).

For example: (Input1, Input2) --> output
```python
("1", "22") --> "1221"
("22", "1") --> "1221"
```

---

### Starting Code


```python
def solution(a, b):
    pass
```

---

### Solution


```python
def solution(a, b):
    return a + b + a if len(a) < len(b) else b + a + b
```

---

### Sample Tests

```python
import codewars_test as test
from solution import solution

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(solution('45', '1'), '1451')
        test.assert_equals(solution('13', '200'), '1320013')
        test.assert_equals(solution('Soon', 'Me'), 'MeSoonMe')
        test.assert_equals(solution('U', 'False'), 'UFalseU')
```
