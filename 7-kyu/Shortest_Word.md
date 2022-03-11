## [Shortest Word](https://www.codewars.com/kata/57cebe1dc6fdc20c57000ac9)

### Instructions

---

Simple, given a string of words, return the length of the shortest word(s).

String will never be empty and you do not need to account for different data types.

---

### Starting Code


```python
def find_short(s):
    # your code here
    return l # l: shortest word length
```

---

### Solution


```python
def find_short(s):
    words = s.split()
    l = len(words[0])
    for e in words:
        if len(e) <= l:
            l = len(e)
    return l
```

---

### Sample Tests

```python
import codewars_test as test
from solution import find_short

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(find_short("bitcoin take over the world maybe who knows perhaps"), 3)
        test.assert_equals(find_short("turns out random test cases are easier than writing out basic ones"), 3)
        test.assert_equals(find_short("lets talk about javascript the best language"), 3)
        test.assert_equals(find_short("i want to travel the world writing code one day"), 1)
        test.assert_equals(find_short("Lets all go on holiday somewhere very cold"), 2)   
        test.assert_equals(find_short("Let's travel abroad shall we"), 2)
```
