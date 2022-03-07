## [Removing Elements](https://www.codewars.com/kata/5769b3802ae6f8e4890009d2)

### Instructions

Take an array and remove every second element from the array. Always keep the first element and start removing with the next element.

Example:


```Python
["Keep", "Remove", "Keep", "Remove", "Keep", ...] --> ["Keep", "Keep", "Keep", ...]
```

None of the arrays will be empty, so you don't have to worry about that!

---

### Starting Code


```python
def remove_every_other(my_list):
    # Your code here!
    pass
```

---

### Solution


```python
def remove_every_other(my_list):
    return my_list[::2]
```

---

### Sample Tests

```python
test.assert_equals(remove_every_other(['Hello', 'Goodbye', 'Hello Again']),
                   ['Hello', 'Hello Again'])
test.assert_equals(remove_every_other([1, 2, 3, 4, 5, 6, 7, 8, 9, 10]),
                   [1, 3, 5, 7, 9])
test.assert_equals(remove_every_other([[1, 2]]), [[1, 2]])
test.assert_equals(remove_every_other([['Goodbye'], {'Great': 'Job'}]),
                   [['Goodbye']])
```
