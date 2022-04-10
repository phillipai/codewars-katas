## [DNA to RNA Conversion](https://www.codewars.com/kata/5556282156230d0e5e000089)

### Instructions

---

Deoxyribonucleic acid, DNA is the primary information storage molecule in biological systems. It is composed of four nucleic acid bases Guanine ('G'), Cytosine ('C'), Adenine ('A'), and Thymine ('T').

Ribonucleic acid, RNA, is the primary messenger molecule in cells. RNA differs slightly from DNA its chemical structure and contains no Thymine. In RNA Thymine is replaced by another nucleic acid Uracil ('U').

Create a function which translates a given DNA string into RNA.

For example:

```python
"GCAT"  =>  "GCAU"
```
The input string can be of arbitrary length - in particular, it may be empty. All input is guaranteed to be valid, i.e. each input string will only ever consist of `'G'`, `'C'`, `'A'` and/or `'T'`.


---

### Starting Code


```python
def dna_to_rna(dna):
    return
```

---

### Solution


```python
def dna_to_rna(dna):
    return(dna.replace('T', 'U'))
```

---

### Sample Tests

```python
import codewars_test as test
from solution import dna_to_rna

@test.describe("Sample Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(dna_to_rna("TTTT"), "UUUU")
        test.assert_equals(dna_to_rna("GCAT"), "GCAU")
        test.assert_equals(dna_to_rna("GACCGCCGCC"), "GACCGCCGCC")
```
