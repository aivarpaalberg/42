# abs()

## Käsk (command)

{% tabs %}
{% tab title="Loomulik keel" %}
[tagasta](../../terminid/sonastik/tagastama-to-return.md#taehendus) numbri absoluutväärtus
{% endtab %}

{% tab title="Python" %}
```
>>> abs(-42)
42
```
{% endtab %}
{% endtabs %}

## Kasutamine

### Argument

[Funktsioonile](../../terminid/sonastik/funktsioon-function.md) **abs()** tuleb edastada **üks** [argument](../../terminid/sonastik/argument.md) mis võib olla:

* [täisarv](../../terminid/sonastik/taeisarv-integer.md#taehendus) (_int_),&#x20;
* ujukomaarv (_floating point number_) või&#x20;
* kompleksarv (_complex number_).&#x20;

Kui argumendiks on kompleksarv siis tagastatakse selle magnituud (_magnitude_)

Juhul kui [argumenti](../../terminid/sonastik/argument.md) ei edastata või see ei ole [täisarv](../../terminid/sonastik/taeisarv-integer.md#taehendus) (_int_), ujukomaarv (_floating point number_) või kompleksarv (_complex number_) siis tõstetakse `TypeError` viga.

### Tagastatav väärtus

[Funktsioon](../../terminid/sonastik/funktsioon-function.md) tagastab sama [andmetüübi](../../terminid/sonastik/andmetueuep-datatype.md) (_data type_) mis talle välja kutsudes [argumendina](../../terminid/sonastik/argument.md) edastati v.a. kompleksarvu korral kui tagastatakse ujukomaarv (_floating point number_)&#x20;

| Argumendi tüüp                   | Tagastatava väärtuse tüüp                                                |
| -------------------------------- | ------------------------------------------------------------------------ |
| [täisarv](abs.md#viited) (_int_) | [täisarv](../../terminid/sonastik/taeisarv-integer.md#taehendus) (_int_) |
| ujukomaarv (_float_)             | ujukomaarv (_float_)                                                     |
| kompleksarv (_complex number_)   | ujukomaarv (_float_)                                                     |

### Näited

Täisarvu (_int_) ja ujukomaarvu (_floating point number_) absoluutväärtus ning kompleksarvu (_complex number_) magnituut:

```python
>>> abs(-42)
42
>>> abs(4.2)
4.2
>>> abs(4 + 2j)
4.47213595499958
```

`TypeError` viga funktsiooni väljakutsumisel ilma argumendita või argumendiga, mis pole õige andmetüübiga (s.t. täisarv, ujukomaarv või kompleksarv):

```python
>>> abs()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: abs() takes exactly one argument (0 given)
>>> abs('1')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: bad operand type for abs(): 'str'
```

### Viited

* Pythoni ametlik dokumentatsioon (inglise keeles): [abs()](https://docs.python.org/3/library/functions.html#abs)
* Pythoni interaktiivses interpretaatoris sisesta `help(abs)`
