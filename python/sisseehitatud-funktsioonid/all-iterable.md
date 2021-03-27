---
description: >-
  tagasta True kui itereeritava kõik elemendid on tõesed (true) või kui
  itereeritav on tühi.
---

# all\(iterable\)

## Üksikasjalikumalt

Funktsioon `all()`on samaväärne \(_equivalent_\) alljärgnevaga:

```python
def all(iterable):
    for element in iterable:
        if not element:
            return False
    return True
```

Koodist on näha, et funktsioon rakendab lühist \(_short circuit_\) s.t. et esimese väära \(_False_\) korral tagastab funktsioon väärtuse ning järelejäänud elemente enam ei kontrollita.

### Argumendid

Funktsioonile tuleb välja kutsudes edastada üks [argument](../../terminid/sonastik/argument.md) mis peab olema **itereeritav** \([sõne](../sisseehitatud-tueuebid/sone-str/), loend, hulk, sõnastik jne\). 

Juhul kui argumenti ei edastata või edastatud argumendiks ei ole itereeritav, siis tõstetakse `TypeError`erand.

### Tagastatav väärtus

Funktsioon tagastab tõesusväärtuse \(booli\):

|  Väärtus | Tingimus\(ed\) |
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

