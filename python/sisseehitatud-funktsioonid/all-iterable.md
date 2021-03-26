---
description: >-
  tagasta True kui itereeritava kõik elemendid on tõesed (true) või kui
  itereeritav on tühi.
---

# all\(iterable\)

## Üksikasjalikumalt

[Argumendiks](../../terminid/sonastik/argument.md) peab olema itereeritav \(kui ei ole, siis tõstetakse `TypeError`erand\).

```python
>>> all('abc')
True
>>> all('')
True
>>> all([1, 2, 3])
True
>>> all([0, 1, 2])
False
```

## Viited

* Pythoni ametlik dokumentatsioon \(inglise keeles\): [all\(iterable\)](https://docs.python.org/3/library/functions.html#all)

