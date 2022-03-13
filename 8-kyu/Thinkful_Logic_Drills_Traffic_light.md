## [Thinkful - Logic Drills: Traffic light](https://www.codewars.com/kata/58649884a1659ed6cb000072)

### Instructions

---

You're writing code to control your town's traffic lights. You need a function to handle each change from `green`, to `yellow`, to `red`, and then to `green` again.

Complete the function that takes a string as an argument representing the current state of the light and returns a string representing the state the light should change to.

For example, `update_light('green')` should return `'yellow'`.

---

### Starting Code


```python
def update_light(current):
    # Your code here.
```

---

### Solution


```python
def update_light(current):
    if current == 'green': return 'yellow'
    elif current == 'yellow': return 'red'
    else: return 'green'
```

---

### Sample Tests

```python
import codewars_test as test
from solution import update_light

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(update_light('green'), 'yellow')
        test.assert_equals(update_light('yellow'), 'red')
        test.assert_equals(update_light('red'), 'green')
        
```
