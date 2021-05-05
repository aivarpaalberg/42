---
description: >-
  tagasta True kui sõne kõik tähemärgid on väiketähed ja sõnes on vähemalt üks
  tähemärk, muudel juhtudel tagasta False
---

# str.islower\(\)

## Käsk \(command\)

Kasutades seda [sõne](../) \(_str_\) [meetodit](../../../../terminid/sonastik/meetod-method.md) \(_method_\) anname [programeerimiskeeles](../../../../terminid/sonastik/programmeerimiskeel-programming-language.md) \(_programming language_\) käsu mis [loomulikus keeles](../../../../terminid/sonastik/loomulik-keel-natural-language.md) \(_natural language_\) on väljendatav kui: 

{% hint style="info" %}
tagasta True kui sõne kõik [tähed](../../../../terminid/sonastik/taeht-letter.md) \(_letters_\) on väiketähed ja sõnes on vähemalt üks täht, muudel juhtudel tagasta False
{% endhint %}

## Kasutamine

```python
>>> 'tere'.islower()   
True                    # kõik tähed on väiketähed
>>> 'Tere'.islower()
False                   # kõik tähed ei ole väiketähed
>>> ''.islower()
False                   # pole ühtegi väiketähte
>>> '1'.islower()
False                   # pole ühtegi väiketähte
>>> '1a'.islower()
True                    # kõik tähed on väiketähed
>>> '1A'.islower()
False                   # pole ühtegi väiketähte
```

## Abiinfo ja viited

* Pythoni ametlik dokumentatsioon \(inglise keeles\): [str.islower\(\)](https://docs.python.org/3/library/stdtypes.html#str.islower)
* Pythoni interaktiivses interpretaatoris sisesta `help(str.islower)`

