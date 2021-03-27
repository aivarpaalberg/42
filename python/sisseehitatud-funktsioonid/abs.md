---
description: tagasta numbri absoluutväärtus
---

# abs\(\)

## Üksikasjalikumalt

### Argument

Funktsioonile tuleb edastada üks [argument](../../terminid/sonastik/argument.md) mis võib olla täisarv \(_int_\), ujukomaarv \(_floating point number_\) või kompleksarv \(_complex number_\). Kui argumendiks on kompleksarv siis tagastatakse selle magnituud \(_magnitude_\)

Juhul kui argumenti ei edastata või see ei ole täisarv \(_int_\), ujukomaarv \(_floating point number_\) või kompleksarv \(_complex number_\) siis tõstetakse `TypeError` erand.

### Tagastatav väärtus

Funktsioon tagastab sama andmetüübi mis talle välja kutsudes edastati v.a. kompleksarvu korral kui tagastatakse ujukomaarv \(_floating point number_\) 

| Väärtus | Tingimus\(ed\) |
| :--- | :--- |
| täisarv  | argumendiks täisarv \(_int_\) |
| ujukomaarv  | argumendiks ujukomaarv või kompleksarv |

### Näited

Täisarvu \(_int_\) ja ujukomaarvu \(_floating point number_\) absoluutväärtus ning kompleksarvu \(_complex number_\) magnituut:

```python
>>> abs(-42)
42
>>> abs(4.2)
4.2
>>> abs(4 + 2j)
4.47213595499958
```

### 

### Viited

* Pythoni ametlik dokumentatsioon \(inglise keeles\): [abs\(\)](https://docs.python.org/3/library/functions.html#abs)

