## [Create Phone Number](https://www.codewars.com/kata/525f50e3b73515a6db000b83)

### Instructions

---

Write a function that accepts an array of 10 integers (between 0 and 9), that returns a string of those numbers in the form of a phone number.

#### Example
```python
create_phone_number([1, 2, 3, 4, 5, 6, 7, 8, 9, 0]) # => returns "(123) 456-7890"
```
The returned format must be correct in order to complete this challenge.
Don't forget the space after the closing parentheses!

---

### Starting Code


```python
def create_phone_number(n):
    #your code here
```

---

### Solution


```python
def create_phone_number(n):
    list = []
    count = 0
    for e in n:
        if count == 0:
            list.append('(')
        if count == 3:
            list.append(')')
        if count == 3:
            list.append(' ')
        elif count == 6:
            list.append('-')
        list.append(e)
        count += 1
    return(''.join(map(str, list)))
```

---

### Sample Tests

```python
import codewars_test as test
from solution import create_phone_number

@test.describe("Create Phone Number")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(create_phone_number([1, 2, 3, 4, 5, 6, 7, 8, 9, 0]), "(123) 456-7890")
        test.assert_equals(create_phone_number([1, 1, 1, 1, 1, 1, 1, 1, 1, 1]), "(111) 111-1111")
        test.assert_equals(create_phone_number([1, 2, 3, 4, 5, 6, 7, 8, 9, 0]), "(123) 456-7890")
        test.assert_equals(create_phone_number([0, 2, 3, 0, 5, 6, 0, 8, 9, 0]), "(023) 056-0890")
        test.assert_equals(create_phone_number([0, 0, 0, 0, 0, 0, 0, 0, 0, 0]), "(000) 000-0000")
```
