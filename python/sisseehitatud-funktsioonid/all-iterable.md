---
description: >-
  tagasta True kui itereeritava kõik elemendid on tõesed (true) või kui
  itereeritav on tühi.
---

# all\(iterable\)

## Üksikasjalikumalt

### Argumendid

Funktsioonile tuleb välja kutsudes edastada üks [argument](../../terminid/sonastik/argument.md) mis peab olema **itereeritav** \([sõne](../sisseehitatud-tueuebid/sone-str/), loend, hulk, sõnastik jne\). Juhul kui argumenti ei edastata või edastatud argumendiks ei ole itereeritav, siis tõstetakse `TypeError`erand.

### Tagastatavad väärtused

| Tagastatav väärtus | Tingimus\(ed\) |
| :--- | :--- |
| **True** | kõik itereeritava elemendid on tõesed või itereeritav on tühi |
| **False** | vähemalt üks itereeritava element on väär |

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

