## [Find the unique number](https://www.codewars.com/kata/585d7d5adb20cf33cb000235)

### Instructions

---

There is an array with some numbers. All numbers are equal except for one. Try to find it!
```python
find_uniq([ 1, 1, 1, 2, 1, 1 ]) == 2
find_uniq([ 0, 0, 0.55, 0, 0 ]) == 0.55
```
It’s guaranteed that array contains at least 3 numbers.

The tests contain some very huge arrays, so think about performance.

---

### Starting Code


```python
def find_uniq(arr):
    # your code here
    return n   # n: unique number in the array
```

---

### Solution


```python
def find_uniq(arr):
    return min(set(arr), key=arr.count)
```

---

### Sample Tests

```python
try:
    import codewars_test as test
except:
    pass


@test.describe("Basic Tests")
def f():
    @test.it("Simple tests")
    def _():
        test.assert_equals(find_uniq([ 1, 1, 1, 2, 1, 1 ]), 2)
        test.assert_equals(find_uniq([ 0, 0, 0.55, 0, 0 ]), 0.55)
        test.assert_equals(find_uniq([ 3, 10, 3, 3, 3 ]), 10)
```
