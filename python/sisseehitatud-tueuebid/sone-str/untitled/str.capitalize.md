# str.capitalize\(\)

## Käsk \(command\)

`tagasta sõne kus esimene märk on muudetud suurtäheks ja kõik ülejäänud väiketähtedeks`

## Kasutamine

`str.capitalize` väljakutsumisel ei anta sellele argumente.

```python
>>> 'tere maailm'.capitalize()
'Tere maailm'
>>> 'tEre MAAilm'.capitalize()
'Tere maailm'
>>> s = 'Tere Maailm'
>>> s.capitalize()
'Tere maailm'
>>> str.capitalize('tere maailm')
'Tere maailm'
```

Tasub silmas pidada, et kui sõne \(_str_\) sisaldab nime vms sõna mis peab olema kirjutatud suure tähega siis antud meetod annab soovimatu tulemuse:

```python
>>> 'Suure-Jaani linn'.capitalize()
'Suure-jaani linn'
```

### Abiinfo ja viited

* Pythoni ametlik dokumentatsioon \(inglise keeles\): [str.capitalize\(\)](https://docs.python.org/3/library/stdtypes.html#str.capitalize)
* Pythoni interaktiivses interpretaatoris sisesta `help(str.capitalize)`



