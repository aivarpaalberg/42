---
description: muudetavate objektide väärtus saab muutuda kuid nad säilitavad oma identiteedi
---

# muudetav \(mutable\)

## Üksikasjalikumalt

Objektid mille väärtus võib muutuda öeldakse olevat **muudetavad** \(_mutable_\). Nende objektide väärtus võib muutuda kuid nende identiteet jääb samaks.

```python
>>> spam = [1, 2, 3]
>>> spam.append(4)
>>> spam
[1, 2, 3, 4]
```

## Viited

* Pythoni dokumentatsioon \(inglise keeles\): [mutable](https://docs.python.org/3/glossary.html#term-mutable)
* Pythoni dokumentatsioon \(inglise keeles\): [Objects, values and types](https://docs.python.org/3/reference/datamodel.html#objects-values-and-types)


