## [Sort the odd](https://www.codewars.com/kata/578aa45ee9fd15ff4600090d)

### Instructions

You will be given an array of numbers. You have to sort the odd numbers in ascending order while leaving the even numbers at their original positions.

Examples:

```Python
[7, 1]  =>  [1, 7]
[5, 8, 6, 3, 4]  =>  [3, 8, 6, 5, 4]
[9, 8, 7, 6, 5, 4, 3, 2, 1, 0]  =>  [1, 8, 3, 6, 5, 4, 7, 2, 9, 0]
```


---

### Starting Code


```python
def sort_array(source_array):
    # Return a sorted array.
```

---

### Solution


```python
def sort_array(source_array):
    odd = sorted(list(filter(lambda x: x % 2, source_array)))
    l, c = [], 0
    for i in source_array:
        if i in odd:
            l.append(odd[c])
            c += 1
        else:
            l.append(i)    
    return l
```

---

### Sample Tests

```python
test.assert_equals(sort_array([5, 3, 2, 8, 1, 4]), [1, 3, 2, 8, 5, 4])
test.assert_equals(sort_array([5, 3, 1, 8, 0]), [1, 3, 5, 8, 0])
test.assert_equals(sort_array([]),[])
```
