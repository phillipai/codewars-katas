## [Reversed Words](https://www.codewars.com/kata/51c8991dee245d7ddf00000e)

### Instructions

---

Complete the solution so that it reverses all of the words within the string passed in.

Example:

```python
"The greatest victory is that which requires no battle" --> "battle no requires which that is victory greatest The"
```

---

### Starting Code


```python
def reverse_words(s):
    return s
```

---

### Solution


```python
def reverse_words(s):
    split_words = s.split()
    s = " ".join(split_words[::-1])
    return s
```

---

### Sample Tests

```python
import codewars_test as test

try:
    from solution import reverseWords as reverse_words
except ImportError:
    from solution import reverse_words

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it("Basic Tests")
    def basic_tests():
        test.assert_equals(reverse_words("hello world!"), "world! hello")
```
