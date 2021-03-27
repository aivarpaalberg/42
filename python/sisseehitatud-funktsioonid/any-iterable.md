---
description: >-
  tagasta True kui vähemalt üks itereeritava element on tõene (true); tagasta
  False kui itereeritav on tühi
---

# any\(iterable\)

## Üksikasjalikumalt

Funktsioon `any()` on samaväärne \(_equivalent_\) alljärgnevaga:

```python
def any(iterable):
    for element in iterable:
        if element:
            return True
    return False
```

Koodist on näha, et funktsioon rakendab lühist \(_short circuit_\) s.t. et esimese väära \(_True_\) korral tagastab funktsioon väärtuse ning järelejäänud elemente enam ei kontrollita.

### Argument

Funktsioonile tuleb välja kutsudes edastada üks [argument](../../terminid/sonastik/argument.md) mis peab olema **itereeritav** \([sõne](../sisseehitatud-tueuebid/sone-str/), loend, hulk, sõnastik vms\).

Juhul kui argumenti ei edastata või edastatud argument ei ole itereeritav tõstetakse `TypeError` erand.

### Tagastatav väärtus

Funktsioon tagastab tõesusväärtuse \(booli\).

| Väärtus | Tingimus\(ed\) |
| :--- | :--- |
| True | vähemalt üks itereeritava element on tõene¹ |
| False | itereeritav on tühi või kõik elemendid on väärad¹ |

¹ vt [tõesuse testimine](../sisseehitatud-tueuebid/toesuse-testimine.md)

### Näited

Kas loendis on mõni 3-ga jaguv arv?

```python
>>> loend = [2, 5, 7, 11, 15, 20]
>>> any(num % 3 == 0 for num in loend)
True
>>> loend = [2, 5, 7, 11, 16, 20]
>>> any(num % 3 == 0 for num in loend)
False
```

### Viited

* Pythoni ametlik dokumentatsioon \(inglise keeles\): [any\(_iterable_\)](https://docs.python.org/3/library/functions.html#any)
* Pythoni interaktiivses interpretaatoris sisesta `help(any)`

