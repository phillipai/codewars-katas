## [Simple Fun #176: Reverse Letter](https://www.codewars.com/kata/58b8c94b7df3f116eb00005b)

### Instructions

---

### Task
Given a string `str`, reverse it omitting all non-alphabetic characters.

### Example
For `str = "krishan"`, the output should be `"nahsirk"`.

For `str = "ultr53o?n"`, the output should be `"nortlu"`.

### Input/Output
- `[input] string str`
A string consists of lowercase latin letters, digits and symbols.

- `[output] a string`

---

### Starting Code


```python
def reverse_letter(string):
    #do your magic here
```

---

### Solution


```python
def reverse_letter(string):
    return ''.join(e for e in string[::-1] if e.isalpha())
```

---

### Sample Tests

```python
test.describe("Basic test")

test.assert_equals(reverse_letter("krishan"),"nahsirk")

test.assert_equals(reverse_letter("ultr53o?n"),"nortlu")

test.assert_equals(reverse_letter("ab23c"),"cba")

test.assert_equals(reverse_letter("krish21an"),"nahsirk")
```
