## [Remove First and Last Character](https://www.codewars.com/kata/56bc28ad5bdaeb48760009b0)

### Instructions

---

It's pretty straightforward. Your goal is to create a function that removes the first and last characters of a string. You're given one parameter, the original string. You don't have to worry with strings with less than two characters.

---

### Starting Code


```python
def remove_char(s):
    #your code here
```

---

### Solution


```python
def remove_char(s):
    return(s[1:-1])
```

---

### Sample Tests

```python
import codewars_test as test
from solution import remove_char

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(remove_char('eloquent'), 'loquen')
        test.assert_equals(remove_char('country'), 'ountr')
        test.assert_equals(remove_char('person'), 'erso')
        test.assert_equals(remove_char('place'), 'lac')
        test.assert_equals(remove_char('ok'), '')
        test.assert_equals(remove_char('ooopsss'), 'oopss')
    
```
