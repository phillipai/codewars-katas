## [Who likes it?](https://www.codewars.com/kata/5266876b8f4bf2da9b000362)

### Instructions

---

You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement the function which takes an array containing the names of people that like an item. It must return the display text as shown in the examples:

```python
[]                                -->  "no one likes this"
["Peter"]                         -->  "Peter likes this"
["Jacob", "Alex"]                 -->  "Jacob and Alex like this"
["Max", "John", "Mark"]           -->  "Max, John and Mark like this"
["Alex", "Jacob", "Mark", "Max"]  -->  "Alex, Jacob and 2 others like this"
```
Note: For 4 or more names, the number in `"and 2 others"` simply increases.

---

### Starting Code


```python
def likes(names):
    # your code here
    pass
```

---

### Solution


```python
def likes(names):
    
    if not names:
        return 'no one likes this'
    elif len(names) == 1:
        return ''.join(names) + ' likes this'
    elif len(names) == 2:
        return ' and '.join(names) + ' like this'
    elif len(names) == 3:
        return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this'
    elif len(names) > 3:
        return names[0] + ', ' + names[1] + ' and ' + str(len(names) - 2) + ' others like this'
```

---

### Sample Tests

```python
import codewars_test as test
from solution import likes

@test.it('Basic tests')
def _():
    test.assert_equals(likes([]), 'no one likes this')
    test.assert_equals(likes(['Peter']), 'Peter likes this')
    test.assert_equals(likes(['Jacob', 'Alex']), 'Jacob and Alex like this')
    test.assert_equals(likes(['Max', 'John', 'Mark']), 'Max, John and Mark like this')
    test.assert_equals(likes(['Alex', 'Jacob', 'Mark', 'Max']), 'Alex, Jacob and 2 others like this')
```
