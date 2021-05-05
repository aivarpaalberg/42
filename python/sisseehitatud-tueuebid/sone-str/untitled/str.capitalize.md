---
description: >-
  tagasta sõne kus esimene märk on muudetud suurtäheks ja kõik ülejäänud
  väiketähtedeks
---

# str.capitalize\(\)

## Käsk \(command\)

Kasutades seda [sõne](../) \(_str_\) [meetodit](../../../../terminid/sonastik/meetod-method.md) \(_method_\) anname käsu mis [loomulikus keeles](../../../../terminid/sonastik/loomulik-keel-natural-language.md) \(_natural language_\) on väljendatav kui: 

{% hint style="info" %}
tagasta sõne \(_str_\) kus esimene [märk](../../../../terminid/sonastik/maerk-character.md) \(_character_\) on muudetud suurtäheks ja kõik ülejäänud väiketähtedeks
{% endhint %}

Kuna sõne \(_str_\) on [muutumatu](../../../../terminid/sonastik/muutumatu-immutable.md) \(_immutable_\) siis tagastatav sõne on uus [objekt](../../../../terminid/sonastik/objekt-object.md) \(_object_\). Kui seda ei seota \(_bound_\) nimega siis ei ole see hiljem ligipääsetav \(_accessible_\).

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



