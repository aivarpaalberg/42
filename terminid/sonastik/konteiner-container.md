---
description: objekt mis sisaldab viiteid teistele objektidele
---

# konteiner \(container\)

## Üksikasjalikumalt

Pythoni konteineriteks \(_container_\) on näiteks ennikud \(_tuples_\), loendid \(_lists_\) ja sõnastikud \(_dictionaries_\). 

Viide on osa konteineri väärtusest. Enamasti kui me räägime konteineri väärtusest \(_value of container_\) mõtleme me väärtusi ja mitte selles sisalduvate objektide identiteete; kuid kui me räägime konteineri muudetavusest \(_mutability of container_\) siis mõeldakse konteineris vahetult sisalduvate objektide identiteete. Seega kui [muutumatu](muutumatu-immutable.md) konteiner \(_immutable container_\) nagu näiteks ennik \(_tuple_\) sisaldab viidet \(_reference_\) [muudetavale](muudetav-mutable.md) objektile siis enniku \(_tuple_\) väärtus muutub kui viidatud muudetav objekt muutub:

```python
>>> spam = ([1, 2, 3], [4, 5, 6])  # muutumatu konteiner ennik (tuple)
>>> type(spam)   
<class 'tuple'>                
>>> spam[0]                        # ennikus sisalduv viide loendile
[1, 2, 3]
>>> type(spam[0])
<class 'list'>                  
>>> spam[0].insert(0, 0)           # viidatud objekti muutmine
>>> spam
([0, 1, 2, 3], [4, 5, 6])          # enniku väärtus muutub
```

## Viited

* Pythoni ametlik dokumentatsioon \(inglise keeles\): [Objects, values and type](https://docs.python.org/3/reference/datamodel.html#objects-values-and-types)
* termin [muudetav \(mutable\)](muudetav-mutable.md)
* termin [muutumatu \(immutable\)](muutumatu-immutable.md)

