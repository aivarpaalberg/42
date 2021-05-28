# abs\(\)

## Käsk \(command\)

{% hint style="info" %}
tagasta numbri absoluutväärtus
{% endhint %}

## Kasutamine

### Argument

[Funktsioonile](../../terminid/sonastik/funktsioon-function.md) **abs\(\)** tuleb edastada üks [argument](../../terminid/sonastik/argument.md) mis võib olla täisarv \(_int_\), ujukomaarv \(_floating point number_\) või kompleksarv \(_complex number_\). Kui argumendiks on kompleksarv siis tagastatakse selle magnituud \(_magnitude_\)

Juhul kui [argumenti](../../terminid/sonastik/argument.md) ei edastata või see ei ole täisarv \(_int_\), ujukomaarv \(_floating point number_\) või kompleksarv \(_complex number_\) siis tõstetakse `TypeError` erand.

### Tagastatav väärtus

[Funktsioon](../../terminid/sonastik/funktsioon-function.md) tagastab sama [andmetüübi](../../terminid/sonastik/andmetueuep-datatype.md) \(_data type_\) mis talle välja kutsudes [argumendina](../../terminid/sonastik/argument.md) edastati v.a. kompleksarvu korral kui tagastatakse ujukomaarv \(_floating point number_\) 

| Argumendi tüüp | Tagastatava väärtuse tüüp |
| :--- | :--- |
| täisarv \(_int_\) | täisarv \(_int_\) |
| ujukomaarv \(_float_\) | ujukomaarv \(_float_\) |
| kompleksarv \(_complex number_\) | ujukomaarv \(_float_\) |

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
* Pythoni interaktiivses interpretaatoris sisesta `help(abs)`

