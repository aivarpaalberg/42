---
description: väärtus mis edastatakse funktsioonile (või meetodile) seda välja kutsudes
---

# argument

## Üksikasjalikumalt

Argumente on kahte liiki:

* **võtmesõna argument** \(_keyword argument_\)- argumendid millele eelneb identifikaator \(`nimi=`\) funktsiooni väljakutses või edastatakse \(_passed_\) kui väärtus sõnastikus \(_dict_\) millele eelneb `**`. 
* **kohaargument** \(_positional argument_\) - argumendid mis ei ole võtmesõna argumendid on kohaargumendid. Kohaargumendid võivad ilmuda \(_appear_\) argumentide loendi alguses või edastatakse itereeritava elementidena millele eelneb `*`. 

Argumendid omistatakse \(_assigned_\) nimelistele lokaalsetele muutujatele \(_local variables_\) funtsiooni kehas \(_body_\)

### Võtmesõna argument

Kui on [funktsioon](funktsioon-function.md) `summa` ja sellel on kaks võtmesõna argumenti: `hind` ja `kogus` siis saab seda funktsiooni välja kutsuda kahel viisil:

```python
summa(hind=4, kogus=2)        # identifikaatoritega
summa(**{hind:4, kogus:2})    # sõnastikuga
```

Sõnastiku saab funktsioonile edastada ka nimena:

```python
andmed = {hind: 4, kogus:2}
summa(**andmed)               # nimega sõnastikuga
```

### Kohaargument

Kui on [funktsioon](funktsioon-function.md) `summa`ja selle on kaks kohaargumenti siis saab seda funktsiooni välja kutsuda kahe viisil:

```python
summa(4, 2)      # kohaargumentidega
summa(*(4, 2))   # itereeritavaga
```

Itereeritava saab edastada ka nimena:

```python
andmed = (4, 2)
summa(*andmed)   # nimega itereeritavaga
```

### Viited

* Pythoni ametlik dokumentatsioon \(inglise keeles\): [argument](https://docs.python.org/3/glossary.html#term-argument)

