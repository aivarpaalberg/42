---
description: fikseeritud väärtusega objekt
---

# muutumatu \(immutable\)

## Üksikasjalikumalt

Muutumatute \(immutable\) objektide hulka kuuluvad numbrid \(_numbers_\), sõned \(_strings_\) ja ennikud \(_tuples_\). Sellist objekti ei saa muuta. Selleks, et salvestada teistsugune väärtus tuleb luua uus objekt. Muutumatud objektid mängivad olulist rolli kohtades kus on vajalik konstantsed paiskeväärtused \(_hash value_\), näiteks sõnastiku \(_dict_\) võti \(_key_\).

Muutumatu \(_immutable_\) konteiner objekti \(_container object_\)  mis sisaldab viidet \(_reference_\) muudetavale objektile \(_mutable object_\) võib muutuda kui viidatud objekt muutub; vaatamata sellele loetakse konteinerit muutumatuks. 

Objekti muudetavus on määratud tema tüübiga, näiteks numbrid \(_numbers_\), sõned \(_str_\) ja ennikud \(_tuple_\) on muutumatud aga sõnastikud \(_dict_\) ja loendid \(_list_\) on muutuvad.

Järgneva näiteme kuidas muutumatu andmetüübi \(ennik\) väärtus võib muutuda. Ennik \(_tuple_\) `spam` koosneb kahest loendist \(_list_\). Loendid on [muudetavad](muudetav-mutable.md) ning kui lisada sellele uus liige siis muutub ka ennik \(_tuple_\). See on võimalik tänu selllele et ennik koosneb viidetest loenditele ning need viited ei muutu, muutub objekt millele viidatakse: 

```python
>>> spam = ([1, 2, 3], [4, 5, 6])
>>> type(spam)   
<class 'tuple'>                
>>> spam[0]
[1, 2, 3]
>>> type(spam[0])
<class 'list'>                  
>>> spam[0].insert(0, 0)
>>> spam
([0, 1, 2, 3], [4, 5, 6])
```

## Viited

* Pythoni dokumentatsioon \(inglise keeles\): [immutable](https://docs.python.org/3/glossary.html#term-immutable)
* Pythoni dokumentatsioon \(inglise keeles\): [Objects, values and types](https://docs.python.org/3/reference/datamodel.html#objects-values-and-types)

