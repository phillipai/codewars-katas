## [Counting sheep...](https://www.codewars.com/kata/54edbc7200b811e956000556)

### Instructions

---

Consider an array/list of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).

For example,

```python
[True,  True,  True,  False,
  True,  True,  True,  True ,
  True,  False, True,  False,
  True,  False, False, True ,
  True,  True,  True,  True ,
  False, False, True,  True]
```

The correct answer would be `17`.

Hint: Don't forget to check for bad values like `null`/`undefined`

---

### Starting Code


```python
def count_sheeps(sheep):
  # TODO May the force be with you
  pass
```

---

### Solution


```python
def count_sheeps(sheep):
    sum = 0
    for count in sheep:
        if count:
            sum += 1
    return sum
```

---

### Sample Tests

```python
array1 = [True,  True,  True,  False,
          True,  True,  True,  True ,
          True,  False, True,  False,
          True,  False, False, True ,
          True,  True,  True,  True ,
          False, False, True,  True ];
              
test.assert_equals(result := count_sheeps(array1), 17, "There are 17 sheeps in total, not %s" % result)
```
