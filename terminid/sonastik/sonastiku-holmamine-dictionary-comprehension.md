---
description: >-
  kompaktne viis käitlemaks (to process) kõiki või osasid itereeritava elemente
  ja tagastamaks sõnastik (dictionary) tulemustega
---

# sõnastiku hõlmamine \(dictionary comprehension\)

## Üksikasjalikumalt

Itereeritava kõikide elementide käitlemine ja [sõnastiku](sonastik-dictionary.md) tagastamine: `anna täisarv võtmena ja täisarvu absoluutväärtus võtme väärtusena iga täisarvu kohta vahemikus -2..3 (v.a.)`

```python
>>> {i: abs(i) for i in range(-2, 3)}
{-2: 2, -1: 1, 0: 0, 1: 1, 2: 2}
```

Itereeritava osade elementide käitlemine ja [sõnastiku](sonastik-dictionary.md) tagastamine: `anna täisarv võtmena ja täisarvu absoluutväärtuse võtme väärtusena iga täisarvu kohta vahemikus -2..3 (v.a.) mis on paaris`

```python
>>> {i: abs(i) for i in range(-2, 3) if i % 2 == 0}
{-2: 2, 0: 0, 2: 2}
```

## Viited 

Pythoni ametlik dokumentatsioon \(inglise keeles\):

* Documentation &gt; Glossary &gt; [dictionary comprehension](https://docs.python.org/3/glossary.html#term-dictionary-comprehension)

