## [Function 1 - hello world](https://www.codewars.com/kata/523b4ff7adca849afe000035)

### Instructions

#### Description:
Make a simple function called greet that returns the most-famous "hello world!".

#### Style Points
Sure, this is about as easy as it gets. But how clever can you be to create the most creative hello world you can think of? What is a "hello world" solution you would want to show your friends?

---

### Starting Code


```python
# Write a function `greet` that returns "hello world!"
```

---

### Solution


```python
# Write a function `greet` that returns "hello world!" 
def greet():
    return 'hello world!'
```

---

### Sample Tests

```python
import codewars_test as test
from solution import greet

@test.describe("Greet function")
def _():
    @test.it("Making sure greet exists")
    def _():
        try:
            test.expect(greet)
        except NameError:
            test.fail("Greet doesn't exist")
    @test.it("Testing that it returns hello world!")
    def _():
        test.assert_equals(greet(), "hello world!", "Greet doesn't return hello world!")
```
