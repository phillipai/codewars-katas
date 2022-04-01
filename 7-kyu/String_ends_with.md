## [String ends with?](https://www.codewars.com/kata/51f2d1cafc9c0f745c00037d)

### Instructions

---

Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string).

Examples:

```python
solution('abc', 'bc') # returns true
solution('abc', 'd') # returns false
```

---

### Starting Code


```python
def solution(string, ending):
    # your code here...
    pass
```

---

### Solution


```python
def solution(string, ending):
    return True if (string[-len(ending):]) == ending or len(ending) == 0 else False
```

---

### Sample Tests

```python
test.assert_equals(solution('abcde', 'cde'), True)
test.assert_equals(solution('abcde', 'abc'), False)
test.assert_equals(solution('abcde', ''), True)
```
