## [Break camelCase](https://www.codewars.com/kata/5208f99aee097e6552000148)

### Instructions

---

Complete the solution so that the function will break up camel casing, using a space between words.

#### Example
```python
"camelCasing"  =>  "camel Casing"
"identifier"   =>  "identifier"
""             =>  ""
```

---

### Starting Code


```python
def solution(s):
    pass
```

---

### Solution


```python
def solution(s):
    list = []
    for e in s:
        if e.islower():
            list.append(e)
        elif e.isupper():
            list.append(' ' + e)
    return (''.join(list))
```

---

### Sample Tests

```python
test.assert_equals(solution("helloWorld"), "hello World")
test.assert_equals(solution("camelCase"), "camel Case")
test.assert_equals(solution("breakCamelCase"), "break Camel Case")
```
